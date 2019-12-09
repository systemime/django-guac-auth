django-guac-auth
=======================

Django app to facilitate setting up Guacamole database items

[![Build Status](https://travis-ci.org/nimbis/django-guac-auth.svg?branch=master)](https://travis-ci.org/nimbis/django-guac-auth)

[![Coverage](https://coveralls.io/repos/nimbis/django-guac-auth/badge.png?branch=master)](https://coveralls.io/r/nimbis/django-guac-auth?branch=master)


Requirements
------------

* django >= 1.8

Installation
------------

* Run `pip install django-guac-auth` or download this package and run `python setup.py install`

* Ensure that `guac_auth` is in your INSTALLED APPS

Contributing
------------

See the [Contributing Guidelines](CONTRIBUTING.md).

History
-------
See file CHANGES.

Usage
-----

Several utility methods are provided.

    # Set up an RDP connection, guac user, and needed permissions
    ＃设置RDP连接，guac用户和所需的权限
    quick_rdp(guac_username="guactestuser", guac_password="guactest",
              username="Administrator", password="somepass",
              hostname="somehost")
    
    # Set up an RDP connection with the provided parameters
    ＃使用提供的参数建立RDP连接
    quick_rdp_conn(username="Adminstrator", password="somepass",
                   hostname="somehost"):
    
    # Set up a Guacamole user
    ＃设置一个Guacamole用户
    quick_guac_user(username="guactestuser", password="guactest"):
    
    # Destroy all bits set up by quick_rdp()
    ＃销毁quick_rdp（）设置的所有位
    quick_rdp_destroy(guac_username="guactestuser", username="Administrator",
                      hostname="somehost", cleanup_user=True,
                      cleanup_connection=True):
