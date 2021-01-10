# wekart
<img src="https://user-images.githubusercontent.com/62329524/104125001-f4d22f00-534b-11eb-98d4-838393b9083f.png" />
1. this is a basic commerce app similar to amazon or flipkart
1. in this base is an app which handels all the functinality of the app
## installed apps in settings.py
1. **base.apps.BaseConfig**  _for the for store app & registration_
## urls.py
- in this we are using the templates and static files so we have to define the paths for that
```python
path('',include('base.urls'))
path('',include('django.contrib.auth.urls'))
urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
 ```
# base 
## templates
### base 
1. **base.html**  _this is base page which acts as parent page for other pages_
1. **cart.html**  _this is cart page_
1. **checkout.html**  _this is final checkout page_
1. **store.html**  _this is store page which will render all the items_
### register
1. **signup.html** _for signup page_
1. **login.html** _for login page_
## forms.py 
>this is for the django signup customization
## urls.py 
>this contains the views and set them the url
## admin.py 
>we use the admin to create or delete items of the page and we import this from models
## models.py
>we use this for creating the customers, products, order, orderitem, shippingaddress
## views.py
>we use this for rendering the items in the page & validating the signup and login
