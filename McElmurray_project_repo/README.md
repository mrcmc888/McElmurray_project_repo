####
----------------
Cole McElmurray-EMA6938 Final Project
Date: 7/22/26
AI Disclaimer: I used Google Gemini to help with debugging code and finding commands/modules needed for each task.
Every instance of its use is noted in the markdown code.  All ideas and logic are entirely my own.
Topic/Question: Can a random-forest ML model accurately predict the magnetic moments of transition metal halides when using a GroupKFold split by metal, and what chemical properties affect this magnetic moment the most?
----------------
Data set used: Pull from Materials Project Materials Explorer
(https://next-gen.materialsproject.org/materials)
----------------
Setup:
All needed files are copied from EMA6938 environment.
In Anaconda prompt:
conda activate matds
conda env create
Create .env file: Add MP_API_KEY='key'.
Run NOTEBOOKS: 01 -> 02 -> 03 -> 04.  Any other order will not work.
-----------------
Interesting Results:

The results of my Random Forest model WITHOUT GroupKFold (by transition metal):
MAE:  0.106 µB/atom
RMSE: 0.209 µB/atom
R²:   0.709

The results of my Random Forest model WITH GroupKFold (by transition metal):
Mean MAE:  0.182 ± 0.066 µB/atom
Mean RMSE: 0.265 ± 0.092 µB/atom
Mean R²:   0.409 ± 0.161
------------------