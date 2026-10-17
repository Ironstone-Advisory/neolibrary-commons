# NeoLibrary Commons

*Curated by Rob Tyrie, Ironstone Advisory · [ironstoneadvisory.com](https://ironstoneadvisory.com) · [@robtyrie](https://github.com/robtyrie)*

**The open test dataset for [NeoLibrary](https://github.com/Ironstone-Advisory/neolibrary): the Grey Swan Guild sessions corpus.**

NeoLibrary is the engine. This repo is the first dataset it is built and tested against. Content here belongs to its original authors and is shared under Creative Commons Attribution 4.0 (CC BY 4.0).

## Attribution

Use this block wherever the corpus, or anything derived from it, appears:

> Source: Grey Swan Guild (greyswanguild.org), licensed CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Adapted by Ironstone Advisory; changes were made.

Individual items keep their own author and session credits in their metadata.

## Layout

```
corpus/
  workbooks/     longer synthesized works: YYYY-MM-DD-slug/
  sessions/      one folder per session: YYYY-MM-DD-slug/
    item.md      the content (transcript, notes, summary)
    meta.yaml    title, date, speakers, source URL, license, changes made
manifests/
  index.csv      one row per item, generated
schema/
  meta.schema.json
```

## meta.yaml fields

| Field | Required | Example |
|---|---|---|
| `title` | yes | "Grey Swan Watch, Episode 12" |
| `date` | yes | 2023-05-04 |
| `speakers` | yes | list of names as credited |
| `source_url` | yes | where the original lives |
| `license` | yes | `CC-BY-4.0` |
| `changes` | yes | what Ironstone changed: "transcribed", "cleaned", "summarized" |
| `sha256` | yes | hash of `item.md` |

## Adding material

1. Only add items the Guild published under CC BY 4.0, or that the author has licensed that way in writing.
2. Fill every required field in `meta.yaml`. Say what you changed.
3. Do not add private chats, emails or member data. Public sessions only.

## Status

First item loaded: *The Uncertain Edge* workbook (April 2025). Sessions are being loaded in batches.

## License

Content: [CC BY 4.0](LICENSE). To cite the corpus, use [CITATION.cff](CITATION.cff). The NeoLibrary engine itself is Apache 2.0 and lives in a separate repo.
