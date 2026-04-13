## fixGDL
A simple Android app to fix Dynon's HDX GDL90 non-compliance: missing Heartbeat and Ownship messages.

Listens on port 4000 and retransmits locally (127.0.0.1) on port 43211.
* Missing Heartbeat is transmitted
* Bogus Traffic report for your ship (N342ME) modified to Ownship and transmitted
    * this removes the "ghost" traffic of your own ship
    * create the missing Ownship
* All other GDL90 messages are retransmitted without changes (Uplink for weather products, etc.)

### This is a work in progress; future ideas:
* make listen/transmit port/IP and own_ship callsign (or ICAO mode-S?) configurable soon.
* could add non-standard AHRS messages (stratux, iLevil) using Dynon protobuf or serial data as basis
  (but just an idea; I don't use/need a backup AHRS/PFD display).

See related/previous work: [GDL90 Tester](https://github.com/b-spatz/gdl90)
