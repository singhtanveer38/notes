1.	Booted Debian 11 with root user and a non-root user was created.
2.	Non-root user was unable to execute commands with sudo as sudo was not found
3.	Logged into root using ```su```.
4.	Apt was unable to install anything, followed instructions in [errors.md](./errors.md) and [updates.md](./updates.md)
5.	Installed sudo
6.	Change user with ```su - useername
7.	```sudo``` won't work as the user is not in the sudoers file.
8.  Edit ```/etc/sudoers``` and add the following line ```username    ALL=(ALL:ALL) ALL```
