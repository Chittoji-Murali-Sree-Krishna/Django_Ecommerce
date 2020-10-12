# mystore
1. this is a basic commerce app like amazon or flipkart
1. in this we are using two apps one is for login, signup and app itself
## installed apps in settings.py
1. **crispy_forms**  _to use the bootstrap4_
1. **register.apps.RegisterConfig**  _for the login and signup_ 
1. **store.apps.StoreConfig**  _for the for store app_
## urls.py
- in this we are using the templates and static files so we have to define the paths for that
```python
path('',include('store.urls'))
path('',include('django.contrib.auth.urls'))
urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
 ```
# store 
## templates
### store 
1. **base.html**  _this is base page which acts as parent page for other pages_
1. **cart.html**  _this is cart page_
1. **checkout.html**  _this is final checkout page_
1. **store.html**  _this is store page which will render all the items_
## admin.py 
>we use the admin to create or delete items of the page and we import this from models
## models.py
>we use this for creating the customers, products, order, orderitem, shippingaddress
## views.py
>we use this for rendering the items in the page
### store
>main store displays all the items
### cart
>this is a cart page will display items in cart
### checkout
>this is to render checkout page
### updateItem
>this for increasing or decreasing the items in the cart
### processOrder
>this for transaction id so that it will differentiate from each other
## urls.py 
>this contains the views and set them the url
# register
## templates
### register
>register.html // this is a signup page using django syntax
### registration
>login.html // this is a login page using django syntax
## forms.py 
>this is for the django signup customization
## views.py
this is to check wheter the details entered are correct or false, if its true it will save if not it wont save
