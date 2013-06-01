
Description
===========

This library provides helper classes for writing plugins for the server
monitoring tool Munin. It also comes with some prebuilt plugins for
various services including PostgreSQL, Memcached, and Nginx.

Installation
------------

Sample installation on Debian distribution

**dev base requirement**

.. code-block:: console

  apt-get install python-pip git

**Install python-munin**

.. code-block:: console

  cd /usr/local/src/
  git clone https://github.com/samuel/python-munin.git
  pip install python-munin/

**Sample activation plugin** (ex: mysql_replication)

.. code-block:: console

  apt-get install python-mysqldb
  cd /etc/munin/plugins
  ln -s /usr/local/src/python-munin/plugins/mysql_replication mysql_replication
  vi /etc/munin/plugin-conf.d/mysql_replication # edit options
  /etc/init.d/munin-node restart
