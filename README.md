# Failed example of surf hello-world

This example is taken from `surf/examples/hello_world.rs`. 

Toolchain is beta (beta-x86_64-unknown-linux-gnu), 
rustc 1.39.0-beta.2 (5752b6348 2019-09-27)

On `cargo build` it fails with an exception
```
error[E0277]: the trait bound `std::io::Empty: futures_io::if_std::AsyncRead` is not satisfied
  --> /home/akviatko/.cargo/registry/src/github.com-1ecc6299db9ec823/surf-1.0.2/src/http_client/mod.rs:64:21
   |
64 |             reader: Box::new(std::io::empty()),
   |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^ the trait `futures_io::if_std::AsyncRead` is not implemented for `std::io::Empty`
   |
   = note: required for the cast to the object type `dyn futures_io::if_std::AsyncRead + std::marker::Send + std::marker::Unpin`

error: aborting due to previous error

For more information about this error, try `rustc --explain E0277`.
error: could not compile `surf`.

To learn more, run the command again with --verbose.
```