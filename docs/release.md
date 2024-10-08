# Release process

## Prerequisites

Install [Cargo release](https://github.com/crate-ci/cargo-release):

```bash
cargo install cargo-release
```

## Actions

1. Start of with a clean repo on the master branch
2. Dry-run the release for the next version, e.g.
    - `cargo release patch`
    - `cargo release minor`
    - `cargo release major`
3. Release the next version by providing the `-x` flag, e.g.
    - `cargo release patch -x`
    - `cargo release minor -x`
    - `cargo release major -x`
4. Create a new release on Github and fill out the release notes
5. Publish the release on GitHub
    - This will trigger the CD-pipeline to publish the crate to crates.io
