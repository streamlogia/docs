# Streamlogia Docs

Documentation site for [Streamlogia](https://streamlogia.com), built with [Mintlify](https://mintlify.com).

## Running locally

### Prerequisites

Install the Mintlify CLI:

```bash
npm install -g mint
```

### Start the dev server

```bash
mint dev
```

The site will be available at `http://localhost:3000`.

## Structure

```
.
├── mint.json               # Navigation, theme, and site config
├── introduction.mdx        # Landing page
├── quickstart.mdx          # "Ship your first log in 2 minutes" guide
├── authentication.mdx      # API key overview
├── api-reference/
│   ├── ingest.mdx          # POST /v1/ingest
│   ├── stream.mdx          # WebSocket stream
│   ├── list-logs.mdx       # GET /v1/projects/:id/logs
│   ├── log-stats.mdx       # GET /v1/projects/:id/logs/stats
│   ├── organisations.mdx   # Org CRUD
│   ├── projects.mdx        # Project CRUD
│   ├── api-keys.mdx        # API key reference
│   └── errors.mdx          # Error codes and handling
└── sdks/
    ├── javascript.mdx      # Node.js / JS SDK
    ├── python.mdx          # Python SDK
    ├── go.mdx              # Go SDK
    └── curl.mdx            # cURL examples
```

## Editing content

Pages are written in [MDX](https://mdxjs.com/) and support standard Markdown plus Mintlify components (`<Note>`, `<Warning>`, `<CodeGroup>`, `<ParamField>`, `<ResponseField>`, `<Card>`, `<Steps>`, etc.). Refer to the [Mintlify component docs](https://mintlify.com/docs/content/components) for the full list.

## Navigation

All navigation is defined in `mint.json` under the `navigation` key. Each entry is a group with a label and a list of page paths (without the `.mdx` extension):

```json
{
  "group": "Ingest",
  "pages": [
    "api-reference/ingest",
    "api-reference/stream"
  ]
}
```

Add a new page by creating the `.mdx` file and adding its path to the relevant group in `mint.json`.

## SDK samples

Code samples in `sdks/` follow the official SDK repositories:

| SDK | Repository |
|-----|------------|
| JavaScript | [streamlogia/javascript-sdk](https://github.com/streamlogia/javascript-sdk) |
| Python | [streamlogia/python-sdk](https://github.com/streamlogia/python-sdk) |
| Go | [streamlogia/go-sdk](https://github.com/streamlogia/go-sdk) |

When an SDK changes, update the corresponding `sdks/*.mdx` file to match.
