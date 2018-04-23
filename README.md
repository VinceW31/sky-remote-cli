# Summary

This project is still under development.

This project is a fully documented (for basic user easy install) installation for controlling a UK SkyHD box with Google home/Mini via a Raspberry Pi.  

It contains all the steps and files necessary to complete the project from end to end.  In order to complete this project you will need:
Google Home/Mini device (or Google Assistant on your phone will do).
Raspberry Pi.
Blank SD card 8Gb for Raspberry Pi.
SkyHD Box.
Internet connection.

The project uses the Google Home/Mini assistant to capture your voice command, this is then sent automatically to IFTTT (you will need to set up a free account) which detects certain keyword triggers and then sends commands back to your Raspberry Pi to excecute the remote commands directly to your SkyHD box.  

# No-IP.com

Text here

# IFTTT

Text here

# Raspberry Pi

Text here

# Install sky-remote-cli & Python program

Text here

A command line app to send remote control commands to a Sky TV box. Compatible with Sky+HD and Sky Q.

## Usage

#### Installation

You'll need to install this globally with the `-g` flag.

```
npm install -g sky-remote-cli
```

#### Controlling a Sky TV box

The first argument must be the IP address of the Sky box you want to control. All arguments after that are commands to send to the box - you can send just one command or many at once (they will be sent in sequence). If connecting to a Sky Q box running formware older than v0.60, pass the `--sky_q_legacy` flag. The previously used `--sky_q` flag now has no impact (but is still accepted for compatability).

###### Turn the box on / off
```
sky-remote-cli 192.168.0.40 power
```

*or, for Sky Q (with older firmware <0.60):*

```
sky-remote-cli --sky_q_legacy 192.168.0.40 power
```

###### Channel up, pause, show info
```
sky-remote-cli 192.168.0.40 channelup pause i
```

###### Change channel to 101
```
sky-remote-cli 192.168.0.40 1 0 1
```

#### Remote control commands

`sky` `power`

`tvguide` or `home` `boxoffice` `services` or `search` `interactive` or `sidebar`

`up` `down` `left` `right` `select`

`channelup` `channeldown` `i`

`backup` or `dismiss` `text` `help`

`play` `pause` `rewind` `fastforward` `stop` `record`

`red` `green` `yellow` `blue`

`0` `1` `2` `3` `4` `5` `6` `7` `8` `9`


## See also

- http://github.com/dalhundal/sky-remote - The underlying Node module used by this tool
- http://github.com/dalhundal/sky-q - A Node module for interacting with Sky Q boxes
