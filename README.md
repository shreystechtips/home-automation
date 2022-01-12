# home-automation
A collection of smart home setup configurations and scripts!


### Setting up port forwarding

A VM was created to connect as a proxy to the rpi:
Anyone --- GCP VM --- Rpi

NOTE on GCP Billing: Setting up the cloud instance can all be done Under [GCP free tier](https://cloud.google.com/free/docs/gcp-free-tier/#compute). Make sure to select `standard PD` when setting up the boot disk for the compute engine.

1. Rpi port to GCP 
    - Somehow ssh is port forwarded to the VM 

2. GCP port access
    - VM port <####> is opened for access to anyone under TCP using [this](https://stackoverflow.com/questions/21065922/how-to-open-a-specific-port-such-as-9090-in-google-compute-engine)
    - To test if the port can be accessed, serve a basic html page using [this](https://stackoverflow.com/questions/6084360/using-node-js-as-a-simple-web-server):
      - ```sudo apt-get install npm```
      - ```npx http-server -p 9090```
