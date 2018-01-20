.. _xupd_status:

status
==========

.. include:: ../../defines.rst

.. code-block:: bash

    $ usage: xupd status [-dir [DIR]] [-apiKey [API KEY]] [-productId [PRODUCT ID]]


This command is for checking the difference between your local product and last committed one to the server. It is for information only and it doesn't change anything.

.. code-block:: text

   optional-arguments:
         -dir              Product dir. if it isn't specified then 
                           the current working dir is considered as the product's one.
                           
         -apiKey           Distributor api key, if it isn't specified then 
                           the value will be searched in the client settings.

         -productId        Product public id, if it isn't specified then 
                           the value will be searched in the file *productId* inside 
                           the *x-updater* folder.


**Examples**:

.. code-block:: bash

   $ xupd client status


.. code-block:: bash

   $ xupd client status -dir="myProductFolder" \
                        -apiKey=ca5c22db1805612b49264281bffcfa86caa4a879 \
                        -productId=7b8ea61ebb1082b9e8300c304b182f808d1bccae