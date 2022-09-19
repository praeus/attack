Play the demo game at https://liluo.io/praeus/attack-extension-demo.

# GDevelop Attack System and Demo Game
This is a demonstration of the GDevelop Attack extension, which works together with existing GDevelop extensions to create a complete attack system with both melee and ranged attacks. The Attack extension depends on the FireBullet and Health extensions.

# Attack System

This includes several behaviors which work with the the FireBullet and Health extensions to create a complete attack system. The behaviors are Attack, HandheldItem, SwingItem, and HealthBar.

## Attack Extension Setup
There will typically be between two and four objects: the Attacker, the Target, the Weapon, and the Bullet. To set them up:
1. Add the Health behavior to both the Attacker and the Target.
2. Add the Attack behavior to the Attacker.
3. Add either the FireBullet or SwingingItem behavior to the Weapon (if there is one).
4. Use the appropriate "Check X damage" action for the type of attack on each frame.
5. Use the "Attack by..." actions to attack, either by swinging or by firing (or both, or neither).

The attack damage, interval, range, direction, and speed can be configured in the Attack behavior properties. The Attack behavior also maintains a death count and a kill count for the attacker.

## Swinging Behaviors

This also includes behaviors which allow an object to be held and swung like a sword. There are two behaviors which tend to go together, although they could be used separately (e.g. a non-swinging item, like a key).

1. HandheldItem: An object with this behavior can be held by another object at a named point.
    - For the object holding the item, create a custom point or move the "Center" or "Origin" points to wherever the object should be held (the "hand"). 
    - For the item being held, move the "Center" point to wherever the object should be held (like the hilt of a sword).
2. SwingingItem: An object in this behavior can be swung like a sword.
    - You can configure the starting angle, swing speed and swing arc length.
    - The swing can also be inverted to go in the opposite direction.

# Health Bar

As a bonus, this extension includes a behavior for a health bar which can hover above a character and change in response to the character's health.

This works with the "Health" extension to display health information in a health bar which can also hover over the character. 

To use it:
1. Add the HealthBar behavior to the object.
2. Attach the health bar to the object using the "Attach health bar" action.
3. Update the health bar every frame using the "Update health bar" action.

## Attack Demo Game
This game is a demonstration of the Attack extension. This extension is combined with the FireBullet and Health extensions to make a complete character attack system with melee and ranged weapons. These and other extensions are used to create a game where two characters - a wizard and a knight - can fight each other to the death - over and over again - with fire and sword!

You can control the wizard with Up, Down, Left, Right, and "f" to fire ("A" on gamepad). Also, use "z" ("LB") and "x" ("RB") to zoom in and out. Keep moving to stay away from the knight - but you have to stop to fire!
