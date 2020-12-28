# zabbix-nextcloud
### Monitoring Nextcloud 20.0.3 with Zabbix 5.2.

1. Define the Nextcloud user and domain in the `nextcloud.conf` file. The user must be in the Nextcloud `admin group`.

2. Install the `curl` and `jq` package on the host that has the zabbix-agent installed.

3. Insert the `nextcloud.conf` file on the host that has zabbix-agent installed in the `/etc/zabbix/zabbix_agentd.conf.d/` directory and `restart` the service.

4. Import the `zbx_export_templates.yaml` template into the zabbix server.

5. Create the Host on the zabbix server and associate the `Nextcloud` template.

5. Add an additional Macro on the host created in step 5, with the name `{$NCPW}` and the user password Nextcloud in the `Value` field.

#### Note: 
In the nextcloud.conf file you will have 4 configuration options.

1. Project with a certificate signed by a certification authority and par with JQ

2. Project with certificate signed by a certification authority and par with PYTHON3

3. Project with self-signed certificate and par with JQ

4. Project with self-signed certificate and parse with PYTHON3
