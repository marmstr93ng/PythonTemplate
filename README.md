# PythonTemplate
A template layout of a Python project

1. Create repository in github - No additional files
2. Navigate to desire local repository location
3. Run [git-python-env](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-python-env)

***OR***

1. Create repository in github - No additional files
2. Navigate to desire local repository location
3. ```git clone https://github.com/marmstr93ng/___.git``` - Refer to the url of the github repo
4. Download Python template files and place in the local repository location
5. Modify the Readme as appropriate
6. ```git add .``` - Adds all files
7. ```git commit -m "first commit"``` - Commit all added files
8. ```git push -u origin master``` - Push to the github repo
9. ```python -m venv venv``` - Setup Python Virtual Enviroment

NOTE:All git commands entered through git bash (Right click on Repo and click "Git Bash Here").

---

# INFO
## Virtual Enviroments (Venv)
Creates an isolated python enviroment, keeping project dependencies independent from each other

Pipenv has been depricated in all my projects and I have reverted back to Venv which is part of the standard library (I try and keep to the standard lib as much as possible). 

1. ```python -m venv venv```
2. ```cd venv/Scripts```
- Add wheel ```python -m pip install --upgrade pip setuptools wheel```
- To enter the virtual enviroment ```activate```
- To exit the virtual enviroment ```deactivate```

[Venv Tutorial](https://chriswarrick.com/blog/2018/09/04/python-virtual-environments/)

## Pip
pip is the package installer for Python. You can use pip to install packages from the Python Package Index and other indexes

- ```pip install <package>```  - installs package to current enviroment
- ```pip uninstall <package>``` - uninstalls package from current enviroment

## Requirements.txt
A file which contains all the python packages used in the project

- ```pip freeze > requirements.txt``` - Capture the python requirements 
- ```pip install -r requirements.txt```  - Install all python packages specified in requirements file 

[How to include a Github repo in the requirements file](https://stackoverflow.com/questions/16584552/how-to-state-in-requirements-txt-a-direct-github-source)

Use [Git Frigid](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-frigid)/[Git Warm](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-warm) when installing and unistalling python packages to keep the requirements.txt up-to-date

## Git

1. ```git add .``` - Adds all files
2. ```git commit -m "commit message"``` - Commit all added files
3. ```git push -u origin master``` - Push to the github repo

***or***

Run [git-ship](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-ship) - updates requirement.txt and then follows commit sequence

## Visual Studio Code Tips

- Use a custom virtual enviroment by selecting it with the command ```python: Select Interpreter```
- Open intergrated terminal ```ctrl+'``` or View > terminal
[Enviroments](https://code.visualstudio.com/docs/python/environments)

---

# PC Setup Instructions

1. [Install Python](https://www.python.org/)
2. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
3. ```git config --global user.name "<name>"``` - Change the user's name
4. ```git config --global user.email "<email>"``` - Change the user's email address
5. Add [Shortcut Git CMDs](https://github.com/marmstr93ng/Shortcut)
6. [Create a new repository](https://github.com/marmstr93ng/PythonTemplate#pythontemplate) ***or*** [Clone an existing repository](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-setup-python-clone)

NOTE: Setup [SSH](https://github.com/marmstr93ng/PythonTemplate#ssh) may be neccessary

## SSH
### Setup SSH Key
```Generate SSH Keyssh-keygen -t rsa -b 4096 -C "your_email@example.com"```
- On "Enter a file in which to save the key," press Enter. This accepts the default file location.
- At the prompt, type a secure passphrase.

#### Add SSH Key to SSH-Agent
- Ensure ssh-agent is enabled: ```eval "$(ssh-agent -s)"```
- Add your SSH key to the ssh-agent: ```ssh-add ~/.ssh/id_rsa```

#### Add SSH key to Github Account
- Copy the SSH key to your clipboard. ```clip < ~/.ssh/id_rsa.pub```
- In the top right corner of any page, click your profile photo, then click Settings
- In the user settings sidebar, click SSH keys.
- Click New SSH key.
- Name and add Key

#### Test SSH Connection
```ssh -T git@github.com```

# Other Links
1. [Documenting with Sphinx](http://www.sphinx-doc.org/en/stable/tutorial.html)
2. [Unit tests](https://docs.python.org/3.5/library/unittest.html)
3. [Packages](https://uoftcoders.github.io/studyGroup/lessons/python/packages/lesson/)
