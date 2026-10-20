# Profile diagrams

The editable sources are in `assets/diagrams/`. Open any `.drawio` file in Draw.io Desktop or diagrams.net. The PNGs also contain editable diagram XML.

Export both themes from each source with Draw.io Desktop 31.5.3 or a compatible version:

```sh
for source in assets/diagrams/*.drawio; do
  drawio -x -f png --theme light -s 2 -e -o "${source%.drawio}-light.png" "$source"
  drawio -x -f png --theme dark -s 2 -e -o "${source%.drawio}-dark.png" "$source"
done
```

On macOS, use `/Applications/draw.io.app/Contents/MacOS/draw.io` if `drawio` is not on PATH. Keep the sources when exporting. The profile selects the image theme with a `picture` element. Each image links to a full-size light copy for closer inspection.

## Public source references

Checked on 20 October 2026:

- [AgentOps architecture](https://github.com/c-mongan/copilot-cli-agentops-azure/blob/main/docs/architecture.md): native Copilot OpenTelemetry, local strict collector and run ledger, local investigation UI, optional Azure Logs Ingestion/DCR/Log Analytics path.
- [Ireland MCP request flow](https://github.com/c-mongan/ireland-mcp#readme): validated requests, source adapters, public APIs, cache/retry/circuit-breaker controls and evidence envelopes. The assistant produces the final answer from the returned evidence.
- [Support Triage architecture](https://github.com/c-mongan/support-triage-agent-template/blob/main/docs/architecture.md): intake, parallel research, evidence synthesis, report and human review. The diagram groups the research tracks for readability.

The diagrams are summaries, not exhaustive component maps. Dashed AgentOps connections are optional. Project README files and architecture documents remain the source of truth.
