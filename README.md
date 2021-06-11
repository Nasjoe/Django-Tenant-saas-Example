# Django Tenant Example.

This application enables Django powered websites to have multiple tenants via PostgreSQL schemas. A vital feature for every Software-as-a-Service website.

Django provides currently no simple way to support multiple tenants using the same project instance, even when only the data is different. Because we don’t want you running many copies of your project, you’ll be able to have:

    Multiple customers running on the same instance

    Shared and Tenant-Specific data

    Tenant View-Routing
    
https://django-tenants.readthedocs.io/en/latest/index.html

Base of TiBillet.re


## Installation for test :

```shell
cd Docker/Development
cp env_example .env

# populate .env file with your variables.

docker-compose --build up -d

# Go inside the Django Container :
docker exec -ti tibillet_django bash

# --> within the container :
  # on crée la DB :
  python manage.py migrate
  
  # on crée le premier tenant "demo" :
  python manage.py create_demo_tenant
  
  # Web Server ( only for test and dev ! )
  python /DjangoFiles/manage.py runserver_plus 0.0.0.0:8002
   
```

Test with www.$DOMAIN and demo.$DOMAIN
Don't forget to change your /etc/host if you are in localhost :)

Enjoy !

# Credits :

## Développement :

Jonas TURBEAUX & Nicolas DIJOUX
pour Peaks2Prod & 3Peaks Production.

Free for personal and commercial use under the MIT 3.0 license

## Graphisme : 

Massively by HTML5 UP
html5up.net | @ajlkn
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)


This is Massively, a text-heavy, article-oriented design built around a huge background
image (with a new parallax implementation I'm testing) and scroll effects (powered by
Scrollex). A *slight* departure from all the one-pagers I've been doing lately, but one
that fulfills a few user requests and makes use of some new techniques I've been wanting
to try out. Enjoy it :)

Demo images* courtesy of Unsplash, a radtastic collection of CC0 (public domain) images
you can use for pretty much whatever.

(* = not included)

AJ
aj@lkn.io | @ajlkn


Credits:

	Demo Images:
		Unsplash (unsplash.com)

	Icons:
		Font Awesome (fontawesome.io)

	Other:
		jQuery (jquery.com)
		Scrollex (github.com/ajlkn/jquery.scrollex)
		Responsive Tools (github.com/ajlkn/responsive-tools)
