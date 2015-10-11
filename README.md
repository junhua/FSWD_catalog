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