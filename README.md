# SciVal for Claude Code

SciVal is an analytical skillset for Claude Code that rigorously evaluates the scientific validity of claims, statements, or drafts against publicly available, high-impact scientific literature.

## Usage
Once installed, trigger the tool by asking Claude Code to run it:
`Run SciVal on this statement: "Microplastics cross the blood-brain barrier in mammalian models."`

## What it does
1. Maps the claim to the Hierarchy of Evidence.
2. Evaluates statistical rigor and absence of bias.
3. Generates a 1-10 Scientific Validity Scoring Matrix.
4. Suggests an empirically calibrated rewrite of the original statement.

## Security
This plugin is purely prompt/context-based. It does not contain executable scripts or custom MCP servers. It relies entirely on Claude's native web-search and reasoning capabilities.
