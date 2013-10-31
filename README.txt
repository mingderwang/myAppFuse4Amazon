AppFuse Web Services Archetype
--------------------------------------------------------------------------------
If you're reading this then you've created your new project using Maven and
myAppFuse4Amazon.  You have only created the shell of an AppFuse Java EE
application.  The project object model (pom) is defined in the file pom.xml.
The application is ready to serve up web services with Enunciate and CXF. The
pom.xml file is pre-defined with Hibernate as a persistence model. To change it,
please read http://appfuse.org/display/APF/Persistence.

To get started, please complete the following steps:

1. Download and install a MySQL 5.x database from 
   http://dev.mysql.com/downloads/mysql/5.0.html#downloads.

   need to add username and password to pom.xml as follows;

        <!-- Database settings -->
        <dbunit.dataTypeFactoryName>org.dbunit.ext.mysql.MySqlDataTypeFactory</dbunit.dataTypeFactoryName>
        <dbunit.operation.type>CLEAN_INSERT</dbunit.operation.type>
        <hibernate.dialect>org.hibernate.dialect.MySQL5InnoDBDialect</hibernate.dialect>
        <jdbc.groupId>mysql</jdbc.groupId>
        <jdbc.artifactId>mysql-connector-java</jdbc.artifactId>
        <jdbc.version>5.1.22</jdbc.version>
        <jdbc.driverClassName>com.mysql.jdbc.Driver</jdbc.driverClassName>
        <jdbc.url>jdbc:mysql://localhost/${db.name}?createDatabaseIfNotExist=true&amp;amp;useUnicode=true&amp;amp;characterEncoding=utf-8&amp;amp;autoReconnect=true</jdbc.url>
        <jdbc.username>user</jdbc.username>
        <jdbc.password>password</jdbc.password>

2. Run "mvn jetty:run" and view the application at http://localhost:8080.

3. More information can be found at:

   http://appfuse.org/display/APF/AppFuse+QuickStart

