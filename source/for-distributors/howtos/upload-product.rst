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

**Example**:

.. code-block:: bash

   $ cd path_to_product
   $ xupd client set -apiKey=ca5c22db1805612b49264281bffcfa86caa4a879
   $ xupd status
   $ xupd commit -type=beta -slots=50


.. note::
   In the previous version after your changes were uploaded you had to run X-Updater-client to initialize preparation process on the server then you had to wait for an email that confirms that the server has indeed prepared the files. Now if ``xupd commit`` doesn't return an error then all went well.