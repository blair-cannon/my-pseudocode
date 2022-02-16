# Robot building a snowman

## ABOUT:
-A snowman is three balls of snow stacked horizontally, starting large at the bottom and smallest at the top.
-Decorated to mimic a person, all decorations are placed on one side of snowman to be seen from a front view. 
-Snow can be packed together with pressure and moisture. 
-Each section starts as a snowball.
-A snowman needs a flat surface to be built on to not fall.
-Snow can melt.
-Some snow is not optimal for building a snowman.

 ## INIT: Create my variables for the program 
1. Snow: 
    * The material used to make snowman
    * Clumps together with other snow when rolled along the ground in a ball
    *PROPERTIES:*
    -snowAmount
    -snowDensity
2. Sticks
    * Used as arms
    * Punctures middle section of snowman without breaking it
    * Angles upward coming out of each side on snowman
    * Does not go all the way through section
    *PROPERTIES:*
    -stickLength
    -stickLocation
    -stickPunctureDistance
3. Scarf
    * Long, flat piece of material
    * Wraps around mid-section of the top and middle sections
    * Can break off top section if looped too tight
    *PROPERTIES:*
    -scarfLength
    -scarfLocation
4. Carrot
    * Used as a nose
    * Needs to enter top section of snowman without breaking it
    * Punctures flat into the center of the top section, parallel with the ground
    *PROPERTIES:*
    -carrotLocation
    -carrotLength
    -carrotPunctureDistance
5. Buttons
    * Used as eyes
    * Is laid on front side of top section and pushed in to stick, does not puncture
    * Above the carrot in a straight line with a 3 inch gap
    *PROPERTIES:*
    -buttonLocationX
    -buttonLocationY
6. Pebbles
    * Used for the smile
    * Laid in the shape of one parenthesis, with the two higher ends facing 
    * Is laid on front side of top section and pushed in to stick, does not puncture
    *PROPERTIES:*
    -smileLocation
    -shirtButtonLocations
7. Hat
    * Material with a flat brim and a covering for the head 
    * Lays on the very top of the snowman, right on top of the top section
    *PROPERTIES:*
    -hatLocation
8. Outside 
    *PROPERTIES:*
    -temperature
    -ground

## Functionality: 

**PREPARATION STAGE:**

    FUNCTION checkTemperature:
        * IF temperature > 32 degrees Fahrenheit
                THEN
                    Say "It is too warm to build a snowman."
                        END
        
    FUNCTION checkSnow:
        a. IF snowAmount <= 4 inches
                THEN
                    Say "The amount of snow is not enough to build a snowman."
                        END
        b. IF snowDensity != heavy (stays together when pressed)
                THEN
                    Say "The snow's density is too powdery to build the snowman."
                        END 

    FUNCTION gatherMaterials: 
        * full sized carrot (1)
        * buttons (2)
        * pebbles (10)
        * sticks (2)
        * scarf (1)
        * hat (1)

    FUNCTION pickSpot:
        * IF ground != flat
            THEN pickSpot(new)

**BUILDING STAGE:**

    FUNCTION formSection(section, size):
        a. Pack snow into a ball.
        b. Place snowball on ground and roll snowball in snow.
                * IF snowball starts to look cylindrical
                    THEN
                        rotate snowball every 5 rolls to distribute snow evenly
        c. Pat snowball every 3 rolls to pack in the newly added snow.
        d. Stop rolling when section reaches specified size (in feet).
        e. Rub over any lumps until curvage is smooth.
    
    FUNCTION levelTop:    
        * Gently flatten the top side of section by rubbing over the snow to shave off a level surface for the next ball.
       
    FUNCTION stack(smaller section, larger section): 
        * Place smaller section in the center of the larger section.
    
    FUCTION glueSections:
        * Pack snow from ground in between the two sections for a unified look and for stability.

**DECORATION STAGE**

    FUNCTION placeCarrot:
        a. let carrotLocation = center of top section, parallel to ground
        b. Puncture top section of snowman at carrotLocation with flat end of carrot, pointy side sticking out
        c. let carrotPunctureDistance = 1 / 3 carrotLength

    FUNCTION placeButton
        a. let buttonLocationY = 1 inch above carrotLocation 
        b. let buttonLocationX = 1 inch from carrotLocation (left or right) 
        c. Press and twist button into spot until it is glued

    FUNCTION placeSmile
        a. let smileLocation = 1 inch below carrotLocation
        b. Draw parenthesis shape with pebbles, with the highest end points pointing up
        c. Press and twist pebbles into spot until glued
    
    FUNCTION placeHat
        a. let hatLocation = top of snowman
        b. Raise hat higher than snowman and place it down on the top of top section
        c. Hollowed covering for head contains top of snowman

    FUNCTION placeScarf
        a. let scarfLocation = in between top and middle sections
        b. Place 1 / 2 scarfLength on either side of snowman 

    FUNCTION placeShirtButtons
        a. let shirtButtonLocations = along a vertical line at the center mark of the middle section (6 inches from either side)
        b. Press and twist pebbles into spot until they are glued
        c. let shirtButtonLocations == same side of snowman as carrotLocation

    FUNCTION placeStick
        a. IF stickLength > 1 ft
            THEN
                break off excess stickLength
        b. let stickLocation = 6 in from center point of middle section
        c. Puncture middle section of snowman with stick at stickLocation, angling stick upwards
        d. let stickPunctureDistance = 1 / 4 stickLength 

**EXTRA**

    FUNCTION fixCrack
        * Mend a crack by rubbing on more snow and applying pressure

## START: Start the program

     checkTemperature
     checkSnow
     gatherMaterials
     pickSpot

     formSection(bottom, 2)
     levelTop(bottom)
     formSection(middle, 1)
     stack(middle, bottom)
     glueSections(middle,  bottom)
     levelTop(middle)
     formSection(top, 0.5)
     stack(top, middle)
     glueSections(top, middle)

     placeCarrot
     placeButton(left)
     placeButton(right)
     placeSmile(7)
     placeHat
     placeScarf
     placeShirtButtons(3)
     placeStick(left)
     placeStick(right)

## END: End the program
