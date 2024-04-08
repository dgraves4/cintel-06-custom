# cintel-06-custom: Custom NBA Stats App
This is a cutom project showcasing an application that includes interactive analytics and continuous intelligence elements. 

## Requirements (for local environment only)
- faicons
- pandas
- numpy
- plotly
- shiny
- shinylive
- shinywidgets
- scipy

## Try in the Browser

Go to PyShiny Playground at <https://shinylive.io/py/examples/#basic-app>.
Copy and paste content from [dashboard/app.py](dashboard/app.py) and run.
The PyShiny Playground includes these packages already, so you won't need requirements.txt:

- <https://shiny.posit.co/py/docs/shinylive.html#python-packages>

## Get the Code

Fork this project into your own GitHub account and/or just borrow code from app.py.
Clone your GitHub repo down to your local machine.
Use your GitHub **username** in place of dgraves4 and your GitHub **repo name** in place of cintel-06-custom.
[GitHub CLI](https://cli.github.com/) may work better on some machines.

```bash
git clone https://github.com/dgraves4/cintel-06-custom
```

## Run Locally - Initial Start

After cloning your project down to your Documents folder, open the project folder for editing in VS Code.

Create a local project virtual environment named .venv, activate it, and install the requirements.

When VS Code asks to use it for the workspace, select Yes.
If you miss the window, after installing, select from the VS Code menu, View / Command Palette, and type "Python: Select Interpreter" and select the .venv folder.

Open a terminal (VS Code menu "View" / "Terminal") in the root project folder and run these commands (for Windows - the activate command is slightly different Linux/Mac).

```bash
py -m venv .venv
source .venv\Scripts\Activate
py -m pip install --upgrade pip setuptools
py -m pip install --upgrade -r requirements.txt
```

Open a terminal (VS Code menu "View" / "Terminal") in the root project folder and run these commands.

```bash
shiny run --reload --launch-browser dashboard/app.py
```

Open a browser to <http://127.0.0.1:8000/> and test the app.

## Run Locally - Subsequent Starts

Open a terminal (VS Code menu "View" / "Terminal") in the root project folder and run these commands.

```bash
source .venv\Scripts\Activate
shiny run --reload --launch-browser dashboard/app.py
```

## After Changes, Export to Docs Folder

Export to docs folder and test GitHub Pages locally.

Open a terminal (VS Code menu "Terminal" / "New Terminal") in the root project folder and run these commands.

```bash
shiny static-assets remove
shinylive export dashboard docs
py -m http.server --directory docs --bind localhost 8000
```

Open a browser to <http://[::1]:8000> and test the Pages app.

## Push Changes back to GitHub

Open a terminal (VS Code menu "Terminal" / "New Terminal") in the root project folder and run these commands.

```bash
git add .
git commit -m "Useful commit message"
git push origin main
```

## Enable GitHub Pages

Go to your GitHub repo settings and enable GitHub Pages for the docs folder.

## Sources 
- Data from API-NBA: https://rapidapi.com/api-sports/api/api-nba  
- Shiny for Python: https://shiny.posit.co/py/
- Favicon generator: https://favicon.io/