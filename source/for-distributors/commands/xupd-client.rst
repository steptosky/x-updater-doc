.. _xupd_client:

client
==========

.. include:: ../../defines.rst

.. code-block:: bash

    $ usage: xupd client [sub-command] [arguments]


This command can be used to manage client settings. The client settings is stored in your PC you can set new values or read current ones.

.. code-block:: text

   sub-commands
         set                      set value
         get                      get value

   arguments:
        -apiKey        [set, get] distributor's api key


**Examples**:

- Set the |distributor| api key

.. code-block:: bash

   $ xupd client set -apiKey=ca5c22db1805612b49264281bffcfa86caa4a879