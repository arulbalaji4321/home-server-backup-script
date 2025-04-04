###### crontab setup:

sudo crontab -e

select your desired text editor

then add this below line at the end of the crontab file

0 0 * * SUN /usr/bin/sudo /home/arul/back-up-script/backup-server


###### Explaination:

* * * * *
│ │ │ │ │
│ │ │ │ └── Day of the week (0 - 6) (Sunday = 0)
│ │ │ └──── Month (1 - 12)
│ │ └────── Day of the month (1 - 31)
│ └─────── Hour (0 - 23)
└───────── Minute (0 - 59)



0 0 * * SUN:

    0 minute: The job runs at the 0th minute (on the hour).

    0 hour: The job runs at midnight (00:00).

    * day of the month: This means it can run on any day of the month (not restricted).

    * month: This means it can run in any month.

    SUN: The job runs only on Sundays (which are represented by 0 or SUN in cron).


