**GDScript** is a high-level, object-oriented programming language specifically designed for [[Godot]]. It features a syntax similar to [[🐍Python]], making it easy to learn and use.

### Basic Syntax and Examples

#### Variables
Variables are declared using the `var` keyword.
```JavaScript
var health: int = 100
var name: String = "Player"
var position = Vector2(10, 20) # Type inferred as Vector2
```
#### Constants
Constants are defined using the `const` keyword.
```Javascript
const MAX_HEALTH = 100
```
#### Functions
Functions are defined using the `func` keyword
```Javascript
func take_damage(amount: int) -> void:
   health -= amount
   if health <= 0:
       print("Player has died!")
```
#### Control Structures
GDScript supports standard control structures like `if`, `for` and `while`
```Javascript
if health > 0:
   print("Player is alive")
else:
   print("Player is dead")
for i in range(5):
   print(i) # Prints 0 to 4
```