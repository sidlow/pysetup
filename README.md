# Windows Env
## Git
https://git-scm.com/download/win  
tortoise for git (use for visual aid)  
In the project folder  
`git init`  
 `git config --global user.name "Your Name"`  
 email as well?  
     
## Python/Pip
setting up virtual envs in python  
python -m venv webappenv  
python3 -m venv webap  
mkdir source  
mkdir source\labs  
cd source\labs  
python -m venv venv  
	This will create an virtual env just called 'venv'  
pip installl --upgrade pip  
python -m pip install --upgrade pip (this works for pip update in venv)  
commandline >> \venv\scripts\activate.bat  
PS >>  .\venv\Scripts\activate  

## Conda
Miniconda install  
create env  
`conda create -n test python=3.9`  
Powershell you may need to initialise conda first  
`conda init powershell`  
`conda activate test`  
to remove an env  
`conda env remove -n test`


### links
https://project-awesome.org/markusschanta/awesome-jupyter  
https://jupyterlab.readthedocs.io/en/stable/  
https://blog.jupyter.org/jupyterlab-3-0-is-out-4f58385e25bb  
https://python.plainenglish.io/what-the-newly-released-jupyterlab-3-has-to-offer-a9a144d93046  
https://towardsdatascience.com/a-quick-and-easy-guide-to-managing-conda-environments-87bfe7bab065 
https://towardsdatascience.com/creating-a-solid-data-science-development-environment-60df14ce3a34   
https://towardsdatascience.com/jupyter-is-now-a-full-fledged-ide-c99218d33095  
https://blog.jupyter.org/a-visual-debugger-for-jupyter-914e61716559  
https://tdhopper.com/blog/my-python-environment-workflow-with-conda  
https://towardsdatascience.com/the-point-of-no-return-using-nbdev-for-the-past-6-months-changed-the-way-i-code-in-jupyter-2c5b0e6d2c4a  
https://towardsdatascience.com/a-step-by-step-introduction-to-starting-nbdev-exploratory-programming-4a761ed1f796  
https://nbdev.fast.ai/tutorial.html  
https://pete88b.github.io/fastpages/nbdev/fastai/jupyter/2020/07/24/nbdev-deep-dive.htmlopnpyx  
https://medium.com/@saneshashank/nbdev-is-all-you-need-51d1b4be7e34  
https://tomassetti.me/working-with-excel-in-python/  

## libs to install
jupyterlab 3 use the conda-forge channel
`conda install -c conda-forge jupyterlab`
pandas  
openpyxl  
matplotlib  
scipy  
scikit-learn    
nbdev `conda install -c fastai nbdev`

## nbdev notes
conda install of nbdev didn't work for me.
### steps
#### Install git
#### Install miniconda
#### create repos directory
#### cd to repos
#### git init
#### create virtual env
#### activate the env
#### install jupyterlab
`conda install -c conda-forge jupyterlab`
#### install nbdev (used pip install as the conda install didn't seem to work)
`pip install nbdev`
#### create github repo for project from nbdev template (make sure name is same as project)
https://github.com/fastai/nbdev_template/generate
#### git clone in repos directory
`git clone https://github.com/[githubrepo]`
#### 
#### cd to the name of the project
#### run


## to look at
nbdev # extends dev emv in jupyterlabs (https://nbdev.fast.ai/tutorial.html)
viola #Voilà turns Jupyter notebooks into standalone web applications. (https://blog.jupyter.org/and-voil%C3%A0-f6a2c08a4a93)
xlwings # gives more manipulation options of excel via python see the python for excel Orielly book (including replacing vba with python for pro ed)
nb2xls or XlsxPandasFormatter # jupyter notebooks to excel spreadsheet
pytest
black on jupyter?
sqlalchemy - SQL 
beeware - UI - desktop
check out xeus-python https://github.com/jupyter-xeus/xeus-python (looks like it might be Conda specific)

for pandas:
pyjanitor - convenient dat celaning functions that can be chained

plotting graphing: check piviz ecosystem (conda focus)
matplotlib
seaborn
bokeh
![image](https://user-images.githubusercontent.com/8316686/111890700-2a785000-8a40-11eb-8c61-80fedd19b024.png)
This image is from Practical Data Analysis Using Jupyter Notebook(2020) Marc Wintjen, Andrew Vlahutin


ML:
scikit

 inport xml.dom.minidom
