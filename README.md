Introduction
============

Proxytop is a self contained real time monitoring tool for ProxySQL, a high performance, 
high availability, protocol aware proxy for MySQL and forks (like Percona Server and MariaDB).  

### How to install:

```
## You may first need to install system Python and MySQL dev packages 
## e.g. "sudo apt install python-dev libmysqlclient-dev"
pip install MySQL-python npyscreen
wget -P /usr/bin https://raw.githubusercontent.com/sysown/proxytop/master/proxytop
```

### How to run:

To connect to a local ProxySQL server configured with the default settings just run the file:
```
$ proxytop
```

The script supports connecting to a non-default confication using command line parameters:
```
usage: proxytop [-h] [-H HOST] [-P PORT] [-u USER] [-p PASSWORD] [-f DFILE]

optional arguments:
  -h, --help            show this help message and exit
  -H HOST, --host HOST  ProxySQL hostname / IP address (default=127.0.0.1)
  -P PORT, --port PORT  ProxySQL Admin port (default=6032)
  -u USER, --user USER  ProxySQL Admin username (default=admin)
  -p PASSWORD, --password PASSWORD
                        ProxySQL Admin password (default=admin)
  -f DFILE, --dfile DFILE
                        Use the MySQL defaults file specified (expects a
                        [proxysqladmin] group)
```

### Interactive shortcuts:

- The arrow keys and "tab" allow for navigating the menus
- "s" will change the sort order (available in Connection Pool and Query Rules views)
- "l" allows for filtering in the Query Rules view (specify full search term e.g. `rule_id: 1`)
- "+" or "-" to increase or decrease the refresh interval

### Other information:

- Scrolling is available in all views in case the lists exceed screen size
- The default interval for refresh is 1 second
- The Process List's minimum refresh interval is 5 seconds in order to avoid overloading ProxySQL Admin

![alt text](http://www.proxysql.com/assets/images/proxytop-sample.png)
