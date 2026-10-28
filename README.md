# Linting for everyone

Vale checks prose against your style guide. markdownlint checks Markdown structure. Both give people and agents consistent feedback, while you judge the writing and refine the rules.

## Slides

- [Linting for everyone](https://jgagne.github.io/linting-for-everyone/)
- [index.md](index.md) (source)

## Editor demo

Download and unzip [editor-demo.zip](https://github.com/jgagne/linting-for-everyone/raw/refs/heads/main/editor-demo.zip) for the draft, revised text, bundled Vale rules, and VS Code setup shown in the slides. Open its README for instructions.

## Browser playground

Open [ProseLint Web](https://proselintweb.com/editor), enable its **Std** package (standard rules), and paste this Markdown:

```markdown
# Getting started

You can utilize the tool to simply extract data.

[Click here](https://example.com) to learn more.

You do not need an account.

The file was created by the tool.
```

1. Start with the standard rules. Review the suggestions for “do not” and “was created”.
2. Download [PlainLanguage.yml](demo-rules/PlainLanguage.yml) and [ClickHere.yml](demo-rules/ClickHere.yml), then load them through **Custom Rules → Import**. These add simpler wording and descriptive link text.
3. Revise and check again. Download and import [FillerWords.yml](demo-rules/FillerWords.yml) to catch “simply”. Remove “simply” and check again.

The [demo rules](demo-rules/) are based on [Apify Vale styles](https://github.com/apify/vale-rules), with adaptations for browser import.

Zero findings means the enabled checks passed. Review the writing, too.

## Resources

- [Vale quickstart](https://docs.vale.sh/topics/quickstart)
- [Vale configuration generator](https://vale.sh/generator)
- [Apify Vale styles](https://github.com/apify/vale-rules)
- [markdownlint](https://github.com/DavidAnson/markdownlint)
- [Markdown reference](https://www.markdownguide.org/basic-syntax/)
- [Vale agent skills](https://vale.sh/skills)

### In your editor

- [Vale for VS Code](https://marketplace.visualstudio.com/items?itemName=ChrisChinchilla.vale-vscode)
- [Vale for WebStorm](https://plugins.jetbrains.com/plugin/19613-vale-cli)
- [Vale for Zed](https://zed.dev/extensions/vale)

## Build the slides

```bash
# HTML
npx @marp-team/marp-cli index.md --html --allow-local-files -o index.html

# PDF
npx @marp-team/marp-cli index.md --html --allow-local-files -o linting-for-everyone.pdf
```


Built with [Marp](https://marp.app).
