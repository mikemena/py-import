# py-import

# Python virtual enviornment set up

Python 3 comes with a virtual enviornment module built-in called 'venv'. There's no need to download anything. Just jump in and create a vm

1- In terminal navigate to the project folder

2 - To create a virtual enviornment. In this example calling it 'pyimport':

    python3 -m venv pyimport_venv

3 - Activate the virtual enviornment by sourcing the activate script in its bin directory

    source pyimport_venv/bin/activate

4 - To deactivate the virtual enviornment, just type 'deactivate':

    deactivate

5 - In .gitignore file, you may want to add the virtual enviornment folder as 'venv/' is not picking the folder up.

6 - To delete, just delete the virtual enviornment folder from the project directory

# To add folder to sys.path list in order to find the module in given folder

## PYTHONPATH

PYTHONPATH is an environment variable which you can set to add additional directories where python will look for modules and packages.

Before we modify it, let’s check its contents (to make sure we are not overwriting) using echo $PYTHONPATH in the terminal :

    echo PYTHONPATH

If nothing is returned, then create it

    need to define...

If PYTHONPATH is returned, then append it. You must add your new directory to PYTHONPATH, separated by a colon (:) from its existing contents.

    export PYTHONPATH=$PYTHONPATH:$(pwd)/utils

Note: Once you close python, the list will revert to the previous default values. If you’d like to permanently add a directory to PYTHONPATH, add the export command (export PYTHONPATH=$PYTHONPATH:$(pwd)/utils) to your ~/.bashrc.
