## linux-power-control
Simple server to remotely shutdown or restart your linux machine via post requests.


## Setup

1. Edit the port number in `config.json` to the port you want the server to listen on.


2. Edit `linux-power-control.service` with the correct path and username. Then copy it to SystemD service directory. EX `cp linux-power-control.service /etc/systemd/system/` then run `sudo systemctl daemon-reload` followed by `sudo systemctl enable linux-power-control.service` and `sudo systemctl start linux-power-control.service` to enable it to run on boot.
 

 ## Usage

 You can sent post requests to `http://YOURIP:PORT` in the form of `{"command": "off/reboot"}`to reboot or shutdown the system. I use this in my other project [Nezuko](https://github.com/callmekory/nezuko)
 to restart my VM's and other computers.