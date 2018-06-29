# PLC Common Objects

Commonly-used objects for Rockwell PLCs

## Watchdog

*Sets up two-way handshaking between an external device and the PLC.*

This routine expects that the external device sets the tag `watchdog_INT` to a randomly generated integer. The PLC will then subtract 1 from the random number and write it back to `watchdog_INT`. If the value does not get randomly set for 3 minutes, the PLC will set the `watchdogTimeout` tag to `True`.

## NTP

*Fetches the current time from an NTP server and sets the PLC time accordingly.*

Based on code provided by Rockwell Automation.
