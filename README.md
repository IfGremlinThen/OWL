# Open Wine Launchers
Open Wine Launchers ("OWL") is a collection of custom launch scripts for applications using Wine or Proton. 🦉

## Purpose
To provide a uniform method of launching Windows applications on Linux from any era using a portable compilation of Wine and/or Proton.

## How it works
This project assumes that you have a local folder containing a fully-functional release of Wine for 32-bit applications and Proton ([umu-launcher](https://github.com/Open-Wine-Components/umu-launcher)) for 64-bit applications.

`environment.sh` defines the paths to Wine and Proton and sets the environment variables which may be called by each application's `start.sh` script.  `start.sh` serves as both a launch command and a config setting the application's Wine prefix, launch flags, and other toggles specific to it's needs.

## Addendum
It is strongly recommended that Windows applications are launched alongside [opensnitch](https://github.com/evilsocket/opensnitch) to prevent them from dialing home.  To prevent a game from establishing an outgoing connection, create a rule _"from this executable"_ and set it to _"Reject"_.  Certain games (such as XCOM: Enemy Unknown) will wait until a network timeout before launching if the rule is set to _"Deny"_.
