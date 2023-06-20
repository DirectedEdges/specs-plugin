# Dark Mode

EightShapes Specs plugin output can be toggled to the EightShapes Specs mode to dark.

The *dark mode* feature is only available via the Pro subscription to the EightShapes Specs plugin, and requires that the file reside in an location that supports two or more modes per variable collection. [read more](#modes)

* [How it works](#howitworks)
* [FAQs](#faqs)

## How it works <a id="howitworks"></a>

When the [Spec Styling](styling-specs.md) setting is set to an option that generates or applies existing styling, a color values are added as a dark mode to the `EightShapes Specs` variable collection.

Once the dark mode variables are available, you can toggle plugin output to dark mode at the page level, specifications or single spec level, and even just for an artwork frame.

### Page level

// Screenshot: page level spec

* Ensure no item is selected on the page
* Click the Mode icon in the `Page` section of the `Design` panel
* Set the `EightShapes Specs` mode to `Light` or `Dark`

### All Specifications or a specific spec

// Screenshot: spec-by-spec

* Selected the `Specifications` frame or an individual spec frame
* Click the Mode icon adjacent in the `Layer` section header of the `Design` panel
* Set the `EightShapes Specs` mode to `Light` or `Dark`

### Artwork frames <a id="artwork-frames"></a>

In the artwork frame, which may combine your item with markers for Anatomy element numbers or Layout padding, you can toggle it specifically for `Light` or `Dark` mode.

* Select the `Artwork` frame. 
    * Pro tip: Press and hold CMD / CTRL while hovering the `Artwork` frame to select it directly.
    * Another pro tip: Press and hold SHIFT + CMD / CTRL to select multiple `Artwork` frames at once.
* Click the Mode icon adjacent in the `Layer` section header of the `Design` panel
* Set the `EightShapes Specs` mode to `Light` or `Dark`

The frame itself, as well as plugin elements like markers and annotations, should swap colors relative to the mode selected. Your artwork, presumably not styled with `EightShapes Specs` variables, should be unimpacted.

// Screenshot: dark artwork within light spec

// Screenshot: light artwork within dark spec

## FAQs <a id="faqs"></a>

#### Why doesn't my `EightShapes Specs` Figma variables collection include a `dark` column? <a id="modes"></a>

Dark mode requires that your account supports two or more modes per variable collection. This depends on your Figma account type, such as (at the time of this writing) Starter accounts that limit variable collections to one mode. In this case, upgrade your Figma account. Additionally, files in Drafts also may limit variable collections to a single mode. In this case, move your file to a project folder.

Then, run the plugin again with the proper [Spec Styling](styling-specs.md) setting to add Dark mode variable values to the collection.

#### When I format a full spec as dark, some elements of my artwork are no longer visible. How can I fix that?

As described in [Artwork frames](#artwork-frames), manually adjust the mode of Artwork frame or adjust the color variable values in the `EightShapes Specs` collection. 
