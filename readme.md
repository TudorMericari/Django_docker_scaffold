This repo is a scaffold for djanog, postgre, nginx stack for django app development.

# Preparation
- Create new django app in app directory

# Development
docker-compose up --build
$ docker-compose exec web python manage.py migrate 
# Production
$ docker-compose -f docker-compose.prod.yml up -d --build
$ docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
$ docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear

# Customization
- Modify env files for database configuration.