# Woma Extension and Evaluation Proposals

## WEEP0 14-Aug-2021 The First WEEP
There are Woma Extension and Evaluation Proposals. The name Woma Extension & Evaluation Proposals can be shortened to WEEP. There is a continuous record of WEEP, published in the woma repository under QQ.md. A WEEP should be called WEEP followed by an integer. The integer is one value higher than the last WEEP published.
A new WEEP should also be of the format `## WEEPX 03-Jun-1993 A Title Case Title`

## WEEP1 14-Aug-2021 Static Compilation of CPython Extensions
Woma is a compiled language targetting CPython extensions and [Aspidites](https://github.com/rjdbcm/Aspidites) is the reference implementation.
Woma can be compiled to Python, Cython, or C but generally the Aspidites toolchain works in the following order:
1. Woma is compiled to Python and checked for static and bytecode validity. (without parsable cdef and cpdef statements)
2. PEP 561 stubs are generated as is py.typed.
3. The validated Python is converted to Cython. (cdefs and cpdefs included)
4. Cython compiles using the host architecture's compiler and linker.

## WEEP2 14-Aug-2021 FORMAL.txt and Attempto Controlled English
Every WEEP must be formalized in FORMAL.txt using Attempto Controlled English.

## WEEP3 12-Oct-2021 WEEP2 SUPERSEDED
~~Every WEEP must be formalized in FORMAL.txt using Attempto Controlled English.~~
Every WEEP will be here from now on.

## WEEP4 12-Oct-2021 WEEP1 SUPERSEDED
Woma is a compiled language targetting CPython extensions and [Aspidites](https://github.com/rjdbcm/Aspidites) is the reference implementation.
Woma can be compiled to Python, Cython, or C but generally the Aspidites toolchain works in the following order:
1. Woma is compiled to Python and checked for static and bytecode validity. (without parsable cdef and cpdef statements)
~~2. PEP 561 stubs are generated as is py.typed.~~
2. py.typed is generated.
3. The validated Python is converted to Cython. (cdefs and cpdefs included)
4. Cython compiles using the host architecture's compiler and linker.

## WEEP5 13-Oct-2021 Trigrams and Reserved Symbols
Trigrams are the preferred way of implementing language, as opposed to standard library, features. 

The following symbols are reserved for language features having to do with scope:
- <!>
- <@>
- <#>
- <$>
- <%>
- <^>
- <&>
- <*>
- <_>
- <+>

The following symbols are reserved for language features having to do with higher-order function manipulation:
- (!)
- (@)
- (#)
- ($)
- (%)
- (^)
- (&)
- (*)
- (_)
- (+)

## WEEP6 14-Oct-2021 Function Arguments
Arguments must be specified with a bind variable, a default value, and a contract imposing constraints.
e.g. 
```
x = 0 -> number

```

