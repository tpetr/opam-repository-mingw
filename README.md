# opam-repository-mingw

[OCaml for Windows](https://fdopen.github.io/opam-repository-mingw/) was a fork of OCaml providing support for the mingw-w64 and MSVC ports of OCaml maintained by [@fdopen](https://github.com/fdopen).

Its deprecation was announced in [August 2021](https://fdopen.github.io/opam-repository-mingw/2021/02/26/repo-discontinued/) and it has received no updates since November 2022 in [696c4b2](https://github.com/fdopen/opam-repository-mingw/commit/696c4b27488b4b0d3ec3929dbe65565cb91764a1).

OCaml's [setup-ocaml](https://github.com/ocaml/setup-ocaml) GitHub Action as well as other CI systems are still using [fdopen/opam-repository-mingw](https://github.com/fdopen/opam-repository-mingw) with [ocaml/opam-repository](https://github.com/ocaml/opam-repository) added to switch selections to provide newer packages. However, this is problematic when new releases require the constraints of existing packages to be updated.

## Updates

This repository adds packages for OCaml 4.14.1 (released 19 Dec, 2022) and contains updates to _existing_ packages only to allow upstream opam-repository to be safely used, as constraints updated to deal with _new_ releases of packages are copied back to this repository.

All new releases should be made to opam-repository only. This repository will only be periodically updated with constraint changes made in opam-repository. Issues and pull requests towards this goal are warmly welcomed!

## Sunset

[opam 2.2](https://github.com/ocaml/opam) offers full support for native Windows development. As part of the development of opam 2.2, opam-repository's compiler packages will be updated to enable native Windows opam switches without needing this repository.

Packages should then be fixed upstream in the usual way with new releases providing Windows support, with the gradual aim of allowing all Windows users to use ocaml/opam-repository only and cease using this repository completely.
