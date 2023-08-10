# TestAWS

# create project
# create .env file
# add secret key there
# export SECRET_KEY='django-insecure-5a6x!0+dv-wt7w+j1dz0vtxyx!v0=8%*lz#bk#0ajpek=tegrr'
# change settings.py:
# SECRET_KEY = os.environ.get('SECRET_KEY')
# run in terminal:
# source .env
# python3 manage.py runserver
# add to settings file STATIC_ROOT = 'collections/static_collections'
# to collect static files before deployment
# add to settings vers for medias:
# MEDIA_URL = '/media/'
# MEDIA_ROOT = 'collections/media'
# add settings for DB
# DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': os.environ.get('DB_NAME'),
        'USER': os.environ.get('DB_USER'),
        'PASSWORD': os.environ.get('DB_PASSWORD'),
        'HOST': os.environ.get('DB_HOST'),
        'PORT': os.environ.get('DB_PORT', '5432')
    }
}
# add to .env file vars:
export DB_NAME='testDB'
export DB_USER='postgres'
export DB_PASSWORD='julia123'
export DB_HOST='localhost'
export DB_PORT='5432'
# whitenoise setup for static files
# https://whitenoise.readthedocs.io/en/stable/
# pip install whitenoice