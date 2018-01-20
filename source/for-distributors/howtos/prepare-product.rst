.. _prepare_product:

How to prepare your product
========================================================================

.. include:: ../../defines.rst

Before you will be able to use the X-Updater for distribution of your products you have to prepare it.

- If you want to setup a new product no server you have to ask the |administrator| to create a new product there.
- Install dev client (named *xupd*) See :ref:`dev_client_usage`. if you don't have the client you have to ask the |administrator| where you can get it.
- Run ``xupd init -product="product id"`` See :ref:`xupd_init`.

Description of the x-updater files:

- *x-updater/client-configuration* - this file is the configuration for the client. Actually you don't have to change it yourself, **but you must commit this file with your product i.e. don't put it into the x-updater ignore list**.
- *x-updater/productId* - this file contains the public id of your product. **It must be committed with your product i.e. don't put it into the x-updater ignore list***.
- *x-updater/description.txt* - this file should describe your product, for example you can put the changelog there and any other text. **notes:** the content of this file will be shown for the |consumers| while updating. This file is processed while committing so you have to prepare all its content before you :ref:`xupd_commit` a new snapshot.
- *x-updater/xupdignore* - this is the ignore list. See :ref:`use_ignorelist`.

.. note::
     The x-updater automatically ignores unnecessary files like *description.txt*, *xupdignore*.

.. note::
  - The files *info.msg*, *x-updater/info.msg*, *x-updater/x-updater.cnf*, *.xupdignore*, *x-updater/.xupdignore* are not used anymore and should be deleted after ``xupd init``.