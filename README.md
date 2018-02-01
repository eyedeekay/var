# Whonix - I2P 
#### This Repo contains various files related to my Whonix-I2P Development/Porting
# Disclaimer!
This Repo is just a dumping ground for all sort of files, they may not work or/and could break your system !!
### ToDo:
- fix reseed using http://trac.i2p2.i2p/ticket/1130
- add proper logs and error handling
- fix tunnel build notification
- add autostart
- rework folders and script
- fix wrong foxyproxy version and/or replace it
- fix permissions
- find a way to access Plugin folder from Workstation
- ...
- create debian pckg
- msg whonix and find testers
As soon as everything works  I will delete this repo and create a proper one with instructions...
#### Note :
###			Currently it's working but still has some Issues, Bug reports/PR's welcome
## Testing/Setup
### [Qubes OS only]
- Clone your existing Whonix Gateway and Worksation Templates
- Download the Repo to your (cloned) Whonix GW Template
- Run `anon-i2p-gw-template-config` as root in the (cloned) Whonix GW template
- Wait until it finishes after that power down the TemplateVM and create a new ProxyVM (eg. sys-i2p) from 
the (cloned) Whonix GW Template.
- Start the ProxyVM (sys-i2p) and run `anon-i2p-gw-proxyvm-config` as root , reboot the ProxyVM (sys-i2p)
- Download the Repo to your (cloned) Whonix WS Template and run `anon-i2p-ws-template-config`
- Create a AppVM (eg. anon-i2p) and run `anon-i2p-ws-appvm-config` from the previusly Cloned Repo folder
- Now you can run `sudo i2p-launcher start &` on your ProxyVM (sys-i2p) to start the I2P Router
- Your AppVM (anon-i2p) Torbrowser (should) now forward any .i2p domain to i2p


`sudo tail -f /var/log/i2p/wrapper.log` for debuging

### Known Issues/Bugs

- currently disabled console port redirection to the Workstation ( use lynx or iceweasel on the GW to manage i2p or via config)
- DNS could give some Issues
- long startup time (just get a cup of coffee)


### More to come ...
