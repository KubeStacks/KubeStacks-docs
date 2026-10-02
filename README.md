<div align="center">

<img src="favicon.svg" width="88" alt="KubeStacks icon" />

# KubeStacks docs

**The documentation for [KubeStacks](https://github.com/KubeStacks/KubeStacks), at
[docs.kubestacks.com](https://docs.kubestacks.com).**

Installing it, using it, running it for your team, and every setting: the source of the docs
for the calm, fast Kubernetes app for your desktop and your cluster.

[![CI](https://github.com/KubeStacks/KubeStacks-docs/actions/workflows/ci.yml/badge.svg)](https://github.com/KubeStacks/KubeStacks-docs/actions/workflows/ci.yml)
[![Docs](https://img.shields.io/badge/docs-docs.kubestacks.com-2a78d6)](https://docs.kubestacks.com)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue)](LICENSE)

</div>

<a href="https://docs.kubestacks.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/docs-dark.png" />
    <img src=".github/assets/docs-light.png" alt="The KubeStacks docs: the introduction, “Your clusters, at a glance”, next to the sidebar of guides, with a screenshot of a cluster's overview in KubeStacks." />
  </picture>
</a>

## What's in it

| Section                                                                   | Folder              | What it covers                                                          |
| ------------------------------------------------------------------------- | ------------------- | ----------------------------------------------------------------------- |
| [Get started](https://docs.kubestacks.com)                                | `get-started/`      | The desktop app, KubeStacks in your cluster, a tour, and signing in     |
| [Clusters](https://docs.kubestacks.com/clusters/connect)                  | `clusters/`         | Kubeconfigs, namespaces, and the permissions each feature needs         |
| [Explore](https://docs.kubestacks.com/explore/overview)                   | `explore/`          | The overview, every list, the detail panel, health, and finding things  |
| [Make changes](https://docs.kubestacks.com/changes/safely)                | `changes/`          | Actions, YAML, creating objects, bulk changes and the guard rails       |
| [Debug](https://docs.kubestacks.com/debug/logs)                           | `debug/`            | Logs, shells, debug containers and port forwards                        |
| [Metrics](https://docs.kubestacks.com/metrics/live-usage)                 | `metrics/`          | Live usage, and usage history from Prometheus or VictoriaMetrics        |
| [Helm](https://docs.kubestacks.com/helm/releases)                         | `helm/`             | Releases, upgrades and rollbacks, installs, and charts on your computer |
| [Custom resources](https://docs.kubestacks.com/custom-resources/overview) | `custom-resources/` | Every kind the cluster serves, built-in views, and writing your own     |
| [In your cluster](https://docs.kubestacks.com/server/overview)            | `server/`           | Installing the chart, sign-in, security, and every setting              |
| [Reference](https://docs.kubestacks.com/reference/keyboard-shortcuts)     | `reference/`        | Shortcuts, the view format, kinds, troubleshooting and the FAQ          |

The site is built with [Mintlify](https://mintlify.com). Besides the pages:

| File                        | What it does                                                                  |
| --------------------------- | ----------------------------------------------------------------------------- |
| `docs.json`                 | Navigation, theme, colors, and the current KubeStacks version (`{{version}}`) |
| `style.css`                 | KubeStacks' own look: its colors, key caps, screenshots and health labels     |
| `screenshots.js`            | Shows screenshots at full size when one is zoomed                             |
| `.github/scripts/check.mjs` | Checks what Mintlify doesn't: screenshots, icons, page metadata and variables |

Screenshots aren't kept here. KubeStacks takes them of its demo clusters, in light and dark,
and the pages show them straight from
[its repository](https://github.com/KubeStacks/KubeStacks/tree/main/docs/screenshots), so the
docs always show the app as it is.

## Running it locally

You need [Node.js](https://nodejs.org) 20 or later.

```sh
npx mint dev                    # the docs at http://localhost:3000, reloading as you edit
npx mint validate               # fails on any build warning or error
npx mint broken-links           # every link between pages
node .github/scripts/check.mjs  # screenshots, icons, page metadata and variables
```

CI runs the last three on every pull request. What's merged to `main` goes live at
[docs.kubestacks.com](https://docs.kubestacks.com).

## Contributing

Fixes and improvements are welcome, from a typo to a new page. [CONTRIBUTING.md](CONTRIBUTING.md)
covers how pages are written, where screenshots come from, and what to check before you open a
pull request. To report something wrong in the docs, open an
[issue](https://github.com/KubeStacks/KubeStacks-docs/issues/new/choose). Bugs and ideas for
the app itself go to [KubeStacks](https://github.com/KubeStacks/KubeStacks/issues).

## License

[Apache License 2.0](LICENSE), like KubeStacks.

<sub>Kubernetes is a registered trademark of the Linux Foundation.</sub>
