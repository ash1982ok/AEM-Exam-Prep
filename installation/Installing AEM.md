#Installing AEM

Installation is available in two forms:
* A standalone executable jar file referred to as a quickstart file.
* A war file to be deployed in a third-party application server.


1) The quickstart jar file contains the full stack needed for AEM.

2) The war file version of AEM includes all of the same components, except that the HTTP service is delegated to the application server 
within which the war file is deployed.


#PREREQUISITES

* The Java Runtime Environment (JRE). Version 1.7 is preferred.
* The default installation of AEM (in either jar or war form) includes a built in persistent storage layer in which all content is ultimately stored. In some cases users may choose to re-configure AEM to use an external third-party database for storage. Any such database (e.g. MangoDB) must, of course, be installed separately from AEM.
* 3 GB free disk space
* 1.5 GB memory, If you are using AEM DAM, you must increase the heap size when starting AEM WCM.

#Installing an Author Instance

Port - 4502 

1) Create a directory and name it author.

2) Copy the cq5-<version>.jar file into author/ and copy a valid license.properties to the same folder.

3) Rename cq5-<version>.jar to cq5-author-p4502.jar.

4) Start AEM
    
    i) Double-click the cq5-author-p4502.jar file.
    
    ii) or Command line
        
        * 32bit VM type:
        java -Xmx1024M -jar cq5-author-p4502.jar
        
        * 64bit VM, type:
        java -XX:MaxPermSize=256m -Xmx1024M -jar cq5-author-p4502.jar

If you need a different port this can be set in the filename.
5) open url - http://localhost:4502/

#Installing an Publish Instance

Use the same procedure as in Author only change port number and name to publish i.e. cq5-publish-4503.jar
