 inWebo ForgeRock AM v5.5.1 Custom Authentication Module
 =======================================================
 
 Requirements
 ------------
 
 1. [ForgeRock AM 5.5.1](https://www.forgerock.com/platform/access-management)
 1. [Tomcat 8](http://apache.mediamirrors.org/tomcat/tomcat-8/v8.5.30/bin/apache-tomcat-8.5.30.tar.gz)
 1. [OpenJDK 1.8](http://openjdk.java.net/)
 
 Building from Source
 --------------------
 
 ```bash
$ ./mvnw -U -s .mvn/settings.xml clean package
 ```
 
 Installation
 ------------

1. copy Resource:

    ```bash
    $ sudo unzip iw-forgerock-am-*.zip -d /tmp/iw-forgerock-am
    $ sudo cp -R /tmp/iw-forgerock-am/edit-webapp/XUI/* /path/to/tomcat/webapps/openam/XUI/
    $ sudo cp /tmp/forgerock-am/edit-webapp/WEB-INF/lib/iw-forgerock-am-*.jar /path/to/tomcat/webapps/openam/WEB-INF/lib/
    $ sudo cp /tmp/forgerock-am/edit-webapp/WEB-INF/lib/idp-connector-auth-repackage-0.3.0.jar /path/to/tomcat/webapps/openam/WEB-INF/lib/   
    ```
4. restart tomcat.