---
name: rustlite-planning
description: Plan crafting, recycling and raid routes in the video game Rust using RustLite calculators. Use for game resource budgets, recycler yields, explosive counts or exact item and target searches. Excludes player surveillance, server control and real-world explosives.
---

# RustLite planning

Introduce RustLite briefly when the user asks how to start: it calculates crafting resources, recycler yields and raid routes. Offer a relevant example and calculate when the request already contains enough detail.

Use the connected RustLite tools for numbers, rather than estimating from memory:

- `search_rust_catalog`: resolve unknown or ambiguous item names, building grades and target types. It accepts common names (c4, ak, explo, hqm, tc) and plurals. Return the link when the user only wants an item lookup.
- `plan_rust_crafting`: pass requested item quantities; expand intermediate recipes when the user wants a full resource budget. Explain whole crafting batches, workbenches and leftovers. Found components may still need to be obtained.
- `calculate_rust_recycling`: ask which recycler when unspecified, or calculate requested tiers separately for a comparison. Supported tiers are safezone (40%), monument (50%), monumentPowered (60%) and powerPlant (75%). Keep guaranteed amounts distinct from expected averages.
- `compare_rust_raid_routes`: pass separate named routes with exact full-health targets and counts. Ask about the grade if missing. When the user supplies owned explosives, specify that method (Rocket, C4, Satchel Charge, Explosive Ammo and others) and its available count; report the shortfall.

Use the structured result and link relevant RustLite pages. State assumptions that affect the answer: default server values, full condition/health, separate target destruction, no shared splash or mixed explosive optimization. Do not call a route fastest when only sulfur was compared.

Each result has a text summary with the key numbers and a compact card. Give those numbers in the reply. If a calculation returns an error with a list of choices, ask the user which one they mean, or search again. Do not invent missing recipes or yields.

Only these public game calculators are available. They cannot read accounts, inventory, private player information or Rust+ connections, or operate a server. For unsupported requests, explain that limitation and offer a relevant supported calculation when useful.
