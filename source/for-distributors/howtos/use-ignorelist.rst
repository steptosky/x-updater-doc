.. _use_ignorelist:

How to use ignore list
========================================================================

Ignore list is located *x-updater/xupdignore*

Ignore list uses a prefix and postfix conception.
The prefix and postfix should be separated by * if there is no * presented then text considered as prefix.
For example: *folder2/*ex* any file or folder that starts with *folder2/* and ends with *ex* will be ignored.

**Examples:**

.. code-block:: text

    folder1/A - ignore file or whole folder 'A'
    folder1/A/* - ignore whole folder 'A'.
    folder2/*ex - ignore all files in the folder 'folder2' that end with 'ex'
    *ex - ignore all files in all the folders that end with 'ex'

You can use *!* or *not* for the files that you don't want to ignore.

**This example shows how to ignore whole folder except one file:**

.. code-block:: text

    folder1/A/* - ignore whole folder 'A'.
    !folder1/A/myFile - but don't ignore the file 'myFile' in the folder 'A'
    # the previous line can also be written the following way:
    not folder1/A/myFile

.. note::
   All paths must be specified relative to the product folder, not relative to the location of the ignore list!