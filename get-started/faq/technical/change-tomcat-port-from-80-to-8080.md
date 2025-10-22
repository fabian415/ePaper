# Change Tomcat Port from 80 to 8080

1. 打開終端機，轉換工作目錄到 /opt/advantech/epd/etc/tomcat
2. 使用 nana 編輯器修改 server.xml 為以下內容:

```
sudo nano server.xml
```



3. 打開防火牆設定，新增 8080 阜號

```
sudo ufw allow 8080
```

