## Prerequisites

- **IN-CORE account**
    A user must have an **IN-CORE** account. If you don't have an account, see IN-CORE [account](account) section.

- **Virtual environment**
    We recommend that users get familiar with Python virtual environment managers called Anaconda or Miniconda.

    * These are tools that help keep dependencies separate for different projects. If you decide, however, to use 
    a virtual environment or manager you must do it now, in this prerequisite step.

    * An environment managers are available by downloading OS specific installers. Note that Anaconda/Miniconda 
    distribution will include Python (Anaconda also includes a collection of over 1,500+ open source packages), so installing Python first isn't needed if you use Anaconda/Miniconda. With Anaconda you already have installed Jupyter notebook. The `conda` is the preferred interface for managing installations and virtual environments with the Anaconda/Miniconda Python distribution.

- `Python 3.5+` <https://www.python.org/>
    It is common to have more than one Python version installed on your computer. Make sure you are running 
    the correct, Anaconda version of Python (you can check by running `python --version`) 
    and/or `import sys;sys.executable` in Python console.

- `Jupyter notebook` <https://jupyter.org/>
    We recommend using Jupyter Notebook for running the **pyIncore** projects. It as an open-source application 
    that allows you to create projects (documents) that contain live Python code, visualizations and documentation. 
    Jupyter Notebook is already installed with Anaconda distribution; it has to be installed separately 
    in your virtual environment on Miniconda distribution.

In the next section we provide installation instructions for environment manager using [Miniconda](https://docs.conda.io/en/latest/miniconda.html). Similar instructions apply to full [Anaconda](https://docs.anaconda.com/anaconda/install/) manager. Python 3.x will be installed with both distributions. The following instructions were tested for Mac, Windows and Linux 64-bit OS (The 32-bit has not been tested yet).

### Windows 64-bit

1. Download the latest Miniconda3 installer for Windows from the [Miniconda](https://docs.conda.io/en/latest/miniconda.html) web page.

2. Run the installer setup locally (select the *Just Me* choice) to avoid the need for administrator privileges.

3. Leave the default folder path (`C:\Users\<user>\..\miniconda3`).

4. Do not add Anaconda to the PATH. Do, however, register Anaconda as the default Python environment.

5. Open up an Anaconda prompt from the Windows Start menu. The `base` environment is being activated and the prompt changes to: `(base) C:\Users\<user>`:

    ![Windows Menu.](images/win_prompt1.jpg)


6. Create the python environment (`pyincoreEnv` for example) and activate it (or stay in the `base`):
    ```
    conda create -n pyincoreEnv python=3
    conda activate pyincoreEnv
    ```

7. Add [conda-forge](https://conda-forge.org/) package repository to your environment:
    ```
        conda config --add channels conda-forge
    ```

8. Install Jupyter Notebook. Jupyter Notebook is already installed with Anaconda distribution; it has to be installed separately in your virtual environment on Miniconda:
    ```
        conda install jupyter
    ```

### Mac and Linux OS

1. Download the latest Miniconda3 installer from the [Miniconda](https://docs.conda.io/en/latest/miniconda.html) web page.

2. Run the installer setup locally (select the *Install for me only* on Mac/Linux) to avoid the need for administrator privileges.

3. Leave the default folder path (`/Users/<username>/miniconda3` or `/home/<username>/miniconda3`).

4. Do not add Anaconda to the PATH. Do, however, register Anaconda as the default Python environment.

5. Open up a Terminal. The `base` environment is being activated and the prompt changes to: `(base)/Users/<username>` or `(base)/home/<username>`:

6. Create the python environment (`pyincoreEnv` for example) and activate it (or stay in the `base`):
    ```
    conda create -n pyincoreEnv python=3
    conda activate pyincoreEnv
    ```

7. Add [conda-forge](https://conda-forge.org/) package repository to your environment:
    ```
        conda config --add channels conda-forge
      ```

8. Install Jupyter Notebook. Jupyter Notebook is already installed with Anaconda distribution; it has to be installed separately in your virtual environment on Miniconda:
    ```
        conda install jupyter
    ```
   
Mac OS specific notes: We use `matplotlib` library to create graphs. There is a Mac specific installation issue addressed at StackOverflow [link 1](https://stackoverflow.com/questions/4130355/python-matplotlib-framework-under-macosx) and [link 2](https://stackoverflow.com/questions/21784641/installation-issue-with-matplotlib-python). In a nutshell, insert line:
    ```
        backend : Agg
    ```
    
into `~/.matplotlib/matplotlibrc` file. You must create the file (`matplotlibrc`) if it does not exist.

