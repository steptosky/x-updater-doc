.. _distributors_faq:

FAQ
========================

.. include:: ../defines.rst

How to report a bug?
-----------------------------------------------------------------------------------------------------------------------------------
You have to contact the |administrator| via email. 

Write subject 
.. code-block:: text

[X-Updater][bug] Subject

How to get support?
-----------------------------------------------------------------------------------------------------------------------------------
You have to contact the |administrator| via email

Write subject 
.. code-block:: text

[X-Updater][support] Subject

X-Updater restores files that can be changed by my application. How to tell the X-Updater not to restore them?
-----------------------------------------------------------------------------------------------------------------------------------
This problem often occurs if you use the same settings file to configure your application and to store user's data.

In general you have to design your application in such a way that application's data and user's data use different files and you shouldn't distribute the files that are used to store user's data.

Another way is to not distribute settings file and check whether settings file exist by your application. If it doesn't then create it by your application with necessary default values.

But if you can't use the abovemented ways for some reasons you can use tags in ignore list but it is just a workaround and is not recommended. 
To enable this you have to contact the |administrator|


My product has extended versions. How can I distribute all of them?
-----------------------------------------------------------------------------------------------------------------------------------
In this context 'extended' is considered a completely new product in x-plane.org store.
You have to contact the |administrator| to get the instructions.


My product has some variations e.g. different colors, plug-ins, textures etc... How can I distribute those variations?
-----------------------------------------------------------------------------------------------------------------------------------
Actually there is no way to distribute products with variations now. But we know about this problem and we are thinking about how to implement this feature.

Pay attention it might be like 'extended' feature described above but actually it is a different thing and it doesn't depend on the store.


