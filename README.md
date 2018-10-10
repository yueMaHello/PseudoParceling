# PseudoParceling
The purpose of 'pseudo parceling' is to split an irregular large parcel into several small ones with equal size. 
Since there is no built-in function of Postgres, I created this script to solve this problem.

### How to use it:
You need to change some code to connect to your own Postgres database.
You may want to use QGIS to connect to Postgres database so that you can see the effect.

### How the algorithm works:
I didn't find a simple algorithm to do it. I just created my own algorithm based on my math skill. 
The big parcel will be divided vertically then adjust the splitted line to make sure the area is correct.
Then horizontally cut this new parcel into x-pieces. Also, the horizontal line is adjusted little by little to meet the area requirement.



