# Info

Forked from Nextcloud official examples

**Make sure to randomize the passowrd in db.env!!**


## Fix HTTPS issues

Since Nextcloud runs behind reverse proxy, it thinks its running on HTTP and some functionalities like Windows Sync will break.

To fix that, go to the app container -> config/config.php and add/change these two arguments accordingly.

 ```php
 'overwrite.cli.url' => 'https://nextcloud.mydomain.com',
 'overwriteprotocol' => 'https',
 ```
