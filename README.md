# Laravelify docs

The documentation at **https://docs.laravelify.cloud**, built with [Mintlify](https://mintlify.com).

```bash
npx mint dev       # preview at http://localhost:3000
npx mint broken-links
```

## Structure

| Path | What |
| --- | --- |
| `docs.json` | Navigation, colors, logo, navbar, beta banner |
| `*.mdx`, `*/` | Pages, grouped like the sidebar |
| `snippets/install-command.mdx` | The install command, the one place its URL is written |
| `logo/`, `favicon.svg`, `images/` | Brand assets |

Push to `main` and Mintlify publishes the change in about a minute.

## Contributing

Fix a typo or improve a page with a pull request. Keep pages short, use the components already in use (`<Steps>`, `<Tabs>`, `<Note>`), and check every command against the panel's code.
