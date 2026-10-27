# Browser demo rules

Import both YAML files into ProseLint Web alongside Vale Std.

PlainLanguage.yml is unchanged from ApifyStyleGuide/styles/Apify/PlainLanguage.yml.
ClickHere.yml retains the original regex, raw scope, severity, and diagnostic. It uses `tokens` plus `nonword: true` instead of `raw`, because the original raw-only rule failed browser import. The adapted version imported and exported unchanged and ran successfully in Firefox.

The original and adapted ClickHere rules produced identical findings locally for all four configured link labels and negative controls (descriptive link and plain prose).

Verified sequence: std-demo.md with Std alone gives 2 suggestions; adding both custom rules gives 1 warning and 3 suggestions; std-demo-final.md gives 0 findings. Drafts are in ../vale-drafts-demo/ and screenshots in ../img/demo-01-std-findings.png, demo-02-std-plus-apify.png, and demo-03-clean.png.

References:

- [ProseLint Web import/export documentation](https://proselintweb.com/blog/custom-rules-proselint-web-v020)
- [Vale existence: tokens, raw, and nonword](https://docs.vale.sh/checks/existence)

## Third-rule reveal

FillerWords.yml is a demo excerpt of the existing Apify.FillerWords rule with only its `simply ` removal retained. The complete source also flags “Click here”, duplicating the link check. The excerpt preserves the original severity and diagnostic.

After the first two custom rules pass, adding this third rule flags “simply”. Removing it produces zero findings under Std plus all three demo rules. Verified in Firefox; captures: demo-04-filler-reveal.png and demo-05-complete.png. Final text: ../vale-drafts-demo/std-demo-complete.md.
