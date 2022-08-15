# History Speeches Blog — training SPA project

It's my first trainig fullstack project — an SPA blog dedicated to known speeches of historical figures.

I'm a big fan of public speaking and Pavel Durov. 

I found out Pavel Durov was keen on public speeches as well. He even had a special section at his site durov.com where he posted MP3 files with Kennedy, Luther King and other famous people speaking up.

Unfortunately, the site durov.com/speeches hasn't been saved. You can now only see it using Wayback Machine. The downside is you can't listen to MP3 files.

So I decided to restore 'the largest collection of speeches on the Russian network', as Durov called it. 

[You can watch the screencast of site working on Google Disc →](https://drive.google.com/file/d/1fj1SxhLKdCE5vUZ16jCP3Ksn8MXWxH_D/view?usp=sharing).
## Build Setup

### Backend
Don't forget to type in your secret key in settings.py.

You should also add your mail and app-key from your mail service in views.py.

```bash
# install dependecies
pip install -r requirements.txt

# make migrations
python manage.py makemigrations

# migrate
python manage.py migrate

# serve at http://127.0.0.1:8000/
python manage.py runserver
```
For detailed explanation on how things work, check out [Django docs](https://docs.djangoproject.com/en/4.1/)


### Frontend

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
