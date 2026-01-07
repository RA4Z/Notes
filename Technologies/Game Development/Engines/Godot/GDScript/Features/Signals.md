In [[GDScript]], Signals are a feature that enable nodes to communicate with each other without direct references

### Emitting Signals
You can define custom signals in [[GDScript]] using the _signal_ keyword. For example
```Javascript
extends Node2D
signal health_depleted
var health = 10
func take_damage(amount):
   health -= amount
   if health <= 0:
       health_depleted.emit()
```

Here, the _health_depleted_ signal is emitted when the player's health reaches zero. Signals can also include arguments
```Javascript
signal health_changed(old_value, new_value)
func take_damage(amount):
   var old_health = health
   health -= amount
   health_changed.emit(old_health, health)
```

### Connecting Signals
#### Connecting in the Editor
- Select the node emitting the signal
- Open the **Node** tab and double-click the desired signal
- Choose the target node and specify the callback function
- The editor generates a function like `_on_node_signal()` in the target node's script

#### Connecting via Code
To connect a signal programmatically, use the `connect()` method
```Javascript
func _ready():
   var timer = get_node("Timer")
   timer.timeout.connect(_on_timer_timeout)
func _on_timer_timeout():
   print("Timer finished!")
```

Signals can be connected to methods for event handling
```Javascript
func _ready():
   connect("health_changed", self, "_on_health_changed")
func _on_health_changed(new_health):
   print("Health is now:", new_health)
```

### Pratical Use Cases
- Updating a UI element when a game entity's state changes
- Triggering animations or effects when an event occurs
- Managing interactions between game objects, such as detecting collisions or area entries