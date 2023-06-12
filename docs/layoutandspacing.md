# Layout and spacing

* [What it includes](#whatitincludes)
* [How it works](#howitworks)
* [FAQs](#faqs)
* [Examples](#examples)

## What it includes <a id="whatitincludes"></a>

The Layout and Spacing section includes:
* Content that specifies relevant layout attributes
* Visual annotations in artwork overlaid and adjacent to the relevant element layer

Relevant content includes:
* Element name
* Element Figma layer type (indicated by an icon)
* Visual autolayout attributes, such as:
  * `Layout direction`
  * `Layout alignment`
  * `Vertical resizing` (such as `Fixed`, `Hug` and `Fill`)
  * `Horizontal resizing` (such as `Fixed`, `Hug` and `Fill`)
  * `Padding`
  * `Padding left`
  * `Padding top`
  * `Padding right`
  * `Padding bottom`
  * `Item spacing` (sometimes referred to as "gap")

Relevant visual annotations include:
* Element overlay (blue)
* Padding overlay (green)
* Item spacing overlay (orange)
* Padding markers
* Item spacing markers
* Layout direction icon (pointer to the right or down)
* Layout alignment icon (3x3 grid with cell filled to identify alignment, such as "top right")
* Resizing markers, denoting `Fill`, `Fixed` or `Hug`

## How it works <a id="howitworks"></a>

The plugin traverses the item to find any layer configured with Figma autolayout to create an exhibit for that layer.

## FAQs <a id="faqs"></a>

### Can I choose to simplify annotations to not include so much "marker junk" on the periphery?

Not all users value markers for attributes like resizing, alignment and direction. A request for [a setting to hide these markings](https://github.com/EightShapes/specs-plugin/issues/79) is in the backlog.

## Examples <a id="examples"></a>
![image](https://github.com/EightShapes/specs-plugin/assets/1165904/a2ccab12-d9fb-4b96-b351-b92c9747edad)
