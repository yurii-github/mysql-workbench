
# Yurii Comments

## Install

install `mariadb-client` or `mysql-client` or community client. I preffer to install server so
```
apt install mysql-community-server 
```

install JRE
```
apt install default-jre
```

install dev dependencies
```
apt install build-essential cmake autoconf automake pkg-config libtool libzip-dev libxml2-dev libsigc++-2.0-dev libglade2-dev libglu1-mesa-dev libgl1-mesa-glx \
mesa-common-dev  libmysqlcppconn-dev uuid-dev libpixman-1-dev libpcre3-dev libpango1.0-dev libcairo2-dev \
libboost-dev libsqlite3-dev swig libvsqlitepp-dev libgdal-dev libgtk-3-dev libgtkmm-3.0-dev libssl-dev libsecret-1-dev libproj-dev \
libssh-dev rapidjson-dev libantlr4-runtime-dev python3-dev
```

build

```
cd /home/yurii/Source/mysql-workbench-repo
mkdir wb-build
cd /home/yurii/Source/mysql-workbench-repo/wb-build
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr -DWITH_ANTLR_JAR=/home/yurii/Source/mysql-workbench-repo/antlr-4.9.1-complete.jar -Wno-dev ..
make
```

install
```
cd /home/yurii/Source/mysql-workbench-repo/wb-build
sudo make install
```

## Dev

TODO: read https://mariadb.com/kb/en/incompatibilities-and-feature-differences-between-mariadb-105-and-mysql-80/

---------------------------


# MySQL Workbench

Copyright (c) 2007, 2022, Oracle and/or its affiliates.

This is a release of [MySQL Workbench](https://mysqlworkbench.org), a graphical tool for working with MySQL servers and databases.

![Home screen on Windows](https://dev.mysql.com/doc/workbench/en/images/wb-home-screen-new.png)

License information can be found in the [License](License.txt) file.

This distribution may include materials developed by third parties. 
For license and attribution notices for these materials, please refer to the [License](License.txt) file. 

For more information on MySQL Workbench, visit 
  [http://dev.mysql.com/doc/workbench/en](http://dev.mysql.com/doc/workbench/en)

For additional downloads and the source of MySQL Workbench, visit
  [http://dev.mysql.com/downloads](http://dev.mysql.com/downloads)

MySQL Workbench is brought to you by the MySQL team at Oracle.

# Overview

[MySQL Workbench](https://mysqlworkbench.org) is a graphical tool for working with MySQL servers and databases. MySQL Workbench fully supports MySQL server versions 5.6 and higher.

MySQL Workbench functionality covers five main topics:

* **SQL Development:** Enables you to create and manage connections to database servers. Along with enabling you to configure connection parameters, MySQL Workbench provides the capability to execute SQL queries on the database connections using the built-in SQL Editor.

* **Data Modeling (Design):** Enables you to create models of your database schema graphically, reverse and forward engineer between a schema and a live database, and edit all aspects of your database using the comprehensive Table Editor. The Table Editor provides easy-to-use facilities for editing Tables, Columns, Indexes, Triggers, Partitioning, Options, Inserts and Privileges, Routines and Views.

* **Server Administration:** Enables you to administer MySQL server instances by administering users, performing backup and recovery, inspecting audit data, viewing database health, and monitoring the MySQL server performance.

* **Data Migration:** Allows you to migrate from Microsoft SQL Server, Microsoft Access, Sybase ASE, SQLite, SQL Anywhere, PostreSQL, and other RDBMS tables, objects and data to MySQL. Migration also supports migrating from earlier versions of MySQL to the latest releases.

* **MySQL Enterprise Support:** Support for Enterprise products such as MySQL Enterprise Backup, MySQL Firewall, and MySQL Audit.

![Performance dashboard](https://dev.mysql.com/doc/workbench/en/images/wb-performance-dashboard.png)

The [code repository on Github](https://github.com/mysql/mysql-workbench) is where we publish a snapshot of our internal repository everytime a new release of the product is published. Use the [MySQL bug system](http://bugs.mysql.com/) to report any issue you have. You can use Github or the MySQL bug system to contribute to the development. File a pull request on Github or a new issue on the MySQL Bug system with your patch and we will take care of it.
