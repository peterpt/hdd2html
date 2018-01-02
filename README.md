# hdd2html
A tool for cloud administrators

# Screenshot
Screenshot from configured webpage in server
<img src="https://s14.postimg.org/uhz4wk7cx/hdd2html.png" width="50%"></img>

# How it works
I did this script because i was in need for it to use in my server .
hdd2html creates an webpage in user desired location and retrieve all data from pre-configured hard drives to that
created webpage .
Data as : Hard disk brand , total HDD space , free space , and will present a progress bar for visual .
user can add many partitions as it needs to hdd2html .
hdd2html autoinstall itself on user system on first run , but do not auto-configures itself .
For that , user must run after installation hdd2html -c to configure .
hdd2html does a loop every 10 minutes to check hard disks , and on every loop it will update the pre-configured webpage .
After the configuration , hdd2html will configure itself on rc.local file in /etc/rc.local , so it can run everytime
webserver starts or restarts .
I did it , so i dont need to remote shell my cloud server to monitor the HDD space left on server .
This way i can access this webpage remotely on my webserver http://myserver.com/somedir/space.html .

# How to install
- git clone https://github.com/peterpt/hdd2html.git
- cd hdd2html && ./hdd2html

after executing , it will be installed on /usr/local/sbin folder , and will create its work directory on :
- /usr/local/share/hdd2html

Note : Do not delete any file inside its working directory .

# To configure
hdd2html -c

# Instalation video
-will be next



