# OCaml
### notes, command-line, and program output

NOTES:
64-bit Ubuntu quad core
The OCaml native-code compiler, version 4.10.0


Sat, 22 Feb 2020 17:01:13 GMT

MAKE:
mv binarytrees.ocaml-2.ocaml binarytrees.ocaml-2.ml
/opt/src/ocaml-4.10.0/bin/ocamlopt -noassert -unsafe -fPIC -nodynlink -inline 100 -O3 unix.cmxa -ccopt -march=core2 binarytrees.ocaml-2.ml -o binarytrees.ocaml-2.ocaml_run
rm binarytrees.ocaml-2.ml

2.59s to complete and log all make actions

COMMAND LINE:
./binarytrees.ocaml-2.ocaml_run 21

PROGRAM OUTPUT:
stretch tree of depth 22	 check: 8388607
2097152	 trees of depth 4	 check: 65011712
524288	 trees of depth 6	 check: 66584576
131072	 trees of depth 8	 check: 66977792
32768	 trees of depth 10	 check: 67076096
8192	 trees of depth 12	 check: 67100672
2048	 trees of depth 14	 check: 67106816
512	 trees of depth 16	 check: 67108352
128	 trees of depth 18	 check: 67108736
32	 trees of depth 20	 check: 67108832
long lived tree of depth 21	 check: 4194303
    

### Rust


notes, command-line, and program output

NOTES:
64-bit Ubuntu quad core
rustc 1.41.0 (5e1a79984 2020-01-27)
LLVM version: 9.0


Fri, 31 Jan 2020 00:34:30 GMT

MAKE:
/opt/src/rust-1.41.0/bin/rustc -C opt-level=3 -C target-cpu=core2 -C lto -C codegen-units=1 -L /opt/src/rust-libs binarytrees.rs -o binarytrees.rust-2.rust_run

17.17s to complete and log all make actions

COMMAND LINE:
./binarytrees.rust-2.rust_run 21

PROGRAM OUTPUT:
stretch tree of depth 22	 check: 8388607
2097152	 trees of depth 4	 check: 65011712
524288	 trees of depth 6	 check: 66584576
131072	 trees of depth 8	 check: 66977792
32768	 trees of depth 10	 check: 67076096
8192	 trees of depth 12	 check: 67100672
2048	 trees of depth 14	 check: 67106816
512	 trees of depth 16	 check: 67108352
128	 trees of depth 18	 check: 67108736
32	 trees of depth 20	 check: 67108832
long lived tree of depth 21	 check: 4194303
    

