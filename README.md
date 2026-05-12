# AI Prompt Benchmark

Simple benchmark cases for comparing prompt quality in small frontend tasks.

## Repository Structure

```text
test-create/
  bad/
  good/

test-update/
  bad/
  good/
```

Each scenario is split into:

- `bad/`: weaker or less specific prompt setup
- `good/`: stronger or more detailed prompt setup

Typical files inside each case:

- `*-prompt.md`: the prompt used for the task
- `index.html`: the generated or updated single-file app
- `*-result.md`: execution notes or summary

## Current Scenarios

### `test-create`

Compares prompt quality when creating a Todo List UI from scratch.

### `test-update`

Compares prompt quality when updating an existing Todo List UI while preserving the original logic and features.

## How To Use

1. Open a scenario folder such as `test-update/good/`
2. Read the prompt file
3. Review the resulting `index.html`
4. Compare the paired `bad/` and `good/` outputs

You can open each `index.html` directly in a browser because these examples use plain HTML, CSS, and Vanilla JavaScript.

## Goal

This repository is intended to make prompt differences easier to inspect by comparing:

- clarity of requirements
- quality of UI output
- preservation of existing features
- completeness of work summary

## Notes

- No backend or database is required for these examples.
- The Todo examples persist data with `localStorage`.
- Result files may include timing notes and short implementation summaries.
