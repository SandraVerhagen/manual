# Getting Anaconda to work in terminal

```{admonition} User types
:class: tip
This page is useful for user type 5-6.
```

(vscode-setup-bash)=
````{tab} Windows - Git Bash (preferred)

There are two things to do before you can use conda in your Git Bash CLI (possibly in VS Code): 1) adding Anaconda to your PATH variables (as user, *not* as system/admin), and 2) setting up Anaconda to run on Git Bash.

1. update the `PATH` variables: 
* search for 'env' in the windows search to find the settings page. Anaconda doesn't recommend adding them to the system `PATH`, therefore when searching for the setting with the Windows search, so be careful to open **"edit environment variables for your account"**; do **not** "edit the system environment variables". 
* Identify the box for adding variables for a specific user (the top box), not the system. 
* select the line with 'Path' and click edit
* Add the `Anaconda3` and `Anaconda3/Scripts` directories to `PATH`.

You will know if this worked because the `conda` commands below will not produce an error. You can also check by opening a Git Bash terminal and listing your Anaconda environments with `conda env list`.

2. To setup Anaconda, open git bash and run the collowing commands (note, the first two commands to create `myenv` can be skipped if you already have an Anaconda environment; e.g., default is `base`):
* `conda create -n myenv python`  
* `conda install -n myenv numpy`  
* run `conda init bash` to link conda to Git Bash
* restart shell (type `exit` to close)
* run `conda activate myenv` 
* restart shell

Check if it worked by opening a notebook in an aribtrary `DIR` using the command `jupyter lab --notebook-dir DIR`.
````
````{tab} MacOS
Usually, Anaconda works by default in the MacOS terminal. To check if it works for you type `conda` in the termal and execute. If you get help page for `conda`, you're all set. In VS code, open a new terminal by clicking **View > Terminal** in the top menu bar.

If you don't get a help page but something like:

    zsh: command not found: conda

then do the following:

1. Find out where Anaconda is installed on your system. If you left everything as default during the installation, Anaconda is installed in `/Users/<username>/anaconda3` if you used the install script, or in `/Users/<username>/opt` if you used the graphical interface to install Anaconda.

2. Execute the following line:

        source <anaconda-installation-dir>/bin/activate

3. Then:

        conda init zsh

4. Restart the terminal / VS Code then test by executing `conda` again. This time, it should give you the help page. You now have access to you Anaconda environments in your command line.
````
````{tab} Windows - Powershell

```{note}
This is not the preferred installation method: Powershell has a different set of terminal commands that are not Unix-based, whereas Git Bash does. Since the vast majority of coding information and examples on the internet related to Jupyter and other open source projects uses Unix-based commands, we strongly recommend you always run Git Bash for your work in the terminal.
``` 
````