# Anti Recoil Helper Package :

## AntiRecoil.py :

Features : Recoil Control, DataLogger, Supports a number of different guns.

### Recoil Control : 

The current Recoil-Control uses 'pynput' library for mouse movements, which might not work in multiplayer-online-games, modify your code with respective to interception driver as in **'d3adsh0t.py'** using the interception wrapper, most of the infrastructure of the code will be the same for mouse movements only the location would be different and you might have to loop it in the values in dictionary of 'current gun'.

The DataLogger helps one to log the position of bullet, switch off AntiRecoil and switch on the DataLogger and shoot on a wall/screen, and press on the 'animation of pierced bulltes' in succession, your first bullet is automatically logged, you are requested to log from 2nd to 10th bullet by 'clicking on the animation of pierced bullet in game' you can only record the coor of first 10 bullets at a time. You can do this a number of time's to have your data, once you have enough data switch off the DataLogger by pressing the Toggle key and paste it on a txt file and save, Processing of this data is done in **VisualizeData.py** and relative movements is also obtained from there.

Once Processing is Done in **VisualizeData.py** and relative movements are obtained (w.r.t Bullet - Bullet), Modify the dictionary of the respective gun in regards to the returned value from **VisualizeData.py**, you could also add a small code to induce randomness in performing Anti-Recoil by allowing a offset(rather move within a random circle whoose radius = Variance in bullet - bullet data) to be more Human-Like.

F1 key is used as a Toggler for AntiRecoil (ON / OFF)

F2 - F6  keys are used to switch GUN's

F7 key is used as a Toggler for Data Logger

## VisualizeData.py

Features : Parses Data from .txt, ScatterPlot Of Relative-X-Variation and Relative-Y-Variation for each bullet 'for all data collected' with their means,
returns the **Mean Relative Movement for X and Y** for each bullet - bullet for reducing recoil.

This is just a helper function which helps you to understand the distribution of data with human-intuition, currently it only returns the Mean-Relative-Movement among your whole data for bullet to bullet.

![](/samples/Analysis.jpeg)


