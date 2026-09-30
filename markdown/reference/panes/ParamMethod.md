# ParamMethod

ParamMethod panes wrap methods on parameterized classes and rerenders the plot when any of the method's parameters change. By default ParamMethod will watch all parameters on the class owning the method or can be restricted to certain parameters by annotating the method using the param.depends decorator. The method may return any object which itself can be rendered as a Pane.

Use `pn.ui.ParamMethod` to create this component.

## API

```{autoclass} panel.param.ParamMethod
   :members:
```
