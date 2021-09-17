Pseudocoding a Scrambled Egg

PLAIN TEXT STEPS:
Ingredients:
- Egg
- Milk (optional; 1 tbsp per egg)
- Water (optional; 1 tbsp per egg)
- Butter
- Salt
- Pepper

Equipment:
- Nonstick skillet
- Whisk
- Rubber Spatula
- Medium Bowl
- Plate

Steps:
1. Crack egg into bowl.
2. Beat with whisk until uniform.
3. Add milk/water
4. Stir until uniform.
3. Place butter on nonsticket skillet.
4. Heat skillet over low-medium heat.
5. When hot (butter is melted), pour egg mixture in skillet. Let cook for a few seconds.
6. While there is runny eggs, stir/fold eggs in skillet and scrape eggs off bottom and sides of pan.
7. Remove pan from heat when eggs are cooked.
8. Tansfer eggs to plate.
9. Add salt/pepper to season to taste.

PSEUDOCODE:
OBJECTIVE:
* Provide consumer with scrambled eggs based on desired number of eggs, consistency, and taste.

OBJECTS:
* Consumer
    - numberOfEggs (positive integer)
    - consistency (string=plain/creamy/fluffy)
    - taste (string=plain/salty/peppery/both)
* Egg
    - isCracked (boolean; default: false)
* Milk
    - volume (positive integer)
* Water
    - volume (positive integer)
* Mixture
    - ingredients (array)
    - isUniform (boolean; default: false)
    - isCooked (boolean; default: false)
    - isSalted (boolean; default: false)
    - isPeppered (boolean; default: false)
* Skillet
    - isButtered (boolean; default: false)
    - isMelted (boolean; defauly: false)
    - isHot (boolean; default: false)
* Stove
    - isOn (boolean; default: false)
* ScrambledEggs


FUNCTIONS:
* Consumer (3 values)
    - desiredEggs(int) - sets numberOfEggs to int
    - desiredConsistency(str) - sets consistency to str
    - desiredTaste(str) - sets taste to str
* Egg 
    - crackEgg() - set isCracked to true
* Milk/Water
    - setVolume() - set volume based on numberOfEggs
* Mixture
    - addEgg() - add Egg object to ingredients array
    - addMilk() - add Milk object to ingredients array
    - addWater() - add Water object to ingredients array
    - stirMixture() - set isUniform to true
* Skillet
    - addButter() - set isButtered to true
    - meltButter() - set isMelted to true
    - cookMixture() - set isCooked to true
* Stove
    - powerOn() - set isOn to true
    - placeSkillet() - set isHot to true
* Plate(Mixture)


SCENARIO:
Consumer wants 3 eggs scrambled with creamy consitency and salty taste.

<code>
START

INIT()
    CREATE Consumer
    CREATE Mixture
    CREATE Skillet
    CREATE Butter
    CREATE Stove

Consumer.desiredEggs(3)
Consumer.desiredConsistency("creamy")
Consumer.desiredTaste("salty")

IF numberOfEggs > 0 THEN

    powerOn()

    FOR x in numberOfEggs
        CREATE Egg
        crackEgg
        addEgg
    ENDFOR

    IF consistency == "creamy" THEN
        CREATE Milk
        setVolume(numberOfEggs)
        addMilk()
    ELSE IF consietency == "fluffy" THEN
        CREATE Water
        setVolume(numberOfEggs)
        addWater()
    ENDIF

    stirMixture()
    placeSkillet()
    addButter()

    IF isOn THEN
        meltButter()
    ENDIF

    IF isMelted AND isUniform THEN
        cookMixture()
    ENDIF

    CASE taste is
        salty: isSalted == true
        peppery: isPeppered == true
        both: isSalted == true
              isPeppered == true
    ENDCASE

ENDIF

Plate(Mixture)
    IF isCooked THEN
        CREATE ScrambledEggs
    ENDIF

END
</code>