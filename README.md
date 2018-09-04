# PythonTemplate
A template layout of a Python project

1. Create repository in github - No additional files
2. Create a local directory
3. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
4. ```git init``` - creates an empty git repository in the local directory
5. ```git config --global user.name "<name>"``` - Change the user's name
6. ```git config --global user.email "<email>"``` - Change the user's email address
7. Download Python template files and place in the local directory
8. '''git add .''' - Adds all files
9. ```git commit -m "first commit"``` - Commit all added files
10. ```git remote add origin https://github.com/marmstr93ng/___.git``` - Refer to the url of the github repo
11. ```git push -u origin master``` - Push to the github repo

All git commands entered through git bash.

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
