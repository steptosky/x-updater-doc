.. _upload_product:

How to upload your product or its update
========================================================================

.. include:: ../../defines.rst

- Setup your ``xupd`` client if you haven't done so. See :ref:`xupd_client`.
- Put necessary information into ``x-updater/description.txt`` file.

.. warning::
   If you forget to put changes into this file there is no way to fix it except ask the |administrator|

- Use command ``xupd status`` if you want to see the changes before uploading them. See :ref:`xupd_status`.
- Use command ``xupd commit`` to upload your changes and make new snapshot. Since your changes are uploaded they immediately are available for the |consumers|. See :ref:`xupd_commit`.

**Examples**:

.. code-block:: bash

   # It initializes and commits your product
   $ xupd init -productId=7b8ea61ebb1082b9e8300c304b182f808d1bccae
   $ xupd commit -apiKey=ca5c22db1805612b49264281bffcfa86caa4a879 \
                 -productId=7b8ea61ebb1082b9e8300c304b182f808d1bccae \
                 -desc="any text here"

.. code-block:: bash

   # Sets you distributor api key into local storage. 
   # It allows you to not specify it each time when you want to use status or commit command.
   $ xupd client set -apiKey=ca5c22db1805612b49264281bffcfa86caa4a879
   # go into product folder
   $ cd path_to_product
   # It initializes your local product in the current working dir
   # Also it allows you to not specify peoductId each time when you want to use status or commit command.
   $ xupd init -productId=7b8ea61ebb1082b9e8300c304b182f808d1bccae
   # It checks changes
   $ xupd status
   # It makes snapshot on the server with your changes
   # and starts distributing it
   $ xupd commit -desc="any text here"



.. note::
   In the previous version after your changes were uploaded you had to run X-Updater-client to initialize preparation process on the server then you had to wait for an email that confirms that the server has indeed prepared the files. Now if ``xupd commit`` doesn't return an error then all went well.