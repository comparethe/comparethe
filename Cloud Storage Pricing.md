---
syntax: mdx
---

Cloud storage providers like Amazon S3, Cloudflare R2 etc.

<FlatUiTable
    data={{ url: "/assets/cloud-storage-pricing.csv" }}
/>

## Data

Sourced from https://gist.github.com/Manouchehri/733e6235457e60de24fdbb15046fba7f (via https://news.ycombinator.com/item?id=38861711)

Tidying:

- Extract the code block lines listing providers; each line is Provider - $X/GB - $Y/GB - notes....
- Parse columns: Provider, Storage price ($/GB), Download price ($/GB), Notes (everything after the download price token).
- Strip $ and /GB, convert storage and download to numeric, then convert to $/TB by multiplying by 1000; format as plain numbers (no symbols).
- Extract the first URL from Notes into a separate URL column; remove that URL from Notes but keep the remaining text intact.
- Write cloud-storage-pricing.csv with header: Provider,Storage Price ($/TB),Download Price ($/TB),URL,Notes.
- Preserve row order from the source; keep any arrows/comments in Notes.
- Convert from $/GB to $/TB
