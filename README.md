# Rust hooks for pre-commit

[Rust](https://www.rust-lang.org) tools package for [pre-commit](https://pre-commit.com).

## Using rust tools with pre-commit

```yaml
-   repo: https://github.com/doublify/pre-commit-rust
    rev: master
    hooks:
    -   id: fmt
    -   id: cargo-check
```

## Using in a monorepo where Cargo.toml is not in the root of the repository.

```yaml
  - repo: https://github.com/substra-it/pre-commit-rust
    rev: v1.0
    hooks:
      - { id: fmt, args: [--manifest-path, ${RUST_PROJECT_PATH}/Cargo.toml, --] }
```

## Passing arguments to rustfmt

```yaml
-   repo: https://github.com/doublify/pre-commit-rust
    rev: master
    hooks:
    -   id: fmt
        args: ['--verbose', '--edition', '2018', '--']
```
