# cron-mysqlbackup
A simple bash script to backup mysql databases in 4 different folders, every time the script run remove the older folder and create a new one.


<b>USAGE</b>

Replace those parameters with yours:

USER="mysql user"

PASSWORD="mysql password"

OUTPUT="full path to the folder where to save the backups es: /home/user/mysqlbackupfolder/"

MYSQL="full path to the mysql executable es: /etc/mysql/bin/mysql"

MYSQLDUMP="full path to the mysqldump executable es: /etc/mysql/bin/mysqldump"


<b>CRONJOB</b>

If you want to run the script every add the script to crontab, 

run: crontab -e

in that case I run the script at 23pm every 2 days

0 23 */2 * * /bin/sh /PATH_TO_SCRIPT/mysqlbackup.sh
