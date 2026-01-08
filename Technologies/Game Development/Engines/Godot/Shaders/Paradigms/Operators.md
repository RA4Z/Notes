[[Shading Language]] supports the same set of operators as GLSL ES 3.0.

| Precedence  | Class                  | Operator         |
| ----------- | ---------------------- | ---------------- |
| 1 (highest) | parenthetical grouping | **()**           |
| 2           | unary                  | **+, -, !, ~**   |
| 3           | multiplicative         | **/, *, %**      |
| 4           | additive               | **+, -**         |
| 5           | bit-wise shift         | **<<, >>**       |
| 6           | relational             | **<, >, <=, >=** |
| 7           | equality               | **==, !=**       |
| 8           | bit-wise AND           | **&**            |
| 9           | bit-wise exclusive OR  | **^**            |
| 10          | bit-wise inclusive OR  | **\|**           |
| 11          | logical AND            | **&&**           |
| 12 (lowest) | logical inclusive OR   | **\|**           |
