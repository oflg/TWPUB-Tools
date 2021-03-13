# TWPUB Tools

TWPUB is a new format for electronic publications that encourages readers to reuse and remix material, and explore new ways to support active reading.

We aim to re-imagine electronic publications as dynamic, mouldable, customisable shared cultural assets. Our goal is to create an ecosystem of readers and a library/store that makes it easy to create and consume these new-style publications. We hope that readers will come for the great experience, publishers will come to reach the readers, and that authors will be happy with the increased reader engagement.

View the demo at https://twpub.github.io/TWPUB-Tools/

## Introduction

This repository contains two tools:

* ''epub2twpub'' is a command line tool to convert EPUB files into TWPUB format
* ''twpub-wiki/plugins/twpub-tools'' is a TiddlyWiki plugin containing tools for viewing and annotating TWPUBs

The repository also contains:

* ''bin'' – scripts for working with the tools, including setting up a TiddlyWiki plugin library to contain the demo TWPUBs
* ''epubs'' – demonstration EPUB files that get built into the 
* ''fixtures'' – test fixtures for testing epub2twpub

## Setup

Install the latest Node.js and npm from https://nodejs.org/

Clone this repository and install its dependencies:

```
npm install
```

To install subsequent upstream changes from TiddlyWiki 5:

```
npm update
```

## Tests

To run the test suite:

```
npm test
```

## Develop

* Converts the library of epubs in `/epubs` into a plugin library serving TWPUBs
* Builds a TiddlyWiki including the TWPUB-Tools plugin
* Runs an HTTP server to serve the wiki and the plugin library at http://127.0.0.1:8080/

```
npm start
```

## Build

Builds the files for the app without running the HTTP server

```
npm run build
```

The output files will be in `./output`.

## Usage of ''epub2twpub''

To run the ''epub2twpub'' converter:

```
node epub2twpub --epub <path-to-input-epub-file> --output <path-to-output-twpub-file>
```
