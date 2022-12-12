1. new bridge and overlay netwroks can be created 
command : docker network create --driver=bridge name

docker network create --driver=bridge --subnet=172.99.11.0/24 --gateway=172.99.11.1 new_bridge_2

[root@ip-172-31-11-240 ~]# docker network inspect new
[
    {
        "Name": "new",
        "Id": "21fcc76093e7f489d319798c23766d51684c46655c0a838d773573572649961f",
        "Created": "2022-12-12T12:51:22.457358321Z",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": {},
            "Config": [
                {
                    "Subnet": "172.19.0.0/16",
                    "Gateway": "172.19.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {},
        "Options": {},
        "Labels": {}
    }
]




----------------------
multiple new net. can be created 
network can be added or removed from containers without the need to restart 
- in multi network , external connectivity from the fitst netwreok 
- --------------
remove network 
docker network rm host
Error response from daemon: host is a pre-defined network and cannot be removed
------------------------------
