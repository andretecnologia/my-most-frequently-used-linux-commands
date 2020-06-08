# My most frequently used linux commands


```
sudo find / -size +1G
```


```
lsof -w -n -i tcp:8080
```


```
kill -9 pid _number
```


```
ps aux | grep -i vim
```


```
lsof -i:8080
```


```
crontab jobs
```


```
ncdu df -h df-l espadrilles em disco
```


```
Find / -type f -size +50M -exec du -h {} \; sort -n
```


```
nmon
```


```
nmtui
```


```
sudo update-alternatives --config javac
```


```
java -version
```


```
sudo apt install default-jdk
```

# Tomcat

```
sudo groupadd tomcat
```


```
sudo useradd -s /bin/false -g tomcat -d /opt/tomcat tomcat
```


```
curl -O https://downloads.apache.org/tomcat/tomcat-8/v8.5.55/bin/apache-tomcat-8.5.55.tar.gz
```


```
sudo mkdir /opt/tomcat
```


```
sudo tar xzvf apache-tomcat-*tar.gz -C /opt/tomcat --strip-components=1 
```


```
cd /opt/tomcat
```


```
sudo chgrp -R tomcat /opt/tomcat
```


```
sudo chmod -R g+r conf
```


```
sudo chmod g+x conf
```


```
sudo chown -R tomcat webapps/ work/ temp/ logs/
```


```
sudo update-java-alternatives -l
```


```
/usr/lib/jvm/java-1.11.0-openjdk-amd64
```

```
sudo nano /etc/environment
```

```
JAVA_HOME="/usr/lib/jvm/java-1.11.0-openjdk-amd64/bin/"
```

```
echo $JAVA_HOME
```

```
sudo nano /etc/systemd/system/tomcat.service
```

```
sudo systemctl daemon-reload
```

```
sudo iptables -I INPUT -p tcp --dport 8080 -j ACCEPT
```

```
ps aux | sort -rnk 4 | head -5 nano /proc/meminfo && htop && free -h   
```

```
tail -f logs/catalina.out
```


```
export PATH=$PATH:/usr/local/mysql/bin
```

# Apache

```
cd /etc/apache2/sites-available/
```


```
sudo nano -m site.com.br.conf
```


```
sudo service apache2 reload
```


```
sudo a2dissite site.com.br.conf
```


```
sudo a2ensite site.com.br.conf
```


```
netstat -tlpn| grep apache
```


```
ss -tlpn| grep apache
```

# NGINX

```
nano /etc/nginx/sites-enabled/default
```


```
systemctl restart nginx
```


```
netstat -tlpn| grep nginx
```

```
 ss -tlpn| grep nginx
```


# Angular


```
ng build --base-href /frontend/ --deploy-url /frontend/ --prod
```