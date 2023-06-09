# Anatomy

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/6371108a-b40f-4823-90d7-ce64dcd7989f)

## What it includes

The Anatomy section includes:

1. An itemized element list (the "content") that can include:
  * All text, line, polygon, star, rectangle, and similar layers encountered
  * All frame layers to which relevant attributes are associated
  * All nested component instances, but _not_ any children layers within those nested instances
2. A frame (the "artwork) that includes a cloned version of the selected item and annotated markers associating each element with the enumerated item in the list

Relevant content can include:
* Element name
* Element Figma layer type (indicated by an icon)
* Dependency ("Depends on"), associating a nested instance with it's origin component
* Visual attributes, such as `background color`, `width` and `opacity`, that – if Properties is also produced – are limited to those that do not vary across property options
* Configured property values of nested instances

## How it works

To produce the anatomy, the plugin traverses the node’s layers to itemize and mark text, instances, and other shapes as elements.

Each itemized component is enumerated in the content, with instances highlighting dependency name and relevant prop values and other nodes reflecting visual attributes and styles. In the artwork, markers are placed on the periphery, prioritizing the left edge and finding a location on any edge that hasn’t already been used.

The plugin stops traversing into a the hierarchy of a component (like Card) when it runs into a nested component (like CardText). Spec authors are encouraged to run the plugin again on each relevant nested component. Refer my writing on Subcomponents for learn more.

The results work for most practical component displays, even if it’s not perfect. In extreme cases, components with many sibling elements “cross the streams” (nod to Ghostbusters) of each marker’s tail and many components left unmarked. In these cases, spec authors can prune and tailor what markers work best.

## Examples

### Material modal date picker

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/81ff8fd9-6438-4297-b767-7dab7aa1291f)

In this extreme example, the Anatomy itemizes every cell of the calendar. As markers surround the date picker in a first ring, the plugin then begins including a second ring of markers slightly offset until those, too, run out of space. For each element, the plugin attempts to place a marker on all four sides in the first ring, then all four sides of the second ring, and then gives up.
