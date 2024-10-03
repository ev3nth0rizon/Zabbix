# Zabbix Inventory for Zabbix Active Agent 2
Updated SpookOz's Powershell script for Zabbix Active Agent 2
Original author - https://github.com/SpookOz

Updates: 
1) Adapted for Zabbix Active Agent 2 (tested only on 7.0.3 agents and server)
2) corrected taking Hostname directly from .conf file


Keys for zabbix_agent2.conf:
AllowKey=system.run[powershell.exe -NoProfile -ExecutionPolicy Bypass -file "$Env:Programfiles\Zabbix Agent 2\zabbix_agent2.d\plugins.d\get-inventory.ps1" -nowait]
AllowKey=system.run[powershell.exe -NoProfile -ExecutionPolicy Bypass -command Invoke-WebRequest -Uri https://clck.ru/3Desqa -OutFile '$env:Programfiles\Zabbix` Agent` 2\zabbix_agent2.d\plugins.d\get-inventory.ps1']
DenyKey=system.run[*]
