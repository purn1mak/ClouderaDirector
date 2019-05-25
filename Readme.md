# Instructions to use Google plugin for Cloudera Director.

Clone this git project and then move the jar file to the appropriate Director Google directory.

Follow the following steps or DIY.

*Install git
sudo yum install git

* Get enhanced Director from Git.
git clone https://github.com/purn1mak/ClouderaDirector.git

* Move jar file to google provider location.
cd /var/lib/cloudera-director-plugins/google-provider-2.0.3/
sudo cp ~/ClouderaDirector/google-provider-2.1.0-SNAPSHOT.jar .
sudo mv google-provider-2.0.3.jar ~/.
sudo mv google-provider-2.1.0-SNAPSHOT.jar google-provider-2.0.3.jar


* Stop Director
sudo service cloudera-director-server stop

* Start Director
sudo service cloudera-director-server start
