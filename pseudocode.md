START: Start the program: Building a snowman

INIT: Create my variables for the program <br>
Snow
Sticks
Scarf
Carrot
Buttons
Pebbles
Hat

    FUNCTION dressAppropriate:
        warm clothes
        gloves
        
    FUNCTION checkSnow
        a. IF snowAmount >= 4 inches, continue.
            ELSE snowAmount is not enough to build the snowman.
        b. IF snowDensity = heavy (stays together when pressed), conitnue.
            ELSE snowDensity is too powdery to build the snowman. 

    FUNCTION gatherMaterials: 
        full sized carrot (1)
        buttons (2)
        pebbles (10)
        sticks (2)
        scarf (1)
        hat (1)

    FUNCTION formSection:
        a. Pack snow into a snowball.
        b. Add snow to your hands until the snowball gets to heavy.
        c. Place snowball on ground and roll snowball in snow.
                *IF snowball starts to look cylindrical, rotate snowball every 5 rolls to distribute snow evenly.
        d. Pat snowball every 3 rolls to pack in the newly added snow.
        e. IF forming bottom section, stop rolling when snowball is 2 feet wide.
                ELSE IF forming middle section, stop rolling when snowball is 1 feet wide.
                        ELSE IF forming top section, stop rolling when snowball is 0.5 feet wide.
        f. Gently flatten the top side of bottom and middle sections as a surface for the next ball.
       
    FUNCTION stack(smaller section, larger section): 
        a. Place smaller section in the center of the larger section.
        b. Pack snow from ground in between the two sections for a unified look.

    FUNCTION decorate:
        a. Place a carrot in the middle of the top section with the pointy side pointing out as a nose.
        b. Place two buttons as eyes above the carrot spaced evenly on the right and left side of the top section.
        c. Place pebbles below the carrot in a row for the smile on the top section.
        d. Place a hat on the top on the top section.
        e. Place a scarf between the top section and the middle section.
        f. Place 3 pebbles in a vertical line on the middle section as shirt buttons.
        g. Place two sticks, one on each side of snowman, into the middle section as arms. 

1. dressAppropriate
2. checkSnow
3. gatherMaterials
4. formSection(bottom)
5. formSection(middle)
6. formSection(top)
7. stack(middle, bottom)
8. stack(top, middle)
9. decorate



END: End the program
