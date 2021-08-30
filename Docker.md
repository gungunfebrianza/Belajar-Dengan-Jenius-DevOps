# Belajar Dengan Jenius DevOps

## Author : Gun Gun Febrianza

-------



# Table of Contents

1. Docker
   - Docker Installation
   - Container
     - List Container
     - Stop Container
   - Images
     - Pulling Image
     - List Images



--------



# Docker

Untuk menggunakan **docker** pastikan anda terhubung dengan internet.

## Docker Installation

Untuk melakukan installation pada sistem operasi [ubuntu](https://docs.docker.com/engine/install/ubuntu/), **download script** di bawah ini :

```bash
$ curl -fsSL https://get.docker.com -o get-docker.sh
```

Selanjutnya eksekusi **script** menggunakan **sudo** atau **root** :

```bash
$ sudo sh get-docker.sh
```

Untuk memastikan **docker** telah berjalan eksekusi perintah di bawah ini :

```bash
~$ systemctl status docker
● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Sun 2021-08-29 18:55:15 UTC; 2min 35s ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 27282 (dockerd)
      Tasks: 13
     Memory: 32.1M
     CGroup: /system.slice/docker.service
             └─27282 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock
```

Untuk melihat versi **docker** yang digunakan :

```bash
$ docker version
```

-----



## Container

```bash
$ docker run nginx
```



### List Container

Untuk melihat **list container** yang berjalan eksekusi perintah di bawah ini :

```bash
$ docker ps
```

Di bawah ini adalah **List Container** yang tersedia :

| Container ID | Image | Command      | Created            | Status                | Ports  | Names                |
| ------------ | ----- | ------------ | ------------------ | --------------------- | ------ | -------------------- |
| eacb8e1b03db | Nginx | "/docker..." | About a minute ago | Up About a minute ago | 80/tcp | infallible_mizhakani |

Untuk melihat seluruh **list container** eksekusi perintah di bawah ini :

```bash
$ docker ps -a
```



### Stop Container

Untuk menghentikan sebuah container eksekusi perintah di bawah ini :

```bash
$ docker stop infallible_mizhakani
```



---



## Images

**Images** atau **Docker Images** adalah sebuah **object** yang isinya dapat berubah **OS Filesystem**, **applications**, dan seluruh **application dependencies**. 

Untuk melihat **list images** dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker image ls
```

Jika kita baru pertama melakukan instalasi, maka belum terdapat **image** dalam mesin komputer kita.

### Pulling Image

Jika kita ingin mendapatkan sebuah **images** terdapat istilah **pulling**, artinya kita akan melakukan **download** sebuah **docker image** yang akan kita simpan dalam mesin komputer kita.

```bash
$ docker image pull ubuntu:latest
```

Untuk memastikan **image** telah kita dapatkan eksekusi perintah :

```bash
$ docker image ls
```



### List Images

Untuk mendapat **list images** yang telah terpasang dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker images
```







Disini terdapat dua **lifecycle** : 

1. **Operator**

   Bagian **operator** akan melakukan **download image (Docker Image)**, menjalankan **container**, mengelola **container** sampai akhirnya melakukan operasi **destroy container** ketika sudah tidak digunakan.

2. **Developer**

   Bagian **developer** akan lebih fokus melakukan pengembangan aplikasi, explorasi **containerized apps**, kloning dan modifikasi **containerized apps**, dan menjalankannya sebagai **container**.





# Cheatsheet

docker run x 

docker version

docker ps // list container

docker ps -a // see all container

docker stop <name_container> // stop container

docker rm <name_container> //remove container

docker images //list available images

docker rmi nginx //remove images

docker pull nginx //store images

docker exec <name_container> cat /etc/hosts //execute command & running container, print the contents
