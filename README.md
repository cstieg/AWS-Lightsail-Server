# AWS-Lightsail-Server

## Configuration Details
* IP Address: 34.204.85.30
* SSH Port: 2200
* URL: http://34.204.85.30/

## Summary of Installation
* Created virtual instance of Ubuntu server with Amazon Lightsail
* Upgraded packages to be up to date
* Changed SSH port from 22 to 2200 and allowed a corresponding custom port on the Lightsail account
* Changed firewall on server to default to deny incoming and allow only 80 (www), 2200 (ssh) and 123 (ntp).  Default to allow outgoing and activated firewall.
* Created user grader and added to sudoers file.  Created a key pair and added the public key to authorized_keys
* Installed Flask for Python to run app
* Installed Git, cloned Item Catalog respository to the server
* Installed Apache server, directed server to point to WSGI file which calls the Flask app
* Installed PostgreSQL, created user 'catalog'.  Created database 'catalog' and created tables and indexes using an SQL file
* Updated database connection info in database.py
