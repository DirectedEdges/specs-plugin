# Layout Columns

The plugin enables users to arrange specs artwork and content in the [Properties](../properties.md), [Modes](modes.md) and [Layout](../layoutandspacing.md) sections in a vertical stacked or multi-column format.

The *Layout columns* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [What is included](#whatisincluded)
* [How it works](#howitworks)
* [Examples](#examples)

## What is included <a id="whatisincluded"></a>

By default, the plugin vertical arranges side-by-side displays of specification content (on the left) and artwork (on the right). Alternatively, you can set the plugin to automate the arrangement of artwork/content combinations into 2, 3, or 4 columns and also resize overall spec width to reflow those columns after specs are generated.

## How it works <a id="howitworks"></a>

When specs are set to layout in two or more columns, the plugin will:

* Generate specification displays as it would for a one column default display
* Identify the max width of artwork and content frames
* Set the mininum width of all artwork frames to match the maximum existing width
* Set the width of all content frames to the maximum content frame width
* Set the width of each section and subsection to enable display of the selected quantity of columns
* Add blank "spacer" exhibits, a common techique in CSS's flexbox, to sustain equal column widths as displays wrap across two or more rows

For sections and subsections that include fewer or more items than the column quantity, commensurate whitespace will remain to the right the last item in the last row.

Once the specs are generated, a user can adjust the width of the `Specification` frame and spec artwork and content will adjust and resize within the layout (such as to show five columns) within reasonable limits.

## Examples <a id="examples"></a>

### Three columns, resized

You can resize the `Specification` layer and items should adjust the size to fill the space until sufficient space for another column is available.

### Four columns

### Five columns

You can resize the `Specification` layer after specs are generated to show more items per row.