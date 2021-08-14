# woma programming language
This is the README for the woma language specification; see [Aspidites](https://github.com/rjdbcm/Aspidites)
for the reference compiler implementation written in Python.

## specification
Woma has a specification that is published as a series of WEEP(Woma Extension & Evaluation Proposals), see [QQ.md](QQ.md).

## motivation

- Formal verification is an afterthought in most high-level programming languages. e.g. PEP-484 for Python, JML for Java, SPARK for Ada (pre-2014) etc.

## goals

- Formally verifiable CPython extension specification language. 
- Robust and consistent foreign function interface using libffi (currently plan on using the CPython ctypes module).
- Ultra-smooth runtime exception handling with useful warnings.
- Demonic non-determinism, favors type-refinement over termination.
- Terseness and beauty, in order to make code both concise ___and___ readable.
- Great for writing high-integrity code that works natively with CPython.
- Usable for general purpose scripting ___or___ scientific computing.

## paradigms

- [`refinement-type system`](https://arxiv.org/pdf/2010.07763.pdf)
- [`pragmatic`](https://www.adaic.org/resources/add_content/standards/05rm/html/RM-2-8.html)
- `declarative`
- [`functional`](https://towardsdatascience.com/why-developers-are-falling-in-love-with-functional-programming-13514df4048e?gi=3361de79dc98)
- [`constrained logic`](https://www.cse.unsw.edu.au/~tw/brwhkr08.pdf)


## contributing

If you'd like to help with the woma standard as a developer check out the Issues page or fork and make a pull request.
Now, for early woma adopters that do not wish to do any technical writing, reporting inconsistencies or contradictions is always appreciated.
If you'd like to help out financially, [Aspidites](https://github.com/rjdbcm/Aspidites)' maintainer accepts [Liberapay](https://liberapay.com/rjdbcm/).
