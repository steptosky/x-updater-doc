.. _beta_access:

Beta/Alpha access
======================

.. include:: ../defines.rst


The updater gives you 3 types of snapshots *release, beta, alpha* with different access level. 
When you create a new snapshot using the commit command you are given a chose as per the type of the snapshot.
X-Updater client will give the |consumer| will be presented a chose as per which type of snapshot to update.

- release - the widest access type. Any |consumer| who has a valid login and password (key) can download the snapshot. 

- beta - this access type has limited access. You can grant the access in three ways:
	- to everyone - which means every |consumer| will have a chose of using the beta snapshot 
	- to a selected group - similar to private beta test, only the people you chose will be able to get the beta
	- to a limited number of people (slots) - you select a number of available beta test slots which are filled when a |consumer| selects the beta snapshot download. The slots are used up until the amount of available slots is zero. Then you need to give out more slots. If a slot has been taken by a |consumer| it remains his until you reset the access for all testers. 

- alpha - this snapshot can be accessed only by the selected group of beta testers (see above). Thus, any beta tester in the selected group has the chose of getting the alpha, provided you have created a separate alpha version of course. This should be used for quick tests of fixes or new functionality. 

.. note::
   The access types are prioritized. This means that if a |consumer| has requested an alpha but your last snapshot was a beta, he will get the beta. The prioritization is as follows: ``release > beta > alpha``.

**Examples**
    
    - we make a new beta snapshot and add 100 new beta slots. Note, the ``-slots`` argument can be only used with ``-type=beta``

    .. code-block:: bash

   		$ xupd client commit -desc="my new commit" -type=beta -slots=100

    - we make a release and reset the beta access for all |consumers| with slots

    .. code-block:: bash

   		$ xupd client commit -desc="my new commit" -type=release -resetBetaAccess

.. note::
   To change the number of available slots, take access away, reset the beta access etc. you can contact the |administrator|. This might be needed if you made a mistake, need to change something or want to add slots without making a new snapshot.

