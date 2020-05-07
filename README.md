# Foundryvtt-docker
Image based on foundryvtt based on node

Generate the dockefile with:

```doker build Dockerfile -t foundryvtt:${VERSION}```

Copy your options.json file inside 

```cp options.json /opt/foundrydata/Config/options.json```

Start the docker container mapping ports, certificate and configuration.

```docker run foundryvtt:${VERSION} -d /opt/foundrydata:/root/.local/share/FoundryVTT -d /opt/certificates:/root/certificates -p 5530:30000```

If you want set a password in the setup options. 
