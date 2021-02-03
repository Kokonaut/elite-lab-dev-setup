# Installing Python and VSCode on MacOS

## Quick Overview
As Mac users, you don't need anything extra to run the Terminal! Luckily Mac provides this to you as an application.

We will be introducing you to the terminal and installing the basic requirements needed to get you started with Python development.

## Finding the Terminal

The terminal is a powerful tool for unlocking everything you can do with your computer. 

MacOS provides access to the terminal via the terminal app. Finding it is simple, you can either:
* Hit Command+Space and type in Terminal. Double click the terminal app.
* Go to your Applications folder. Find Utilities. Double click the terminal app inside of Utilities.

## Set up Python

MacOS uses default Python 2.x out of the box. Unfortunately, support for 2.x is dropping, so we need to make sure that 3.x is installed.

To check whether you have Python 3.x installed, try the following command:
```
  python3 --version
```

This should return something like `Python 3.7.9`

The second two numbers don't matter, just check that the leading version number is 3.

If your output looks like that, then move onto the next section.

If you see a command such as: `command not found: python3`
then you will need to install Python onto your computer.

I highly suggest using a package manager for installing Python and other programs to your computer via terminal. 

What we'll be doing here is installing a common package manager to your computer, which will make actually installing Python a breeze.

First, copy + paste this command into your terminal:
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Agree to all the changes it prompts you.

Afterwards, installing Python is as easy as typing in this command:
```
  brew install python
```

Confirm that you have python3 installed with the command
```
  python3 --version
```

## Install virtualenv

VirtualEnv is a python dependency manager that will allow you to keep separate Python libraries for each of your projects.

You can install it with this command:

```
  sudo pip3 install virtualenv
```

Verify that its installed with

```
  virtualenv --version
```


## Download your Text Editor

You can use any text editor you'd like. If you don't have one of choice yet, then I highly suggest using VSCode.

You can find the download link here: https://code.visualstudio.com/download


## Create your first Flask app

I suggest creating a dedicated folder for all your coding projects. I have a file called `workspace/` (but feel free to call it whatever you wish).

* Navigate to wherever you want to organize your coding projects. You can either use Finder or the Terminal.

* Create a new folder. Label it `hello_world`

* Open the folder with VSCode.

  * You can either right click on the folder and open it with VSCode

  * Or you can open VSCode, go to the top left corner, and go to File > Open... and then find your folder from there

* On the top left of your screen, find "Terminal". Click to expand, and then click on "New Terminal" in the expanded list

* Now we will create a virtual environment for our folder (think of it like creating a new folder where all our dependencies go)
```
  virtualenv venv
```
(If this does not work for you, you can also try)
```
  python3 -m venv venv
```

* You should see a new folder called `venv/`. You usually do not need to modify this folder.

* Next, activate it with this command
```
  source venv/bin/activate
```

* If successful, you should see a `(venv)` or something similar next to your prompt. This means that the virtual environment is active, and anything you install via pip will be installed to that folder

* Next let's install the Flask dependency to your project
```
  pip3 install Flask
```

* You should see some text scroll by, indicating that you are downloading Flask

* Create a file inside your project folder called `app.py`.

* Paste this code into that file
```
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
	return 'Hello World'

if __name__ == '__main__':
	app.run(debug=True)
```

* Now go to the terminal and you can start Flask with
```
  flask run
```
(or you can use)
```
  python3 -m flask run
```

You should see text similar to
```
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

This means that you're server is running locally! You can visit the URL given to you to find the Hello World message.

## Extra

If you finish early, then go read up on Command Line basics. This will be invaluable for anytime you work with the terminal.

https://ubuntu.com/tutorials/command-line-for-beginners#1-overview

https://www.guru99.com/linux-commands-cheat-sheet.html