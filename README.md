# My most frequently used linux commands
```
sudo ps -ef | grep java
```

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

# Maven | Oracle | Springboot

```
mvn install:install-file -Dfile=path/to/your/ojdbc7.jar -DgroupId=com.oracle -DartifactId=ojdbc7 -Dversion=12.2.0.1 -Dpackaging=jar
```

# Aliases

```
alias git-add-commit='git add . && git commit -m'

alias git-master-delete='git checkout master && git branch -d'

alias bash='nano /home/user/.bashrc'

alias bash-source='source /home/user/.bashrc'

alias git-andre='git config --global user.name andretecnologia && git config --global user.email '

alias mudar-para-dev-b='git config --global user.name "" && git config --global user.email '

alias mudar-para-dev-a='git config --global user.name ""  && git config --global user.email '

alias git-enegocios='git config --global user.name && git config --global user.email '

alias git-list='git config --list'

alias git-log='git log --oneline'

alias ssh-email='ssh-keygen -t rsa -b 4096 -C'

alias ssh-eval='eval "$(ssh-agent -s)"'

alias ssh-adiciona='ssh-add ~/.ssh/id_rsa'

alias ssh-copy='xclip -sel clip < ~/.ssh/id_rsa.pub'

export PATH="$PATH:/snap/bin/code"

export PATH="$PATH:/snap/intellij-idea-community/current/bin"

#grep -i chave_de_pesquisa arquivo
#grep -l solicitação ./*

#installdeb dpkg -i package management system -install

alias install-deb='sudo dpkg -i'

alias preparesonar='sudo rm -Rf /opt/sonarqube && cd /opt && sudo unzip /opt/sonarqube.zip && sudo /opt/sonarqube/bin/linux-x86-64/sonar.sh console' 

alias consolesonar='/opt/sonarqube/bin/linux-x86-64/sonar.sh console'

alias runsonar='mvn clean install sonar:sonar -Dsonar.host.url=http://localhost:9000'

alias robot3t='cd /opt/robo3t-1.3.1-linux-x86_64-7419c406/bin && ./robo3t' 

alias gitaddall='git add . && git reset src/main//resources/application-local.yml'

```
