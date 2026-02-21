# Automated Theorem Prover

## What do you want to build?

Build an automated theorem prover in OCaml (or Haskell) that can prove theorems in first-order logic using resolution-based methods. The prover should accept formulas in a standard notation, convert them to clausal form, and search for proofs.

The implementation must include:
- Formula parser: first-order logic with quantifiers (∀, ∃), connectives (∧, ∨, ¬, →, ↔), predicates, functions, and equality
- Clausification pipeline: negation normal form → Skolemization → conjunctive normal form → clause set
- Unification algorithm (Robinson's) with occurs check
- Resolution strategies:
  - Binary resolution
  - Factoring
  - Ordered resolution with literal selection
  - Set-of-support strategy
- Equality handling: paramodulation or superposition calculus
- Proof output: human-readable proof trace showing each inference step
- TPTP format parser (standard theorem prover input format)
- Timeout and search depth limits
- Counter-model generation for non-theorems (when possible)

## How do you consider the project is success?

1. Proves all 20 problems from TPTP "easy" category (SYN, PUZ domains, rating 0.0-0.3)
2. Solves Pelletier's problems 1-20 (standard first-order logic benchmark)
3. Unification correctly handles nested function terms (validated on 15 test cases)
4. Skolemization preserves satisfiability — clausified formulas are equisatisfiable with originals
5. Proof traces are valid — each step follows from a legitimate inference rule
6. Equality reasoning handles at least: symmetry, transitivity, congruence (proves `a=b ∧ b=c → f(a)=f(c)`)
7. Prover terminates on non-theorems within timeout (doesn't loop forever) and reports "not proved"
8. Test suite with at least 30 tests covering parsing, unification, clausification, and proof search
