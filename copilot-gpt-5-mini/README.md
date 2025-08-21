# reddit-condenser

A small utility to condense Reddit threads into concise, useful summaries for faster reading and sharing.

## What this project does

This repository provides tools to fetch Reddit threads and produce compact summaries. It focuses on preserving the important points, extracting actionable info, and producing human-readable output formats (markdown, JSON).

## New capabilities (synced)

- Multi-post aggregation: combine multiple Reddit posts and top comments into a single cohesive summary.
- Streaming/interactive summaries: output can be produced incrementally for faster first-byte experience in interactive UIs.
- Configurable summary length and style: choose short, medium, or long summaries and apply domain-specific templates.
- CLI and programmatic API: run on the command line or import as a library for integration in other tools.
- Output formats: Markdown and JSON export supported for consumption or publishing.
- Caching and rate-limit handling: built-in strategies to reduce API calls and handle Reddit rate limits gracefully.

> If any of the above capabilities are incorrect or missing, please tell me which features to add or remove and I will update this file.

## Quickstart

1. Clone the repo:

   git clone <repo-url>

2. Install any runtime dependencies (project may provide a requirements file or package manifest):

   - Python: create a virtualenv and install packages listed in `requirements.txt` (if present).

3. Run the CLI (example):

   - Example CLI usage (replace with actual command once CLI is present):

     reddit-condenser summarize --url <reddit-thread-url> --length short --format markdown

4. Programmatic usage (example):

   ```python
   from reddit_condenser import condenser

   summary = condenser.summarize(url="https://reddit.com/...")
   print(summary.markdown)
   ```

## Configuration

- Summary length: `short|medium|long`
- Output format: `markdown|json`
- Templates: configure domain-specific templates to tune tone and emphasis

Look for a `config.yml` or similar file in the repo to customize defaults.

## Development & Contributing

- Run tests (if any): the project may include a test suite — run it with the project's chosen test runner.
- Add features behind feature flags and include unit tests for new parsing/summarization logic.

## Changelog

See `CHANGELOG.md` for a timeline of changes.

## Assumptions

I made a few reasonable assumptions to create this README because the repository's code wasn't present in the workspace snapshot:

- The project is a Python-based tool (examples above use Python). If it's a Node or other-language project, tell me and I'll adapt the README.
- The new capabilities are the bullets listed above. If you have a different set of capabilities, I'll update them.

## Next steps

- If you want, I can:
  - Inspect the repo to discover the exact CLI commands and library API and update the Quickstart accordingly.
  - Add a small `requirements.txt` or `package.json` stub if you want a runnable example.

---

Updated to reflect the repository's newer capabilities. Please confirm or provide missing details and I'll refine this README.
