# José Santos's resume

[![Release](https://img.shields.io/github/release/josemrsantos/automated-cv.svg?style=flat)](https://github.com/josemrsantos/automated-cv/releases/latest)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat)](./LICENSE)
[![Build status](https://img.shields.io/github/actions/workflow/status/josemrsantos/automated-cv/general.yaml?style=flat)](https://github.com/josemrsantos/automated-cv/actions?query=workflow%3Ageneral)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?style=flat)](https://github.com/semantic-release/semantic-release)

My resume written in LaTeX based on [Awesome-CV](https://github.com/posquit0/Awesome-CV) with a complete CI/CD pipeline. Fully automated testing, building & release process is powered by GitHub Actions & [semantic-release](https://github.com/semantic-release/semantic-release). The output pdf can be found in the [releases section](https://github.com/josemrsantos/automated-cv/releases/latest).

## Download: [resume.pdf](https://josemrsantos.github.io/automated-cv/resume.pdf)

When GitHub Pages is enabled for this repo (source: the `gh-pages` branch), the latest PDF is published at `https://<username>.github.io/automated-cv/resume.pdf`.

## Local Development

### Setup

The following tools are recommended for local work:

- `git`: `>=2`
- Build: TeX Live with `latexmk` (LuaLaTeX) **or** Docker (`>=18.09`) for a containerized build
- Tests: Node.js `>=16` to install and run Prettier locally
- `make` (standard on macOS/Linux)

First clone the repository:

```shell
git clone git@github.com:josemrsantos/automated-cv.git
```

Install local dev tools (Prettier):

```shell
npm install
```

### Test & Build Locally

- format (write): `npm run format`
- format (check): `npm run format:check`
- test: `make test` (runs Prettier; set `RUN_SUPER_LINTER=1` to run super-linter via Docker)
- build: `make build` (uses local `latexmk` when available, otherwise Docker)
- build a variant: `make build RESUME_TEX=src/resume_industry.tex` (outputs `resume_industry.pdf`)
- run test & build: `make all`

### Contributing / commit conventions

Commits follow [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, `ci:`, `refactor:`), because semantic-release derives the version number and changelog from them. Work happens on a branch and is merged into `main` through a pull request.

## Use of AI assistance

I used an LLM to help convert my CV content into the LaTeX (`.tex`) files in `src/sections/`, as I have not worked with LaTeX before. I reviewed the generated code, built the PDF and ran the checks myself, and the repository work (forking, branching, commits, pull request and CI setup) was done by me.

## Credits

The list of some third party components used in this project, with due credits to their authors and license terms. More details can be found in their README documentations.

- [posquit0/Awesome-CV](https://github.com/posquit0/Awesome-CV)
- [xu-cheng/latex-action](https://github.com/xu-cheng/latex-action)

Forked from [ezpzbz/automated-cv](https://github.com/ezpzbz/automated-cv), which was itself forked from [kirintwn/resume](https://github.com/kirintwn/resume).
