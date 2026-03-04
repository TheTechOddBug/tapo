## Code Review Checklist

1. Run `cargo check` and fix any errors
2. Run `cargo clippy` and address any warnings
3. Run `cargo fmt` to ensure code is properly formatted
4. Check if any Python stubs (.pyi) need updating for changed Rust types
5. Review error handling — no unwrap() in library code
6. Verify ownership/borrowing is correct (no unnecessary clones)
7. Present a summary of findings
