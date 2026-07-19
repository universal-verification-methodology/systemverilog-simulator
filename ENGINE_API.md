# Public engine API (rev5)

ESM module: [`assets/engine.mjs`](assets/engine.mjs)

Stable exports for platform tools (learning monorepo). The full IDE bundle remains obfuscated separately.

## Teaching / combinational

| Export | Role |
|--------|------|
| `normalizeTeachingBoolExpr(expr, names)` | Map `·`/`*`/`+`/`!` / juxtaposition → Verilog ops |
| `createCombEvaluator(expr, names)` | Compile `assign F = …` once; `evalRow` / `evalAll` |
| `evalCombTruthTable(expr, names)` | One-shot `0/1/X` column of length `2^n` |
| `createGateNetEvaluator({ names, gates, output })` | Gate netlist → continuous assigns; `evalBitMap` / `evalAll` |
| `createSession(source, opts)` | Interactive `start` / `step` / `runToEdge` / `poke` / `peek` |

## Core

| Export | Role |
|--------|------|
| `parseLiteral` / `Value` | Literals and bit vectors |
| `simulate` / `compile` / `createSim` | Full subset run / session |
| `parse` / `elaborate` / `evalExpr` | Lower-level pipeline |

Pin a `revN` tag or commit when importing from Pages/CDN.
