# Build any blog with Django

[![alt text](https://github.com/justdjango/dream_blog/blob/master/thumbnail.png "Logo")](https://youtu.be/HWg3zXWwre8)

This [tutorial series](https://youtu.be/HWg3zXWwre8) shows how to connect any HTML blog template to Django, leaving you with an awesome looking, fully-functional blog.

Get the original HTML template [here](https://bootstrapious.com/p/bootstrap-blog)

# Running the blog
1. Install Postgres
```
sudo apt update
sudo apt install postgresql postgresql-contrib
```
2. Create the DB
```
sudo -u postgres psql
create database mydb;
create user myuser with encrypted password 'mypass';
grant all privileges on database mydb to myuser;
```
3. Install python's project dependencies
```
pip install -r requirements.txt
```
if you faced an error installing the psycopg2 library, try running the following commands:
```
sudo apt-get install postgresql
sudo apt-get install python-psycopg2
sudo apt-get install libpq-dev
```
4. Update the settings.py file in blog directory with your DB's connection

5. Run the Django app:
```
python manage.py makemigrations
python manage.py migrate --run-syncdb
python manage.py createsuperuser
python manage.py collectstatic
python manage.py runserver 7777
```


