# Automatic Text Summarizer


## Features:
- Summarize both English and Tamil text.
- Summarize text via either copy-paste paragraph or URL.
- User can save summarized text.
- Summarize pdf file to text file.

User can choose one of the following algorithms for text summarization:
- Frequency Algorithm
- Sentence Matching

## Dependencies
- nltk
- beautiful soup
- django

## Installation

1. Go to folder you want to put the cloned project in your terminal & type: <br>
    `git clone https://github.com/buvanapavitra/textSummarizerTEAM11.git`

2. Install the project dependencies:<br>
    `pip install -r requirements.txt`

3. In settings.py, replace value of SECRET_KEY with your own key(set environment variable).   
```SECRET_KEY = os.environ.get('SECRET_KEY', '-1')```
- You can generate your secret key [here](https://www.miniwebtool.com/django-secret-key-generator/)

4. Create local MySQL database named 'text_summarizer'.
- Edit your database credentials in following lines in settings.py
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'text_summarizer',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': '',
        'PORT': '',
    }
}
```

5. In terminal:  
    * `$ python manage.py migrate` - this will apply migrations to your local MySQL database   
    * `$ python manage.py createsuperuser` - this will create admin support   
    * `$ python manage.py runserver` - Run Server
