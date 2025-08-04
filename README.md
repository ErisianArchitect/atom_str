A simple library for interning strings.

Atoms are string singletons that live for the lifetime of the program. For any given string that is made into an Atom, there will only be one instance of that Atom allocated for the program. After an Atom is created, it can not be destroyed.

```rust
let atom_a = Atom::new("single instance");
let atom_b = Atom::new("single instance");
assert_eq!(Atom::ptr_eq(&atom_a, &atom_b));
```