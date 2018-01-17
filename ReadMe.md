This is a repository with single-page interactive web applications (JS + HTML DOM). The can be considered as exercises with user interactivity. Below this full description of each file is provided.

1) rose-riddle.html
Description:
There ia a riddle. You have to form a buquet with three kinds of roses and you have particular amount of money. There is a questions: how many roses of each color with fixed price will you use?
Interactivity description:
This application interacts with user via seve popup windows (made by prompt() )). These windose set flower colors (ie. red, yellow, etc.) and their prices (integer or float, but always positive; zero value is incorrect). The last popup window sets total amount of money (integer or float, but positive too).
The result is three paragraphs with full description of future buquet, where flower colors are in previoiusly setted values. If it is impossible to form the buquet, application will give «No matches».
The new game can be launched via page refreshing.
Solution
- We have to find all the combinations of buquets out. But there will be possible solutions with some zeros in them. 
- After cutting out combinations with zeros there might be few correct variants. We have to choose only one solution in which all the amounts of flowers are about to similar. 
- The variant with the most similar amount of flowers is required.


2) numbers-riddle.html
Description:
There is a riddle. You have letters combination (AB — C = DE / F = GH * I). You have to transform the letters combination into numbers combination (from 0 to 9 without any repeat) in the way, which save all the equations. If there is no space between letters, the space will not be possible between numbers.
Solution:
- First of all we shall use the function, which transform two integers without space between them into single one.
- After that we start nine included cycles which enumerate the integer. The condition to skip the value in cycle is the one, when two values are matched. By the way, another one is when (AB — C) is less than 0 (in the cycle No.2), one more condition to skip is when combination (DE / F) is float (this one is executed  via comparsion result and floor result of dividing in the cycle No.5), the last one is when the result of combination (GH * I) is more than 99 (cycle No.8).
- Cycle No.8 also compares two equations pairs. If all the condition are matched, the result will write.
Interactivity description:
-This application does not presume any interactivity, but you may skip the results with zeros in their beginning via replacing one commenter row of code into another one (or commenting one row and decommenting another one).

3) square-riddle.html
Description:
You have to pave the way from "In" to "Out" in that way, when the sum of all the selected cells equals 100. You may point the next cells only from the right or from the bottom of previous one.
The last step is on the «Out» cell.
Each playground generates automatically after webpage refreshing (or loading).
Solution:
There is no automatical solution of this riddle.
Interactivity description:
- When you load this app for the first time, you will see the rules of the game descripted before) with the button «Understand».
- After pushing the «Understand» button you will be forvarded to playground.
- You mau use cursor or keyboard or both of them alternatively (right arrow or down arrow) to mark the cells and make the steps.
- The last step in the attempt is the one on the «Out» cell.
- Afthe the last step in the attempt application will check the result. If it equals 100, you will be geeted with popup window with lettering «Congrats! You've won.» After pressing «OK» webpage will be refreshed and new game will start.
- Otherwise you will see «Almost! Try again.» After confirming you will see two buttons «Try Again» and «New Map». Pushing «Try Again» means playing the same map from the beginning. Pushing «New Map» - map will be generated from the very beginning.
- Focused buttons make you navigation through the app easier.

4) symbols-riddle.html
Description:
You have to set all the comands (math actions fulfilled by options in a list) to match the equation. Only one match of the comands is posiible. Your answer might be checked after button «=» pushing.
Each equation generates automatically after webpage refreshing (or loading).
Solution:
- Default playground is made as a table with one row with invisible borders, where each odd cell is filled by some dummy value and each even cell - by select list with commands.
- An executed script generates playground via replacing dummy values by some random values (from the least to the largest value one by one in random  order) and writing invisible paragraph on th webpage with the same integers (it might look like «3 ? 1 ? 6 ? 4 ? 2 ? 5 = 2»).
- After generating playground all the values will be recorded into special variable and after that these values will be proceeded.
- Using five included cycles all the comands will be enumerated one by one and resulted expression will be executed and compared with the last integer in the paragraph. If there will be only on match of the command, this expression will be written. All the results might be shown after button «Show Answer(s)» pushing.
Interactivity description:
- You have to set each comand by select options.
- If one or more comands is not setted up, after button «=» pushing you will see popup window with message «Set all the comands.». After confirmation you may resume your game.
- If there is a match of the comands, the matched value will be disabled.
- If there is more than one comands match, after button «=» pushing you will see popup window with message «Only one comands match is possible. Try again.» After confirmation your progress will be reset, but the task will stay the same.
- If you set all the comands up and want to see if your answer is correct, you have to push the «=» button.
- If your answer was correct, you would see popup window with message «Congrats! You've won!». After confirmation the webpage would be refreshed and the game would start from the very beeginning.
- If your answer wasn't correct, you'd see popup window with message «Almost! [your_answer = your_result] Try the new task?». If you accept the confirmation, webpage will be refreshed and the game will start from the very beeginning. If you decline the confirmation, your progress will be reset, and you will start this task from the beginning.

