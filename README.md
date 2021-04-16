# Windows Env
developer setting apply (excluding RD)
install vs code, notepad++,Windows terminal

Install FiraCode Nerd Font  
(https://www.nerdfonts.com/)  
https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/FiraCode.zip
unzip and double click  
`Fira Code Regular Nerd Font Complete Mono Windows Compatible.otf`
click Install  
To setup in vscode with litagtaions:   
https://tahoeninjas.blog/2019/03/16/setting-fira-code-as-your-default-visual-studio-code-font/   
(menu->preferences->settings)
choose font and add 'FiraCode NF' (including quotes) to the front of the font family  
`'FiraCode NF', Consolas, 'Courier New', monospace`  
Just above is a section called Font Ligatures.  
click on edit in settings.json and replace null with true. should look like this:  
```
{
    "editor.fontFamily": "'FiraCode NF', Consolas, 'Courier New', monospace",
    "editor.fontLigatures": true
}
```


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
Add the conda-forge channel  
`conda config --add channels conda-forge`  
set the channel priority to strict  
`conda config --set channel_priority strict`   
create env  
`conda create -n test python=3.9`  
Powershell you may need to initialise conda first  
`conda init powershell`  
`conda activate test`  
to remove an env  
`conda env remove -n test`  

## libs to install
jupyterlab 3 use the conda-forge channel
`conda install -c conda-forge jupyterlab`
need to install nodejs for jupyter extensions (easy to do with conda)  
`conda install nodejs`  

pandas  
openpyxl  
matplotlib  
scipy  
scikit-learn    
nbdev  
`conda install -c fastai nbdev`

## Jupyterlab
install debugger requires diff kernel
`conda create -n name jupyterlab=3 xeus-python`  
jupytext
`conda install jupytext`
going to play with this and try and make it part of my workflow

for go-to-def functionality  
`jupyter labextension install @krassowski/jupyterlab_go_to_definition`  



sql  
`%load_ext sql`  
%sql mssql+pyodbc://

to get the the qgrid extension working in Jupyter lab see:
github.com/quantopian/qgrid/issues/350

installed the 

### links
http://hanselman.com/tools  
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

## Powershell setup (assuming windows terminal)
programming tags(python) won't show up untill there is a py venv or file setup in theat dir  
powerlines setup 
https://docs.microsoft.com/en-us/windows/terminal/tutorials/powerline-setup  
oh my posh  
https://ohmyposh.dev/docs/  
`Install-Module posh-git -Scope CurrentUser`  
`Install-Module oh-my-posh -Scope CurrentUser -AllowPrerelease`  
probaly get an error like 
Install-Module : A parameter cannot be found that matches parameter name 'AllowPrerelease  
if so open up powershell in admin (right mouse click start)  
`Install-Module -Name PowerShellGet -Repository PSGallery -Force`  
 In new non admin powershell  
 `Import-Module PowerShellGet`  
 then try again  
 to see Posh themes as they'd look in the directory you're currently in  
 `Get-PoshThemes`  
 open settings in Windows Terminal(ctrl+,)  
 add following line to the powershell config entry  
 `"fontFace": "FiraCode NF",`  
 Edit $PROFILE in vs code  
 `code $PROFILE`  
 and add the following line  
 `Set-PoshPrompt -Theme agnoster`  
 reset powershell  
 . $profile  
 and then reload as you customise 
 `Set-PoshPrompt -Theme .mytheme.omp.json`  

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

### General nbdev notes
make sure to uncomment the appropriate commented out sections.  
I forgot to uncomment the description and when I tried to run nbdev_build_lib, it errored out. 

'# default_exp core' in the first line of the notebook is where you set the name of the module that will be exported to a pythom module.  


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

 import xml.dom.minidom
