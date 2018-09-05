# PythonTemplate
A template layout of a Python project

1. Create repository in github - No additional files
2. Create a local directory
3. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
4. ```git init``` - creates an empty git repository in the local directory (.git subdir with necessary metadata)
5. ```git config --global user.name "<name>"``` - Change the user's name
6. ```git config --global user.email "<email>"``` - Change the user's email address
7. Setup SSH if necessary (see below)
8. Download Python template files and place in the local directory
9. '''git add .''' - Adds all files
10. ```git commit -m "first commit"``` - Commit all added files
11. ```git remote add origin https://github.com/marmstr93ng/___.git``` - Refer to the url of the github repo
12. ```git push -u origin master``` - Push to the github repo

All git commands entered through git bash (Right click on Repo and click "Git Bash Here").

## Setup SSH Key

```Generate SSH Keyssh-keygen -t rsa -b 4096 -C "your_email@example.com"```
- On "Enter a file in which to save the key," press Enter. This accepts the default file location.
- At the prompt, type a secure passphrase.

### Add SSH Key to SSH-Agent
- Ensure ssh-agent is enabled: ```eval "$(ssh-agent -s)"```
- Add your SSH key to the ssh-agent: ```ssh-add ~/.ssh/id_rsa```

### Add SSH key to Github Account
- Copy the SSH key to your clipboard. ```clip < ~/.ssh/id_rsa.pub```
- In the top right corner of any page, click your profile photo, then click Settings
- In the user settings sidebar, click SSH keys.
- Click New SSH key.
- Name and add Key

### Test SSH Connection
```ssh -T git@github.com```

# Using Pipenv
1. Install Pipenv on to the PC ```pip install pipenv```
2. Intiate Pipenv in the folder by navigating to the folder and entering ```pipenv install```
3. Install python packages locally ```pipenv install <package name>```
4. Update lock file ```pipenv lock```
5. When a lock file with dependencies is included ```pipenv install``` will install these depedencies

[Pipenv Tutorial](https://robots.thoughtbot.com/how-to-manage-your-python-projects-with-pipenv)

# Other Links
[Documenting with Sphinx](http://www.sphinx-doc.org/en/stable/tutorial.html)

[Unit tests](https://docs.python.org/3.5/library/unittest.html)

[Packages](https://uoftcoders.github.io/studyGroup/lessons/python/packages/lesson/)
