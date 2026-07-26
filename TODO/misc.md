# Errors
400 Bad Request
404 Not Found
406 Not Acceptable
415 Unsupported Media Types
500 Internal Server Error
501 Not Implemented

# General API notes

if the verbose=true header is used, IDs will be pulled and full items will be included in the response 

## Updating objects

Arrays:
- if "++" is first item, add other items to array
- if "--" is first item, remove other items from array

Objectes:
- if set item to `null`, remove item

# Cards

face 0 is generally back/blank side, face 1 is generally front/main side, face 2 is generally flip side

# Card Holders

## Decks
- Define max cards
- Cards in order
- Orientation attribute
- Visual attribute (owner/all/none)
- orientation/face ignored per card

## Hands
Like Decks BUT
- orientation/face determined by card
- always assigned to player?

## Spaces
Like Decks BUT
- orientation/face determined by card
- allows dice, counters 
