04-09-2022
---
# Multicasting
Multicasting consists of sending a message to multiple receivers, like for instance a live sporting event or a multiplayer game.
Sending individual packets can be expensive with many receivers, and broadcasting can lead to sending data to uninterested parties, or data seen by someone who shouldn't.

A *multicast routing* algorithm defines how to send data efficiently and securely to a small group in a larger network.

All multicasting schemes require a way to create and destroy groups, and some way of identifying which machines are members of a group, which are tasks of no concern to the routing algorithm.

## Working principle
Multicast routing sends data on *spanning trees* to deliver packets to all members while making *efficient use of bandwidth*.

Best spanning tree to use depends on whether the group is dense or sparse.

### Dense group
Broadcast is a good start, but this reaches some routers which are not part of the group. One solution is to prune links which do not lead to members. **MOSPF (Multicast OSPF)** and **DVMRP (Distance Vector Multicast Routing Protocol)** are some examples.

Building and pruning spanning trees can be expensive work for the routers of large networks. An alternative is to agree on a root (**core** or **rendeszvous point**) and build a tree by sending a packet from each member to the root, building a tree from the union of the paths traced by these packets.
This approach is obviously not optimal for all sources.