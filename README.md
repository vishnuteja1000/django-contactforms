Django Contact Us Form
====================================

Install
----------------------

Django Contact Us is available directly from `PyPI`_:

::

    $ pip install django-contacts-us


***).** And don't forget to add ``contactus`` to your ``INSTALLED_APPS``.


Requirement
----------------------

* ``Django>=3.0.5`


Database Migration
----------------------

::

    $ ./manage.py makemigrations contactus
    $ ./manage.py migrate contactus





URL configuration
----------------------

The easiest way to set up the views in ``django-contacts-us`` is to just use the provided ``URLconf``, found at ``contactus.urls``.
You can include it wherever you like in your site's URL configuration; for example, to have it live at the URL ``/contact/``:

::

    from django.urls import path, include

    urlpatterns = [
        # ....
        path('contact/', include('contactus.urls')),
    ]


Usage
----------------------

Include the template from ``contact/contact.html`` to your sidebar for example.

::

    {% include "contact/contact.html" %}
 
 