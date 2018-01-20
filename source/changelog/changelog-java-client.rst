.. _changelog_java_client:


The X-Updater Java Client
===========================

0.6.0-beta (19.01.2018)
--------------------------------------------------------------------
- Feature: selecting snapshot types release/beta/alpha.
- Feature: fresh installation.
- Patch: when you select the product dir it now uses the x-updater config from that dir.
         It fixes some problems when client is used as installer.
- Fix: the problem with incorrect updating when path contains more than one folder named 'Aircraft'.
- Fix: the problem when some files can be rewritten while updating but they should be untouched.
- Fix: the problem when some files must be downloaded or updated but for some reason it did not work.

0.5.1-beta (07.07.2017)
--------------------------------------------------------------------
- Fix: bound products path.


0.5.0-beta (29.06.2017)
--------------------------------------------------------------------
- Feature: supporting bound products inside the base product.
- Fix: some minor bugs.


0.4.0-beta (01.04.2017)
--------------------------------------------------------------------
- Feature: related products.
- Feature: bound products.
- Patch: using case sensitive path on windows.
- Fix: some minor bugs.


0.3.1-beta (25.12.2016)
--------------------------------------------------------------------
- Patch: config can have "cache=0" parameter for disabling the cache.


0.3.0-beta (28.11.2016)
--------------------------------------------------------------------
- Patch: some UI elements have been increased.
- Patch: auto-trim for the authentication text (i.e. user name and key).
- Patch: text when product's developer doesn't provide product description.
- Patch: logging.

- Fix: changing mode installer->updater when the client is run inside product's directory.


0.2.7-beta (28.09.2016)
--------------------------------------------------------------------
- Feature: count of the files for deleting.
- Feature: auto open finish page after installation is completed.
- Feature: auto open finish page after verification is completed and there no files to update.

- Fix: auto-run the client after self-update. WARNING: It will have the effect in next time.
- Fix: progress bar value when process is completed.
- Fix: floating error after pressing cancel button.
- Fix: some bugs in the config.


0.2.6-beta (27.09.2016)
--------------------------------------------------------------------
- Feature: link to the support (on finish page and while critical errors)
- Patch: log improvements.


0.2.5-beta (10.09.2016)
--------------------------------------------------------------------
- Patch: internal changes.


0.2.4-beta (24.08.2016)
--------------------------------------------------------------------
- Fix: fixes texts.


0.2.2-beta (15.08.2016)
--------------------------------------------------------------------
- Patch: internal improvements.


0.2.0-beta (12.08.2016)
--------------------------------------------------------------------
- Fix: 60 minutes before timeout now.


0.1.9-beta (07.07.2016)
--------------------------------------------------------------------
- Fix: mixed updater's and installer's configurations.
