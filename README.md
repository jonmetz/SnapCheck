Introduction
==============

This tool allows you to check who on your google contacts has been affected by the recent snapchat leak.
Note that you will need to download the mysqldump of the leak seperately and add it to MySQL.
There is plenty of documentation around the web on populating a database with a mysql dump, so I won't go into it here.

Since the last two digits of each phone number in the leak have been obfuscated there will usually be incorrect matches between your contacts' phone numbers and those
in the leak, because of this, when a match is detected the program will output the full name of your Contact as well as the username of the possible match, usually it
is fairly easy to determine if a match is in fact correct.

Configuration
==============
Aside from entering your google username and password, the only this needs configuration is for the mysql connection, on line 123 of contacts.py you should replace the
arguments to ```MySQLdb.connect``` with the appropriate values

Dependencies
==============

mysql-server

libmysqlclient-dev

python-pip

Once these packages are installed, run ```pip install -r requirements.txt``` to install the rest of the dependancies (note that this may require sudo).


Usage
==============

```python snapcheck.py --user username@gmail.com --password password```

Acknowlegements
================

This script recycled a large part of Google's contacts API example.
