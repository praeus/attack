Play the demo game at https://liluo.io/praeus/attack-extension-demo.

# GDevelop Attack System and Demo Game
This is a demonstration of the GDevelop Attack extension, which works together with existing GDevelop extensions to create a complete attack system with both melee and ranged attacks. The Attack extension depends on the FireBullet and Health extensions.

# Attack System

This extension includes several behaviors which work together create a complete attack system with both ranged and melee weapons. The behaviors are Attack, HandheldItem, SwingingItem, Target, and HealthBar.

## Attack Behavior Setup

There will typically be at least two objects: the Attacker and the Target. To set them up:
1. Add the Attack behavior to the Attacker.
2. Add the Target behavior to the Target.
3. On each frame, use the "Check for damage" action to check if the Target is being damaged by a weapon or projectile.
4. Use the "Attack by..." actions to attack, either by swinging or by firing (or both, or neither).
    - The action can be invoked in response to a specific event, like a key press, or it can be run on every frame to auto-attack.

The attack damage, interval, range, and direction can be configured in the Attack behavior properties. The Attack behavior also maintains a kill count for the attacker. The Target behavior keeps track of damage done and the death count for the target.

## Swinging Behaviors

This also includes behaviors which allow an object to be held and swung like a sword. There are two behaviors which tend to go together, although they could be used separately (e.g. a non-swinging item, like a key).

1. HandheldItem: An item with this behavior can be held by another object at a named point.
    - For the object holding the item, create a custom point or move the "Center" or "Origin" points to wherever the item should be held by the object (the "hand") . 
    - For the item being held, move the "Center" point to wherever it should be held (like the hilt of a sword).
2. SwingingItem: An object in this behavior can be swung like a sword.
    - You can configure the starting angle, swing speed and swing arc length.
    - The swing can follow the rotation of the object holding the item.

# Health Bar
This extension also includes a behavior for a health bar which can hover above a shape painter object and change in response to the damage done to the Target. To use the health bar:
1. Add the HealthBar behavior to the Target.
2. Attach the health bar to the object using the "Attach health bar" action.
3. Update the health bar every frame using the "Update health bar" action.

## Attack Demo Game
This game is a demonstration of the Attack extension. This extension is combined with the FireBullet and Health extensions to make a complete character attack system with melee and ranged weapons. These and other extensions are used to create a game where two characters - a wizard and a knight - can fight each other to the death - over and over again - with fire and sword!

You can control the wizard with Up, Down, Left, Right, and "f" to fire ("A" on gamepad). Also, use "z" ("LB") and "x" ("RB") to zoom in and out. Keep moving to stay away from the knight - but you have to stop to fire!
