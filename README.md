# Using Libs in Dune with OCaml

I cant seem to get libs recognized by the `main.ml` file.

directoy structure is:

```sh
.
├── _build
│   ├── default
│   │   ├── lib
│   │   └── main
│   │       └── bin
│   └── install
│       └── default
│           └── lib
│               └── lib
├── lib
│   └── _build
├── main
│   ├── _build
│   │   └── default
│   └── bin
└── node_modules

16 directories

```
The `/lib` dir has two files, `math.ml` and `math2.ml`.

The `lib` `dune` file is:

```dune
(library
(name lib))
```

`main.ml` compiles and runs with a `hello world` function.

`main/dune`:

```dune
(executable
  (name main))
```

```sh
➜  using-libs main
➜  main dune clean
➜  main dune build main.exe
➜  main dune exec ./main.exe
Hello, world!
```
