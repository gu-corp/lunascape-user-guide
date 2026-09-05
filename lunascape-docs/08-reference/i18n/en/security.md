# Security and write boundaries

The boundaries Lunascape Docs maintains to protect your documents and your device.

## Display

- HTML generated from Markdown and SVG generated from diagrams are sanitized with DOMPurify 3.4.14 before display.
- Arbitrary scripts in MDX are never executed.
- KaTeX runs with `trust: false`, `maxSize: 50` and `maxExpand: 1000`, and trusts neither external HTML nor arbitrary commands.
- The Markmap, WaveDrom, Svgbob, Vega-Lite and Penrose runtimes are loaded locally, at pinned versions, only when the corresponding block is present. External references, raw HTML and executable notations are not allowed, and scripts, external images, `link`, `style` and `foreignObject` are removed from generated SVG.
- TikZ rendering never launches the host's LaTeX. It runs sequentially in a WebAssembly TeX worker with an in-memory file system, bounded in input, queue, memory, execution time (15 seconds) and SVG output, and rejects file I/O instructions.

## Access to documents and files

- Document links and file operations cannot leave the documentation root.
- Creating, renaming, moving and deleting from the INDEX are re-verified on the extension side — documentation root, INDEX revision, canonical path, target type, symbolic-link boundaries and unsaved documents — before they are applied. Requests from a stale menu or another documentation root are not applied.
- INDEX modifications are disabled while a document is being edited or another INDEX operation is being applied.
- Creating from a template re-verifies workspace trust, the documentation root's identity, the INDEX revision, the Standard Pack and generated content, the destination and symbolic-link boundaries after the preview. It never overwrites an existing file and never creates content that differs from the preview or exceeds 4 MiB.
- Saving a configuration file checks its revision immediately beforehand and aborts when an external change is detected.

## Sending data outside

- Documents are never sent anywhere for reading, editing or checking. Document checks run locally and deterministically.
- Only translation (of the current page or in batch) sends documents to a language model, after disclosing the destination and scope and only with explicit approval.
- Translation proposals are presented as a diff, the revisions of the source and target are re-verified, and a proposal is applied only when a person saves it explicitly.
- The specification tool for AI agents returns no document content, workspace names or local paths.

## Git

- Saving only writes the file. No feature stages or commits in Git automatically.
- Existing files such as `_meta.json` are never deleted or modified silently. Orphaned translations are never deleted or moved automatically.

## Related topics

- [Specifications](README.md)
- [Use from AI agents](ai-agents.md)
