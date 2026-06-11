# SciVal for Claude Code

SciVal is an analytical skillset for Claude Code that rigorously evaluates the scientific validity of claims, statements, or drafts against publicly available, high-impact scientific literature.

## Installation
Install it in Claude Code by adding this repo as a marketplace, then installing the plugin from it:

```
claude plugin marketplace add tunabirgun/scival-plugin
claude plugin install scival@scival-marketplace
```

Restart Claude Code afterward to load the skill. To pull later updates, run `claude plugin update scival@scival-marketplace` (also restart to apply).

## Usage
Once installed, run it with the slash command, passing the claim as the argument:

```
/scival:scival Microplastics cross the blood-brain barrier in mammalian models.
```

The skill is invoke-only (`disable-model-invocation: true`), so it runs only when you call the command explicitly; Claude will not trigger it on its own from a plain-language request.

## What it does
1. Maps the claim to the Hierarchy of Evidence.
2. Evaluates statistical rigor and absence of bias.
3. Generates a 1-10 Scientific Validity Scoring Matrix.
4. Suggests an empirically calibrated rewrite of the original statement.

## Security
This plugin is purely prompt/context-based. It does not contain executable scripts or custom MCP servers. It relies entirely on Claude's native web-search and reasoning capabilities.
