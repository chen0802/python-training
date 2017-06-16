# python-ayzenberg

Python training at Ayzenberg, January 2017.

This is a private Git repository. I kindly ask that you keep these materials within the company. Share with your coworkers but not publicly. Thanks!

## Goals

Educate Ayzenberg employees with varying programming backgrounds how to create reusable and scalable solutions for analytical reporting and visualization using Python, hopefully in a way that is useful and rewarding.

Potential benefits:

1.  Reduced cost, in both time and money.
2.  Faster turnaround and feedback loops.
3.  More accurate insights.

## Topics

In no particular order:

-   Python fundamentals
    -   [basic variables and types](variables.md)
    -   control flow: [Boolean logic](logic.md), [loops](loops.md)
    -   collections: [strings](strings.md), [lists, tuples](lists_tuples.md), [dictionaries](dictionaries.md)
    -   [functions](functions.md)
    -   [imports](import.md)
    -   [file input/output](file_io.md)
-   Pandas
    -   [basics, reading data](pandas_basics.ipynb)
    -   [analysis and visualization](pandas_analysis.ipynb)
    -   [merge and join datasets](pandas_join.ipynb)
-   Machine learning: classification, regression
    -   [scikit-learn](sklearn.ipynb)
-   Database interaction: psycopg2, AWS Redshift, PostgreSQL
-   Jupyter/IPython notebook
    -   [introduction](ipython.ipynb)
    -   [cheat sheet](notebook_cheat_sheet.md)
-   Programming workflow: Python scripts, IPython shell console, IPython notebook.
-   [Git version control](git.md)
-   [Basic Unix commands](unix.md)

Topics that are likely not covered:

-   Object-oriented programming; classes.

## Learning Philosophy

1.  Type it in; refrain from cut and paste. Great craftsmen master their tools. For programmers, our primary tool is the keyboard. Eventually, we reach a level of proficiency where it is okay to cut and paste code from elsewhere. But during the learning phase, typing matters.

    Once we become proficient with the keyboard, the code on the screen becomes an extension of our thoughts. We spend less time translating thoughts into code.

    In general, bias toward doing things the hard way, and you will find it accelerates absorption and improves reflexes, recall, and development speed.

2.  Write stuff down. Programming is filled with details, and a notepad helps capture those details. I humbly believe pen and paper is best for retention.

3.  Practice! Theory is not enough. Improve through repetition.

4.  Learn with others. It makes learning easier. Others have probably encountered that same problem you have now.

5.  Ask questions!

## What you can do before Saturday

Before Saturday, there are a few things that you can do to get the most out of the workshop:

1.  Please reply to steve@stevetjoa.com telling me a little bit about your role at Ayzenberg, e.g. daily tasks, current short- and long-term work-related goals, your computer programming experience if any, and how you envision this workshop might benefit or relate to your needs.
2.  Please create an account on [GitHub](https://github.com) if you don’t already have one. Once you do, email me your GitHub username. GitHub is a company/website/service which hosts source code, both open-source and private source code. Companies everywhere use GitHub as a place to organize and track changes to code.
3.  Install git. [Download here](https://git-scm.com/). Then open git to verify that it is installed properly.
    -   On Mac, at the Terminal, just type `git`.
    -   On Windows, open the application "Git Bash". Git Bash should be included in the download above.
4.  Install Python 2 and relevant libraries. Your system may already have Python 2.

    If you’re totally new, the simplest solution is to download and install [Anaconda for Python 2 (2.7)](https://www.continuum.io/downloads), not Python 3. If you can do the following without errors, then you’re set:

    1.  Run the IPython shell. 
        -   For Mac, at the Terminal: `ipython`. 
        -   For Windows, open the application "IPython".

        Type `exit` to exit.
    2.  In the IPython shell, run `import scipy, sklearn, pandas`. If that runs without error, congratulations.
    3.  Run the IPython/Jupyter notebook. 
        -   For Mac, at the Terminal: `jupyter notebook`.
        -   For Windows, open the application "Jupyter Notebook". Alternatively for Windows: open the application "Anaconda Prompt" and type in `jupyter notebook`.
        
        To close the IPython/Jupyter notebook,

        1.  Save the notebook. (Either use keyboard shortcut `s`, or "File | Save" in the menu.)
        2.  Close the window.
        3.  If you opened the notebook from a prompt/shell, from that shell, press `<Ctrl-C>` twice to return to the prompt.

5.  Install a code/text editor such as [Atom](https://atom.io/) or [Sublime Text](https://www.sublimetext.com/) if you don't have one already.

Immediately after installing, if something doesn’t work, try closing the terminal or restarting the OS. Sometimes that can reset the necessary configurations.

If you have any other questions, please feel free to let me know. Thanks, and I look forward to meeting you!

Steve Tjoa, steve@stevetjoa.com
