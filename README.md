# Jargon HR public data

Canonical site: **https://miaotuijian.cn/**
GitHub mirror: https://github.com/vickeyfeng/jargon-hr-data
Data page: https://miaotuijian.cn/data/
Last updated: 2026-11-10

This repository is a citable mirror of the machine-readable data behind Jargon HR, a free, private, rule-based job-description checker.

## Contents

| File | What it is |
|---|---|
| `data/glossary.json` | 33 bilingual hiring and job-market terms: definition, Chinese explanation, why it matters, example, related terms |
| `data/market-facts.json` | UK/US/DE/FR/NL facts (17 total) with official source URLs and pack versions; EU fallback has no country facts |
| `data/examples.json` | Metadata and scores for the seven static example reports |
| `llms.txt` | LLM entry point with canonical links and high-value definitions |
| `llms-full.txt` | Full text corpus: method, market packs, FAQ, glossary, comparisons, changelog |
| `sitemap.xml` | Crawlable URL list |
| `robots.txt` | AI crawler policy and sitemap reference |

## Citation

> Jargon HR. “Jargon HR public data.” 2026-11-10. https://miaotuijian.cn/data/

See `CITATION.cff` for a machine-readable citation. If you use a fact, cite the specific source URL inside `data/market-facts.json` as well.

## Important limits

- Editorial summaries, **not legal, tax, or immigration advice**.
- Market facts can change; verify at the linked source.
- The glossary is a probabilistic reading aid, not a complete dictionary.
- No warranty. No client analytics or tracking is included in this repository.

## License

The JSON datasets and glossary text are licensed under **CC BY 4.0**; see `LICENSE`. Attribute “Jargon HR” and link to https://miaotuijian.cn/.

## Regenerating

This mirror is a copy. The source of truth is the Jargon HR site repository. After changing content:

```bash
cd job-agent/web
node scripts/build-static.cjs
cp data/*.json llms.txt llms-full.txt sitemap.xml robots.txt ../github-data/
```

Do not edit the JSON here by hand.
