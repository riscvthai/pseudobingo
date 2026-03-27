**RISC-V Pseudoinstruction Bingo** — a browser-based classroom game for learning the difference between real RISC-V instructions and pseudoinstructions.

Live at: https://pseudo.riscvthai.org/

\---

## What it does

Instructions are called one at a time. Players mark their bingo card when they recognize a pseudoinstruction. The caller (instructor or automated) works through a shuffled deck. First to complete a row wins.

Teaches: which mnemonics are real ISA instructions vs. assembler conveniences that expand to one or more real instructions (`li`, `mv`, `ret`, `call`, `beqz`, etc.).

## How to run it

No install. No framework. No server-side code required.

```sh
git clone https://github.com/riscvthai/pseudobingo
cd pseudobingo
# open index.html in any browser
```

Or just point a web server at the directory. Static files only.

## How to fork it

The instruction list is a plain JS array at the top of `index.html`. Replace or extend it for your course. Translate the UI strings for your language. Deploy anywhere that serves static HTML.

```js
const instructions = \[
  { mnemonic: "li",   type: "pseudo",  expands: "addi rd, x0, imm" },
  { mnemonic: "add",  type: "real" },
  // add yours here
];
```

## Files

```
index.html      ← game, all self-contained
style.css       ← optional separate stylesheet
README.md
```

## History

Debuted at World RISC-V Days, San Jose, February 2025.
Part of the riscvthai.org educational games suite.

## License

MIT. Fork freely. Attribution appreciated but not required.

## Related

* https://github.com/riscvthai/rvcbingo — compressed instruction variant
* https://github.com/riscvthai/games — full suite index
* https://riscvthai.org — Thai RISC-V educational resource

