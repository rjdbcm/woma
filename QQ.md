# Woma Extension and Evaluation Proposals

## WEEP0 14-Aug-2021 The First WEEP
There are Woma Extension and Evaluation Proposals. The name Woma Extension & Evaluation Proposals can be shortened to WEEP or WEEPs. There is a continuous record of WEEP, published in the woma repository under QQ.md. A WEEP should be called WEEP followed by an integer. The integer is one value higher than the last WEEP published.
A new WEEP should also be of the format `## WEEPX 03-Jun-1993 A Title Case Title`

## WEEP1 14-Aug-2021 Static Compilation of CPython Extensions [SUPERSEDED]
Woma is a compiled language targetting CPython extensions and [Aspidites](https://github.com/rjdbcm/Aspidites) is the reference implementation.
Woma can be compiled to Python, Cython, or C but generally the Aspidites toolchain works in the following order:
1. Woma is compiled to Python and checked for static and bytecode validity. (without parsable cdef and cpdef statements)
2. PEP 561 stubs are generated as is py.typed.
3. The validated Python is converted to Cython. (cdefs and cpdefs included)
4. Cython compiles using the host architecture's compiler and linker.

## WEEP2 14-Aug-2021 FORMAL.txt and Attempto Controlled English [SUPERSEDED]
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
- `<!>` Unassigned
- `<@>` Assigned to enter a loop scope
- `<#>` Assigned to enter a context scope
- `<$>` Unassigned
- `<%>` Unassigned
- `<^>` Assigned to yield to outer scope
- `<&>` Unassigned
- `<*>` Assigned to return to outer scope
- `<_>` Unassigned
- `<+>` Unassigned

The following symbols are reserved for language features having to do with higher-order function manipulation:
- `(!)` Assigned to match construct
- `(@)` Unassigned
- `(#)` Unassigned
- `($)` Unassigned
- `(%)` Unassigned
- `(^)` Unassigned
- `(&)` Unassigned
- `(*)` Unassigned
- `(+)` Unassigned

## WEEP6 14-Oct-2021 Function Arguments
Arguments must be specified with a bind variable, a default value, and a contract imposing constraints such as in the following example:
```
x = 0 -> number
```

## WEEP7 14-Oct-2021 Superseding WEEPs
Superseding WEEPs shoud be formatted as in the following example: `## WEEPY 03-Jun-1993 WEEPX SUPERSEDED`. Any textual information from the superseded WEEP should be kept, using strikethrough text to remove superseded text. The title of the superseded weep should be edited by adding "[SUPERSEDED]" to the end.

## WEEP8 14-Oct-2021 Assigning the (!) Trigram to Pattern Matching
The (!) trigram is to be used for matching indented cases to the right hand bind variable. These cases should be followed by a colon and the action to be preformed upon a successful match. The entire structure looks like as follows:

```
(!)bindvar
  case1: action1
  case2: action2
```

## WEEP9 14-Oct-2021 Adding a Left-hand Variable Binding to (!)
Similar to WEEP8 but implemented as follows.
```
bindvar1(!)bindvar2
  case1: action1
  case2: action2
```

## WEEP10 14-Oct-2021 Arithmetic and Nullity
No arithmetic operation should raise an error. Instead they should be absorbed into nullity. Nullity should be equal and identical to itself but able to carry slotted attributes of the failing operation. The reserved symbol for nullity is the literal ``/0``.

## WEEP11 16-Oct-2021 Reserved Trigrams for Collection Manipulation
The following symbols are reserved for language features having to do with collection manipulation:
- `[!]` Unassigned
- `[@]` Unassigned
- `[#]` Unassigned
- `[$]` Unassigned
- `[%]` Unassigned
- `[^]` Unassigned
- `[&]` Unassigned
- `[*]` Unassigned
- `[_]` Unassigned
- `[+]` Unassigned

## WEEP12 17-Oct-2021 The Woma Interactive Shell and Woma(terse)
There will be an interpreted dialect of Woma, Woma(terse) exclusively for Woma Interactive Shell(WIS) use. The reason for exclusivity is to avoid confusion. In the WIS, the semicolon ``;`` replaces the indentation normally used.

## WEEP13 17-Oct-2021 Syntactically Enforced Default Parameter Values and Constraints
For functions that take parameters, the parameters must be specified with a (preferably reasonable) default value and a constraining contract.

## WEEP14 19-Oct-2021 Nesting Constructs Prohibited
Function definitions and loops may not be nested.
