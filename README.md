The Chester Core

- A Lisp (Racket) based brain for the `Chester` software .

# THE DESIGN 

- Follows `Language Oriented design`.
- Try to follow principles of `SICP` textbook.
- Follow modern `Racket` standards for developemnt.

## THE DSL 

The `DSL` will represent concepts of chess 

### DSL Premitive elements

1. `PICE` : Chess Objects
    * King
    * Queen
    * Rook
    * Bishop
    * Knight
    * Pawn

2. `BOARD` : Chess Domain
    * PICE movement
    * Rules
    * Events
    * State

### Means of Combination 

1. All promitive objects are type of `pice`
2. `pice` has `pice-location` on `board` 
2. `pice` can `pice-mode` on `board` , 
3. All `pice-location` determines the `board-state`
4. Change in `pice-location` for any `pice` cause `board-event`.
5. `board-rule`validates an `board-event`
6. Valid `board-event` cause change in `board-state`.
7. Invalid `board-event` can throw `error` or `warning`.
8. `board-event` can be composed to form complex `board-event`.

## ETC
Use proper commit messages with following format 
```md
[TYPE] <Changes>

Updated Files
<files-name> : <change>
<files-name> : <change>
<files-name> : <change>
```
TYPE Of commits :  REPO-CHANGE , DEVLOPEMNT, FIX, DOCS

- Use Racket test-framework for unit testing.
- Maintain proper folder structure