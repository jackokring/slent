# Slent (A Bad Pancake Day Joke 2024)



## Must Do

1. I must remember to build in a licence notice in the about menu as per the
instructions for a free desktop and web licence of slint.
2. Add in "embedded" python and some `.bashrc` (it's one way of making a binding).
	```
	alias venv='python -m venv'

	# clean cargo better
	valet() {
		# move executables to base directory
		mkdir -p ./valet
		find ./target -type f -executable -exec mv {} ./valet \;
		# remove the target and build directories
		cargo clean
		mkdir -p ./target
		# find the latest
		cp $(/usr/bin/ls -At ./valet | head -n 1) ./target
		# make it the only contents of target
		rm -r ./valet
	}
	```
3. Profit. ;D
4. A canvas object. Ah, a nice pass time app too.
5. Best way of CLI parsing for batch code. `clap` for rust.
6. Chop off extra render modes as 200 MB for a demo debug is big.
  * Learn features of `cargo build --features` pass to submodule.
  * Wayland build suitable for me.
  * Canvas drawing library in common with GUI library?
  * Check `features` for `clap` in `Cargo.toml`?
7. ...

---

# Slint Rust Template (Origional README.md)

A template for a Rust application that's using [Slint](https://slint.rs) for the user interface.

## About

This template helps you get started developing a Rust application with Slint as toolkit
for the user interface. It demonstrates the integration between the `.slint` UI markup and
Rust code, how to trigger react to callbacks, get and set properties and use basic widgets.

## Usage

1. Install Rust by following the [Rust Getting Started Guide](https://www.rust-lang.org/learn/get-started).
   Once this is done, you should have the ```rustc``` compiler and the ```cargo``` build system installed in your path.
2. Install [`cargo-generate`](https://github.com/cargo-generate/cargo-generate)
    ```
    cargo install cargo-generate
    ```
3. Set up a sample project with this template
    ```
    cargo generate --git https://github.com/slint-ui/slint-rust-template --name my-project
    cd my-project
    ```
3. Build with cargo
    ```
    cargo build
    ```
4. Run the application binary
     ```
     cargo run
     ```

We recommend using an IDE for development, along with our [LSP-based IDE integration for `.slint` files](https://github.com/slint-ui/slint/blob/master/tools/lsp/README.md). You can also load this project directly in [Visual Studio Code](https://code.visualstudio.com) and install our [Slint extension](https://marketplace.visualstudio.com/items?itemName=Slint.slint).

## Next Steps

We hope that this template helps you get started and you enjoy exploring making user interfaces with Slint. To learn more
about the Slint APIs and the `.slint` markup language check out our [online documentation](https://slint.dev/docs).

Don't forget to edit this README to replace it by yours
