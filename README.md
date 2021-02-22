# zabbix-barman

This repository contains a Zabbix template (tested on Zabbix 5.0)
to monitor PostgreSQL Barman. It only requires a single user parameter
on the Barman node, everything else is done in Zabbix item preprocessing.

It discovers all configured backups and checks their complete status.

## Installation

- add the given line to your sudoers file/sudoers.d directory
- copy the userparameter to your zabbix configuration
  (usually just in `/etc/zabbix/zabbix_agent2.d/`)
- restart zabbix-agent2
- Import template-barman.xml in your Zabbix Server
- Link the template `Template DB PostgreSQL Barman` to your Barman server

## Requirements

This was developed/tested on Zabbix 5.0, Barman 2.12 and PostgreSQL 12.

Presumably other versions will work, but might be a bit different from this.
