# udacity Full Stack Web Developer Nanodegree Project 3 - Item Catalog

## Requirements

install necessary libraries:
```bash
pip install -r req.txt
```

* python
* [flask v0.10.1](http://flask.pocoo.org) 
* [sqlalchemy v2.0](http://www.sqlalchemy.org)
* [SeaSurf v0.2.1](https://flask-seasurf.readthedocs.org)
* [GitHub-Flask v3.0.1](https://github-flask.readthedocs.org/en/latest/)

##Setup
for GitHub OAuth the Client ID and Client Secret have to be changed in application.py: 

```python
app.config['GITHUB_CLIENT_ID'] = 'XXX'
app.config['GITHUB_CLIENT_SECRET'] = 'YYY'
```

for session managment you should change the secret key of the app:
```python
app_secret = 'ZZZ'
```

the callback url should be something like /github-callback
and can be configured in the head of application.py:


reset database:
```bash
rm catalog.db
python addData.py
```

##Usage
start application
```bash
python application.py
```

##JSON endpoints
[GET]
* /
* /catalog/
* /catalog/\<category_name\>/
* /item/\<item_id\>/
* /login
* /logout
* /github-callback

[POST]
* /catalog/\<category_name\>/add/
* /item/\<item_id\>/edit/
* /item/\<item_id\>/delete/

# Project 5 Configurateion

This project is linked to the Configuring Linux Web Servers course.

Launch your Virtual Machine with your Udacity account
Follow the instructions provided to SSH into your server
Create a new user named grader
Give the grader the permission to sudo
Update all currently installed packages
Change the SSH port from 22 to 2200
Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)
Configure the local timezone to UTC
Install and configure Apache to serve a Python mod_wsgi application
Install and configure PostgreSQL:
Do not allow remote connections
Create a new user named catalog that has limited permissions to your catalog application database
Install git, clone and setup your Catalog App project (from your GitHub repository from earlier in the Nanodegree program) so that it functions correctly when visiting your server’s IP address in a browser. Remember to set this up appropriately so that your .git directory is not publicly accessible via a browser!