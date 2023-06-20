Experiments with self-hosted webfonts embedded in SVG

SVGs created in Affinity Designer with various export options selected. Adobe Illustrator will have its own magic combination of settings that work best.

Each SVG had the following manually added to it:

```html
<defs>
<style type="text/css">
    @import url("/webfonts.css");
</style>
</defs>
```

To test, ensure that you don't have Playfair Display or Lato activated locally.

```bash
python3 -m http.server
```

 `example.svg` appears to render correctly in Chrome and Safari. In Firefox, the Lato text is misaligned.

 `example_no_viewbox.svg` and `example_default_text_spans.svg` can be ignored.

 `population-projections-vs-estimates.svg` has misplaced text. I suspect this could be corrected by tinkering with the settings, though not necessarily for every browser.