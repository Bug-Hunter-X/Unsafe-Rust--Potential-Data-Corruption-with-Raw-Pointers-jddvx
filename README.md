# Unsafe Rust: Raw Pointer Manipulation

This repository demonstrates a potential issue with unsafe Rust code when working with raw pointers and vectors.  Directly modifying the raw pointer of a vector without understanding the memory layout and ownership can lead to data corruption or program crashes.

## Bug Description

The `bug.rs` file contains a code sample where a vector's raw pointer is obtained using `as_mut_ptr()` and directly manipulated. This approach bypasses Rust's memory safety guarantees and can have unpredictable results.  The code attempts to change the first element of the vector and then prints the modified vector.

## Solution

The `bugSolution.rs` file provides a safer and more idiomatic way of modifying the vector's contents. This solution uses safe Rust methods to modify the vector's elements without directly accessing raw pointers, ensuring memory safety and avoiding potential data corruption.