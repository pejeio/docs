[![Docs build](https://github.com/tradingstrategy-ai/docs/actions/workflows/build-and-deploy-dcos.yml/badge.svg)](https://github.com/tradingstrategy-ai/docs/actions/workflows/build-and-deploy-dcos.yml)

# Trading strategy documentation

Documentation for [Trading Strategy algorithmic trading framework and protocol](https://tradingstrategy.ai/).
View [the documentation here](https://tradingstrategy.ai/docs).

# About documentation internals

- The documentation is built on the top of [Sphinx documentation toolchain](https://www.sphinx-doc.org/en/master/)
- [Furo based theme is used](https://github.com/tradingstrategy-ai/furo) (the theme has been modified)
- [API documentation is generated with sphinx-autodoc-typehints](https://github.com/tox-dev/sphinx-autodoc-typehints) 
- [Interactive Jupyter notebook examples are generated with nbsphinx](https://nbsphinx.readthedocs.io/)
- [The documentation is self-hosted using Caddy](github.com/tradingstrategy-ai/proxy-server/)

# Building locally

[pyproject.toml](./pyproject.toml) is automatically pulling the master version of the packages.

To build everything from the scratch: 

```shell
poetry shell
make \
  update-git-submodules \
  poetry-install \
  pip-force-install-deps \
  install-furo \
  rebuild-furo \
  clean-autosummary \
  clean \
  html
```

Then you can open `build/html/index.html` in your local web browser:

```shell
open build/html/index.html
```

See [Makefile](./Makefile) for more recipes.

# Updating theme

[See theme README](https://github.com/tradingstrategy-ai/furo).

To update Furo SCSS changes:

```shell
make rebuild-furo clean html
```

# Community

* [Trading Strategy website](https://tradingstrategy.ai)

* [Blog](https://tradingstrategy.ai/blog)

* [Twitter](https://twitter.com/TradingProtocol)

* [Discord](https://tradingstrategy.ai/community#discord) 

* [Telegram channel](https://t.me/trading_protocol)