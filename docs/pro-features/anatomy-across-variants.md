# Anatomy and Layout Across Variants

The plugin detects additional elements and layout configurations beyond those included in the selected component and displays each in successive additional anatomy and layout rows.

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/522d4f1f-d029-4e98-86ea-0a5a84d3505f)

The *Anatomy and layout across variants* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [What is included](#whatisincluded)
* [How it works](#howitworks)

## What is included <a id="whatisincluded"></a>

When properties are generated, elements and additional layout configurations may be detected in alternatives to the primary variant being annotated. Each will be identified in a successive exhibit, marked in artwork and itemized in relevant attribtes not already displayed in the the Properties section.

## How it works <a id="howitworks"></a>

As the Properties section is generated, each alternative variant is inspected for each property. As variants include distinct elements and layout not already detected, each is inventoried. When the Anatomy and Layout sections are subsequently generated, a row of artwork and annotation is generated for each variant that included one or more additional detected elements.

An element is considered distinct if the combination all following criteria is unique within the inspected frame or component:
1. layer type (such as TEXT or INSTANCE) _and_
2. layer name (such as Settings or Title) _and_
3. layer parent hierarchy (such as Card / Title Lockup / Title) _and_
4. child position of layers at that level of the same type and name

### Examples

* `Card / Title Lockup / Title (TEXT)` is a distinct element from `Card / Title (TEXT)`, since they are at different levels of a layer hierarchy
* `Card / Actions /` with two children both named `Action item` are considered two distinct elements (think of it as `Action item` (1) and `Action item` (2)
* Consider `Card / Title Lockup / Title (TEXT)` as a first child  of `Title Lockup` in variant 1 and `Card / Title Lockup / Title (TEXT)` as a second child in variant 2 (because the first child of `Title Lockup` is an icon instance). Those elements are the _same_ element and would not be included twice in the Anatomy.

