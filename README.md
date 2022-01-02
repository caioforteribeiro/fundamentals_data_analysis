![data analysis image](https://learn.g2.com/hubfs/Imported%20sitepage%20images/1ZB5giUShe0gw9a6L69qAgsd7wKTQ60ZRoJC5Xq3BIXS517sL6i6mnkAN9khqnaIGzE6FASAusRr7w=w1439-h786.png)
# Fundamentals of Data Analysis
## Final project - Winter 2021-2022

**Author:** Caio Forte Ribeiro
<br><br>

***
## About this repository

This repository contains all files required as part of the assessment for the module *Fundamentals of Data Analysis* at GMIT (Winter 2021-22). All code was written in Python ([v. 3.8.8](https://www.python.org/downloads/release/python-388/), realeased on Feb 19, 2021).

Here you will find the following files:
* `cao.ipynb`, a Jupyter notebook with a comparison of CAO points for 2019 to 2021.
* `pyplot.ipynb`, a Jupyter notebook with an explanation of the `matplotlib.pyplot` package and examples of 3 plots using it.
* `requirements.txt`, containing all modules required to run the notebooks.
* a `data` folder with all input and output datasets for the CAO notebook.

<br>

***
## Task
Create a repository containing 2 Jupyter notebooks:
1. [`cao.ipynb`](https://github.com/caioforteribeiro/fundamentals_data_analysis/blob/main/cao.ipynb), with a clear and concise overview of how to load CAO points information from the CAO website into a `pandas` data frame, a comparison of CAO points for 2019, 2020, and 2021, as well as relevant and appropriate plots.
2. [`pyplot.ipynb`](https://github.com/caioforteribeiro/fundamentals_data_analysis/blob/main/pyplot.ipynb), with a clear and concise overview of the `matplotlib.pyplot` Python package,and an in-depth explanation of 3 interesting plots from the package.

The repository should also contain all relevant data and a [`requirements.txt`](https://github.com/caioforteribeiro/fundamentals_data_analysis/blob/main/requirements.txt) file to enable someone to run the notebooks with minimal configuration.

<br>

***
## An overview of the notebooks
### CAO notebook
This notebook starts by pulling the data for each year from the [CAO website](https://www.cao.ie/), which comes in different formats (`.xlsx` for 2021 and 2020, `.pdf` for 2019) and saving a time-stamped local copy of the original data, before loading them into a `pandas` dataframe using `pd.read_excel()` for 2021 and 2020 and `camelot` for 2019. Each dataframe is then cleaned-up (keeping only L8 courses, removing string characters from columns with points, and keeping track of which courses had additional entry requirements) and saved as a `csv` file into the [data folder](https://github.com/caioforteribeiro/fundamentals_data_analysis/tree/main/data).

With all clean dataframes ready, we join them into a consolidated dataframe `allcourses` to perform our comparative analysis (higher entry scores, higher Mid scores, entry scores above 600 per year) and plottings.

### Pyplot notebook
This notebook starts by describing what is the `matplotlib.pyplot` package and what it is used for. It then runs through some basic plots and some of the basic `pyplot` functions before presenting 3 examples of plots done with the package:
1. **Scatterplots:** We used the data from the [Iris dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data) to plot a series of scatterplots of Iris petal and sepal sizes. Here, we also explored the `fig,ax=subplots()` method for plotting.
2. **Pie charts:** A pie chart of the time spent on each activity of a project, using `plt.pie()` and `autopct` to display percentages.
3. **Boxplots:** Again, using data from the [Iris dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data) to plot:
   * Petal and sepal sizes irrespective of the species.
   * Petal and sepal sizes according for each species.


###


<br>

***
## Requirements
**Quick note:** Before starting with specific requirements, if you're on Windows we recommend that you install a third-party console emulator, such as [Cmder](https://cmder.net/). Use the command line interface if on Linux or a Mac.

To run the Jupyter notebook, you will first need to:
1. Have Python installed in your machine. You can download the latest version [here](https://www.python.org/downloads/).
2. Install Jupyter. This can be done with one of the following 2 methods:
   * Using `pip`: 
   ```
   pip install jupyterlab
   ```
   * Installing [Anaconda](https://docs.anaconda.com/anaconda/install/), which comes with Jupyter pre-installed.
3. Install [`Camelot`](https://camelot-py.readthedocs.io/en/master/user/install.html#install) to load CAO 2019 data from a PDF table into `pandas`. After installing the dependencies [Ghostscript](https://ghostscript.com/releases/gsdnld.html) and [ActiveTlc](https://www.activestate.com/products/tcl/#how-do-i-download-tcl-for-windows-linux-or-mac), type the following in your console:
   ```
   conda install -c conda-forge camelot-py
   ```


You can find specific requirements for running the code, such as additional modules to import, in the `requirements.txt` file in this repository.


<br>

***
## How to run the notebooks
1. Clone this repository into your local machine.
2. Open Cmdr (or the command line interface if using Linux or Mac).
3. In the terminal, type:
    ```
    jupyter lab
    ```
4. The Jupyter application should open in your browser. If it doesn't, click [here](https://jupyter-notebook.readthedocs.io/en/stable/troubleshooting.html) for troubleshooting.
5. Navigate through the folders and double-click the files `cao.ipynb` and (or) `pyplot.ipynb`.
6. In the **Run** tab from the top-left menu, click on **Run All Cells**.
7. If you have an issue while running the notebook, try restarting the Kernel:
   * In the **Run** tab from the top-left menu, click on **Restart Kernel and Run All Cells**.

You can also use these buttons for a static view of the notebooks in nbviewer:

* **CAO notebook**

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/caioforteribeiro/fundamentals_data_analysis/blob/main/cao.ipynb)

* **Pyplot notebook**

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/caioforteribeiro/fundamentals_data_analysis/blob/main/pyplot.ipynb)

<br>


***
## Credits
These notebooks heavily relied on the official documentation of all the packages used:

* [Matplotlib.pyplot](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.html)
* [NumPy](https://numpy.org/doc/stable/user/index.html#user)
* [Pandas](https://pandas.pydata.org/docs/user_guide/index.html#user-guide)
* [SciPy](https://docs.scipy.org/doc/scipy/tutorial/index.html)
* [Camelot](https://camelot-py.readthedocs.io/en/master/user/quickstart.html)

We also recommend the following sources:

* [Towards Data Science](https://towardsdatascience.com/)
* [Kaggle](https://www.kaggle.com/)
* [StackOverflow](https://stackoverflow.com/)


<br>

***
## Contact
Feel free to get in touch about this project by sending me an [email](mailto:G00398262@gmit.ie) with your suggestions. 

