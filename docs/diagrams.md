# Portfolio diagrams

These editable A5 landscape diagrams explain the products through a trace waterfall, a geographic data view with a source receipt, and a support-case dossier. They are visual explanations, not exhaustive component maps or screenshots of the applications.

Open `assets/diagrams/*.drawio` in Draw.io Desktop or diagrams.net. The PNG exports also contain editable diagram XML. The profile selects a light or dark export and links to the full-size image.

## Export

Tested with Draw.io Desktop 31.5.3:

```sh
for source in assets/diagrams/*.drawio; do
  drawio -x -f png --theme light -s 3 -e -o "${source%.drawio}-light.png" "$source"
  drawio -x -f png --theme dark -s 3 -e -o "${source%.drawio}-dark.png" "$source"
done
```

On macOS, use `/Applications/draw.io.app/Contents/MacOS/draw.io` if `drawio` is not on PATH. Keep the editable sources.

## Evidence and examples

Checked on 21 October 2026:

- **AgentOps:** [current README](https://github.com/c-mongan/copilot-cli-agentops-azure) and [architecture](https://github.com/c-mongan/copilot-cli-agentops-azure/blob/main/docs/architecture.md). The waterfall is an illustration. Its timing is not production evidence. Native OpenTelemetry feeds local diagnosis; strict defaults exclude prompts, code, arguments and results. Azure upload is optional and off by default. A denial is distinct from a tool error.
- **Ireland MCP:** [README](https://github.com/c-mongan/ireland-mcp) and [recorded demonstration](https://github.com/c-mongan/ireland-mcp/blob/main/docs/demo-video.md). The receipt shows the recorded €1,672.57 monthly rent statistic for Galway City, two-bedroom apartments, Q4 2025. It came from [CSO RIQ02](https://data.cso.ie/table/RIQ02), under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), retrieved on 10 October 2026 from cache. This is a historical registered-tenancy statistic, not current asking rent. The figure is reformatted for explanation. Attribution: Central Statistics Office, Ireland; underlying table: RTB Average Monthly Rent Report. Map icons represent subject groups, not locations, exact coverage or live measurements.
- **Support Triage:** [workflow and synthetic cases](https://github.com/c-mongan/support-triage-agent-template) and [architecture](https://github.com/c-mongan/support-triage-agent-template/blob/main/docs/architecture.md). The dossier is an illustrative summary of synthetic webhook case 002: body parsing breaks HMAC verification; secret rotation is the misleading clue. Evidence rows show the investigation method, not a copied production report. Confidence is categorical, not a numerical probability. A human reviews the report and draft reply.

## Visual sources and asset credits

- Creation and correction workflow: [aymenfurter/skills](https://github.com/aymenfurter/skills), `drawio-pitch` and `drawio-iterate` (MIT). The author's [AI Engineer Coach sample](https://github.com/aymenfurter/skills/tree/main/samples) informed the use of detailed technical illustrations and grouped information. No sample artwork was copied.
- OpenTelemetry icon: [CNCF artwork](https://github.com/cncf/artwork/tree/main/projects/opentelemetry), used to identify the integration. The mark remains subject to the [Linux Foundation trademark policy](https://www.linuxfoundation.org/trademark-usage). No affiliation or endorsement is implied.
- Ireland MCP mark: the project's [favicon](https://github.com/c-mongan/ireland-mcp/blob/main/web/favicon.svg), with the forest/mint direction from its [design guide](https://github.com/c-mongan/ireland-mcp/blob/main/web/DESIGN.md). Project artwork is MIT-licensed, copyright 2026 Conor Mongan.
- Republic of Ireland outline: [Natural Earth 1:50m country boundaries](https://github.com/nvkelso/natural-earth-vector/blob/master/geojson/ne_50m_admin_0_countries.geojson), [public domain](https://www.naturalearthdata.com/about/terms-of-use/). The main polygon is simplified geographic context; offshore islands are omitted. The shape is an editable Draw.io vector stencil.
- Other illustrations and line icons are original native Draw.io geometry created for this profile. They are not copied publisher logos.

The detailed diagrams cover the three CV projects.

## Screenshot-led project grid

The grid uses consistent 16:9 frames. Screenshots are embedded intact in SVG files and cropped only by the display frame. Detailed Draw.io diagrams remain linked separately.

- AgentOps: [run-detail screen](https://github.com/c-mongan/copilot-cli-agentops-azure/blob/main/docs/images/ui-run-detail-dark.png), showing a demo run with a denied call. Demo timings and costs are not production performance claims.
- Ireland MCP: [recorded answer poster](https://github.com/c-mongan/ireland-mcp/blob/main/web/media/chatgpt-demo-poster.jpg). The image contains its historical period, retrieval date, CSO source and CC BY 4.0 attribution.
- Support Triage: a reformatted excerpt from the [recorded Copilot report for synthetic case SUP-1002](https://github.com/c-mongan/support-triage-agent-template/blob/main/docs/demo/copilot/reports/20261007-233738-SUP-1002-triage.md). Confidence and evidence text are quoted from that report. This is a report excerpt, not a product UI screenshot.
- Sligo: [overview screenshot](https://github.com/c-mongan/sligo-geology-viewer/blob/main/docs/assets/overview.png). Contains public Irish geoscience data; see the project's [data attribution](https://github.com/c-mongan/sligo-geology-viewer#data-and-attribution). Geological surfaces and risk context are interpretations, not certified engineering assessments.
- Effects Atlas: [gallery screenshot](https://github.com/c-mongan/effects-atlas/blob/main/docs/screenshots/gallery.jpg).
- LiveKit Voice Studio: [local studio screenshot](https://github.com/c-mongan/livekit-voice-studio/blob/main/docs/studio-local.jpg).

Narrated Deck Studio remains linked under More projects. Earlier cover versions remain recoverable in Git history.
