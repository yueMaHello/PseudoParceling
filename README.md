# Pseudo Parceling
The purpose of 'pseudo parceling' is to split an irregular large parcel into several small ones with equal size. 
Since there is no built-in function of Postgres, I created this script to solve this problem.

### How to use it:
You need to change some code to connect to your own Postgres database.
You may want to use QGIS to connect to Postgres database so that you can see the effect.

### How the algorithm works:
I didn't find a simple algorithm to do it. I just created my own algorithm based on my math skill. 
First, The big parcel will be divided vertically by a line. Then, adjust the vertical splitted line to make sure the area is correct.
After that we need to horizontally cut this new vertical parcel into x-pieces using several lines. Also, each horizontal line is adjusted little by little to meet the area requirement.
There is a for loop to start next vertically cutting process until it couldn't be cut any more. 



