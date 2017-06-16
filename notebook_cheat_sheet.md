# Jupyter/IPython Notebook Cheat Sheet

-   `h`: help

Run cell:

-   `Shift-Enter`: execute the current cell and go to the next cell

-   From the menu, "Cell | Run All": run the entire notebook from top to bottom

Cut, copy, paste:

-   `x`: cut the current cell
-   `c`: copy the current cell
-   `v`: paste below the current cell
-   `z`: undo cell deletion

Merge and split:

-   From the menu, "Edit | Merge Cell Above": merge current cell with the cell above
-   From the menu, "Edit | Split Cell": split the current cell at the cursor into two cells

Insert cell:
-   `a`: insert empty cell above
-   `b`: insert empty cell below

Convert cell format:

-   `m`: convert the current cell to a markdown (i.e. text) cell
-   `y`: convert the current cell to a code (i.e. Python) cell

To convert `ipynb` file to another format. At the Terminal prompt:

    jupyter nbconvert --to html mynotebook.ipynb

To download individual figures from a notebook: This can be done programatically, but I would simply right-click on the figure and select "Download as...".
