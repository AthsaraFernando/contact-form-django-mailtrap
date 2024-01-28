
# Contact-form-django-mailtrap

This can be used to send emails using any SMTP server, like mailtrap,Gmail etc. You may need to setup a virtual environment if you run this on a host.


## Django Initializing Commands 

Command to create the virtual environment (don't need to use this)

```bash
    django-admin startproject myproject .
```
Command to run (needed)

```bash
    python manage.py runserver
```
## Installation

Install the relavant libraries.

## Sender and Reciever

- Sender is the SMTP email Host that we mention in the myproject>settings.py.
- Reciever is in the myproject>views.py ['JohnDoe@gmail.com'], # Send to (your admin email) . [Not for Mailtrap]
- in Mailtrap no matter what the reciever is it will send to the mailtral inbox.

## When using with Mailtrap

Replace below lines in myproject>settings.py 
, go to mailtrap inbox in email testing and find the SMTP details:

- EMAIL_HOST_USER = '######'
- EMAIL_HOST_PASSWORD = '#########'

## When using with Gmail

Replace below lines in myproject>settings.py 
,  don't put email password EMAIL_HOST_PASSWORD instead use app password. to make an app password fo to google mage our google account > security > app password:

- EMAIL_HOST = 'smtp.gmail.com'
- EMAIL_PORT = 587  # Use 587 for TLS, or 465 for SSL
- EMAIL_HOST_USER = 'sendersmail@gmail.com'
- EMAIL_HOST_PASSWORD = 'XXXXXXXXX'



## Tech Stack

Django, HTML, python


