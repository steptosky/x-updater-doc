.. _xupd_init:

init
==========

.. include:: ../../defines.rst

.. code-block:: bash

    $ usage: xupd init [-productId [PRODUCT ID]]


Init a new product in you local product's folder. This command will create *x-updater* folder and all necessary files with necessary content.
This command doesn't create and prepare product on the server for this issue you have to contact |administrator|.


.. code-block:: text

   arguments:
         -productId        Product public id.

   optional-arguments:
         -dir              Product dir. if it isn't specified then 
                           the current working dir is considered as the product's one.


**Examples**:

- Init new product with its public id

.. code-block:: bash

   $ xupd init -productId=7b8ea61ebb1082b9e8300c304b182f808d1bccae
