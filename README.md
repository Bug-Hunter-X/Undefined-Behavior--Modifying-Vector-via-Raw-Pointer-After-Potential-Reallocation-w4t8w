# Rust Undefined Behavior Example

This repository demonstrates a common error in Rust leading to undefined behavior: modifying a vector through a raw pointer after the vector might have been reallocated.

## The Bug
The `bug.rs` file contains code that modifies a vector using a raw pointer. However, the vector's capacity might not be large enough to hold the updated value. This can result in a memory safety violation.

## The Solution
The `bugSolution.rs` file presents a safe alternative that uses vector indexing or other safe methods to modify the vector contents.  It avoids raw pointers to prevent undefined behavior.