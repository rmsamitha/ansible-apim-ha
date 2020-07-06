# WSO2 API Management Ansible scripts
  ``` toml
  git clone https://github.com/ruks/ansible-apim.git
  git checkout 3.1.0
  cd ansible-apim
  ```

## add hosts to the /etc/hosts
  ``` toml
    192.168.114.4	apis.apim.com
    192.168.114.4	portals.apim.com
    192.168.114.4	db.apim.com
    192.168.114.4	tm.apim.com
    192.168.114.25	km.apim.com
    192.168.114.40	pub.apim.com
    192.168.114.49	dev.apim.com
    192.168.114.54	gw.apim.com
    192.168.114.62	analytics.apim.com
    192.168.114.67	worker.apim.com
  ```

## logging to the particular VM 
  + ssh ubuntu@tm.apim.com -i files/keys/apim310.key
  + ssh ubuntu@km.apim.com -i files/keys/apim310.key
  + ssh ubuntu@pub.apim.com -i files/keys/apim310.key
  + ssh ubuntu@dev.apim.com -i files/keys/apim310.key
  + ssh ubuntu@analytics.apim.com -i files/keys/apim310.key
  + ssh ubuntu@worker.apim.com -i files/keys/apim310.key

## Distribution is installed in /mnt/apim-* directory
## Use services to stop/start/restart services ex:
  ```
sudo service wso2apim-tm start
sudo service wso2apim-km start
sudo service wso2apim-gateway start
sudo service wso2apim-publisher start
sudo service wso2apim-devportal start
  ```
 