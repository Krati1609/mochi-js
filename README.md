# 🍡 mochi-js

a tiny javascript interpreter, built from scratch because i wanted to know how the magic actually works.

no babel, no acorn, no "just use a library". just me, a text editor, and way too much chai.

> status: just started. things are probably broken. that's the vibe.

## what is this

mochi takes a small slice of JavaScript, chops it into tokens, turns those into a tree, and then walks the tree to actually run it. it's a toy, not a replacement for V8 (lol), but it's mine and i understand every line.

## how it works (the plan)

```
source code  →  lexer  →  parser  →  AST  →  evaluator  →  output
```

1. **lexer**: reads the raw text and spits out tokens
2. **parser**: turns tokens into an AST
3. **evaluator**: walks the AST and runs it

## roadmap

Development is split into phases. Each phase builds on the one before it.

### Phase 1: Front end
- [ ] Project setup and repository structure
- [ ] Lexer: tokenization of literals, identifiers, keywords, and operators, with source position tracking
- [ ] Parser: recursive-descent parsing of expressions with correct operator precedence
- [ ] AST node definitions
- [ ] Tree-walking evaluator for expressions

### Phase 2: State and control flow
- [ ] Variable declarations (`let`, `const`) and assignment
- [ ] Environment records and lexical scope chains
- [ ] Block scoping
- [ ] Conditional statements (`if` / `else`)
- [ ] Iteration (`while`, `for`)

### Phase 3: Functions
- [ ] Function declarations and expressions
- [ ] Call stack and `return` handling
- [ ] Closures (lexical environment capture)
- [ ] Arrow functions

### Phase 4: Data types
- [ ] Primitive types: boolean, `null`, `undefined`
- [ ] Arrays
- [ ] Objects
- [ ] Property access (dot and bracket notation)

### Phase 5: Tooling and robustness
- [ ] `console.log` and basic built-ins
- [ ] Error reporting with line and column information
- [ ] Interactive REPL
- [ ] Automated test suite
- [ ] Standard library methods (`Array.prototype.push`, `map`, etc.)

### Phase 6: Stretch goals
- [ ] Bytecode compiler
- [ ] Virtual machine for bytecode execution
- [ ] Performance benchmarks against the tree-walking evaluator

## running it

not yet, nothing to run lol. will update this when there is.

## what i'm learning

- how lexers and parsers actually work
- what an AST really is
- how scope and closures work under the hood

(will fill this in as i go)

## license

MIT