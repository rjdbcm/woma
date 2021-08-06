# woma language
This is the README for the woma language specification; see [Aspidites](https://github.com/rjdbcm/Aspidites)
for the reference compiler implementation written in Python.

## motivation

- Formal verification is an afterthought in most high-level programming languages. e.g. PEP-484 for Python, JML for Java, SPARK for Ada (pre-2014) etc.

## goals

- Formally verifiable CPython extension specification language. 
- Robust and consistent foreign function interface using libffi (currently plan on using the CPython ctypes module).
- Ultra-smooth runtime exception handling with useful warnings.
- Demonic non-determinism, favors type-negotiation over termination.
- Terseness and beauty, in order to make code both concise ___and___ readable.
- Great for writing high-integrity code that works natively with CPython.
- Usable for general purpose scripting ___or___ scientific computing.
