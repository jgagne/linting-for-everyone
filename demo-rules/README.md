# Browser demo rules

Import these YAML files into [ProseLint Web](https://proselintweb.com/editor) alongside Vale Std.

- **PlainLanguage.yml** suggests simpler words, such as “use” instead of “utilize”. It is unchanged from the Apify rule.
- **ClickHere.yml** flags vague link text and explains why descriptive links matter. For browser import, it uses `tokens` with `nonword: true` instead of `raw`. The matching pattern and feedback are unchanged.
- **FillerWords.yml** flags “simply”. This demo excerpt keeps one check from the Apify rule to avoid duplicating the link check.

These rules are based on [Apify Vale styles](https://github.com/apify/vale-rules). The browser adaptations were tested in ProseLint Web.

For compatibility details, see the [ProseLint Web import documentation](https://proselintweb.com/blog/custom-rules-proselint-web-v020) and [Vale existence checks](https://docs.vale.sh/checks/existence).
