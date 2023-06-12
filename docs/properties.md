# Properties

* [What it includes](#whatitincludes)
* [How it works](#howitworks)
* [FAQs](#faqs)

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/6b5395e7-c7cf-4bad-88ed-74a135f20604)

## What it includes <a id="whatitincludes"></a>

* A subsection for each Variant property that has all options defined for it relative to the selected configuration
* A subsection for each Boolean property included in the selected item (for instance and component types) or default instance (for a selected component set)

## How it works <a id="howitworks"></a>

For component instances, the plugin iterates through each property to highlight differences per option. For variant props, the plugin compares a default with each alternative option by traversing layers and comparing relevant attributes of each layer to find and display differences.

Boolean props are simplified displays to highlight the property type, default value, and impacted layers marked with a blue highlight. While nearly all boolean props are associated with a single layer in practice, the list of associated layers scales to potentially list two or more.

## FAQs <a id="faqs"></a>

### What if variants vary together, such that combinations of two variant properties result in different visual attributes?

This is referred to as a "compound props" case, where property combinations (such as type and color mode) are required to fully document how styles changes. While not automated, spec authors can run the plugin against different instance configurations to quickly if manually assemble a “compound property” display.

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/b5b35ecb-00b2-499e-84a7-8476e242b506)
