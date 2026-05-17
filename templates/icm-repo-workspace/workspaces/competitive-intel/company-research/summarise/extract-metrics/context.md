# Extract metrics

## Instruction

From the filing reference and news items produced by gather-sources, extract
the company's most recent reported revenue, its year-over-year revenue growth,
and up to three notable product or strategy moves. Cite the source of every
value.

## Input format

The `output.md` files from `gather-sources/fetch-10q/` and
`gather-sources/fetch-news/`.

## Output format

`output.json` with this shape:

```json
{
  "company": "<name>",
  "revenue": { "value": "<amount or null>", "period": "<period>", "source": "<url>" },
  "revenue_growth_yoy": { "value": "<percent or null>", "source": "<url>" },
  "notable_moves": [ { "summary": "<text>", "source": "<url>" } ]
}
```

## Error handling

Any metric that cannot be sourced is recorded as `null` with a `note` field
explaining why. Set `status` to `partial` if any required metric is null.
