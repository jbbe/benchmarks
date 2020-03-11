
build-ml:
	ocamlopt -noassert -unsafe -fPIC -nodynlink -inline 100 -O3  -ccopt -march=core2 nbody.ml -o nbody.ocaml_run

run-ml:
	./nbody.ocaml_run 50000000

build-rs:
	rustc -C opt-level=3 -C target-cpu=core2 -C lto -C codegen-units=1 -C llvm-args='-unroll-threshold=500' nbody.rs -o nbody.rust-3.rust_run

run-rs:
	./nbody.rust-3.rust_run 50000000