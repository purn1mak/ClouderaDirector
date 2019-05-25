# Instructions to install Google plugin for Cloudera Director.

Detailed information about plugin installation, and about the plugins that come pre-installed, is part of the Cloudera Director documentation. This section contains only an overview, and concentrates on information of interest to hot patch plugin authors.

Cloudera Director contains a directory for plugins. The user creates a subdirectory for each plugin. This subdirectory contains the plugin jar and an etc directory for additional filesystem-based plugin configuration information. Cloudera Altus Director will create an empty etc directory if it is absent.

A plugin author may want to provide an archive file which mirrors this structure and provides sample or starter configuration files in the nested configuration directory.

## Installing the plugin
Clone this git project and then move the jar file to the appropriate Director Google plugin location. 

Follow the following steps or DIY. 
Depending on what version of Director is installed your Google plugin directory will have a different version. In this example I am using Director 6.2.1 and the google plugin directory is /var/lib/cloudera-director-plugins/google-provider-2.0.3/


## Install git if its not installed already
sudo yum install git

### Get enhanced Director from Git.
cd ~
git clone https://github.com/purn1mak/ClouderaDirector.git

## Move jar file to google provider location.
cd /var/lib/cloudera-director-plugins/google-provider-2.0.3/  
sudo cp ~/ClouderaDirector/google-provider-2.1.0-SNAPSHOT.jar .   
sudo mv google-provider-2.0.3.jar ~/.   
sudo mv google-provider-2.1.0-SNAPSHOT.jar google-provider-2.0.3.jar   


## Stop Director
sudo service cloudera-director-server stop

## Start Director
sudo service cloudera-director-server start


# Important notice
Copyright © 2015 Cloudera, Inc. Licensed under the Apache License, Version 2.0.

Cloudera, the Cloudera logo, and any other product or service names or slogans contained in this document are trademarks of Cloudera and its suppliers or licensors, and may not be copied, imitated or used, in whole or in part, without the prior written permission of Cloudera or the applicable trademark holder.

Hadoop and the Hadoop elephant logo are trademarks of the Apache Software Foundation. Amazon Web Services, the "Powered by Amazon Web Services" logo, Amazon Elastic Compute Cloud, EC2, Amazon Relational Database Service, and RDS are trademarks of Amazon.com, Inc. or its affiliates in the United States and/or other countries. Google, Google Cloud Platform, GCP, Google Compute Engine, and GCE are registered trademarks of Google Inc. All other trademarks, registered trademarks, product names and company names or logos mentioned in this document are the property of their respective owners. Reference to any products, services, processes or other information, by trade name, trademark, manufacturer, supplier or otherwise does not constitute or imply endorsement, sponsorship or recommendation thereof by us.

Complying with all applicable copyright laws is the responsibility of the user. Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Cloudera.

Cloudera may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document. Except as expressly provided in any written license agreement from Cloudera, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property. For information about patents covering Cloudera products, see http://tiny.cloudera.com/patents.

The information in this document is subject to change without notice. Cloudera shall not be liable for any damages resulting from technical errors or omissions which may be present in this document, or from use of this document.
