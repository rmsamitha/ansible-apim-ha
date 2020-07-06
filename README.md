# WSO2 API Management Ansible scripts
  ```
  git clone https://github.com/ruks/ansible-apim.git
  git checkout 3.2.0
  cd ansible-apim
  ```

## add hosts to the /etc/hosts
  ```
    192.168.114.33	apis.apim.com
    192.168.114.33	portals.apim.com
    192.168.114.33  db.apim.com
    192.168.114.33  tm.apim.com
    192.168.114.51  km.apim.com
    192.168.114.67  pub.apim.com
    192.168.114.80  dev.apim.com
    192.168.114.82  gw.apim.com
    192.168.114.87  analytics.apim.com
  ```

## logging to the particular VM 
  + ssh ubuntu@tm.apim.com -i files/keys/apim310.key
  + ssh ubuntu@km.apim.com -i files/keys/apim310.key
  + ssh ubuntu@pub.apim.com -i files/keys/apim310.key
  + ssh ubuntu@dev.apim.com -i files/keys/apim310.key
  + ssh ubuntu@gw.apim.com -i files/keys/apim310.key
  + ssh ubuntu@analytics.apim.com -i files/keys/apim310.key

## Distribution is installed in /mnt/apim-* directory
## Use services to stop/start/restart services ex:
  ```
sudo service wso2apim-tm start
sudo service wso2apim-km start
sudo service wso2apim-gateway start
sudo service wso2apim-publisher start
sudo service wso2apim-devportal start
sudo service wso2am-analytics-worker start
sudo service wso2am-analytics-dashboard start
  ```
 
## deploy and run ansible
``` 
    ansible-playbook -i dev site.yml
``` 

## Portals
``` 
    https://pub.apim.com:9443/publisher/apis
    https://dev.apim.com:9443/devportal/apis
    https://km.apim.com:9443/carbon
```
