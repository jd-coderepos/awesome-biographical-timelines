# Contributing

Thanks for considering a contribution. This list only accepts resources directly about extracting, generating, or structuring **biographical information from text** — knowledge graphs of people and life events, biographical event/relation extraction, or person-centric timeline construction. General-purpose timeline summarization or knowledge-graph-construction work is in scope only where it's directly relevant (e.g. it's the closest existing method for a related sub-problem).

## Before you submit

- Search the README and open PRs/issues to avoid duplicates.
- Link to the primary source (paper, official dataset page, or official repository) rather than a blog post or secondary write-up, where one exists.
- One entry per pull request is easiest to review; batch related additions if they're from the same paper.

## Format

Each entry is a single list item:

```
- [Title](https://link-to-resource) - One-sentence, factual description.
```

Rules enforced automatically by CI (`awesome-lint`), so a failing check usually points at one of these:

- The description starts with a capital letter and ends with `.`, `!`, `?`, or `…`.
- The link and description are separated by ` - ` (a plain hyphen with a space on each side — not an em dash or en dash).
- No link may appear more than once in the whole file, even across sections.
- No trailing whitespace, no broken Markdown.

Add the entry to the right section:

- **Datasets & Benchmarks** — corpora, benchmarks, and knowledge bases.
- **Methods** — systems, pipelines, and papers that do the extraction, generation, or construction.

Place it near thematically related entries rather than strictly alphabetically.

## How to submit

1. Fork the repo and add your entry.
2. Open a pull request. Two automated checks run:
   - **Lint** — validates formatting against the rules above.
   - **Link check** — verifies the link resolves.
3. A maintainer reviews once checks pass.

Don't want to open a PR yourself? Open an issue with the **Suggest a resource** template instead.

## Reporting a broken link

Links are also checked automatically on a weekly schedule, which files an issue if any are found dead. If you spot one in the meantime, feel free to open an issue or PR directly.
