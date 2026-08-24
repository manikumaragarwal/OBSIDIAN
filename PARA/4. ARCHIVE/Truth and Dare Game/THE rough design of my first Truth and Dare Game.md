Tags: [[coding projects]]

- what the hell
  okay, let me first type out my idea... so that you can undestand my mindset better... again.. since I'm a begginer.. I might be completely off the rails.. but still.. I wanna start building it with bugs and errors.. I wanna learn.. not just deploy the game...

Okay, here's the design for the whole game... I don't want you to spoon feed me.. let me make mistakes.. just act like a teacher whos helping me grow and learn..

The game would be divided into 3 majour sectoins:

1.  1st section: this would appear as soon as you opens the game... this screen would ask for :
    a. Total number of players... if we say 3: 3 input boxed would appear asking like this -

    - player 1 name : \***\*\_\_\_\*\***
    - player 2 name : \***\*\_\_\_\*\***
    - player 3 name : \***\*\_\_\_\*\***

          these names would be stored in an array called playersName

      b. Select a range for random number (this would help us in guessing the number between a range

    after this We press the GAME START button.

2.  2nd section : this is the number guessing screen.. this is the actuall game.. whcih appears after we press GAME start..  
    here, you have a loop.. {

    ROUND-1 :

    take input from `each players... then store all answers in an array called : answerArrays.. now we'll somehow(i don't know now), substract each guess from the randomNumber... and those substractions would be then stored in another Array called distanceFromRandomNumber ... here... we'll somehow we'll arrange the numbers inside this array in Increasing order.. .(lowest difference -> winner) highest difference -> loser) we'll now take the indexes of this array(in the increasing order of difference).. and.. then we'll compare these index with the playersName arrays.. (since the index should be same for both.. if '2' index here comes first.. means... the third player is the winner...)

    now we answer the players in winner -> loser fashion... the looser have to click on the pick dare button.. which would give it a random dare out of the 2 dares we had entered ourselves.}

    after the player press the dare completed button.. the ROUND-2 of the game would start..

    now that i've given you how I am trying to build this... I want your help in helping me chooes all the tools that i'd need.. like all the concepts that are used in this design.. and list them out.. i'll try to build it myself using those tools.. or i'd learn those tools/concepts and then build...

    c. Select Total rounds.. (if the players select 2 rounds). .then 2 input boxes will appear in which you have to fill the dares... now the whole game would run 2 loops..

    also find any design flaws in this (for a begginer.. I know if you compare to a high level game may flaws might arise.. but htink as a begginer)

Okay, for First Let me tell you the whole idea about the game.
It's a simple javascript game/website which let's the user enjoy truth & dare a bit more randomly.. The usual way of playing truth and dare is old..... everyone must have to take turns.. and do whatever is asked of them.. But I have a different idea.. what if it was random.. it's going to be a lot more fun then.

here's My Idea...

# PART-1

- Ask total Number of players: (let : 4)
- this will generate 4 Input boxes... asking each player's name..
- Ask players to select a range... (this will come handy later)
- Ask Players Total number of rounds they're going to play.
- Ask players to add truths or dares beforehand. this will be used later.

# PART-2

- a new page will open after the player have filled all the information in the part-1.
- This is where the Game UI Loads...

- first let me tell the general idea about what's happening here..
  - player's get to select a range... computer generates an random number between that range. each player will have their change to guess a number... which is between the selected range.. the closest amount the 4 player wins the round. and the farthest away losses the round..

# PART-3

- now the looser have to select a dare or truth... these truth or dare would be randomly given to the player.. based onthe list everyone made together (part-1)
- the player performs the truth or dare... then the next round(the whole part-2) begins.. (the number of rounds was already decided).

=======================================================================
