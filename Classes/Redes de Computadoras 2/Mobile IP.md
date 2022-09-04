04-09-2022
---
# Mobile IP - Routing for Mobile Hosts
A mobile host is any device that is used in either a *truly mobile situation*, like in a moving car or train, or in a *nomadic situation*, like a laptop that is used in a series of different locations.

These devices need to stay connected anywhere they go, main complication: to route a packet to a mobile device, *the network has to find it first*.

>The goal is to make it possible to send packets to mobile hosts using their fixed home addresses and have the packets efficiently reach them wherever they may be. The trick, of course, is to find them.

New routes could be computed for each new connection, but that would lead to endless calculations.
Another alternative os to add mobility above the network layer, like a new login on an app, but new connections would have to be established anyways. Adding network-layer mobility fixes this problem.

## Working principle
The basic idea is for the mobile host to tell a host at the home location where it is now. This host , called the *home agent*, receives packets meant for the mobile host and, once it knows its current location, forwards them so they are delivered.

### Walkthrough
The mobile host first needs to get a local address, called a *care of address*. Then it can tell the home agent where it is currently located by sending a registration message with the care of address. 

Next, a sender sends a packet to the mobile host, which is routed to its home location. Because the mobile host is not home, the message is intercepted by the home agent and *encapsulated* with a new header and sent to the care of address. This is called *tunneling*.

When the encapsulated packet arrives, the mobile host unwraps it and receives the message. The mobile host can the reply to the sender directly, and the sender can learn of the care of address, with subsequent packets being sent over a tunnel to the care of address.

The overall route is called *triangle routing*. 

An important detail omitted is security. Packets may be checked for validity and tunnels can be encrypted by encrypting the encapsulated packet as part of the wrapping process.