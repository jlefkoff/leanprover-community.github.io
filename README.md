# Lean prover community website

## Dependencies

* `pip install staticjinja PyYaml mistletoe pybtex pylatexenc`

Building the bibliography requires [`bibtool`](https://github.com/ge-ne/bibtool).

In order to rebuilt the CSS from SCSS, you would also need:

* [sass](https://sass-lang.com/)
* [bootstrap](https://github.com/twbs/bootstrap/archive/v4.4.1.zip)
  should be unpacked at the project root

The website relies on several components which are built in other repositories:
- [`mathlib_stats`](https://github.com/leanprover-community/mathlib_stats)
- [`lean-web-editor`](https://github.com/leanprover-community/lean-web-editor)
- [`mathlib_docs`](https://github.com/leanprover-community/mathlib_docs) (built by CI in mathlib itself)

## Building

* Build CSS if needed: `sass scss/lean.scss > css/lean.css`
* Build site using `make_site.py`. Use option `--local` for local
  viewing (internal url will be prefixed by local file path).
  Use option `--reload` to continuously build when templates are
  changed (this won't work for watching changes in `data/`).

Before going live, we also need to revive the bundle building process
(or remove bundles from documentation).

## TODO

* Use pygment for syntax highlighting
* Better integration with Zulip archive
* Better integration with API docs
* Use webpack or similar to bundle all the javascript?
