# Mellea Cookbook

<img src="https://github.com/generative-computing/mellea/raw/main/docs/mellea_draft_logo_300.png" alt="Mellea logo" height=100>

**Build predictable AI without guesswork.**

In every AI-powered pipeline, the unreliable part is the same: the LLM call itself — silent failures, untestable outputs, no guarantees. [Mellea](https://mellea.ai/) is a Python library for writing *generative programs*, replacing brittle prompts and flaky agents with structured, testable AI workflows built around type-annotated outputs, verifiable requirements, and automatic retries.

This **Cookbook** teaches Mellea through "Recipes" — bite-sized, runnable notebooks that each demonstrate one capability. Open any recipe below in Google Colab and start experimenting in seconds, no local setup required.

[//]: # ([![arXiv]&#40;https://img.shields.io/badge/arXiv-2408.09869-b31b1b.svg&#41;]&#40;https://arxiv.org/abs/2408.09869&#41;)
[![Website](https://img.shields.io/badge/website-mellea.ai-blue)](https://mellea.ai/)
[![Docs](https://img.shields.io/badge/docs-docs.mellea.ai-brightgreen)](https://docs.mellea.ai/)
[![PyPI version](https://img.shields.io/pypi/v/mellea)](https://pypi.org/project/mellea/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/mellea)](https://pypi.org/project/mellea/)
[![uv](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/uv/main/assets/badge/v0.json)](https://github.com/astral-sh/uv)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![Build](https://github.com/ibm-granite-community/mellea-cookbook/actions/workflows/notebooks.yaml/badge.svg)](https://github.com/ibm-granite-community/mellea-cookbook/actions/workflows/notebooks.yaml)
[![GitHub License](https://img.shields.io/github/license/ibm-granite-community/mellea-cookbook)](https://github.com/ibm-granite-community/mellea-cookbook/blob/main/LICENSE)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-3.0-4baaaa.svg)](CODE_OF_CONDUCT.md)

## Recipes

### Getting Started

1. [Quick Start](recipes/QuickStart/QuickStart.ipynb)
   <a target="_blank" href="https://colab.research.google.com/github/generative-computing/mellea-cookbook/blob/main/recipes/QuickStart/QuickStart.ipynb">
   <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
   </a>
1. [Instruct-Validate-Repair](recipes/InstructValidateRepair/InstructValidateRepair.ipynb)
   <a target="_blank" href="https://colab.research.google.com/github/generative-computing/mellea-cookbook/blob/main/recipes/InstructValidateRepair/InstructValidateRepair.ipynb">
   <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
   </a>
1. [Extracting Structured Data from Unstructured Text](recipes/StructuredDataExtraction/StructuredDataExtraction.ipynb)
   <a target="_blank" href="https://colab.research.google.com/github/ibm-granite-community/mellea-cookbook/blob/main/recipes/StructuredDataExtraction/StructuredDataExtraction.ipynb">
   <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
   </a>

## Build Status

<a href="https://github.com/ibm-granite-community/mellea-cookbook/actions/workflows/notebooks.yaml">
  <img src="https://github.com/ibm-granite-community/mellea-cookbook/actions/workflows/notebooks.yaml/badge.svg" alt="Testing Notebooks">
</a>

## Contributing

For information about contributing to this repo, code of conduct guidelines, etc., see the community [CONTRIBUTING][CG] and [Code of Conduct][CoC] guides. All commits require [DCO-signoff][CG-legal] *and* [GPG or SSH signing][CG-signing]. The GitHub recommended code security settings are enforced on this public repository (which include the signing requirement).

<!-- For more background, please see the [community discussions](https://github.com/orgs/generative-computing/discussions). -->

## Licenses

The Mellea Cookbook's base license is CC BY 4.0.

Code in this repository, including in notebook cells, is licensed under Apache 2.0.

Any example datasets committed to this repository are licensed under CDLA Permissive 2.0.

## IBM Public Repository Disclosure

All content in these repositories including code has been provided by IBM under the associated open source software license and IBM is under no obligation to provide enhancements, updates, or support. IBM developers produced this code as an open source project (not as an IBM product), and IBM makes no assertions as to the level of quality nor security, and will not be maintaining this code going forward.

[CoC]: https://github.com/generative-computing/mellea/blob/main/CODE_OF_CONDUCT.md
[CG]: https://github.com/ibm-granite-community/mellea-cookbook/blob/main/CONTRIBUTING.md
[CG-legal]: https://github.com/generative-computing/.github/blob/main/CONTRIBUTING.md#legal
[CG-signing]: https://github.com/generative-computing/mellea/blob/main/CONTRIBUTING.md#developer-certificate-of-origin-dco
