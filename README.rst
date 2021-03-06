Introduction
============

django-fs-email is the Django-related reusable app provides the ability to send multipart emails and store them in a database.

The distinctive feature of this app is storing sent emails in database. It means that you have ability to check each sent email from admin interface.


Installation
============

1. Install ``django-fs-email`` using ``pip``::

    $ pip install django-fs-email

2. Add ``'email'`` to your ``INSTALLED_APPS`` setting::

    INSTALLED_APPS = (
        ...
        'fs_email',
        ...
    )

3. Run ``migrate``::

    $ ./manage.py migrate


Usage
=====

Just import ``send_email`` function and use it::

    from fs_email import send_email

    send_email('from_email@example.com', 'to_email@example.com', 'fs_email/email_template.html', {})

    send_email('from_email@example.com', ['to_email_1@example.com', 'to_email_2@example.com'], 'fs_email/email_template.html', {})


Credits
=======

`Fogstream <http://fogstream.ru>`_
