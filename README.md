## fixgdl
A simple Android app to fix Dynon's HDX GDL90 non-compliance: missing Heartbeat and Ownship messages.

Alpha version here, there be dragons.

Listens on port 4000 and retransmits locally (127.0.0.1) on port 43211.
* Missing Heartbeat is transmitted
* Bogus Traffic report for your ship (N342ME) modified to Ownship and transmitted
    * this removes the "ghost" traffic of your own ship
    * create the missing Ownship
* All other GDL90 messages are retransmitted without changes (Uplink for weather products, etc.)

This is a work in progress; will make listen/transmit/own_ship configurable soon.
