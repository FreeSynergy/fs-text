# FreeSynergy Text - design (draft)

Status: draft, no code. Everything here is a plan; what is not built says so.

## Place in the model (ADR 0076)
Information resources of the kind 'text document'. fs-files holds the bytes and versions, fs-text holds the content and its editing.

## Standards
OpenDocument Text (`.odt`, ISO/IEC 26300); Loro for collaborative editing (ADR 0073); blocks with stable ids (UUIDv7).

## Facets
Wiki (pages in a tree, German and English as ONE page with language variants). The code of fs-wiki becomes the core of fs-text (a later, separate step; no rename now).

## Rules that apply to every FreeSynergy program
- One program, one interface (ADR 0050); commands with `supported` (ADR 0066); capabilities (ADR 0068).
- One manifest (actions, objects, attributes) produces menus, workflow building blocks, REST (OpenAPI), MCP tools and the
  catalog entry (ADR 0076 section 2).
- Layers are separate (ADR 0074): the program delivers functions and data, a frontend arranges, a style styles; motion and
  sound are their own layers. No colors, spacing or fonts in the program.
- Every program ships a default frontend and has at least two frontends in the end.
- Own data stays in the person's own data folder; sync and storage follow fs-objects and fs-files.

## Related decisions
ADR 0076; ADR 0073 (collaboration); ADR 0072 (wiki blocks). All decisions: [fs-documentation](https://github.com/FreeSynergy/fs-documentation).

## Open
Everything: first design round, interface (Cap'n Proto) and manifest, first frontend (pictures first).
