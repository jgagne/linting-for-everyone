# Linting for everyone

Linters for prose: Vale checks writing against your style guide, and markdownlint keeps Markdown clean. Consistent feedback for people and agents, with human judgment still part of the workflow.

## Slides

- [Linting for everyone](https://jgagne.github.io/linting-for-everyone/)
- [index.md](index.md) (source)

```bash
# HTML
npx @marp-team/marp-cli index.md --html --allow-local-files -o index.html

# PDF
npx @marp-team/marp-cli index.md --html --allow-local-files -o linting-for-everyone.pdf
```

With Marp CLI installed, `bash build-slides.sh` also rebuilds the HTML and keeps the presentation backdrop white.

Built with [Marp](https://marp.app).

## Editor demo

Open the [editor demo](editor-demo/) for the draft, revised text, bundled Vale rules, and VS Code setup shown in the slides.

## Browser demo

Open [ProseLint Web](https://proselintweb.com/editor), enable Vale’s standard rules (the package named **Std**), and paste this Markdown:

```markdown
# Getting started

You can utilize the tool to simply extract data.

[Click here](https://example.com) to learn more.

You do not need an account.

The file was created by the tool.
```

1. Start with the standard rules. Review the suggestions for “do not” and “was created”.
2. Import [PlainLanguage.yml](demo-rules/PlainLanguage.yml) and [ClickHere.yml](demo-rules/ClickHere.yml) from Custom Rules → Import. These add simpler wording and descriptive link text.
3. Revise and check again. Then import [FillerWords.yml](demo-rules/FillerWords.yml) to catch “simply”.

The [demo rules](demo-rules/) are based on [Apify Vale styles](https://github.com/apify/vale-rules), with adaptations for browser import.

Zero findings means the enabled checks passed. Review the writing, too.

## Resources

- [Vale quickstart](https://docs.vale.sh/topics/quickstart)
- [markdownlint](https://github.com/DavidAnson/markdownlint)
- [Vale agent skills](https://vale.sh/skills)
