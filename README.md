# -Battling-Knights-game

First, Make sure that you have Python 3.7 installed so that you can run this game. 

I created this game with 7 classes:

      *The `Knight` class to hold properties like ID, position, item equipped, base attack, etc.
      *A `Battle` class which deals with the life and death of knights.
      *A `Serialize` class to read and write to the FS.
      *The `Arena` class to store the positon of everything on the board and moving things around.
      *The `Item` class  to describe items on the board. - An `item` instance will always reference its position .
      *The `POS` class (used by Knight, Item and Arena) to determine their position. - A `pos` instance always knows whether it holds _items_ or a _knight_.
       *A `RunGame` class which brings everything together such as : 
                                                       1.Reading instructions
                                                       2. Setting initial knight positions and
                                                       3. Running the games

With `knight.pos` ; or `arena.board` ; you can determine the position of the knight.


# Knight class:
     
    ID: R
    BaseAttack: 1
    BaseDefence: 1
    pos: <Pos>
    equipped: <Item>
    

# Arena class:

**Methods**
    move_knight - allowed (N,S,E,W)
        move_empty_square - update position
        move_square_with_loot - equip item, according to (A,M,D,H) rule
        move_square_with_knight - attack
        move_square_with_water - drown, drop items

**Properties**

    board - 2 dimensional matrix
            each item is a POS element



## POS class:

    position: (0, 0)
    knight_ids: ()
    item_ids: ()

## Serialize class:

- Read instructions from from the `moves.txt` file
- Serialize to JSON format and write to FS.


## Battle class:

    Battle and kill knights.


## RunGame class:

    Run instructions and update Arena, Knights.


# Usage

If you want To run the app use:
                 python run.py
                 
 If you want To run the test use:

                 python test.py

Moves are read in from `moves.txt`.

you can see output from `state.json

