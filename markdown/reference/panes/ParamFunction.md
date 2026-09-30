# ParamFunction

ParamFunction panes wrap functions decorated with the param.depends decorator and rerenders the output when any of the function's dependencies change. This allows building reactive components into a Panel which depend on other parameters, e.g. tying the value of a widget to some other output.

Use `pn.ui.ParamFunction` to create this component.

## API

```{autoclass} panel.param.ParamFunction
   :members:
```
