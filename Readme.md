## Geoserver.zip Hochladen

```
sudo -i
adduser geoserver
usermod -aG sudo geoserver
exit
ssh geoserver@deine_Hompage

```

* [Download](https://geoserver.org/release/stable/)

* scp Geoserver.zip geoserver@deine_Hompage.de:Geoserver.zip
* ssh geoserver@ahrensburg.city
* git clone https://github.com/thorstenkloehn/geoserver.git .
* sudo cp -u geoserver.deb /etc/init.d/geoserver
* sudo chown -R geoserver .
* sudo chmod a+x /etc/init.d/geoserver
* /etc/init.d/geoserver start

## Geoserver Einstellung
```
nano /home/geoserver/webapps/geoserver/WEB-INF/web.xml

Zeile hinzufügen


<context-param>
  <param-name>GEOSERVER_CSRF_WHITELIST</param-name>
  <param-value>example.org</param-value>
</context-param>

```

