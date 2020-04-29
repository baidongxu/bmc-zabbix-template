# bmc-zabbix-template
get status(power,thermal),detail of hardware(cpu,memory,storage,pci card),software(bmc,bios,driver) of servers(hp,dell,inspur) through zabbix template
Template xxx Warn.xml is the template to get status of the server and trigger if there is warning.
Template xxx Configuration is the template to get hardware and firmware detail of the server and trigger if there is thermal warning.
these data will be store in zabbix database,and you can fetch them into mysql database to show.

steps to setup:
1 setup zabbix4
2 configure the macro and value mapping as shown in the picture macro.png and zbx_export_valuemaps.xml
3 import template
4 define a host
5 link the template to the host
6 see monitoring -> latest data
7 you can change the interval if you apply the template into production,default interval is 5 minutes 
