Steps:
- set sysctl -w vm.max_map_count=262144 or in /etc/sysctl.conf set the value for permanent effect. this will resolve elastic search initialization error.
- in jenkins enable sonarqube scanner plugin in both tools and system tabs. 
ref: https://stackoverflow.com/questions/41064572/docker-elk-vm-max-map-count
- need to create docker group inside jenkins container with same id as host group of docker. (groupadd -g id docker)

docker installed through snap issue:
The output of readlink -f /snap/bin/docker pointing to /usr/bin/snap indicates that the Docker binary installed via Snap is actually a wrapper for the Snap command. This means the actual Docker binary isn't directly available at /snap/bin/docker.


