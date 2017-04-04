# Tomcat docker images

$CATALINA_HOME `/usr/local/tomcat`

## Versions

### 6-jre6

* Tomcat 6.0.35

## Run app

```
docker run -d \
  -v /path/to/your/webapps:/usr/local/tomcat/webapps \
  -p 8080:8080 \
  alteom/tomcat
```
