# Custom spec formatting

You can generate, customize and apply custom styling to format spec outputs with your preferred typography and colors, including colors for light and dark modes of both spec output content and artwork.

This feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [How it works](#howitworks)
* [Customizing outputs](#customizingoutputs)
* [FAQs](#faqs)

## How it works <a id="howitworks"></a>

To apply custom spec formats, configure the `Spec styling` property displayed in the DISPLAY PREFERENCES revealed to Pro subscribers.

#### `None` (default)

When set to `None`, the plugin formats specs with hardcoded colors and text attributes (such as `Font name` and `Font size`) using default values shipped with the plugin.

#### `Use local styles`

When set to `Use local styles`, the plugin will find relevant styles and, if found, apply each to format spec outputs.

* For typography, the plugin looks for local text styles in the file that begin with `EightShapes Specs`.
* For colors, the plugin looks for relevant variables in the `EightShapes Specs` variables collection.

#### `Add local styles`

When set to `Add local styles`, the plugin will find relevant styles and, if found, apply each to format spec outputs.
If the relevant text style or color variable is not found, the plugin will add it to the local file and apply it when producing outputs.

#### `Reset local styles`

When set to `Reset local styles`, the plugin will reset both local text styles and color variables to the default values shipped with EightShapes Specs.

🚨 This will override any customizations you've made to EightShapes Specs plugin text styles and color variables you've made since initially generating them. 🚨

For text styles, the plugin will reset the `Font name` and `Font size` of existing text styles it can find to EightShapes Specs default values. For text styles that cannot be found, the plugin will create a new text style.

For color variables, the plugin will first attempt to find the `EightShapes Specs` variable collection. If it cannot be found, the entire variable collection is created from scratch. If the collection is found, then then plugin will reset value(s) of individual variables it can find. Variables that cannot be found are created from scratch.

### Customizing outputs <a id="customizingoutputs"></a>

Once text styles and color variables are added to the document, you can customize attributes of each.

For example, if your design system's primary `Font name` is `IBM Plex Sans`, you can update the `Font name` each text style to that font name. Subsequent runs of the plugin that configure the `Spec styling` to `Use local styles` or `Add local styles` will continue to apply these updated text styles to spec outputs.

// Add screenshot

Similarly, imagine you would like spec dark mode backgrounds to apply `#1F2328` as the dark mode background color and `#4787DF` as the dark mode spec style and variable pill label color.

// Add screenshot

## FAQs <a id="faqs"></a>

#### Can I associate spec output styling with other text styles and color styles or color variables in the local file or a library?

At this time, the plugin does not support mapping styling formats to other preexisting styles in your local file or in a separate library. To support adding this feature, upvote Issue [#39:Map user-generated text and color styles to plugin output](https://github.com/EightShapes/specs-plugin/issues/39).

#### The EightShapes Specs color variables and text styles show up as publishable when I publish my library. Can the plugin hide those by default?

The Figma plugin API does not yet support setting text styles, variables and variable collections to hide from publishing. When the API supports that, the Specs plugin will hide styles and / or variables from publishing by default.