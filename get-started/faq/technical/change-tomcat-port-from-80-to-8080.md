# Change Tomcat Port from 80 to 8080

1. Open a terminal and navigate to the Tomcat configuration directory: /opt/advantech/epd/etc/tomcat

```
cd /opt/advantech/epd/etc/tomcat
```

2. Edit `server.xml` using the `nano` editor and update it with the required configuration:

```
sudo nano server.xml
```

<figure><img src="../../../.gitbook/assets/未命名 (1).png" alt=""><figcaption></figcaption></figure>

3. Update the firewall settings to allow traffic on port 8080

```
sudo ufw allow 8080
```

<div align="left"><figure><img src="../../../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure></div>

4. Restart the Tomcat service

```
sudo systemctl stop epd-tomcat
sudo systemctl start epd-tomcat
```

5. Restart the Service Monitor and update its configuration to match the new Tomcat port

<pre><code><strong>sudo pm2 stop epd-server-monitor
</strong><strong>sudo SERVER_CONFIG="/opt/advantech/epd/etc/epd" SCRIPT_ROOT_PATH="/usr/local/EPD" SERVICE_PORT="8090" TOMCAT_PORT="8080" RABBITMQ_PORT="15672" pm2 start /usr/local/apps/epd-server-monitor/server/index.js --name epd-server-monitor --max-memory-restart 200M
</strong></code></pre>

<figure><img src="../../../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure>
