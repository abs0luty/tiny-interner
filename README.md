# `ry_interner` crate.
~300 lines of Rust code that implement string internering for your programming language compiler.

## Example
```rs
fn main() {
    let interner = Interner::default();
    let s1 = interner.get_or_intern("test");
    let s2 = interner.get_or_intern("test");
    assert_eq!(s1, s2);

    assert_eq!(interner.resolve(0).unwrap(), "test");
}
```
