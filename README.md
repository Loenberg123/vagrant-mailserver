## Introduction

This repository creates a vagrant machine with postfix, dovecot, mysql, and various anti-spam and anti-virus tools.
Uses postfixAdmin to administer the db, and roundcube for webmail. It also uses Mailgraph for mail stats.

## Tests

Tested in an Ubuntu/trusty64 box

## How to use

Clone the repository and cd into it.

Then do vagrant up.

After this, go to yourdomain/posfixadmin/setup.php and follow the installer.

Run vagrant provision to set the admin user and password for postfixAdmin.

At last, setup roundcube going to yourdomain/installer and follow the instructions.

Roundcube db default values:
- dbname: roundcube
- dbuser: cubeuser
- dbpass: cubepass

Postfix db default values:
- dbname: servermail
- dbuser: usermail
- dbpass: mailpassword

Remember to edit the main.yml for your domain, and passwords, and the vagrantfile for your local net ip.
