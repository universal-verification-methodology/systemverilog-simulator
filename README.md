# HDL Simulator

Browser-based HDL workbench (SystemVerilog subset simulator + waveform UI).

**Release:** `rev4`

## Quick start

Open `index.html` via any static file server, or:

```bash
npx --yes serve . -p 4173
```

Then visit http://127.0.0.1:4173/

## Notes

- This repository contains the **public release build** (bundled / obfuscated workbench).
- **Library API for teaching tools:** `assets/engine.mjs` (minified ESM, stable exports — not heavily obfuscated).
- Source development lives in a separate private repository.
- See `version.json` for the exact revision stamp.
- See `ENGINE_API.md` for the public engine surface used by the learning platform.

## Library (engine.mjs)

```js
import {
  createCombEvaluator,
  evalCombTruthTable,
  parseLiteral,
  simulate,
  compile,
} from "./assets/engine.mjs";

const outs = evalCombTruthTable("A & B", ["A", "B"]); // [0,0,0,1]
```

## License

MIT
