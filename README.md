# Django Skeleton

**What does this skeleton include?**
- Custom authentication with username/email login capablities
- Service Worker using updated version of `django-pwa` to work with django version 4.0
- Javascript file named `base.js` with function for cookie creation (Useful for ajax requests).
- 3rd party links and minified files such as 
    - anime.js v3.2.1
    - jQuery v3.6.0
    - fontawesome
    - bootstrap
- `.env` file with variables and/or variable names set for sendgrid, stripe and more...
- Necessary files for Heroku (e.g. `runtime.txt`, `Procfile`, `Pipfile.lock`, etc.)
- A default image in `static/images`
- CSS file structure (e.g. `base/`, `components/`, `themes/`, etc.)

---
## Setup

### Clone Repository
```
git clone https://github.com/shaun-ps-04/django-skeleton.git .
```

> Remember to uncomment `config/.env` in `.gitignore`


### Replace Git Repository
```bash
rm -rf .git
git init
```

### Create Virtual Environment
```bash
mkdir .venv
pipenv shell
```
> Select Python interpreter with `ctrl + shift + p` and choose the interpreter with the path `.venv/Scrips/python.exe`

### Install Packages
```bash
pipenv install
```

### Generate New Secret Key
```bash
py generate_sk.py
```
> Then replace the secret key in config/.env to the one printed out

### Finishing Setup
```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```
Runserver shortcut (runs on port 9000):
```bash
./server.sh
```

---
**Watch Sass**
In a separate terminal
```bash
cd static/css
sass --watch main.sass main.css
```

---
### Optional

**Include e-mails and payments**
```bash
pipenv install sendgrid stripe
```