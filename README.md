# pleme-kindstr-derive

Paired string round-trip over a unit-variant enum: pub fn as_str(&self) -> &'static str + pub fn from_str_kind(&str) -> Option<Self>, both folded from one variant walk so the inverse-table property holds by construction. Honors per-variant #[kind(name = "...", alias = "...")] helper attrs.

[![Build](https://github.com/pleme-io/pleme-kindstr-derive/actions/workflows/auto-release.yml/badge.svg)](#)
[![crates.io](https://img.shields.io/crates/v/pleme-kindstr-derive.svg)](https://crates.io/crates/pleme-kindstr-derive)

## Install

```toml
[dependencies]
pleme-kindstr-derive = "*"
```

## Generation

This crate is mechanically emitted by [`tatara-rust-ast`](https://github.com/pleme-io/tatara-rust-ast). The author surface is a typed `(defmacro …)` Spec — the proc-macro implementation, tests, Nix flake, caixa wrapper, and CI workflow are all generated. See the catalog at `catalog.json` in the parent registry.
