# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Architecture

### Workspace Members
- **`tapo`** — Core Rust library (published to crates.io)
- **`tapo-py`** — Python bindings via PyO3/maturin (published to PyPI)
- **`tapo-mcp`** — MCP server exposing Tapo devices as AI tools/resources

## Cross-Language Bindings

When modifying Rust code that has Python bindings (tapo-py), always check if corresponding Python type stubs (.pyi files) need updating.

## Problem Solving

When a first fix attempt fails, step back and investigate the root cause before trying another surface-level fix. Explain the diagnosis before proposing the next approach.

## Git Commits

- If Rust code was changed, run `cargo fmt` and `cargo clippy` before committing and fix any issues
- If Python code was changed, run `uv run black .` in `tapo-py/` before committing and fix any issues
- Always sign commits (`git commit -S`)
- Do not include a `Co-Authored-By` line
- Always confirm the commit message with the user before committing
