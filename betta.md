# Betta Blitz
A new shipment of bettas have arrived at your local fish store, and there's a huge crowd of people waiting to buy them! The fish store needs your help ordering these bettas in order of highest value.

Each betta has a unique name associated with it. The first **N** bettas are known famous bettas, which have set costs. The next **M** bettas are descendents of at least 2 bettas from the first **N** bettas. For example, a betta may be the direct offspring of 2 of the first **N** bettas, and it could also be the offspring of one of the first **N** bettas and one of the **M** bettas (which itself is also descended from the first **N** bettas). Note that a betta may be listed before its ancestor!

A betta's value is just its cost. If the bettas is one of the **M** latter bettas, its value should be assigned to the average of all of its ancestors in **N**'s cost. If multiple bettas have the same costs, these bettas should be tie-broken with the following color specification (top of the list = most value):

1. Red
2. Green
3. Blue
4. Orange
5. Pink
6. Purple
7. Black
8. White

Output the bettas' names in order of highest value.

----------------
Input Format:
```
N, M
<name_1> <color> <cost>
...
<name_N> <color> <cost>
<name_1> <color> <parent1_name> <parent2_name>
...
<name_N> <color> <parent1_name> <parent2_name>
```
Output Format:
```
<name (1st highest value)>
...
...
<name (N+Mth highest value, aka lowest value)>
```
----------------
Test Case 1 Input:
```
2, 1
Bubbles Blue 10
Shadow Black 5
Spot Black Bubbles Shadow
```
Test Case 1 Output:

```
Bubbles
Spot
Shadow
```
----------------
Test Case 2 Input:
```
5, 2
Bubbles Blue 10
Shadow Black 6
Crimson Red 5
Freckles Red 2
Boo White 8
Anarchy Black Crimson Spot
Spot Black Bubbles Shadow
```
Test Case 2 Output:

```
Bubbles
Spot
Boo
Anarchy
Shadow
Crimson
Freckles
```
