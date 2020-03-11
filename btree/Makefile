


build-ml:
	mv binarytrees.ocaml-2.ocaml binarytrees.ocaml-2.ml
	ocamlopt -noassert -unsafe -fPIC -nodynlink -inline 100 -O3 unix.cmxa -ccopt -march=core2 binarytrees.ocaml-2.ml -o binarytrees.ocaml-2.ocaml_run
	rm binarytrees.ocaml-2.ml

build-rs:
	rustc -C opt-level=3 -C target-cpu=core4 -C lto -C codegen-units=1 -L /usr/lib/rustlib binarytrees.rs -o binarytrees.rust-3.rust_run

run-rs:
	./binarytrees.rust-3.rust_run 21