# Spec Nested Subcomponents

To ease the specification of [subcomponents and nested components](https://medium.com/eightshapes-llc/subcomponents-753ce9f6600a) encountered, the **Spec nested subcomponents** setting will add any instance encountered within selected items to also be spec'ed during that plugin run.

The *spec nested components* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [How it works](#howitworks)
* [Examples](#examples)
* [FAQs](#faqs)

## How it works <a id="howitworks"></a>

1. Navigate to the plugin  **Settings** tab.
2. Set the **Spec nested subcomponents** toggle to active.

## Examples <a id="examples"></a>

![Spec nested components](https://github.com/EightShapes/specs-plugin/assets/1165904/16fb37af-0d9e-46b2-aff5-ef31a0880ca3)

The first spec run (on the left, set to [Dark mode](dark-mode.md)) did not include nested components, resulting in only the specification of `Button`. The second spec run (on the right, set to light mode) set **Spec nested subcomponents** to active, resulting in the `Icon` and `Icon art asset` components also being included.

## FAQs <a id="faqs"></a>

#### Will all nested components of a detected nested instance be spec'ed?

Not necessarily. Only nested instances of the _original selected item_ will be spec'ed. If a nested instance has other variants with other nested components within that, those many not be included.
