# Woma Programming Language
This is the README for the Woma Programming Language specification; see [Aspidites](https://github.com/rjdbcm/Aspidites) for the reference compiler implementation written in Python. 

**If this wasn't what you were looking for there is another project [WoMa](http://github.com/srbonilla/WoMa) that uses the PyPI namespace woma.** 

## Why Woma?
  
When developing C extensions for Python it is common to struggle with debugging. Being written in C, there is no memory safety which make failures common. These faults tend to take the form of segmentation faults which can be especially difficult to debug. This is especially true of remote builds where you may not even have access to the proper system resources to find the source of a bug. There are tools like Cython that can help to reduce the chances of a encountering an error due to memory violations. These tools, however, are not 100% effective and you can still be left with particularly hard to debug errors. Woma aims to improve this by using contract-based constraints on function parameters and return values. This is combined with syntax that encourages writing and composing short functions. Additionally error messages are highly informative and Woma only allows procured access to Python internals.

## Specification
Woma has a specification that is published as a series of WEEP(Woma Extension & Evaluation Proposals), see [QQ.md](QQ.md).

## Motivation

- Formal verification is an afterthought in most high-level programming languages. e.g. PEP-484 for Python, JML for Java, SPARK for Ada (pre-2014) etc.

## Goals

- Formally verifiable CPython extension specification language. 
- Robust and consistent foreign function interface using libffi (currently plan on using the CPython ctypes module).
- Ultra-smooth runtime exception handling with useful warnings.
- Demonic non-determinism, favors type-refinement over termination.
- Terseness and beauty, in order to make code both concise ___and___ readable.
- Great for writing high-integrity code that works natively with CPython.
- Usable for general purpose scripting ___or___ scientific computing.

## Paradigms

- [`refinement-type system`](https://arxiv.org/pdf/2010.07763.pdf)
- [`pragmatic`](https://www.adaic.org/resources/add_content/standards/05rm/html/RM-2-8.html)
- `declarative`
- [`functional`](https://towardsdatascience.com/why-developers-are-falling-in-love-with-functional-programming-13514df4048e?gi=3361de79dc98)
- [`constrained logic`](https://www.cse.unsw.edu.au/~tw/brwhkr08.pdf)


## Contributing

If you'd like to help with the woma standard as a developer check out the Issues page or fork and make a pull request.
Now, for early woma adopters that do not wish to do any technical writing, reporting inconsistencies or contradictions is always appreciated.
If you'd like to help out financially, [Aspidites](https://github.com/rjdbcm/Aspidites)' maintainer accepts [Liberapay](https://liberapay.com/rjdbcm/).
