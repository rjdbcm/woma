# WEEP0 14-Aug-2021 The First WEEP
There are Woma Extension and Evaluation Proposals. The name Woma Extension & Evaluation Proposals can be shortened to WEEP. There is a continuous record of WEEP, published in the woma repository under QQ.md. A WEEP should be called WEEP followed by an integer. The integer is one value higher than the last WEEP published.
A new WEEP should also be of the format `# WEEPX 03-Jun-1993 A Title Case Title`

# WEEP1 14-Aug-2021 Static Compilation of CPython Extensions
Woma is a compiled language targetting CPython extensions and [Aspidites](https://github.com/rjdbcm/Aspidites) is the reference implementation.
Woma can be compiled to Python, Cython, or C but generally the Aspidites toolchain works in the following order:
1. Woma is compiled to Python and checked for static and bytecode validity. (without parsable cdef and cpdef statements)
2. PEP 561 stubs are generated as is py.typed.
3. The validated Python is converted to Cython. (cdefs and cpdefs included)
4. Cython compiles using the host architecture's compiler and linker.
