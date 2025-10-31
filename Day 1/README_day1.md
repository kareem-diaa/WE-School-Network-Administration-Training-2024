# Day 1 – Configuring a Cisco Network Switch using PuTTY

## Overview
This lab introduced the fundamentals of Cisco switch configuration using the console interface (PuTTY). The goal was to establish device access, secure administrative privileges, and configure basic system settings.

## Objectives
- Establish console connection using PuTTY.
- Configure device hostname and security settings.
- Set up console and privileged EXEC passwords.
- Encrypt passwords and set a Message of the Day banner.
- Save configuration to NVRAM.

## Steps Overview
1. Connect to the switch using the console port and PuTTY.
2. Enter privileged EXEC mode.
3. Configure hostname and security credentials.
4. Encrypt all passwords and set a login banner.
5. Save configuration using `copy run start`.

## Key Commands
```bash
enable
configure terminal
hostname S2
banner motd #
service password-encryption
enable secret cisco123
line console 0
password cisco
login
copy running-config startup-config
````

## Verification

* Check hostname and banner display on login.
* Run `show running-config` to confirm saved settings.
* Disconnect and reconnect via console to verify password prompts.

## Outcome

Switch successfully configured with secure access, hostname, and login banner. Learned basic navigation and configuration of Cisco IOS using console commands.

## Notes

* Always secure privileged EXEC mode with an encrypted password.
* Save frequently to avoid losing configuration after reload.
