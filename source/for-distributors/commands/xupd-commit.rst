.. _xupd_commit:

commit
==========

.. include:: ../../defines.rst

.. code-block:: bash

    $ usage: xupd commit [-dir [DIR]] [-apiKey [API KEY]] [-productId [PRODUCT ID]]
                         [-type [TYPE]] [-slots [SLOTS]] 
                         [-resetBetaAccess] [-force]


This command is for committing and uploading your changes. I.e. this command makes new snapshot in the system.

.. code-block:: text

   arguments:
         -desc             Commit description, for example you can set version. 
                           If you are familiar with git, svn, hg etc... 
                           this description is like their one.

   optional-arguments:
         -dir              Product dir. if it isn't specified then 
                           the current working dir is considered as the product's one.

         -apiKey           Distributor api key, if it isn't specified then 
                           the value will be searched in the client settings.

         -productId        Product public id, if it isn't specified then 
                           the value will be searched in the file *productId* inside 
                           the *x-updater* folder.

         -type             Commit type release, beta, alpha etc...

         -slots            Number of free slots for new public beta consumers.

         -resetBetaAccess  Remove all public beta consumers.

         -force            If there is previous unfinished commit you 
                           can abort it and force to make this one. 
                           This parameter is recommended for continuous integration.

.. note::
   See :ref:`beta_access` for more information about *-type, -slots, -resetBetaAccess*.

**Examples**:

.. code-block:: bash

   $ xupd client commit -desc="my new commit"


.. code-block:: bash

   $ xupd client commit -dir="myProductFolder" \
                        -apiKey=ca5c22db1805612b49264281bffcfa86caa4a879 \
                        -productId=7b8ea61ebb1082b9e8300c304b182f808d1bccae \
                        -desc="my new commit" \
                        -type=beta \
                        -slots=100 \
                        -resetBetaAccess \
                        -force
