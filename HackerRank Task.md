
 RunLevels in Debian
 -----------------------
 We will be talking about SysV-style init systems ,it is the traditional one used in older Debian versions before systemd became the default.
So, In Debian-based systems using the SysV init system, runlevels determine the state of the machine and the services that should be running. Each runlevel corresponds to a specific system mode, and different scripts are executed depending on the runlevel.

RunLevels

| RunLevel | Description                                                                  |
| -------- | ---------------------------------------------------------------------------- |
| 0        | Halt the system >> Shutdown.                                                 |
| 1        | Single-user mode >> maintenance.                                             |
| 2        | Multi-user mode without networking >>Debian default multi-user runlevel.     |
| 3        | Multi-user mode with networking >> commonly used in other distros like RHEL. |
| 4        | Unused/custom >> available for user-defined purposes.                        |
| 5        | Multi-user with graphical environment.                                       |
| 6        | Reboot.                                                                      |
something to consider:-
--------------------------
On Debian systems, runlevel 2 is usually configured the same as 3, 4, and 5 — it's up to the admin to differentiate them if needed.


Runlevel Scripts
------------------
Runlevel scripts are located in: /etc/rcX.d/ (where X is the runlevel number). These directories contain symbolic links to scripts in /etc/init.d/ .

- Scripts starting with "S" are started.
- Scripts starting with "K" are killed (stopped).

by bash scripting you can check and change runlevel.
Examples:
- `/etc/rc2.d/S01networking` will start the networking service in runlevel 2.

- Check current runlevel: `runlevel`.

- Change runlevel: `init 3`.

- Reboot: `init 6`.

- Shutdown: `init 0`.

-------------------------------------------------------------------------------

|     |     |     |
| --- | --- | --- |
|     |     |     |
|     |     |     |
