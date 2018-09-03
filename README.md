Glossary
--------

### CASO

**C**ontext, **a**ction, **s**uccessor context, **o**ther contexts. Reflection
graph format with this basic unit:

```
Context
│
Action
│
├─ Successor context
├─ Other contexts
└─ …
```

This doesn't permit drilling down into child and niece contexts.

### CSR

**C**ontext, **s**ource, **r**esult. Reflection graph format with the basic
unit:

```
Context
├─ Source
│  ├─ Starting context
│  ├─ Action
│  ├─ Successor context
│  ├─ Other contexts
│  └─ …
└─ Result
   ├─ Same as above
   └─ …
```

Does permit drilling down into child and niece contexts.

Repository contents
-------------------

These files use a jumble of schemes and formats. This is bad for comprehension,
but it lets us pick and choose.

- [reflected-locked-pointer.txt](reflected-locked-pointer.txt) CASO:
    - Answer pointer of the same subquestion both in the reflected and the
      actual context.

- [reflected-locked-pointer.edn](reflected-locked-pointer.edn) CSR:
    - Same scenario as in reflected-locked-pointer.txt.
    - Explores EDN representation.
    - And path-based pointers.
    - And "unlocking" pointers of reflected contexts.
    - And age of reflected context.
