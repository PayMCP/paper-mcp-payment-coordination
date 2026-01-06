# Payment Coordination Patterns for MCP (paper + figures)

This repository contains the paper source and figures for:

**Payment Coordination Patterns for MCP: A Design Taxonomy, Reference Wrapper, and Compatibility Snapshot**

## Abstract
The Model Context Protocol (MCP) enables large language model (LLM) applications to invoke server-hosted tools via a standardized client–server protocol. Introducing payment-gated tool execution creates a coordination challenge: clients and servers must enforce payment without degrading user experience or destabilizing tool selection. This paper presents a taxonomy of payment coordination patterns for MCP, analyzes their assumptions and failure modes, and discusses UX and security trade-offs observed across current MCP clients. The work focuses on practical engineering design rather than payment economics and is intended to support practitioners building paid MCP-based systems.

## TL;DR
- A design taxonomy of payment coordination patterns for MCP-based tools
- Covers request/confirm, retry-based, elicitation, progress, dynamic tools, and on-chain flows
- Analyzes UX, safety, and failure modes across current MCP clients
- Focuses on engineering trade-offs, not pricing or payment economics

## Payment coordination patterns covered
- **TWO_STEP** — explicit request → confirm tools
- **RESUBMIT** — error-based retry with `payment_id`
- **X402** — on-chain payment coordination
- **ELICITATION** — in-flow user confirmation
- **PROGRESS** — payment via progress notifications
- **DYNAMIC_TOOLS** — guiding confirmation via tool list changes
- **URL_ELICITATION** — emerging structured URL hand-off

## Download
- **Paper (PDF):** [main.pdf](main.pdf)

## Repository contents
- `main.pdf` — the compiled manuscript.
- `main.tex` — LaTeX source.
- `diagrams/` — figures referenced by the manuscript.

## Reference implementations
The paper is accompanied by reference wrappers:
- **TypeScript:** [https://github.com/PayMCP/paymcp-ts](https://github.com/PayMCP/paymcp-ts)
- **Python:** [https://github.com/PayMCP/paymcp](https://github.com/PayMCP/paymcp)

## Citation
If you use this work, please cite it as:

> Eugene Lobachev, Prasanna Kumar, Arjun Subedi, Bishnu Bista. *Payment Coordination Patterns for MCP: A Design Taxonomy, Reference Wrapper, and Compatibility Snapshot.* (preprint/technical report), 2026.

A BibTeX entry / DOI will be added once available.

## License
This work is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).
See the LICENSE file for details.
