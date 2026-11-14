# Mitos protocol types

This fork maintains the protocol types used by [Mitos](https://github.com/mitos-editor/mitos).
It starts from upstream lsp-types 0.97.0 and adds the following standard protocol structures:

- LSP 3.17 completion-list defaults and textEditText;
- LSP 3.18 completion-list merge rules, snippet workspace edits, and folding refresh;
- integer-granularity semantic-token delta data;
- retention of annotated text edits and deletion annotation identifiers.

This is a focused compatibility update, not a claim of complete LSP 3.18 coverage.
New optional fields are omitted when absent. `TextDocumentEdit.edits` now uses
`DocumentTextEdit` to distinguish plain, annotated, and snippet edits. Semantic token
delta insertion data is a raw integer array, as required by the protocol.

The original upstream documentation follows.

# lsp-types [![Build Status](https://travis-ci.org/gluon-lang/lsp-types.svg?branch=master)](https://travis-ci.org/gluon-lang/lsp-types) [![Documentation](https://docs.rs/lsp-types/badge.svg)](https://docs.rs/crate/lsp-types)

Types useful for interacting with a [language server](https://code.visualstudio.com/blogs/2016/06/27/common-language-protocol).

Supports Language Server Protocol (LSP) version 3.16.0.

Proposed 3.17 features can be activated using the `proposed` feature flag.
- **NOTE** that these are unstable and may change between releases.

## Contributing

If you are making a change which adds, removes or modifies the LSP API it is highly appreciated if you link to the spec where this change is described. This gives context to whether the change should be an experimental addition and lets the reviewer double check the changes easily against the spec.

## Links

[Stable Protocol reference](https://github.com/microsoft/language-server-protocol/tree/gh-pages/_specifications/lsp/3.17/specification.md)

[Proposed Protocol reference](https://github.com/microsoft/language-server-protocol/blob/gh-pages/_specifications/lsp/3.18/specification.md)
