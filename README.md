# odomu

The MITA standard library.

`odomu` contains the generic Lisp/Scheme-style helpers that ship with
[MITA](https://github.com/mitalang/mita): list operations, sequence helpers,
set operations, sorting, hash-table conversion, and the standard macros.

The library is pure MITA source. It has no Rust, C, or network dependencies.

## Layout

| File | Contents |
|---|---|
| `odomu.mita` | Loader for the whole library |
| `core.mita` | Core list, sequence, set, and predicate helpers |
| `lib.mita` | Sorting and hash-table conversion helpers |
| `macros.mita` | `kasi`, `nyekasi`, `kuzitomo`, `todo`, `handler-case`, `tigadomu` |
| `seq.mita` | Multi-list map, folds, take/drop, zip, range, string helpers |

## Usage

From this repository:

```bash
mita odomu.mita
```

Or load it before an application:

```bash
mita odomu.mita app.mita
```

To use it from another MITA project, vendor this repository at `odomu/` (for
example as a git submodule) and add a loader:

```lisp
; odomu.mita
(movoin "odomu/core.mita")
(movoin "odomu/macros.mita")
(movoin "odomu/lib.mita")
(movoin "odomu/seq.mita")
```

Then run from the project root:

```bash
mita odomu.mita app.mita
```

In the main MITA repository this loader already exists at `odomu.mita`, and
`odomu/` is a git submodule pointing at this repository.

## Functions

Core helpers include `lawakucha`, `lawakuchakucha`, `kuchakucha`, `tiga`,
`tigamani`, `si`, `valo`, `mosi`, `tomo`, `domu`, `mito`, `odomu`, `untasi`,
`eleka`, `ika`, `tigakundala`, `mitosi`, `elekasi`, `manisi`, `sadasi`,
`kuchasi`, `tomosi`, `tomotomo`, `lawatomo`, `kundalasi`, `movosi`,
`tigatomo`, `tigakucha`, `kasi`, `nyekasi`, `inusi`, and `indu`.

Sequence helpers include `sitomo`, `mosiunta`, `tigatakekasi`,
`tigadropkasi`, `tigadu`, `manitiga`, `tigamaplawa`, `sadaberusi`, and
`sadaberudomu`.

Sorting and hash helpers include `tigadada`, `tigadada-sort`,
`tigadada-merge`, `tigatake`, `tigadrop`, `mitotiga`, and `tigamito`.

The macros `kasi`, `nyekasi`, `kuzitomo`, `todo`, `handler-case`, and
`tigadomu` live in `macros.mita`.

## Compatibility

The library targets the MITA VM. The native backend supports a subset of MITA
and does not implement every library helper; see the MITA language
specification for the native subset.

## License

Sumeru Akademiya License. See [LICENSE](LICENSE).
