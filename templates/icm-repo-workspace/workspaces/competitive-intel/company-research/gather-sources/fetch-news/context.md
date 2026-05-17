# Fetch news

## Instruction

Collect 3–6 recent news items (within the last 6 months) about the target
company that relate to its products, financial performance, or market
positioning. For each item, record the headline, publisher, date, and URL.

## Input format

A company name, supplied as plain text from the workflow input.

## Output format

`output.md` containing a bulleted list; each item gives the headline,
publisher, date (ISO-8601), and a resolvable URL.

## Error handling

If fewer than 3 relevant items are found, record those that were found and
note the shortfall. Set `status` to `partial` in `metadata.json`.
