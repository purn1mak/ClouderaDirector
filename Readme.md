# Instructions to install Google plugin for Cloudera Director.

Detailed information about plugin installation, and about the plugins that come pre-installed, is part of the Cloudera Director documentation. This section contains only an overview, and concentrates on information of interest to hot patch plugin authors.

Cloudera Director contains a directory for plugins. The user creates a subdirectory for each plugin. This subdirectory contains the plugin jar and an etc directory for additional filesystem-based plugin configuration information. Cloudera Altus Director will create an empty etc directory if it is absent.

A plugin author may want to provide an archive file which mirrors this structure and provides sample or starter configuration files in the nested configuration directory.

## Installing the plugin
Clone this git project and then move the jar file to the appropriate Director Google plugin location. 

Follow the following steps or DIY.

## Install git if its not installed already
sudo yum install git

### Get enhanced Director from Git.
git clone https://github.com/purn1mak/ClouderaDirector.git

## Move jar file to google provider location.
cd /var/lib/cloudera-director-plugins/google-provider-2.0.3/  
sudo cp ~/ClouderaDirector/google-provider-2.1.0-SNAPSHOT.jar   
sudo mv google-provider-2.0.3.jar ~/.   
sudo mv google-provider-2.1.0-SNAPSHOT.jar google-provider-2.0.3.jar   


## Stop Director
sudo service cloudera-director-server stop

## Start Director
sudo service cloudera-director-server start
