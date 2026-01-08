[[Shading Language]] supports the most commons types of flow control:
```C
// `if`, `else if` and `else`.
if (cond) {

} else if (other_cond) {

} else {

}

// Ternary operator.
// This is an expression that behaves like `if`/`else` and returns the value.
// If `cond` evaluates to `true`, `result` will be `9`.
// Otherwise, `result` will be `5`.
int result = cond ? 9 : 5;

// `switch`.
switch (i) { // `i` should be a signed integer expression.
    case -1:
        break;
    case 0:
        return; // `break` or `return` to avoid running the next `case`.
    case 1: // Fallthrough (no `break` or `return`): will run the next `case`.
    case 2:
        break;
    //...
    default: // Only run if no `case` above matches. Optional.
        break;
}

// `for` loop. Best used when the number of elements to iterate on
// is known in advance.
for (int i = 0; i < 10; i++) {

}

// `while` loop. Best used when the number of elements to iterate on
// is not known in advance.
while (cond) {

}

// `do while`. Like `while`, but always runs at least once even if `cond`
// never evaluates to `true`.
do {

} while (cond);
```