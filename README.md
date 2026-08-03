# Leo Zhang

I work on combinatorics, and on software whose claims can be checked by someone
who does not trust me.

## Mixed van der Waerden numbers

I have been computing new terms in families of mixed van der Waerden numbers
whose OEIS entries were last extended by Tanbir Ahmed in 2012 and were still
unchanged when I checked them against the OEIS API on 29 July 2026.

For colour targets `t_1..t_r` and a budget of `j` wildcards,

```
w(j+r; 2^j, t_1..t_r) = 1 + max{ n : [1,n] splits into j singleton classes and
                                 r colour classes, where colour class i contains
                                 no t_i-term arithmetic progression }
```

Each new term needs two independent halves. The lower bound is a colouring, and
a colouring is a certificate — you read the string and apply the definition, no
solver involved. The upper bound asserts that *no* colouring exists, which is
only as trustworthy as the encoding behind it, so that half is where the work is.

**Status, stated exactly.**

- Four new terms established across four families, each shipping evidence
  alongside the claim rather than a solver's word for it.
- **A217058 a(12) = 57 is submitted to the OEIS and under editorial review.**
  It is *proposed*, not approved. Three further terms are prepared for
  submission and have not been submitted.
- DRAT refutation certificates are produced and independently verified for
  small rungs of all four families. **The headline term is not yet certified**
  at that standard, and the write-up says so.
- A fifth term is computed and deliberately withheld: its family-consistency
  gate was interrupted without returning a verdict, so it is excluded from the
  submission pack until that gate runs to completion.

Method, encoding, symmetry breaking and the limits of what has actually been
proved are written up in [MathRecords](https://github.com/GreenPandaTech/MathRecords).
The standalone certificate verifier depends on nothing but the Python standard
library.

## What I build

Roughly one idea, applied repeatedly: a result is worth what its verification is
worth. Compilers and interpreters, a consensus implementation whose safety
properties are machine-checked by deterministic simulation, a physically
validated renderer written with no dependencies, numerical simulation, and a
production web application. Most of it is private.

Mostly Python and TypeScript, with SAT solvers, DRAT/LRAT proof checking, and
whatever numerical method the problem happens to need.

## Currently

Extending the same machine-checkable approach to integer sequences on board
graphs, and reading towards Cambridge and Imperial Computer Science for 2028
entry.

Contact: open an issue on any repository here.
