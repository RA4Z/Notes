In [[🐍Python]], when you pass a variable to a function, the function receives a reference to the object, not the actual variable itself. The behavior depends on whether the object is **[[Mutable]]** or **[[Immutable]]**.

- **[[Immutable]] Objects:** When passed to a function, any modification creates a new object, the original remains unchanged outside the function

- **[[Mutable]] Objects:** When passed to a function, modifications to the object are reflected outside the function, because the function operates on the same object reference

- **Reassignment in Functions:** If a [[Mutable|mutable]] object is reassigned inside a function, it doesn't affect the original outside the function. The reassignment creates a new list object, leaving the original list unchanged

### Summary of Behavior
- **[[Immutable]] Objects:** Behave like "pass-by-value" because changes create new objects
- **[[Mutable]] Objects:** Behave like "pass-by-reference" when modified in place, but reassignment creates a new reference