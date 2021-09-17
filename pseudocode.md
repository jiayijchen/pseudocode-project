Pseudocoding Scrambled Eggs

Plain text:
Ingredients:
- Eggs
- Butter
- Salt

Equipment:
- Nonstick skillet
- Whisk
- Rubber Spatula
- Medium Bowl
- Plate

Steps:
1. Crack (n) eggs into bowl.
2. Beat/whisk until uniform.
3. Spread butter on nonsticket skillet.
4. Heat skillet over low-medium heat.
5. When hot, pour egg mixture in skillet. Let cook for a few seconds.
6. While there is fluid eggs, stir eggs in skillet and scrape eggs off bottom and sides of pan.
7. Remove pan from heat when eggs are set to desired consistency.
8. Plate.
9. Add salt to season to taste.

User-Input
* Amount of eggs (default: 3)
* Final-result consistency?
* Amount of salt (levels?)

Objects:
1. Egg
    * Need fresh egg(s). Default is 1, but ore or less can be added.
2. Butter
    * Slice of butter?
4. Salt
5. Nonstick Skillet
6. Whisk
7. Rubber Spatula
8. Bowl
9. Plate
10. Stove
    * Heat control: low-medium-high

Functions:
* Egg
    - crackEggs
    - beatEggs
    - isCracked() --> True: eggshell removed. False: whole egg
    - isUniform() --> True: eggs beaten to uniform consistency. False: eggs yolks still separated.
    - isScrambled() --> True: eggs are cooked and ready to be eaten. False: eggs are not cooked (runny or fluid)
* Butter
    - isMelted() --> True: butter is melted. False: butter is not melted.