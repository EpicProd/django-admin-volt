# Django Admin Volt

Modern template for **Django admin interface** coded on top of Volt Dashboard (free version) from **Themesberg**. Volt Dashboard is a free and open source Bootstrap 5 Admin Dashboard featuring over 100 components, 11 example pages and 3 plugins with Vanilla JS.

> Originally coded by [Iman Karimi](https://github.com/imankarimi), actively supported by [AppSeed](https://appseed.us/) via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup) - 24/7 LIVE Service.

<br>

**Links & Resources**

- [Django Volt Dashboard](https://appseed.us/admin-dashboards/django-dashboard-volt) - Open-source starter that uses the same UI Kit
- [Django Volt Dashboard](https://django-volt-dashboard.appseed-srv1.com/) - LIVE Demo

<br />

## Why Django Admin Volt?

- Bootstrap 5 Design: **Volt Dashboard** (Free version) provided by **Themesberg**
- New fresh look
- Responsive mobile interface
- Useful admin home page
- Minimal template overriding
- Easy integration

<br />

![Django Admin Volt - Template project for Django provided by AppSeed.](https://user-images.githubusercontent.com/51070104/132288100-0c65159f-71a6-41f0-9f55-9544916385ae.jpg)

<br>

## Installation

```bash
$ pip install django-admin-volt
// OR
$ pip install git+https://github.com/app-generator/django-admin-volt.git
```

* Add 'admin_black' application to the INSTALLED_APPS setting of your Django project settings.py file (note it should be before 'django.contrib.admin'):

```python
    INSTALLED_APPS = (
        ...
        'admin_volt.apps.AdminVoltConfig',
        'django.contrib.admin',
    )
```


* All programs you add in **INSTALLED_APPS** should look like this: **APP_NAME.apps.APP_NAMEConfig**.

> In this feature, we considered that each App can have its own icon, so we ask users to use this feature according to the method. Also in apps.py of each program according to the example add the icon field in the corresponding class. You can go **[here](https://fontawesome.com/v4.7/icons/)** to use more icons


```python

    from django.apps import AppConfig

    class APP_NAMEConfig(AppConfig):
        name = 'APP_NAME'
        icon = 'ICON_CLASS'  # for example: icon = 'fa fa-users'
```

* Make sure ``django.template.context_processors.request`` context processor is enabled in settings.py (Django 1.8+ way):

```python

    TEMPLATES = [
        {
            'BACKEND': 'django.template.backends.django.DjangoTemplates',
            'DIRS': [],
            'APP_DIRS': True,
            'OPTIONS': {
                'context_processors': [
                    ...
                    'django.template.context_processors.request',
                    ...
                ],
            },
        },
    ]
```

:warning: **Warning!!**
* Before Django 1.8 you should specify context processors different way. Also use ``django.core.context_processors.request`` instead of ``django.template.context_processors.request``.

```python
    from django.conf import global_settings

    TEMPLATE_CONTEXT_PROCESSORS = global_settings.TEMPLATE_CONTEXT_PROCESSORS + (
        'django.core.context_processors.request',
    )
```

* Collect static if you are in production environment:

```bash
$ python manage.py collectstatic
```

* Clear your browser cache

<br />

## Screenshots

![Django Admin Volt - Main Django Dashboard screen.](https://user-images.githubusercontent.com/51070104/136143245-85cd8af7-43ea-4956-8fcd-45e307171943.png) 

---
**Django Admin Volt** - Provided by **AppSeed [App Generator](https://appseed.us/)**
