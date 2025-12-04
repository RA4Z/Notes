Is a method in [[🐍Python]] to determine the **Method Resolution Order (MRO)** in class hierarchies, especially when dealing with [[Multiple Inheritance]].

This algorithm is crucial for avoiding ambiguities and conflicts when multiple parent classes define the same method or attribute.

In C3 Linearization, closer classes in the hierarchy take precedence over distant ones

### How it works
The C3 algorithm computes the MRO by merging the MROs of the parent classes while maintaining their order and ensuring monotonicity.
- 1. Start with the target class and add it to the MRO list
- 2. Merge the MROs of the parent classes while preserving their order
- 3. Select the next class from the lists such that it appears only at the start of the lists
- 4. Remove the selected class from all lists and repeat until all classes are processed

### Examples

The MRO for class `D` is computed as `[D, B, C, A, object]`. Ensuring that [[🐍Python]] resolves methods in a consistent and conflict-free manner
```Python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass
```
--------------------
The MRO for `E` is `[E, D, B, C, A, object]`. This ensures that methods are resolved in a logical order, prioritizing closer ancestors over distant ones.
```Python
class A: pass
class B(A): pass
class C(A): pass
class D(B, C): pass
class E(D, C): pass
```