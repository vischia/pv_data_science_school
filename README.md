# My Data Science School
## Exercises

All the material is licensed by the licenses specified in each file.
    
Instructor: Pietro Vischia (pietro.vischia@cern.ch)

This tutorial merges my material from several past tutorials of mine ([vischia:intensiveCourse_public](https://github.com/vischia/intensiveCourse_public), [vischia:data_science_school_igfae2024](https://github.com/vischia/data_science_school_igfae2024), [vischia:adfm_2024-2025](https://github.com/vischia/adfm_2024-2025), [vischia:lisbon-ml-school](https://github.com/vischia/lisbon-ml-school)), and builds on that additional exercises etc.
    
## Tutorial organization

Ideally you would be running the tutorial on your laptop, following the instructions and explanations given by me in the big screen in the room.
The alternative, suggested if you don't have too powerful of a laptop, is to run on Google Colab (see 2.3 below).
If, for any reason, you cannot run the tutorial, you are welcome to just watch the tutorial steps being executed in the big screen by me.

## How to run the tutorial on your local machine

#### 1. Check out the code
```
git clone git@github.com:vischia/pv_data_science_school.git
cd pv_data_science_school/
```
or
```
git clone https://github.com/vischia/pv_data_science_school.git
cd pv_data_science_school/
```

#### 2. Create a python environment and install requirements

If your laptop can run ML models without too much hassle and you have some (approximately 5 GB) free disk space, follow the instructions in `2.1` or `2.2`. Otherwise, I suggest running on Colab by following the instructions in `2.3`.
    
##### 2.1 Using conda

```
conda create --name pv_data_science_school python==3.10
conda activate pv_data_science_school
conda install --file requirements.txt -c conda-forge -c pytorch -c nvidia -c scikit-learn
pip install livelossplot
```

To deactivate the environment, you should run `conda deactivate` from the command prompt.

##### 2.2 Using virtualenv

```
virtualenv -p python3.10 pv_data_science_school
source pv_data_science_school/bin/activate
pip install -r requirements_venv.txt
```

A participant of a previous school (Geoffrey Mullier) reports that on MacOS 12.5 `virtualenv` doesn't work, and that in that case `python3.10 -m venv pv_data_science_school` works as intended.

To deactivate the environment, you should run `deactivate` from the command prompt.

##### 2.3 Using Google Colab (google account needed)

Go to [Google Colab](https://colab.research.google.com/), select `GitHub` as a source, and fill in the path to this repository (`https://github.com/vischia/pv_data_science_school`). Possibly Google will ask for access to your GitHub account, although installing from a public third party repository should not require that, in principle.

When the colab instance is active, open the jupyter notebook `train_hyp.ipynb` and run the cell labelled "*If you are using COLAB*"

Note that, to have persistency of the files and changes, and to be able to push back the repository, you should use the first cells in the notebooks to load your google drive account.

*While we can provide some limited help, it is expected that you set up your workflow in Colab independently.*


#### 3. Run the tutorial

For local environments, run

```
jupyter notebook
```

and open the various notebooks in the browser window that is opened.

From Colab, click on a notebook's name to open it.

If you prefer to run a regular python script, you can convert the notebook using the command:

```
jupyter nbconvert --to script lesson_1.ipynb
```

This will create a file `lesson_1.py` that you can pass as a command line argument to the python interpreter.
You may have to add a few `plt.show()` or `plt.savefig()` to the code here and there, to visualize/save outputs, though.


## Prerequisites

In order to minimize wifi usage at the workshop venue, please set up your environment and run the `prerequisites.ipynb` notebook in advance.
