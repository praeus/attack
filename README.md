# GDevelop Attack System
This includes three new GDevelop extensions which work together with existing GDevelop extensions to create a complete attack system with both melee and ranged attacks. The new extensions are Attack, SwingItem, and HealthBar and they depend on the FireBullet and Health extensions.

## Swing Item
This allows an object to be held and swung like a sword. There are two behaviors which tend to go together, although they could be used separately (e.g. a non-swinging item, like a key).

1. HandheldItem allows you to have the item be held by another object at a named point.
    - For the object holding the item, create a custom point or move the "Center" or "Origin" points to wherever the object should be held (the "hand"). 
    - For the item, move the "Center" point to wherever the object should be held (like the hilt of a sword).
2. SwingingItem actually swings the item. You can configure the starting angle, swing speed and swing arc length. The parameters can also be inverted to swing in the opposite direction.

## Attack Extension
This is meant to be used along with the FireBullet, Health, and SwingItem behaviors. There will typically be three or four objects: the Attacker, the Weapon, the Bullet, and the Target. To set them up:
1. Add the Health behavior to both the Attacker and the Target.
2. Add the Attack behavior to the Attacker.
3. Add either the FireBullet or SwingItem behavior to the Weapon, depending on which you want to attack with.
    1. If using FireBullet, then use the "Check if X is damaging" event on each frame.
4. Add the Armor behavior to the Target. Use this to configure how much damage reduction the character has.
5. Use the "Have X attack..." events to attack, either by swinging or by firing.

The attack damage, interval, range, direction, and speed can be configured in the Attack behavior properties. The Attack behavior also maintains a death count and a kill count for the attacker.

## Attack Demo Game
The game is a demonstration of the Attack extension along with the SwingItem and HealthBar extensions combined with the FireBullet and Health extensions. These and other extensions are used to create a game where two characters - a wizard and a knight - can fight each other to the "death" with fire and sword!

You can control the wizard with Up, Down, Left, Right, "f" to fire, and + and - to zoom. Keep moving to stay away from the knight - but you have to stop to fire!
