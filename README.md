# DBeaver Community Edition for Apache Cassandra

## DBeaver Community Edition

### DBeaver - Universal Database Tool
#### DBeaver Community is a free & open source cross-platform database tool for developers, database administrators, analysts, and everyone working with data. It supports all popular SQL databases like MySQL, MariaDB, PostgreSQL, SQLite, Apache Family, and more.
#### but unfortunately, DBeaver Community Edition DOES NOT support Apache Cassandra

### let us now see how to use DBeaver Community Edition with Apache Cassandra

---

## download DBeaver Community Edition

#### download : https://dbeaver.io/files/dbeaver-ce-latest-win32.win32.x86_64.zip

#### extract the above downloaded zip file
#### we do NOT need to install - just extract and run

##### I stored this software in ` C:\Software\DBeaver2320\ `
##### I can start running DBeaver by running ` C:\Software\DBeaver2320\dbeaver.exe `

<br>

#### on 16-Sep-2023 - I am using ` DBeaver Community version 23.2.0 ` it was released on ` 04-Sep-2023 `.
##### ` dbeaver-ce-23.2.0-win32.win32.x86_64.zip ` is nearly ` 117 MB ` in size.

![DBeaver_01.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_01.jpg)

---

## cassandra-jdbc-wrapper by ing-bank

#### Cassandra JDBC wrapper for the Datastax Java Driver for Apache Cassandra

#### go to https://github.com/ing-bank/cassandra-jdbc-wrapper/releases/latest
#### under Assets download ` cassandra-jdbc-wrapper-<version>-bundle.jar `

#### on 16-Sep-2023 - I am using ` cassandra-jdbc-wrapper-4.9.1-bundle.jar ` it was released on ` 03-Sep-2023 `.
##### ` cassandra-jdbc-wrapper-4.9.1-bundle.jar ` is nearly ` 17 MB ` in size.

##### I stored this JAR file in ` C:\Software\DBeaver2320\customDrivers\ `

---

## DBeaver + JDBC driver

#### in DBeaver : go to -> Menu -> Database -> Driver Manager -> New ->

![DBeaver_02.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_02.jpg)

#### go to -> Libraries Tab -> Add File -> select "cassandra-jdbc-wrapper-<version>-bundle.jar"

![DBeaver_03.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_03.jpg)

#### go to -> Settings Tab -> configure following :
```
  Driver Name : Apache Cassandra
  Driver Type : Generic
  Class Name  : com.ing.data.cassandra.jdbc.CassandraDriver
```
#### click OK and close the "Create new driver" dialog.

![DBeaver_04.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_04.jpg)

#### click Close to close the "Driver Manager" dialog.

![DBeaver_05.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_05.jpg)

---

## DBeaver connect to Cassandra Cluster

#### in DBeaver : go to -> Menu -> Database -> New Database Connection ->
#### select "Apache Cassandra" -> click "Next >" ->

![DBeaver_06.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_06.jpg)

#### fill in the details :
```
JDBC URL format : jdbc:cassandra://[Host]:[Port]/[keyspace]?localdatacenter=[DC_Name]

Authentication : Username & Password
```
#### click "Test Connection ..."

![DBeaver_07.jpg](https://github.com/sarma1807/DBeaver_for_Cassandra/blob/main/images/DBeaver_07.jpg)
