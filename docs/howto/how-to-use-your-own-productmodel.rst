=================================
How to use your own product model
=================================

You can use your own product base model with the django shop, by setting the
``SHOP_PRODUCT_MODEL`` setting to point at a different model. The setting
format is the same as for the address model, for example::

    SHOP_PRODUCT_MODEL = 'myapp.models.MyBaseProduct'


Minimal required API for Product models
=======================================

* A ``get_name`` method that returns a string.
* A ``get_price`` method that returns a ``Decimal``.
* A ``get_absolute_url`` method that returns a URL as a string.
* The default manager must have a ``active`` method that returns a queryset of
  active products.
