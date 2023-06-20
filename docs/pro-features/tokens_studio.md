# Tokens Studio formatting

* [What it includes](#whatitincludes)
* [How it works](#howitworks)
  * [Supported attributes](#supported)
  * [Attributes not supported](#notsupported)
* [Examples](#examples)

The EightShapes Specs plugin Pro upgrade formats attributes as tokens managed by the [Tokens Studio for Figma](https://docs.tokens.studio/) plugin available in the [Figma Community](https://www.figma.com/community/plugin/843461159747178978/Tokens-Studio-for-Figma-(Figma-Tokens)).

<img width="447" alt="CleanShot 2023-06-12 at 10 41 08@2x" src="https://github.com/EightShapes/specs-plugin/assets/1165904/51cbcfc8-1de7-43dd-bc58-3bff0b99f05f">

## What it includes <a id="whatitincludes"></a>

* Hardcoded values are replaced with detected Tokens Studio tokens in all three sections: Anatomy, Properties, and Layout and Spacing.
* Tokens Studio tokens, when detected, are favored over both hardcoded attribute values as well as applied Figma styles for color, text and effects. When both a Figma style and Token Studio token are encountered, the Tokens Studio token is displayed.

## How it works <a id="howitworks"></a>

To display Tokens Studio tokens:

1. Open the EightShapes Specs plugin.
2. Click on the Upgrade button.
3. Checkout to subscribe to EightShapes Specs plugin Pro.
4. Select one or more items to which Tokens Studio tokens have been applied.
5. Click on the Create Specs button.
6. View results

### Supported attributes <a id="supported"></a>

Relative to Tokens Studio's [available properties](https://github.com/tokens-studio/figma-plugin/blob/main/src/constants/Properties.ts), the EightShapes Specs plugin currently supports the following attributes:

* `Background blur`
* `Border color`
* `Border radius`
* `Border radius bottom left`
* `Border radius bottom right`
* `Border radius top left`
* `Border radius top right`
* `Border width`
* `Border width bottom`
* `Border width left`
* `Border width right`
* `Border width top`
* `Box shadow`
* `Dimension`, as applied to:
  * `Spacing` > `Gap`, `All`, `Left`, `Right`, `Bottom`, `Top`
  * `Sizing` > `Height`, `Width`
  * `Border Radius` > `All`, `Top`, `Bottom`, `Right`, `Left`
  * `Border Weight` > `All`, `Top`, `Bottom`, `Right`, `Left`
  * `Background blur`
* `Fill`
* `Font family`
* `Font size`
* `Height`
* `Horizontal resizing`
* `Item spacing` (in Token Studio, `Gap`)
* `Line height`
* `Layer blur`
* `Layout alignment`
* `Layout direction`
* `Letter spacing`
* `Opacity`
* `Padding top`
* `Padding bottom`
* `Padding left`
* `Padding right`
* `Paragraph indent`
* `Paragraph spacing`
* `Sizing`, as applied to:
  * `Sizing` > `Height`, `Width`
* `Spacing`
* `Text align horizontal`
* `Text case`
* `Text decoration`
* `Typography`
* `Vertical resizing`
* `Width`

### Attributes not supported <a id="notsupported"></a>

The following attributes to which Token Studio tokens can be applied are not detected by the EightShapes Plugin.

* `Alpha` (the `a` of `rgba` values)
* `Asset`
* `Border` as a composite of `borderColor`, `borderWidth` and `borderStyle`
* `Composition` is not supported, due to:
  * `Composition` can be applied to a layer simultaneously with other Tokens Studio values (like `Fill` color), and Tokens Studio API returns both tokens as validly applied. To deconflict and determine which token "wins" would be complicated and computationally expensive.
  * `Composition` (which can combine attributes like `Fill`, `Border width left`, `Corner radius` and `Padding top`) would require decomposition into distinct attributes to jointly and individually be compared across all layers, options, props and anatomy elements compared by the specs plugin. Implementation complicatedness and computational cost (1,000s of potential per run) carry significant risk to EightShapes Specs plugin performance and stability compared to benefit and relative priority of other potential plugin features at this time.
  * Simply showing `Composition` when present is under consideration, but would run counter to expectations of how attributes are shown based on layer differences across variants. Since it's impossible (for now) to deconflict a `Composition` with other attributes, it could result in misleading displays.
  * Custom `Composition` is neither supported by existing native Figma capabilities nor indicated on Figma's near-term roadmap.
* `Description`
* `Dimension`, as applied to:
  * `Sizing` > `All`, which sets both height and width simultaneously such that neither is detected.
  * `Border width`, when all sides (`Top`, `Bottom`, `Left` and `Right`) are individually set and resolve to the same value, such as 8px. In this case, Figma does not return a `Mixed` value even though there are separate tokens applied by Tokens Studio.
  * `Border radius`, when all corners (`Top left`, `Bottom left`, `Top right` and `Bottom right`) are individually set and resolve to the same value, such as 8px. In this case, Figma does not return a `Mixed` value even though there are separate tokens applied by Tokens Studio.
* `Font weight`
* `Sizing`, as applied as:
  * `Sizing` > `All`, which sets both height and width simultaneously such that neither is detected.
* `Visibility`

## Examples <a id="examples"></a>

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/a89e94e6-28ad-440d-bc28-da3988a26df8)
Comparing Anatomy attributes of basic outputs (on the left) versus Token Studio tokens (on the right)

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/edba0906-312e-44eb-9e7b-8eac878fbe30)
Comparing Layout and spacing attributes of basic outputs (on the left) versus with Token Studio tokens (on the right)


