<p align="center">
  <a href="https://docs.laravelify.cloud">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/laravelify-cloud/laravelify/main/brand/laravelify-brand-assets/04-social/png/laravelify-readme-banner-dark-1600.png">
      <img alt="Laravelify documentation" src="https://raw.githubusercontent.com/laravelify-cloud/laravelify/main/brand/laravelify-brand-assets/04-social/png/laravelify-readme-banner-light-1600.png">
    </picture>
  </a>
</p>

<p align="center">
  <a href="https://docs.laravelify.cloud"><b>Read the docs</b></a> ·
  <a href="https://laravelify.cloud">Website</a> ·
  <a href="https://laravelify.cloud/#install">Install command builder</a> ·
  <a href="https://github.com/laravelify-cloud/laravelify">Panel repository</a> ·
  <a href="https://github.com/laravelify-cloud/laravelify/releases">Releases</a>
</p>

# Laravelify documentation

The source of **[docs.laravelify.cloud](https://docs.laravelify.cloud)**, the documentation of [Laravelify](https://github.com/laravelify-cloud/laravelify): the open-source, self-hosted control panel that deploys Laravel, PHP, Node.js, React, Vue, Angular, Next.js, Nuxt, and more to your own Ubuntu server.

The site is built with [Mintlify](https://mintlify.com). Every push to `main` is published in about a minute.

## What the docs cover

| Section | Pages |
| --- | --- |
| **Getting started** | [Introduction](https://docs.laravelify.cloud/introduction), [Quickstart](https://docs.laravelify.cloud/quickstart): from a fresh server to a deployed site |
| **Installation** | [Requirements](https://docs.laravelify.cloud/installation/requirements), [Install](https://docs.laravelify.cloud/installation/install) (the one-line installer, choosing PHP and Node.js versions, unattended installs), [Configuration](https://docs.laravelify.cloud/installation/configuration), [Updating](https://docs.laravelify.cloud/installation/updating), [Uninstall](https://docs.laravelify.cloud/installation/uninstall) |
| **Concepts** | [Architecture](https://docs.laravelify.cloud/concepts/architecture) (nginx, PHP-FPM, PM2, Supervisor, tunnels, no Docker), [Features](https://docs.laravelify.cloud/concepts/features) |
| **Websites** | [Groups and websites](https://docs.laravelify.cloud/websites/groups-and-websites), [Frameworks](https://docs.laravelify.cloud/websites/frameworks), [Example projects](https://docs.laravelify.cloud/websites/example-projects), [Laravel](https://docs.laravelify.cloud/websites/laravel), [Next.js](https://docs.laravelify.cloud/websites/nextjs), [GitHub](https://docs.laravelify.cloud/websites/github), [Environment, nginx, and processes](https://docs.laravelify.cloud/websites/environment-nginx-processes), [Cloudflare tunnels](https://docs.laravelify.cloud/websites/cloudflare-tunnels) |
| **Backups** | [Backups to S3](https://docs.laravelify.cloud/backups/backups): schedules, Full backup, looking inside, restoring |
| **Monitoring & alerts** | [Overview](https://docs.laravelify.cloud/monitoring/overview), [Server](https://docs.laravelify.cloud/monitoring/server), [Heartbeats](https://docs.laravelify.cloud/monitoring/heartbeats), [Telegram](https://docs.laravelify.cloud/monitoring/telegram) |
| **Security** | [Authentication](https://docs.laravelify.cloud/security/authentication), [Site security](https://docs.laravelify.cloud/security/site-security), [Users and permissions](https://docs.laravelify.cloud/security/privilege-separation) |
| **Tools** | [MCP for AI assistants](https://docs.laravelify.cloud/tools/mcp), [File manager, terminal, and deployments](https://docs.laravelify.cloud/tools/file-manager-and-terminal), [Database](https://docs.laravelify.cloud/tools/database), [Logs and health](https://docs.laravelify.cloud/tools/logs-and-health), [Server services](https://docs.laravelify.cloud/tools/server-services), [Settings](https://docs.laravelify.cloud/tools/settings) |
| **Help** | [Troubleshooting](https://docs.laravelify.cloud/troubleshooting), [Contributing](https://docs.laravelify.cloud/contributing) |

## Run the docs locally

You need Node.js 20 or newer.

```bash
git clone https://github.com/laravelify-cloud/laravelify-docs.git
cd laravelify-docs
npx mint dev            # preview at http://localhost:3000, reloads on save
npx mint broken-links   # check every internal link before you push
```

## Structure

| Path | What |
| --- | --- |
| `docs.json` | Navigation (the sidebar groups and their pages), colors, logo, navbar links, the beta banner |
| `introduction.mdx`, `quickstart.mdx`, `troubleshooting.mdx`, `contributing.mdx` | Top-level pages |
| `installation/`, `concepts/`, `websites/`, `backups/`, `monitoring/`, `security/`, `tools/` | Pages, one folder per sidebar group |
| `snippets/install-command.mdx` | The install command: the one place its URL is written, included wherever it is shown |
| `logo/`, `favicon.svg`, `images/` | Brand assets and screenshots |

A new page needs two things: the `.mdx` file (with a `title` and `description` in its front matter) and its path in the right group of `docs.json`.

## Writing guide

- **Check every command and every setting name against the panel's code** ([laravelify-cloud/laravelify](https://github.com/laravelify-cloud/laravelify)). A command in the docs is one people will paste into their server.
- **Write for someone doing the task.** Short sentences, one idea each, the steps in the order they happen, and the panel's own words for buttons and tabs (**Server → Redis**, **Settings → MCP**).
- **Use the components already in use:** `<Steps>` for procedures, `<Tabs>` for alternatives, `<Note>` and `<Warning>` for what must not be missed, `<AccordionGroup>` for long lists.
- **Keep secrets out of examples.** Use `panel.example.com`, `change-me`, and `eyJh…` for tokens.
- When the panel changes, the docs change in the same release: the [changelog](https://github.com/laravelify-cloud/laravelify/blob/main/CHANGELOG.md) lists what each version did.

## Contributing

Found a mistake, a missing step, or something unclear? Open a pull request. Small fixes (a typo, a wrong command, a dead link) can be edited right on GitHub with the pencil icon. For a bigger change, open an [issue](https://github.com/laravelify-cloud/laravelify/issues) first so we can agree on it.

Questions about Laravelify itself go to the [panel's issues](https://github.com/laravelify-cloud/laravelify/issues).

## License

The documentation is part of Laravelify and licensed under the [MIT license](LICENSE).
