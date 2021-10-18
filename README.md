# SWDEVSETUP

## Cloning the LIVE System

If you want to create a development System for your Shopware 5 shop, 
you have to copy all your project files into a sub directory like "/_dev/" via console.
There are two ways to handle that with better performance than copying it with WinSCP.
One is copying it with rsync and the other is via the basic cp command.

> I only used the basic cp command, i guess rsync would be faster!

Here is the command to copy the live system into a sub dir
```
cp -ra `ls -A | grep -v "_dev"` _dev/
```
Maybe your /_dev/ dir doesn't have access rights at this point, so check for it with ls -la command, if the dir doesn't have it extend the rights with
```
chmod +x _dev/
```

At this point you need to copy your live database and you edit your config.php in the Shopware 5 Project Folder and add your dev database credentials
