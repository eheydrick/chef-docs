=====================================================
Release Notes: |chef client| 12.5
=====================================================

.. include:: ../../includes_chef/includes_chef.rst

What's New
=====================================================
The following items are new for |chef client| 12.5 and/or are changes from previous versions. The short version:

* **Rename "resource attributes" to "resource properties"** One of the outcomes of `RFC-054 <https://github.com/chef/chef-rfc/blob/master/rfc054-resource-attribute-improvements.md>`__ is that |company_name| will be more clear about what a node attribute is versus a resource property. In previous releases of |chef|, resource properties are referred to as attributes. Starting with |chef client| 12.5 (and retroactively updated for all previous releases of the docs), "resource attributes" will now be referred to as "resource properties". This is a semantic change in the docs that makes it more clear for everyone---they should have been called "resource properties" originally---but otherwise does not change any workflows or break anything.
* **New way to build custom resources** The process for extending the built-in collection of resources in |chef| has been simplified. It is defined only in the ``/resources`` directory using a simplified syntax that easily leverages the built-in collection of resources. The ``/providers`` directory is no longer required.
* **The terms LWRP and HWRP are deprecated** The new way to refer to creating a custom resource is "custom resource" and the acronyms LWRP ("lightweight resource provider") and HWRP ("heavyweight resource provider") are deprecated. They are older, legacy terms that refer to specific ways of building custom resources. The current version of |chef| supports the older lightweight/heavyweight approaches, but adds additional ways of building custom resources.
* **ps_credential helper to embed usernames and passwords** Use the ``ps_credential`` helper to embed a ``PSCredential`` object---security credentials, such as a user name or password---in a script defined by the |resource dsc_script| resource.

.. https://github.com/chef/chef/pull/3776#issuecomment-135525399


``ps_credential`` Helper
-----------------------------------------------------
.. include:: ../../includes_resources/includes_resource_dsc_script_helper_ps_credential.rst

Custom Resources
-----------------------------------------------------
.. include:: ../../includes_custom_resources/includes_custom_resources.rst

.. note:: See https://docs.chef.io/custom_resources.html for more information about custom resources, including a scenario that shows how to build a ``website`` resource. Read this scenario as an HTML presentation at https://docs.chef.io/decks/custom_resources.html.

Syntax
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_custom_resources/includes_custom_resources_syntax.rst

.. include:: ../../includes_custom_resources/includes_custom_resources_syntax_example.rst


Changelog
=====================================================
https://github.com/chef/chef/blob/master/CHANGELOG.md
