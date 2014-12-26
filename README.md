splunk-elasticsearch
====================

I have created a small search command for Splunk which will allow you to search Elastic Search and display the results in the Splunk GUI


This project is now a valid splunk application and installs as you would any other splunk applications

Steps to use
Install python if it is not installed

Install ElasticSearch https://github.com/elasticsearch/elasticsearch-py
"pip install elasticsearch "

git clone "This Project"
rsync -av splunk-elasticsearch $SPLUNK_HOME/etc/apps

Now you should be able to do a simple search like 

| esearch oldest=now-40d earliest=now limit=1000 index=nagios* | search *SOMETHING*" 

