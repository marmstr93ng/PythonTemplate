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

## Requirements.txt
- Generate a python requirements file which contains all the python libraries used in the project
```pip freeze > requirements.txt```

- Install all python libraries specified in requirements file
```pip install -r requirements.txt```

[How to include a Github repo in the requirements file](https://stackoverflow.com/questions/16584552/how-to-state-in-requirements-txt-a-direct-github-source)

If a new library has been included in the Virtual environment the requirements.txt will need to be updated. Remembering to do this manually could be problematic. Instead the requirements file should be updated and added to the commit if there is a change! To overcome the shortfall of having to manually keep the requirements up-to-date, use [git-ship](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-ship) to automatically update the requirements.txt file.


## Visual Studio Code Tips

- Use a custom virtual enviroment by selecting it with the command ```python: Select Interpreter```
- Open intergrated terminal ```ctrl+'``` or View > terminal
[Enviroments](https://code.visualstudio.com/docs/python/environments)

---

# PC Setup Instructions

1. [Install Python](https://www.python.org/)
1. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2. ```git config --global user.name "<name>"``` - Change the user's name
3. ```git config --global user.email "<email>"``` - Change the user's email address
4. Setup SSH if necessary (see below)
5. Add [Shortcut Git CMDs](https://github.com/marmstr93ng/Shortcut)
6. [Create a new repository](https://github.com/marmstr93ng/PythonTemplate#pythontemplate) ***or*** [Clone an existing repository](https://github.com/marmstr93ng/Shortcut/blob/master/README.md#cmd--git-setup-python-clone)

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
