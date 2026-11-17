# SciVal

A Claude Code skill that evaluates the scientific validity of a claim, statement or draft against high-impact published literature.

## Install

```bash
claude plugin marketplace add tunabirgun/scival-plugin
claude plugin install scival@scival-marketplace
```

Restart Claude Code to load the skill. To update, run `claude plugin update scival@scival-marketplace` and restart.

## Use

Pass the claim as the argument to the slash command:

```text
/scival:scival Microplastics cross the blood-brain barrier in mammalian models.
```

The skill sets `disable-model-invocation: true`, so it runs only when called explicitly and never from a plain-language request.

The report contains:

- an executive summary with a verdict from Unassailable to Pseudoscientific;
- a 1-10 validity matrix covering evidence tier, statistical power, replication, contemporary consensus and bias;
- a literature analysis with counter-evidence and boundary conditions;
- a calibrated rewrite of the original statement;
- peer-reviewed references in APA 7th edition, with non-scholarly sources listed separately.

Evidence is weighted by recency: in an actively studied field, dated work is flagged as a vulnerability unless it remains the current consensus.

## Limits

The plugin is prompt-only, with no scripts or MCP servers. It relies on Claude's web search and reasoning, and the skill does not specify the weights behind the overall index.

## License

MIT. See [LICENSE](LICENSE).
