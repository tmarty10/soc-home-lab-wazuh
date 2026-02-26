Notes: 

-Ubuntu version: Ubuntu 24.04.4 LTS

-VM specs: 6GB Ram , 1 Processor , 4 Cores

-Network mode: NAT

-Install Command:   Install Script = curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh     
                    Download Script = (original) sudo bash wazuh-install.sh -a  ----->  (adjusted) sudo bash ./wazuh-install.sh -a -i

-Time install took: 15 mins

-Issues:

  -incompatibility with wazuh and my ubuntu version
     
      Changed command to ignore compatibility: sudo bash ./wazuh-install.sh -a -i
              - added ./ to target specific file in folder and -i to ignore the unexpected verion


Terminal during install
![Wazuh Install](ubuntu-screenshots/wazuh-install.png)

Wazuh Download
![Wazuh Download](ubuntu-screenshots/wazuh-download.png)

Confirm Services Running
![Wazuh Dashboard Running](ubuntu-screenshots/wazuh-dash-running.png)
![Wazuh Manager Running](ubuntu-screenshots/wazuh-manager-running.png)

Wazuh IP
![Wazuh IP Address](ubuntu-screenshots/wazuh-ip.png)

Waszuh dashboard
![Wazuh Dashboard](ubuntu-screenshots/wazuh-dashboard.png)









