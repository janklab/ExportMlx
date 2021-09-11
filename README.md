# ExportMlx: Export Matlab Live Scripts to Markdown

[ExportMlx](https://github.com/janklab/ExportMlx) is a tool to export Matlab Live Scripts (`.mlx` files) to Markdown and other formats.

[![Travis Build Status](https://travis-ci.com/janklab/ExportMlx.svg?branch=main)](https://travis-ci.com/github/janklab/ExportMlx)  [![CircleCI Build Status](https://circleci.com/gh/janklab/ExportMlx.svg?style=shield)](https://circleci.com/gh/janklab/ExportMlx) [![Azure Build Status](https://dev.azure.com/janklab/ExportMlx/_apis/build/status/janklab.ExportMlx?branchName=main)](https://dev.azure.com/janklab/ExportMlx/_build/latest?definitionId=1&branchName=main)

## Summary

This tool lets you generate project documentation and web site content from live scripts in your project. This is a nice way of generating rich documentation with included graphics that are up to date with your latest code. Especially nice for tutorials and examples.

See the [User Guide](https://exportmlx.janklab.net/UserGuide.html) for examples of what it can do. The User Guide is itself generated from a Matlab live script using ExportMlx!

## PRERELEASE ALPHA SOFTWARE

This is pre-release, alpha (not even beta!) quality software! It is an experimental work in progress. Everything about it, especially its public API, is subject to change at any time. And it is probably buggy.

DO NOT USE THIS SOFTWARE IN PRODUCTION SYSTEMS!

## Acknowledgments

ExportMlx is based on, and started out as a fork of, MathWorker Michio Inoue's [livescript2markdown](https://github.com/minoue-xx/livescript2markdown) tool. ExportMlx can largely be viewed as a productization of livescript2markdown.

The Live Script to LaTeX export code is informed by Pavel Roslovets's [Live-Script-to-Markdown-Converter toolbox](https://github.com/roslovets/Live-Script-to-Markdown-Converter).

## License Warning

ExportMlx is licensed under a nonstandard MathWorks-specific variant of the BSD 2-Clause License that includes this additional clause:

```text
* In all cases, the software is, and all modifications and derivatives of the
  software shall be, licensed to you solely for use in conjunction with
  MathWorks products and service offerings.
```

This is because livescript2markdown is licensed that way, and ExportMlx contains derivatives of its code.

## Requirements

Matlab version, I dunno, R2019b or later?

## Introduction

ExportMlx provides tools for exporting Matlab Live Scripts to Markdown and other formats.

This code has been tested with multiple live scripts but please note that it's not perfect. It's expected that you need some manual editing (for now!).

## Installation

Download this distro or repo and put it somewhere on your disk.

Add its `Mcode/` directory to your Matlab path using `addpath()`.

## Usage

Quick summary:

* `livescript2markdown` â Export a Live Script `.mlx` file to Markdown. (This is what you probably want.)
* `mlx2latex` â Do just the `.mlx` to `.tex` export step.
* `lslatex2markdown` â Do just the `.tex` to `.md` conversion step.

Super quick example:

```matlab
janklab.exportmlx.livescript2markown('MyLiveScript.mlx')
```

See the [User Guide](https://exportmlx.janklab.net/UserGuide.html) for fuller instructions and feature description.

## Project Goals

The goals of ExportMlx, specifically as an enhanced fork of [livescript2markdown](https://github.com/minoue-xx/livescript2markdown), are:

* Automate the full process from `.mlx` to `.md`.
* Become suitable for use in automated document generation processes.
  * Get the exported Markdown good enough that no manual touch-up is needed in normal cases.
* Make the code as modern as possible (as of R2019b).
* Produce nicely-formatted output files.
* Support additional output formats.

## Author

ExportMlx was developed by [Andrew Janke](https://apjanke.net) based on [livescript2markdown](https://github.com/minoue-xx/livescript2markdown) by [Michio Inoue](https://github.com/minoue-xx).

The project home page is the [GitHub repo page](https://github.com/janklab/ExportMlx). Bug reports and feature requests are welcome. The online documentation is on the [ExportMlx web site](https://exportmlx.janklab.net), but that is very much a work in progress.

ExportMlx is part of the [Janklab](https://janklab.net) suite of open source libraries for Matlab.

ExportMlx's repo structure is based on Janklab's [MatlabProjectTemplate](https://github.com/apjanke/MatlabProjectTemplate).

Code was written while listening to [live Phish shows](https://www.livephish.com/).

## Contributing

Contributions are appreciated! Right now I mostly need feature requests, bug reports, and especially example Live Script files that ExportMlx can be tested against.

All contributions to ExportMlx must be dual-licensed under the BSD 3-Clause License and the special MathWorks-specific variant of the BSD 2-Clause License that ExportMlx is currently licensed under. This is so that ExportMlx can be easily relicensed to BSD 3-Clause in the future if its underlying `livescript2markdown` code is similarly relicensed. (Which would be nice, IMHO.)

See the [CONTRIBUTING](https://github.com/janklab/ExportMlx/blob/master/.github/CONTRIBUTING.md) file for more info, including coding guidelines.
