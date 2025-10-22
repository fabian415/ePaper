# Change Tomcat Port from 80 to 8080

1. 打開終端機，轉換工作目錄到 /opt/advantech/epd/etc/tomcat
2. 使用 nana 編輯器修改 server.xml 為以下內容:

```
sudo nano server.xml
```

<figure><img src="../../../.gitbook/assets/未命名 (1).png" alt=""><figcaption></figcaption></figure>

3. 打開防火牆設定，新增 8080 阜號

```
sudo ufw allow 8080
```

<div align="left"><figure><img src="../../../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure></div>

4. 重啟 Tomcat 服務

```
sudo systemctl stop epd-tomcat
sudo systemctl start epd-tomcat
```

5. 重啟 Service Monitor，並更改 Service Monitor 在 Tomcat 連線上的設定

<pre><code><strong>sudo pm2 stop epd-server-monitor
</strong><strong>sudo SERVER_CONFIG="/opt/advantech/epd/etc/epd" SCRIPT_ROOT_PATH="/usr/local/EPD" SERVICE_PORT="8090" TOMCAT_PORT="8080" RABBITMQ_PORT="15672" pm2 start /usr/local/apps/epd-server-monitor/server/index.js --name epd-server-monitor --max-memory-restart 200M
</strong></code></pre>

<figure><img src="../../../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure>
