# Two Way Comparisons

The plugin can compare all attributes and props of nested instances across every combination of two properties of an instance or component. For example, if a button has properties for `state` (such as `default`, `hover`, and `focus`) and `variant` (such as `filled`, `outline` and `text`), the plugin will compare all layers across all combinations of both properties.

The *Two way* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [Why use this feature](#whyuseit)
* [What is included](#whatisincluded)
* [How it works](#howitworks)

## Why use this feature <a id="whyuseit"></a>

Imagine a Button component with three properties:

* `variant` (`filled`, `outline` and `text`)
* `state` (`default`, `hover` and `active`)
* `size` (`small`, `medium`, and `large`)

By default, the Properties section will start with the configuration of the selected item and compare variants in each direction. For example, if the selected item has a configuration of `variant`:`default`, `state`:`default` and `size`:`medium`, then the plugin creates a subsection per property:

* For `variant`, a comparison of `filled`, `outline` and `text` where `state`:`default` and `size`:`medium` 
* For `state`, a comparison of `default`, `hover` and `active` where `variant`:`default` and `size`:`medium` 
* For `size`, a comparison of `small`, `medium`, and `large` where `variant`:`default` and `state`:`default`

However, this does not cover many possible combinations, such as comparing `state`s when `variant` is `outline`, `size`s when `state` is hover, and `variant` when `size` is large.

## What is included <a id="whatisincluded"></a>

When an two way comparison is generated, the plugin will display artwork for every combination of two properties hierarchichally.

## How it works <a id="howitworks"></a>

When the two-way setting is enabled and one component or instance with two or more variant properties is selected, the plugin will enable the user to select properties (property level 1 and property level 2) in separate menus.

Based on the pair of configured properties, the plugin will:

* Display the two-way comparison as the first section of Properties
* Create a subsection for every option (`filled`, `outline` and `text`) of the first property (such as `variant`)
* Create an exhibit (artwork and specs content) for every option (`default`, `hover` and `active`) of the second property within each subsection, corresponding to the option of the first property
* Compare layers across all options (columns) within a row
* Compare layers of the same option (column) across each row
