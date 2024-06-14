# Custom spec formatting

You can generate, customize and apply custom styles and variables to format specification typography, colors, and layout and spacing.

This feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [How it works](#howitworks)
* [Customizing outputs](#customizingoutputs)
* [FAQs](#faqs)

## How it works <a id="howitworks"></a>

To customize specification formats:
1. Subscribe to the Pro version.
2. In the `Settings` tab, select `Typography`, `Color` or `Spacing`.

When the plugin runs, it will generate relevant variables and/or text styles and apply each to your specification output. You can then customize those styles and variables to format current and future specifications.

### `Typography`

For typography, the plugin looks for local text styles in the file that begin with `EightShapes Spec`. If a text style does not exist, the plugin adds the text style to the local file. As specifications are subsequently produced, each text style is applied to relevant frames throughout the output.

EightShapes Spec text styles in local file:

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/ef64d4ca-995e-4942-b7d2-b89b43a1caf1)

Text style applied to spec output:

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/7a57bb75-0ba3-49d8-92dd-0e99bc04339c)

For example, if your design system's primary `Font name` is `IBM Plex Sans`, you can update the `Font name` each text style to that font name. Subsequent runs of the plugin that configure the `Spec styling` to `Use local styles` or `Add local styles` will continue to apply these updated text styles to spec outputs.

![Spec Styling Change Font Name](https://github.com/EightShapes/specs-plugin/assets/1165904/13009a8c-5532-4406-8fdc-4739fff601cd)

### `Colors`

For colors, the plugin looks for relevant variables in a variable collection named `EightShapes Specs`. If a color variable does not exist, the plugin adds the variable to the local variable collection. As specifications are subsequently produced, each color is applied to relevant frames and text throughout the output.

EightShapes Specs variable collection:

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/5ddd6790-af15-455a-8dfd-bd591355ef3d)

EightShapes Specs variable applied to spec output.

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/68fa88cf-2fe5-4416-9eb5-5379e64c0856)

Similarly, imagine you would like spec dark mode backgrounds to apply `#1F2328` as the dark mode background color and `#4787DF` as the dark mode spec style and variable pill label color.

![Spec Styling Change Dark Mode Token Value](https://github.com/EightShapes/specs-plugin/assets/1165904/b69ffafd-3702-488d-954b-379e0f9f78ac)

### `Layout and spacing`

For layout, the plugin looks for relevant variables in a variable collection named `Specs Layout`. If a layout and spacing variable does not exist, the plugin adds the variable to the local variable collection. As specifications are subsequently produced, each layout variable is applied to relevant frames throughout the output.

Specs Layout variable collection:

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/2bb266d9-338f-48f2-8188-9747bacc6bc6)

Specs Layout variable applied to spec output:

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/741e44ba-94d6-4ae2-ac96-4fa69694bf14)

## FAQs <a id="faqs"></a>

#### Can I associate spec output styling with other text styles and color styles or color variables in the local file or a library?

At this time, the plugin does not support mapping styling formats to other preexisting styles in your local file or in a separate library. To support adding this feature, upvote Issue [#39:Map user-generated text and color styles to plugin output](https://github.com/EightShapes/specs-plugin/issues/39).

#### Color variables and text styles added by the plugin show up as publishable when I publish my library. Can the plugin hide those by default?

The Figma plugin API does not yet support setting text styles, variables and variable collections to hide from publishing. When the API supports that, the Specs plugin will hide styles and / or variables from publishing by default.
