# my-first-blog
Django Girls Tutorial Project

https://tutorial.djangogirls.org/en/

https://jessicakan789.pythonanywhere.com 

# Start-up notes
```
# go to djangogirls directory
cd djangogirls

# create virtual environment
python -m venv myvenv

# run local server/website
python manage.py runserver
```

# Create a blog post
```
# command line
python manage.py shell

# python
from blog.models import Post
from django.contrib.auth.models import User

me = User.objects.get(username='jessica')
Post.objects.create(author=me, title='Sample title', text='Test')
post = Post.objects.get(title="Sample title")
post.publish()
```

## Notes

* my_site is the project
* blog is the app
* models.py contains information about each table in the database
* views.py consists of functions that get the information
* templates displays the information from views.py
* urls.py defines the endpoint where the template is displayed
