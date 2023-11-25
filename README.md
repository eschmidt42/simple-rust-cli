# simple rust cli

This repository is a template to develop a rust-based cli tool and create binaries using github cicd with each release for a range of operating systems and rust releases.

## local setup

Get rust, see https://rustup.rs/.

Get the repo

    git clone https://github.com/eschmidt42/simple-rust-cli

Then run

    cd simple-rust-cli
    cargo test

If this worked you are good to go to develop locally.

## github setup

`./.github/workflows` contains `push_pull.yml` and `release.yml` to run github pipelines after push/pull or release events on github.

The `release.yml` produces tarballs of the rust code for `simple-rust-cli` compiled to binaries and tries to store them in a manually created release. In order to do that you have to make sure that in your repo settings under `Workflow permission` "read and write permission" is given as well as "Allow GitHub Actions to create and approve pull request" is ticked.

## Note

You'll certainly want to give your cli tool a different name. To do this you'll have to replace `simple-rust-cli` in:
* `Cargo.toml`
* `.github/workflows/`
    * `push_pull.yml`
    * `release.yml`

Happy tinkering! :)