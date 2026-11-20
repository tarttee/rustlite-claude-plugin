# RustLite for Claude

RustLite plans your next move in the video game Rust. It calculates the resources for a craft, including whole
batches and intermediate recipes, the yield of a recycler at four efficiency tiers, and the explosive count and
sulfur cost of a raid route on full-health targets. Each answer comes with a compact card and a link to the
matching page on [rustlite.com](https://rustlite.com). No RustLite account is required.

## What is inside

- A connection to the public RustLite server at `https://api.rustlite.com/mcp`. It has four read-only tools:
  `search_rust_catalog`, `plan_rust_crafting`, `calculate_rust_recycling` and `compare_rust_raid_routes`.
- The `rustlite-planning` skill. It tells Claude when to ask for a building grade or recycler tier, and which
  assumptions to state.

## Try it

- "What resources do I need to craft 10 rockets, including intermediate recipes?"
- "Compare recycling 10 gears at a safe-zone recycler and a powered monument recycler."
- "Compare two sheet metal doors with one stone wall using rockets. I have three rockets."

Results use default server values. Server mods, item condition and shared explosion damage can change them.

## Install

In Claude Code:

```
/plugin install rustlite --marketplace tarttee/rustlite-claude-plugin
```

To add only the server in Claude Code, run
`claude mcp add --transport http rustlite https://api.rustlite.com/mcp`. In Claude, add the same URL as a
custom connector under Settings, Connectors.

## Links

- Documentation: https://rustlite.com/claude
- Support: https://rustlite.com/claude/support (email admin@rustlite.com)
- Privacy: https://rustlite.com/claude/privacy
- Terms: https://rustlite.com/terms
