Munin Plugins
=============
Plugins for Munin.

ffmap
-----
Load `nodes.json` from a ffmap aka a Freifunk Node Map and extract
number of nodes, active gateways, mesh connections and the like.

You can configure collections of personal nodes in munin plugin configuration, e.g. in `/etc/munin/plugin-conf.d/munin-node` by creating a new section ffmap like this:

```
[ffmap]
user nobody
env.nodesurl http://map.md.freifunk.net/nodes.json

env.pers_collection_n 2

env.pers_collection_1_name Netz39 e.V.
env.pers_collection_1_node_n 3
env.pers_collection_1_node_1_name Netz39
env.pers_collection_1_node_1_ids 12:fe:ed:ce:ae:be,10:fe:ed:cd:ae:be
env.pers_collection_1_node_2_name spielknoten
env.pers_collection_1_node_2_ids ea:94:f6:a2:1a:7a,e8:94:f6:a2:1a:7a
env.pers_collection_1_node_3_name Sonnenstudio
env.pers_collection_1_node_3_ids 24:a4:3c:d9:4d:28,26:a4:3c:d9:4d:28

env.pers_collection_2_name Seconde Group
env.pers_collection_2_node_n 1
env.pers_collection_2_node_1_name Some Node
env.pers_collection_2_node_1_ids e8:94:f6:4f:d3:28
```
