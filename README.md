# Udacity Linux Server Configuration

This is a web server hosted by Amazon Lightsail that serves my **[Catalog App](https://github.com/pauloflah/Catalog-App/)** with Apache, mod_wsgi, and Python 2.

### Connection Information

**IP Address:** 18.222.61.145

**SSH Port:** 2200

**URL:** [http://18.222.61.145.xip.io/](http://18.222.61.145.xip.io/)

### Software Resources

* Flask
* SqlAlchemy
* Sqlite 3
* Apache 2
* mod_wsgi

### Third-Party Resources

PuTTY SSH Client was used to connect to the server. SSH keypairs were generated using the ssh-keygen command in the Linux terminal. puttygen from PuTTY Tools was used to convert the keys from OpenSSH format to the .ppk format.

### Summary of Configuration Changes Made

The grader user account was added to the server and given sudo privileges. Server was configured through UFW firewall and the Amazon Lightsail manager to only listen on ports TCP 80, 123, and 2200. The 000-default.conf file for Apache2 was modified to run a small .wsgi configuration file that launches the Catalog App. Catalog App was pulled down from GitHub, and slightly modified from the original with nano so that it could run on the server. Debugging was performed by reading through Apache2's error.log file.

### How to Use

Open the [URL](http://18.222.61.145.xip.io/) in your web browser. **[Catalog App](https://github.com/pauloflah/Catalog-App/)** is a web application that provides a catalog of items that users can modify with their Google+ or Facebook accounts.
