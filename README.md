# Opentracker Server Startup Scripts (1.0.0)
Startup scripts for the Opentracker game server - uses the "screen" command to manage session. This also restarts the Opentracker server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/OpentrackerStartup) - [Official Forum](https://gameplayer.club/index.php/ourforum/9)

---
These start up the Opentracker server at boot time with a "screen" process.

1. Copy **opentracker** into **/etc/init.d** - make sure it is executable
2. Copy **startopentracker** into **/root/opentracker** - make sure it is executable
4. Run "**systemctl enable opentracker**" (only needed once, will stick)
5. Run "**systemctl start opentracker**" - starts Opentracker without restarting the server

When you want to view the Opentracker console, just enter "**screen -r**" in your shell.

To disconnect from the Opentracker console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/opentracker/nostart**". To reenable it type "**rm /root/opentracker/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
