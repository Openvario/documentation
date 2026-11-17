# Documentation for the OpenVario Project

## Markdown documentation (primary)

The documentation tree is under [`docs/`](docs/):

- [Manufacturing](docs/manufacturing/)
- [Assembly](docs/assembly/)
- [Installation](docs/installation/)
- [User guide](docs/user-guide/)

Tone and language for edits: [`.cursor/rules/documentation-tone.mdc`](.cursor/rules/documentation-tone.mdc).

## LaTeX PDFs

Legacy LaTeX PDFs require:

```sh
sudo apt install make texlive-latex-extra texlive-plain-generic imagemagick
```

Build:

```sh
make pdf
```

This builds `ug_openvario`, `dev_openvario`, and `release_notes` into each
project’s `output/` directory.
