# Overview

Dioxus aims to provide a fast, friendly, and portable toolkit for building user interfaces with Rust.

This guide assumes you'll be building a SPA (single page application) for the web. The process for building desktop apps, server-rendered apps, static sites, and mobile apps, is more-or-less the same. You can check out the [Platform Specific Guides](../platforms/00-index.md) for more information on setting up Dioxus for any of the various targets you are building for.

# Setting up Dioxus

Dioxus requires a few main things to get up and running:

- The [Rust compiler](https://www.rust-lang.org) and associated build tooling

- An editor of your choice, with the [Rust-Analyzer LSP plugin](https://rust-analyzer.github.io)

Dioxus integrates very well with the Rust-Analyzer IDE plugin which will provide appropriate syntax highlighting, code navigation, folding, and more.

We also recommend installing the Dioxus CLI. The Dioxus CLI automates building and packaging for various targets and integrates with simulators, development servers, and app deployment. It'll be our one-stop-shop for anything related to building and sharing our Dioxus Apps. To install the CLI, you'll need cargo (should be automatically installed with Rust):

```
$ cargo install dioxus-cli
```

You can update the dioxus-cli at any time with:

```
$ cargo install --force dioxus-cli
```

If your version of the CLI is out of date, it'll remind you to update whenever a new version is uploaded to Rust's package manager [crates.io](https://crates.io). We use a dedicated 1st-party CLI to save you from having to run potentially untrusted code every time you add a crate to your project - as is standard in the NPM ecosystem. You can vet the source of the Dioxus-CLI yourself at its [GitHub repo](https://github.com/jkelleyrtp/dioxus/tree/master/packages/cli).

If you want to keep your traditional `npm install XXX` workflow for adding packages, you might want to install `cargo-edit` and a few other fun `cargo` extensions:

- [cargo edit](https://github.com/killercup/cargo-edit) for adding dependencies from the CLI
- [cargo-expand](https://github.com/dtolnay/cargo-expand) for expanding macro calls
- `cargo tree` - an integrated cargo command that lets you inspect your dependency tree

That's it! We won't need to touch NPM/WebPack/Babel/Parcel, etc.

# Important tools

With Rust, things like benchmarking, testing, and documentation are included in the language. We strongly recommend going through the official Rust book _completely_. However, our hope is that a Dioxus app can serve as a great first project. With Dioxus you'll learn about:

- Error handling
- Structs, Functions, Enums
- Closures
- Macros

We've put a lot of care into making Dioxus syntax familiar and easy to understand, so you won't need knowledge on async, lifetimes, and smart pointers until you really start building complex Dioxus apps.

We strongly encourage exploring the guides for more information on how to work with the integrated tooling:

- [Testing](Testing.md)
- [Documentation](Documentation.md)
- [Benchmarking](Benchmarking.md)
- [Building](Building.md)
- [Modules](Modules.md)
- [Crates](Crates.md)