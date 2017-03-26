# Pingpong 


### Установка pingpong

Установим зависимость для pingpong

``` shell
    sudo apt update
    sudo apt install openjdk-8-jdk openjdk-8-jre openjdk-8jre-headless libgif7 ca-certificates-java java-common
```

Клонируем репозиторий
``` shell
git clone https://github.com/oleggh2017/pingpong.git
```
Заходим в папку с пакетами и устанавливаем
``` shell
cd pingpong/packages
sudo dpkg -i  pingpong_1_0_0.deb
```
Установили pingpong перейдем браузере на http://localhost:8080/ и увидим сообщение Pong.

Cмотрим какая версия у нас установлена
``` shell
apt search pingpong
Sorting... Done
Full Text Search... Done
pingpong/now 1.0.0 all [installed,local]
  Pingpong
```
Установим версию 1.1.0
``` shell
sudo dpkg -i pingpong_1_1_0.deb
```
Установили версию 1.1.0
``` shell
(Reading database ... 421089 files and directories currently installed.)
Preparing to unpack pingpong_1_1_0.deb ...
Unpacking pingpong (1.1.0) over (1.0.0) ...
Setting up pingpong (1.1.0) ...
Processing triggers for systemd (229-4ubuntu16) ...
Processing triggers for ureadahead (0.100.0-19) ...
```

Переходим в браузер на http://localhost:8080/ и видим сообщение Pong!!!

Посмотрим какая версия у нас установлена
``` shell
apt search pingpong
Sorting... Done
Full Text Search... Done
pingpong/now 1.1.0 all [installed,local]
  Pingpong

```

Удаление пакета
``` shell
    sudo dpkg -r pingpong
```



### Сборка пакета

Установим зависимость для pingpong

``` shell
    sudo apt update
    sudo apt install openjdk-8-jdk openjdk-8-jre openjdk-8jre-headless libgif7 ca-certificates-java java-common
```

Установим утилиты для сборки.
``` shell
    sudo apt install maven
```


Клонируем репозиторий
``` shell
git clone https://github.com/oleggh2017/pingpong.git
```

Заходим в pingpong

``` shell
cd pingpong
```
Собирем пакет

``` shell
    mvn compile
    mvn package
```

Собранный пакет лежит в pingpong/deb/target