Heroku buildpack: Python
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for Python apps.


Usage
-----

Example usage:

    $ ls
    Procfile  r.txt  web.py

    $ heroku create --buildpack git://github.com/rozha/heroku-buildpack-python.git

    $ git push heroku master
    ...
    -----> Python app detected
    -----> Installing runtime (python-3.4.3)
    -----> Installing dependencies using pip
           Downloading/unpacking requests (from -r r.txt (line 1))
           Installing collected packages: requests
           Successfully installed requests
           Cleaning up...
    -----> Discovering process types
           Procfile declares types -> (none)

You can also add it to upcoming builds of an existing application:

    $ heroku buildpacks:set git://github.com/rozha/heroku-buildpack-python.git
