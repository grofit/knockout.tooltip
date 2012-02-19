# Knockout.Tooltip

A simple binding for knockout 2.0 to enable qtip2 tooltips via data bindings.

## Installing

Just add jquery.qtip2, then knockout.tooltip.js to your project, as it relies upone the jquery qtip2 library, which in turn relies upon Jquery.

## Example

A simple example of adding a tooltip with content:
```
<a id="some-anchor" data-bind="tooltip: 'This is an anchor, could be a link if you wanted'" /> 
```

An example of a tooltip with content and a title:
```
<a id="some-anchor" data-bind="tooltip: { content: 'Some content goes here', title: 'Anchor Title' }" /> 
```

You can also use options to change element specific tooltips
```
<input id="some-input-element" type="text" data-bind="tooltip: { content: 'Content here', options: { hide: { event: 'unfocus' } } }" />
```

Finally there is some default behaviour pre-set for tooltips, which can be overridden like so, giving all tooltips the same behaviour:
```
ko.bindingHandlers.tooltip.defaultTooltipOptions = { hide: { event: 'unfocus' }, style: { classes: 'ui-tooltip-red' } }
```