Cole McElmurray-EMA6938 Final Project<br>
Date: 7/22/26<br>
AI Disclaimer: I used Google Gemini to help with debugging code and finding commands/modules needed for each task.<br>
Every instance of its use is noted in the markdown code.  All ideas and logic are entirely my own.<br>
Topic/Question: Can a random-forest ML model accurately predict the magnetic moments of transition metal halides and what chemical properties affect it the most from a dataset of 816 materials pulled from Materials Project?<br>

Data set used: Pull from Materials Project Materials Explorer<br>
(https://next-gen.materialsproject.org/materials).<br>
The data is pulled in Notebook 01.  No manual intervention by the user is needed.<br>

Setup:<br>
All needed files are copied from EMA6938 environment.<br>

In Anaconda prompt:<br>
conda activate matds<br>
conda env create<br>
Create .env file: In either JupyterLab sidebar or your own stored directory, create a file named .env.  The text of this file should include only MP_API_KEY='key'.  Copy and paste your own Materials Project API key in place of 'key'.<br>
Run NOTEBOOKS: 01 -> 02 -> 03 -> 04.  Any other order will not work.<br>
When running a new notebook: Select the kernel from the previous notebook before running or you will get "variable name is not defined" errors.<br>

Interesting Results:<br>

The results of my Random Forest model WITHOUT GroupKFold (by transition metal):<br>
MAE:  0.083 µB/atom<br>
RMSE: 0.170 µB/atom<br>
R²:   0.835<br>
R² (GroupKFold): 0.385<br> (EXTREME DROP)

