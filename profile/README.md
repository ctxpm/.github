# ctx

**A package manager for context.**

Teams and AI agents work from the same material: how the team works, what the domain
words mean, which standards apply, what was decided and why. That material usually lives
in copied folders, or rides along in a package manager built for code.

`ctx` treats it as what it is: versioned packages of Markdown and YAML, with dependencies,
that you install where your tools read them.

```sh
curl -fsSL https://ctxpm-registry.web.app/install.sh | sh

ctx login
ctx install team-handbook
```

## What you get

- **Typed, versioned packages.** A package has a type (`project`, `discipline`, `team`, …),
  a semantic version and dependencies. Published versions never change.
- **Access per package.** Public, or shared with named people and whole email domains.
  A package you cannot read does not show up for you at all.
- **One native binary.** No Node, npm or other runtime; it talks to the registry over
  HTTPS. Built for macOS, Linux and Windows.
- **Reproducible installs.** `ctx.toml` says what you want, `ctx.lock` pins what you got,
  and every download is checked against its SHA-256 before it is unpacked.
- **Publishing from CI without secrets.** A package can trust a GitHub Actions workflow;
  no tokens to store or rotate.
- **Your own registry if you want one.** The registry is a Firebase project you can deploy
  yourself. Nothing is tied to ours.

## Where things are

| | |
|---|---|
| [`ctxpm/ctx`](https://github.com/ctxpm/ctx) | The CLI, the registry backend, the web app and the package format |
| [ctxpm-registry.web.app](https://ctxpm-registry.web.app) | The registry: browse packages and manage who can read them |
| [Package format](https://github.com/ctxpm/ctx/blob/main/docs/package-format.md) | What a package is and how to make one |
| [Running a registry](https://github.com/ctxpm/ctx/blob/main/registry/README.md) | Access model, write API and deployment |

## Status

Early. The CLI, the registry and the web app work end to end and have a first release,
but expect breaking changes before 1.0. Issues and ideas are welcome in
[`ctxpm/ctx`](https://github.com/ctxpm/ctx/issues).

Apache-2.0 licensed.
