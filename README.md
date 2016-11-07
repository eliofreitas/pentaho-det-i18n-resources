i18n Resources Bundle Sample
============

Description
--------
This project describes a sample OSGI bundle with localization resources contributions/updates (this sample was based on
the pentaho-det project - https://github.com/pentaho/pentaho-det)
The properties files should be in the src/main/resources/i18n folder. You can specify a folder structure inside the main
i18n folder, which will represent the key for the properties file:
 e.g.: src/main/resources/i18n/sub1/sub2/message.properties correspondes to the key sub1.sub2.messages
To specify the properties file language use the java standard:
  <YOUR_PROPERTIES>.properties - Default properties file;
  <YOUR_PROPERTIES>_en.properties - EN properties file;
  <YOUR_PROPERTIES>_pt_PT.properties - PT Portugal properties file;
To update or fix existing properties files that already exist in the system you should specify a priority for the file.
The priority is specified in the file name, in the format <fileName>.properties.<proirity> where priority is a numeric value.
For instance, if you wish to update a properties file messages.properties that exists in the system, the bundle should
contain in the same folder structure as the system, a file with the name messages.properties.2.

Building
--------
$: mvn clean package

Installing
--------
1. Copy the generated jar file to the karaf/deploy folder which will automatically trigger the install.
Note: The karaf system shouldhave the pentaho-i18n-bundle installed

