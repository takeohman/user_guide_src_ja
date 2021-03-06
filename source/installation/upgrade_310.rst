###################################
3.0.6 から 3.1.0 へのアップグレード
###################################

アップグレードを行う前に、
index.phpファイルを静的ページに置き換えて、オフラインにする必要があります。

Step 1: CodeIgniter ファイルのアップグレード
============================================

*system/* ディレクトリのすべてのファイルとディレクトリを新しいものに置き換えてください。

.. note:: ユーザバージョンのファイルがディレクトリ内にある場合には、
	最初にそれらのコピーを取っておいてください。

Step 2: Check your PHP version
==============================

We recommend always running versions that are `currently supported
<https://secure.php.net/supported-versions.php>`_, which right now is at least PHP 5.6.

PHP 5.2.x versions are now officially not supported by CodeIgniter, and while 5.3.7+
may be at least runnable, we strongly discourage you from using any PHP versions below
the ones listed on the `PHP.net Supported Versions <https://secure.php.net/supported-versions.php>`_
page.

Step 3: If you're using the 'odbc' database driver, check for usage of Query Builder
====================================================================================

:doc:`Query Builder <../database/query_builder>` functionality and ``escape()`` can
no longer be used with the 'odbc' database driver.

This is because, due to its nature, the `ODBC extension for PHP <https://secure.php.net/odbc>`_
does not provide a function that allows to safely escape user-supplied strings for usage
inside an SQL query (which our :doc:`Query Builder <../database/query_builder>` relies on).

Thus, user inputs MUST be bound, as shown in :doc:`Running Queries <../database/queries>`,
under the "Query Bindings" section.
