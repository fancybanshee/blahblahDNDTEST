I plan on making these optional and defaulted to 'off' will enable with a check box maybe? I haven't looked into this much

    Removed the extra " on line 9539
    added 2 attributes, line 3194 "hiddenlightloadmax" "hiddenheavyloadmin"
    added hidden attributes "encumbrmaxdexhidden" "encumbracphidden" "encumbrspeedhidden" "encumbrrunhidden" to do less sheet worker math and store values that will be checked later
    (I changed "encumbrload" to its actual in game multiplier (Light: 1, Medium: 0.667, Heavy: 0.67) it makes the math a lot easier to do
    *I can make this update to another value if this might break macros
    Removed all references of the older values, (only "encumbrmaxdex" "encumbracp" "encumbrspeed30" the 2nd "encumbrspeed30" "encumbrspeed20" "encumbrrun" use this value in any way)
    changed one "encumbrspeed30" to "encumbrspeed" this attribute will check the "acitemspeed" attribute and correctly display
    *I would like this to check players speed from "speed" and use a dropdown for armor type if possible
    added stat "acitemrun" so players may put in there armor run multiplier and will update in the encumbrance section

The jist is that I made hidden values for 'acitemX' and hidden values for base encumbrance penalties and check which is worse for the player, following the rules found on the SRD. uses if statement to check "totalcarriedweight" and set "encumbrload" to the correct value.

If you this interests you I can fully flesh it out for the current sheet, this does include adding all weapon and armor weights (using ammunition as an amount value) player speed will be taken into account using a dropdown for armor type (light, medium, heavy) and setting "acitemspeed" and "acitemrun" based on the armor type multiplier ((Light: 1, Medium: 0.667, Heavy: 0.67) then rounding to the nearest 5, which follows the speed chart found at the bottom of this page.

my sheet uses a piecemeal armor rule from dnd 2e so to make it easier to read and more relevant I have added a slice that only compares armor and shield stats and comparing them to encumbrance penalties then setting the dropdown "encumbrload" based on "totalweightcarried" I made this pretty quickly but I hope it gets the point across.
