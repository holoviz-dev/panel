# Vtk Interactive

```python
import panel as pn
import pyvista as pv

from pyvista import examples

pn.extension('vtk', sizing_mode='stretch_width')
```

For this example we use the pyvista library to load a dataset and generate easily a VTK scene

```python
m = examples.download_st_helens().warp_by_scalar()

# default camera position
cpos = [
    (567000.9232163235, 5119147.423216323, 6460.423216322832),
    (562835.0, 5114981.5, 2294.5),
    (-0.4082482904638299, -0.40824829046381844, 0.8164965809277649)
]

# pyvista plotter
pl = pv.Plotter(notebook=True);
actor = pl.add_mesh(m, smooth_shading=True, lighting=True)
pl.camera_position = cpos #set camera position

# save initial camera properties
renderer = list(pl.ren_win.GetRenderers())[0]
initial_camera = renderer.GetActiveCamera()
initial_camera_pos = {
    "focalPoint": initial_camera.GetFocalPoint(),
    "position": initial_camera.GetPosition(),
    "viewUp": initial_camera.GetViewUp()
}

# Panel creation using the VTK Scene created by the plotter pyvista
orientation_widget = True
enable_keybindings = True
vtkpan = pn.pane.VTK(
    pl.ren_win, margin=0, sizing_mode='stretch_both', orientation_widget=orientation_widget,
    enable_keybindings=enable_keybindings, min_height=600
)
vtkpan
```

### Colorbars and actor selection

```python
# Creation of a mapping between Custom name and the VTK object reference
actor_ref = ["None", actor.__this__]
actor_names = ["None", 'St Helen']
actor_opts = {k:v for k,v in zip(actor_names, actor_ref)}

options = {}
actor_selection = pn.ui.Select(
    value=None, options=actor_opts, margin=10, label="Actor Selection"
)
actor_selection
```

### VTK Scene Parameters (Background, Lights,...)

```python
# Scene Layout
color = ''.join(['#'] + ['{:02x}'.format(int(v*255)) for v in pl.background_color[:3]])
bind_and_orient = pn.ui.CheckBoxGroup(
    value=['Orientation Widget', 'Key Bindings'], options=['Orientation Widget', 'Key Bindings']
)
reset_camera = pn.ui.Button(label='Reset Camera')
background_color = pn.ui.ColorPicker(value=color, label='Background Color')
scene_props = pn.Column(bind_and_orient, reset_camera, background_color, sizing_mode='stretch_width')

# Light properties
light_box_title = pn.widgets.StaticText(value='Light properties')
light_type = pn.ui.Select(value='HeadLight', options=['HeadLight', 'SceneLight', 'CameraLight'])
light_intensity = pn.ui.FloatSlider(start=0, end=1, value=1, label="Intensity")
light_props = pn.Column(light_box_title, light_type, light_intensity, sizing_mode='stretch_width')

pn.Column(scene_props, light_props, max_width=320)
```

### Actor Properties

```python
#layout actor props
opacity = pn.ui.FloatSlider(value=1, start=0, end=1, label='Opacity', disabled=True)
lighting = pn.ui.Toggle(value=True, label='Lighting', disabled=True)
interpolation = pn.ui.Select(value='Phong', options=['Flat','Phong'], label='Interpolation', disabled=True)
edges = pn.ui.Toggle(value=False, label='Show Edges', disabled=True)
edges_color = pn.ui.ColorPicker(value='#ffffff', label='Edges Color', disabled=True)
representation = pn.ui.Select(value='Surface', options=['Points','Wireframe','Surface'], label='Representation', disabled=True)
frontface_culling = pn.ui.Toggle(value=False, label='Frontface Culling', disabled=True)
backface_culling = pn.ui.Toggle(value=False, label='Backface Culling', disabled=True)
ambient = pn.ui.FloatSlider(value=0, start=-1, end=1, label='Ambient', disabled=True)
diffuse = pn.ui.FloatSlider(value=1, start=0, end=2, label='Diffuse', disabled=True)
specular = pn.ui.FloatSlider(value=0, start=0, end=10, label='Specular', disabled=True)
specular_power = pn.ui.FloatSlider(value=100, start=0, end=100, label='Specular Power', disabled=True)

actor_props = pn.Column(
    opacity, lighting, interpolation, edges, edges_color,
    representation, frontface_culling, backface_culling,
    ambient, diffuse, specular, specular_power
)

actor_props
```

Linking all widgets together using jslinks

```python
#Linking
light_type.jslink(vtkpan, code={'value':"""
const light = target.renderer_el.getRenderer().getLights()[0]
if (source.value == 'HeadLight')
    light.setLightTypeToHeadLight()
else if (source.value == 'CameraLight')
    light.setLightTypeToCameraLight()
else if (source.value == 'SceneLight')
    light.setLightTypeToSceneLight()
target.renderer_el.getRenderWindow().render()
"""})

light_intensity.jslink(vtkpan, code={'value':"""
const light = target.renderer_el.getRenderer().getLights()[0]
light.setIntensity(source.value)
target.renderer_el.getRenderWindow().render()
"""})

bind_and_orient.jslink(vtkpan, code = {'value':"""
target.orientation_widget = source.value.includes("Orientation Widget")
target.enable_keybindings = source.value.includes("Key Bindings")
"""})

reset_camera.js_on_click(args={'target': vtkpan, 'initial_camera':initial_camera_pos},
                         code="target.camera = initial_camera");

background_color.jslink(vtkpan, code={'value':"""
const hextoarr = (color) => {return [parseInt(color.slice(1,3),16)/255, parseInt(color.slice(3,5),16)/255, parseInt(color.slice(5,7),16)/255]}
target.renderer_el.getRenderer().setBackground(hextoarr(source.color))
target.renderer_el.getRenderWindow().render()
"""});

opacity.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setOpacity(source.value)
    target.renderer_el.getRenderWindow().render()
}
""")

lighting.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setLighting(source.active)
    target.renderer_el.getRenderWindow().render()
}
""")

edges.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setEdgeVisibility(source.active)
    target.renderer_el.getRenderWindow().render()
}
""")

interpolation.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    if (source.value=="Flat") {
      actor.getProperty().setInterpolationToFlat()
    } else{
       actor.getProperty().setInterpolationToPhong()
    }
    target.renderer_el.getRenderWindow().render()
}
""")

edges_color.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const hextoarr = (color) => {return [parseInt(color.slice(1,3),16)/255, parseInt(color.slice(3,5),16)/255, parseInt(color.slice(5,7),16)/255]}
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setEdgeColor(hextoarr(source.color))
    target.renderer_el.getRenderWindow().render()
}
""")

representation.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    if(source.value=="Points"){
        actor.getProperty().setRepresentationToPoints()
    }else if(source.value=="Wireframe"){
        actor.getProperty().setRepresentationToWireframe()
    }else if(source.value=="Surface"){
        actor.getProperty().setRepresentationToSurface()
    }
    target.renderer_el.getRenderWindow().render()
}
""")

frontface_culling.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setFrontfaceCulling(source.active)
    target.renderer_el.getRenderWindow().render()
}
""")

backface_culling.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setBackfaceCulling(source.active)
    target.renderer_el.getRenderWindow().render()
}
""")

ambient.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setAmbient(source.value)
    target.renderer_el.getRenderWindow().render()
}
""")

diffuse.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setDiffuse(source.value)
    target.renderer_el.getRenderWindow().render()
}
""")

specular.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setSpecular(source.value)
    target.renderer_el.getRenderWindow().render()
}
""")

specular_power.jscallback(args={"target":vtkpan, "actor_selection":actor_selection}, value="""
if (actor_selection.value!="None"){
    const actor = target.getActors(actor_selection.value)[0]
    actor.getProperty().setSpecularPower(source.value)
    target.renderer_el.getRenderWindow().render()
}
""")

actor_selection.jslink(target=vtkpan, code = {'value' : """
if (source.value!="None"){
    const actor = target.getActors(source.value)[0]
    target.outline.setInputData(actor.getMapper().getInputData())
    target.renderer_el.getRenderer().addActor(target.outline_actor)
    
    //synchronize actor props and widgets values
    const properties = actor.getProperty()
    opacity.setv({value: properties.getOpacity()}, {silent: true})
    lighting.setv({active: !!properties.getLighting()}, {silent: true})
    edges.active = !!properties.getEdgeVisibility()
    const actor_color = "#" + properties.getEdgeColor().map((c) => ("0" + Math.round(255*c).toString(16,2)).slice(-2)).join('')
    edges_color.setv({color: actor_color}, {silent: true})
    const interp_string = properties.getInterpolationAsString()
    interpolation.setv({value: interp_string[0] + interp_string.slice(1).toLocaleLowerCase()}, {silent: true})
    const repr_string = properties.getRepresentationAsString()
    representation.setv({value: repr_string[0] + repr_string.slice(1).toLocaleLowerCase()}, {silent: true})
    frontface_culling.setv({active: !!properties.getFrontfaceCulling()}, {silent: true})
    backface_culling.setv({active: !!properties.getBackfaceCulling()}, {silent: true})
    ambient.setv({value: properties.getAmbient()}, {silent: true})
    diffuse.setv({value: properties.getDiffuse()}, {silent: true})
    specular.setv({value: properties.getSpecular()}, {silent: true})
    specular_power.setv({value: properties.getSpecularPower()}, {silent: true})
    //enable widgets modifications
    opacity.disabled = false
    lighting.disabled = false
    interpolation.disabled = false
    edges.disabled = false
    edges_color.disabled = false
    representation.disabled = false
    frontface_culling.disabled = false
    backface_culling.disabled = false
    ambient.disabled = false
    diffuse.disabled = false
    specular.disabled = false
    specular_power.disabled = false
} else {
    target.renderer_el.getRenderer().removeActor(target.outline_actor)
    opacity.disabled = true
    lighting.disabled = true
    interpolation.disabled = true
    edges.disabled = true
    edges_color.disabled = true
    representation.disabled = true
    frontface_culling.disabled = true
    backface_culling.disabled = true
    ambient.disabled = true
    diffuse.disabled = true
    specular.disabled = true
    specular_power.disabled = true
}
target.renderer_el.getRenderWindow().render()

"""}, args={"opacity":opacity, "lighting":lighting, "interpolation": interpolation, "edges": edges, "edges_color": edges_color,
            "representation": representation, "frontface_culling": frontface_culling, "backface_culling": backface_culling,
            "ambient": ambient, "diffuse": diffuse, "specular": specular, "specular_power": specular_power});

controllers = pn.Column(
    actor_selection,
    pn.ui.Tabs(
        ('Scene Controls', pn.Column(scene_props, light_props)),
        ('Actor Props', actor_props),
        sx={'.MuiBox-root': {"overflowX": "clip"}}
    )
)

pn.Column(
    "This example demonstrates the use of **VTK and pyvista** to display a *scene*",
    pn.Row(
        vtkpan,
        controllers
    ), min_height=600
)
```

### Served App

```python
if pn.state.served:
    pn.ui.Page(
        main=[vtkpan],
        sidebar=[controllers],
        title="VTK - Mt. St Helens",
    ).servable()
```
