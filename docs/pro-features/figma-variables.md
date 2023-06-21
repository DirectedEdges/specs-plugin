# Figma Variables Formatting

The plugin will detect, format and compare attribute values mapped to Figma variables.

![VariableFormatting](https://github.com/EightShapes/specs-plugin/assets/1165904/d326e718-35c3-4ecb-b54b-8b4746dc065d)

The *Figma variables formatting* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [What is included](#whatisincluded)
* [How it works](#howitworks)
* [Examples](#examples)
* [FAQs](#faqs)

## What is included <a id="whatisincluded"></a>

For any variable on a supported attribute, the variable is displayed in a pill format and includes the variable collection name, variable name, and variable raw value. For colors, the pill also includes a square swatch corresponding to the variable hex value.

## How it works <a id="howitworks"></a>

When a supported attribute (like `Fill color` or `Width` or `Item spacing`) of an element (like a frame, instance or text) is set to a Figma variable, the plugin will:

- Display that element in the content for that alternative
- Display that attribute value formatted as a Figma variable

For the Properties section, the plugin compares values of many attributes on every node (layer) of every alternative option in a variant set. When a variable is detected on an attribute, the plugin will distinguish that alternative from others that apply a different variable OR a Tokens Studio token OR a hardcoded value, even if that hardcoded value is the same as the variable's value.

## Examples <a id="examples"></a>

![VariablesInProperties](https://github.com/EightShapes/specs-plugin/assets/1165904/f414e29c-b1e0-4298-b128-fc3ee74fc73f)

Background and text color of a component instance mapped to `Alert/Basic/Background` and `Alert/Basic/Element` variables, respectively, of the `ESDS Color` variable collection

## FAQs <a id="faqs"></a>

#### If both a Figma variable and Tokens studio token studio are encountered, what happens?

The plugin prioritizes formats – and, when comparing attributes across properties, distinguishes values – in the following order:

* Figma variable
* Figma style (for color, text and effect)
* Tokens Studio token
* Hardcoded value

The plugin will only display an attribute value based on the first format it encounters. When more than one format could be matched, only the first format is considered.
