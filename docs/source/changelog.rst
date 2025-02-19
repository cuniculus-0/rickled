.. Natural Selection documentation master file, created by
   sphinx-quickstart on Tue Sep 22 22:57:54 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. _changelog-page:

Changelog
**************************

History
==========================

Version 1.1.0 (2024-02-05)
--------------------------

* Added `set` to BaseRickle, as a equivalent to the `get` method.
* Updated the `get` method to handle document paths.
* Added `remove` method to delete items from object.
* Added the `__delitem__` dunder, now able to `del rickle['key']`.
* Fixed bug where `search_path` was exiting loops in dictionary too early (after first find).
* Implemented type guessing of params for functions when using path like calling.
* Added ability to add params to callable. Example `rickle('/path/to/func', x=1, y='str')`.
* Bug fix in trying to parse URL by user `deajan`, commit `7cb1773`.


Version 1.0.2 (2023-12-12)
--------------------------

* Added `strict` boolean parameter for allowing properties that are reserved keywords.

Version 1.0.1 (2023-10-03)
--------------------------

* Added the ability to load a Rickle from URL at init.
* Added the `-b` flag to `serve` CLI tool to open host on browser.
* Bug fix in `infer_read_file_type` when reading unknown file suffix.
* Renamed the `-i` flag to `-a` in `serve` CLI tool.

Version 1.0.0 (2023-09-20)
--------------------------

* Added the schema validation tool `Schema` in `tools`.
* Added all CLI tools.
* Now releasing version 1.0.0

Version 0.3.5 (2023-09-09)
--------------------------

* Added the first of the `rickled.tools`, the `Converter`.
* Added first CLI tools `rickle conv` and `rickle serve`.

Version 0.3.4 (2023-07-20)
--------------------------

* Fixed error when importing from `rickled.net` when openssl is not installed.

Version 0.3.3 (2023-07-20)
--------------------------

* Adding optional install of `twisted` library.
* Added `serve_rickle_http` and `serve_rickle_https` to `rickled.net` to serve Rickles as REST API.


Version 0.3.2 (2023-04-07)
--------------------------

* When calling `dict()` on rickle, hot loaded items were not being serialised. Fixed.

Version 0.3.1 (2023-04-02)
--------------------------

* Fixed issue for path based query, where Rickle objects are considered callable (rightfully).
* Uses `inspect.isfunction` instead of `callable`.
* Added `meta` to base class for getting metadata of a property.

Version 0.3.0 (2023-02-16)
--------------------------

* Bumped up to minor 3, close to releasing version 1.0 after http server is implemented.
* Added the `hot_load` property to API calls, making it load on call instead of only on start.
* Added the `hot_load` property to HTML page, making it load on call instead of only on start.
* Added the `hot_load` property to add file, making it load on call instead of only on start.

Version 0.2.7 (2023-02-15)
--------------------------

* Complete revamp of internal versioning.

Version 0.2.6 (2023-02-15)
--------------------------

* Fixed the same bug, but the root cause. The fact that modules are imported before proper install.

Version 0.2.5 (2023-01-18)
--------------------------

* Fixed a bug where requests is not installed


Version 0.2.4 (2022-09-02)
--------------------------

* Added ability to get nodes by using Unix style paths to get to nodes.
* Added a safe load environment variable "RICKLE_SAFE_LOAD" to override all lambda loads (as a safety measure).
* Added ``search_path`` to search for a key in the Rickle.
* Removed ``includes_self_reference`` due to confusion.
* Added a third way to load CSV files, see example documentation.
* Added ``load_as_rick`` to ``add_api_json_call``.


Version 0.2.3 (2022-03-13)
--------------------------

* Merged but cleaned up contributions by Fabian.

Version 0.2.2 (2022-02-14)
--------------------------

* Added ``do_recursive`` param to ``.get`` to optionally do a deeper recursive search.
* Do you agree that valentine's day is bullshit? Because my gf doesn't.

Version 0.2.1 (2021-12-08)
--------------------------

* Added ``add_class_definition`` to define classes.
* Created a new class, ``ObjectRickler``, to dump (almost) any object or convert to Rickle.
* Added ``add_module_import`` to Rickle, with functionality to add global Python module imports.

Version 0.2.0 (2021-12-06)
--------------------------

* Renamed project to ``Rickled`` to avoid any possible lawsuits from money hungry media execs.
* Pickle Rick was a great name, possibly even considered a parody which is protected under copyright law.
* But rather safe than sued..

Version 0.1.14 (2021-10-28)
--------------------------

* Added new ``add_html_page`` to load HTML text.
* Added new ``add_csv_file`` to load CSV files as either a list of lists, or list of PickleRicks.

Version 0.1.13 (2021-10-07)
--------------------------

* Added ability to load from multiple YAML files or JSON files from start up.

Version 0.1.12 (2021-09-23)
--------------------------

* Fixed major bug, YAML was not loaded!
* Adding preload arguments for load and replace values within YAML files using ``_|PARAM|_``
* Added new API JSON call method, to load and create a Rick from an API response ``add_api_json_call``.
* Added new ability to load other YAML, JSON, or text files from within, using ``add_from_file``.
* Added ``add_base64`` to load base 64 encoded data.

Version 0.1.11 (2021-09-09)
--------------------------

* Fixed bug in ``get`` for finding values.
