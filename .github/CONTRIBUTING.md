## Contributing guidelines

Thank you for your interest in contributing to Fabrik! Here are a few pointers about how you can help.

### Setting things up

To set up the development environment, follow the instructions in [README](https://github.com/Cloud-CV/Fabrik/blob/master/README.md).

### Finding something to work on

The issue tracker of Fabrik a good place to start. If you find something that interests you, comment on the thread and we’ll help you get started.

Alternatively, if you come across a new bug in the application, please file a new issue and comment if you would like to be assigned. The existing issues are tagged with one or more labels, based on the part of the application it touches, its importance etc., that can help you in selecting one.

If neither of these seem appealing, please post on our channel and we will help find you something else to work on.

### Instructions to submit code

Before you submit code, please talk to us via the issue tracker so we know you are working on it.
	
Our central development branch is master. Coding is done on feature branches based off of development and merged into it once stable and reviewed. To submit code, follow these steps:

1. Create a new branch off of development. Select a descriptive branch name.
	```
        git fetch upstream
        git checkout master
        git merge upstream/master
        git checkout -b your-branch-name
	```
2. Commit and push code to your branch:

    - Commits should be self-contained and contain a descriptive commit message.
    - Please make sure your code is well-formatted and adheres to PEP8 conventions (for Python) and the `.eslint` located in the repository (for JavaScript).
    - Please ensure that your code is well tested.
    - We highly encourage to use `flake8` to follow the PEP8 styling. Run the following command before creating the pull request:
	```
	flake8 ./
	```
    - Also, for build errors and checking adherence to `.eslint`, run the following command during development:
	```
	webpack --progress --colors --watch
	```            
    - If you are using Sublime Text, you can lint code while writing it. Install the following plugins for Sublime Text.
        ```
        SublimeLinter
        SublimeLinter-contrib-eslint
        SublimeLinter-flake8
        ```
        *For installing the Sublime Package Control Manager in Sublime-Text Editor use [this](https://packagecontrol.io/installation#st2) link.*

3. Once the code is pushed, create a pull request:

    - On your Github fork, select your branch and click “New pull request”. Select your target branch (for example “master”) as the base branch and your branch in the “compare” dropdown.
If the code is mergeable (you get a message saying “Able to merge”), go ahead and create the pull request.
    - Check back after some time to see if the Travis checks have passed, if not you should click on “Details” link on your PR thread at the right of “The Travis CI build failed”, which will take you to the dashboard for your PR. You will see what failed / stalled, and will need to resolve them.
    - If your checks have passed, your PR will be assigned a reviewer who will review your code and provide comments. Please address each review comment by pushing new commits to the same branch (the PR will automatically update, so you don’t need to submit a new one). Once you are done, comment below each review comment marking it as “Done”. Feel free to use the thread to have a discussion about comments that you don’t understand completely or don’t agree with.

    - Once all comments are addressed, the reviewer will give an LGTM (‘looks good to me’) and merge the PR.

Congratulations, you have successfully contributed to Project Fabrik!
