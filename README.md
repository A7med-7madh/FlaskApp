# Item Catalog Web Application
This web app is a project for the Udacity [FSND Course](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004).

## About
This project is a RESTful web application utilizing the Flask framework which accesses a SQL database that populates categories and their items. OAuth2 provides authentication for further CRUD functionality on the application. Currently OAuth2 is implemented for Google Accounts.

### Features
- Proper authentication and authorisation check.
- Full CRUD support using SQLAlchemy and Flask.
- JSON endpoints.
- RESTful web application.
- Implements oAuth using Google Sign-in API.

### Project Structure
```
.....................................................................................................................
├── app.py
├── client_secrets.json
├── database_setup.py
├── DB_Populator.py
├── login_decorator.py
├── README.md
├── static
│   └── style.css
└── templates
    ├── delete.html
    ├── delete_category.html
    ├── edit_category.html
    ├── index.html
    ├── items.html
    ├── layout.html
    ├── login.html
    ├── new-category.html
    ├── new-item-2.html
    ├── new-item.html
    ├── update-item.html
    └── view-item.html
.....................................................................................................................
```

## Steps to run this project

1. Download and install [Vagrant](https://www.vagrantup.com/downloads.html).

2. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

3. Clone or download the Vagrant VM configuration file from [here](https://github.com/udacity/fullstack-nanodegree-vm).

4. Open the above directory and navigate to the `vagrant/` sub-directory.

5. Open terminal, and type

   ```bash
   vagrant up
   ```

   This will cause Vagrant to download the Ubuntu operating system and install it. This may take quite a while depending on how fast your Internet connection is.

6. After the above command succeeds, connect to the newly created VM by typing the following command:

   ```bash
   vagrant ssh
   ```

8. Type `cd /vagrant/` to navigate to the shared repository.

9. Download or clone this repository, and navigate to it.

11. Install or upgrade Flask:
    ```bash
    sudo python3 -m pip install --upgrade flask
    ```
12. Run the following command to set up the database:
    ```bash
    python3 database_setup.py
    ```
13. Run the following command to insert dummy values. **If you don't run this, the application will not run.**
    ```bash
    python3 DB_Populator.py
    ```
14. Run this application:
    ```bash
    python3 app.py
    ```
15. Open `http://localhost:5000/` in your favourite Web browser, and try it :)

## Skills Honed
@@ This web app is a project for the Udacity FSND Course.
1. Python
4. OAuth
5. Flask Framework

## Debugging
In case the app doesn't run, make sure to confirm the following points:
- You have run `python3 DB_Populator.py` before running the application. This is an essential step.
- The latest version of Flask 1.x is installed.
- The latest version of Python 3.6.x is installed. In the vagrant machine, you may find Python 3.5.x installed by default. To install Python 3.6.x, follow [this answer](https://askubuntu.com/a/865569/571299). To invoke Python 3.6, type `python3.6` instead of `python3`.

## Known Issue
This app might show an empty username if you sign in with a custom-domain-based Google account. For instance, if you use a Google account `someone@example.com`, this app might show an empty username. So, make sure to use an email with `gmail.com` domain only for best experience.

## Help and Support
In case you run into any trouble, create an issue on GitHub. I will make sure to look into it as soon as possible.
