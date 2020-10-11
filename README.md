# mystore
- this is a basic commerce app like amazon or flipkart
- in this we are using two apps one is for login, signup and app itself
## installed apps in settings.py
- crispy_forms // to use the bootstrap
- register.apps.RegisterConfig // for the login and signup 
- store.apps.StoreConfig // for the for store app
## urls.py
- in this we are using the templates and static files so we have to define the paths for that
- path('',include('store.urls'))
- path('',include('django.contrib.auth.urls'))
- urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
# store 
## templates
### store 
- base.html // this is base page which acts as parent page for other pages
- cart.html // this is cart page
- checkout.html // this is final checkout page
- store.html // this is store page which will render all the items
## admin.py 
we use the admin to create or delete items of the page and we import this from models
## models.py
we use this for creating the customers, products, order, orderitem, shippingaddress
## views.py
we use this for rendering the items in the page
