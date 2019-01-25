# zorio

## Overview

Port of a subset of Rust's standard library I/O module to no_std.

The implementation is taken directly from [libstd](https://github.com/rust-lang/rust/tree/master/src/libstd/io)
with small number of changes to make it work with no_std.
All interfaces and implementation match the original code since they did not need to be altered.
The only exception to this is Error/ErrorKind types where I rolled with something simpler for now.

All credit for this work goes to the incredible Rust developers.

## Story

While working on a bare metal Raspberry Pi 3 project, I found that libcore lacks
data reading/writing functions available in libstd. Since most of them are generic
and operate on streams that are not tied to file/os implementation, why not make them
available to the world of embedded development.

## Status

The following modules were ported over:

| Module            | Status      |
|-------------------|-------------|
| buffered          | Skipped     |
| cursor            | Done        |
| impls             | Done        |
| lazy              | Skipped     |
| mod               | Done        |
| stdio             | Skipped     |
| util              | Skipped     |

## Credits

- Rust developers for providing an incredible language to develop in
