In [[GDScript]], moves the body based on [[velocity]]. If the body collides with another, it will slide along the other body rather than stop immediately. If the other body is a [[CharacterBody3D]] or [[RigidBody3D]], it will also be affected by the motion of the other body.

Modifies [[velocity]] if a slide collision occurred. To get the latest collision call [[get_last_slide_collision()]], for more detailed information about collisions that occurred, use [[get_slide_collision()]].

When the body touches a moving platform, the platform's velocity is automatically added to the body motion. If a collision occurs due to the platform's motion, it will always be first in the slide collisions.

Returns `true` if the body collided, otherwise, returns `false`.