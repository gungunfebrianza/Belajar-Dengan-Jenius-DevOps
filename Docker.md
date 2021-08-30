# Belajar Dengan Jenius DevOps

## Author : Gun Gun Febrianza

-------



# Table of Contents

1. [Docker](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#docker)
   - [Docker Installation](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#docker-installation)
   - [Container](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#container)
     - [Run Container](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#run-container)
     - [List Container](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#list-container)
     - [Stop Container](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#stop-container)
     - [Remove Container](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#remove-container)
   - [Images](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#images)
     - [Pulling Image](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#pulling-image)
     - [List Images](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#list-images)
     - [Remove Images](https://github.com/gungunfebrianza/Belajar-Dengan-Jenius-DevOps/blob/main/Docker.md#remove-images)
   - Docker Commands
     - Execute Command
     - Attach & Detach Mode
     - Image Tag
     - Interactive Mode
     - Volume Mapping
     - Inspect Container



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

### Run Container

Untuk menjalankan sebuah **Container** eksekusi perintah di bawah ini :

```bash
$ docker run nginx
```



----



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

---



### Stop Container

Untuk menghentikan sebuah **container** eksekusi perintah di bawah ini :

```bash
$ docker stop infallible_mizhakani
```

Kita juga dapat menghentikan **container** yang sedang berjalan menggunakan perintah **CTRL + C**.

----



### Remove Container

Untuk mencabut sebuah **container** eksekusi perintah di bawah ini :

```bash
$ docker rm infallible_mizhakani
```



---



## Images

**Images** atau **Docker Images** adalah sebuah **object** yang isinya dapat berubah **OS Filesystem**, **applications**, dan seluruh **application dependencies**. 

Untuk melihat **list images** dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker image ls
```

Jika kita baru pertama melakukan instalasi, maka belum terdapat **image** dalam mesin komputer kita.

----



### Pulling Image

Jika kita ingin mendapatkan sebuah **images** terdapat istilah **pulling**, artinya kita akan melakukan **download** sebuah **docker image** yang akan kita simpan dalam mesin komputer kita.

```bash
$ docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
e1acddbe380c: Pull complete
e21006f71c6f: Pull complete
f3341cc17e58: Pull complete
2a53fa598ee2: Pull complete
12455f71a9b5: Pull complete
b86f2ba62d17: Pull complete
Digest: sha256:4d4d96ac750af48c6a551d757c1cbfc071692309b491b70b2b8976e102dd3fef
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest
```

Untuk memastikan **image** telah kita dapatkan eksekusi perintah :

```bash
$ docker images
```

Perintah di atas akan menampilkan **output** sebagai berikut :

| Repository |  Tag   |   Image ID   |   Created   |  Size  |
| :--------: | :----: | :----------: | :---------: | :----: |
|   nginx    | latest | dd34e67e3371 | 12 days ago | 133 MB |



------



### List Images

Untuk mendapat **list images** yang telah terpasang dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker images
```



----



### Remove Images

Sebelum menghapus sebuah **images** pastikan terlebih dahulu tidak terdapat **container** yang menggunakannya, dan container harus di **remove** terlebih dahulu. Untuk menghapus sebuah **images** yang telah terpasang dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker rmi nginx
Untagged: nginx:latest
Untagged: nginx@sha256:4d4d96ac750af48c6a551d757c1cbfc071692309b491b70b2b8976e102dd3fef
Deleted: sha256:dd34e67e3371dc2d1328790c3157ee42dfcae74afffd86b297459ed87a98c0fb
Deleted: sha256:ec6149850eea7af0bfa5f4aa0130d2c3cbae06e4b5da8c748d8b6b1b0cb81d07
Deleted: sha256:2a3d94c7adfe6e94ef038a9b3ea3631168e979f8ddb49a38b203e364627af2d9
Deleted: sha256:2bbff8011bb867605e83fdb8095f94a347307726b8cce81d752886a8af974aea
Deleted: sha256:f151353bef203bd70680578f33abd9667b65434ffadf547f900dca09927cc435
Deleted: sha256:47c01ba78b6d0bdef530c46858d4c83b87452d42dc9faa54b02b3e026107ff27
Deleted: sha256:f68ef921efae588b3dd5cc466a1ca9c94c24785f1fa9420bea15ecc2dedbe781
```



----



### List Images

Untuk mendapat **list images** yang telah terpasang dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker images
```



---



## Docker Commands

### Execute Command

Kita dapat mengeksekusi sebuah perintah di dalam sebuah **container** :

```bash
$ docker exec <container-name> ls
bin
boot
dev
docker-entrypoint.d
docker-entrypoint.sh
etc
home
lib
lib64
media
mnt
opt
proc
root
run
sbin
srv
sys
tmp
usr
var
```



----



### Attach & Detach Mode

Untuk menjalankan sebuah **container** dalam **mode detach** eksekusi perintah di bawah ini :

```bash
$ docker run -d <image>
73e1e391d1733e655ccb108184608c6116dfd7928a8e7b678a97311580f788f0
```

**Container** akan berjalan di dalam **background**, untuk memastikan **container** sudah berjalan di dalam **background** eksekusi perintah **docker ps** :

| Container ID | Image      | Command       | Created       | Status           | Ports    | Names     |
| ------------ | ---------- | ------------- | ------------- | ---------------- | -------- | --------- |
| 73e1e391d173 | your-image | python app.py | 3 minutes ago | Up 3 minutes ago | 8000/tcp | zan_kodok |

Untuk terhubung kedalam sebuah **container** atau melakukan **mode attach** eksekusi perintah di bawah ini :

```bash
$ docker attach 73e1e
```

Gunakan **Container ID** sebagai **argument** untuk **attach mode**.

---



### Image Tag

Kita dapat menggunakan **tag** untuk melakukan **pull image docker** menggunakan versi tertentu, di bawah ini adalah contoh kita melakukan **pulling redis** menggunakan versi **5.0** :

```bash
$ docker pull redis:5.0
```

Selanjutnya kita cek **images redis** yang telah kita **pull** :

```bash
$ docker images
```

Perintah di atas akan menampilkan **output** sebagai berikut :

| Repository | Tag  |   Image ID   |   Created   |  Size  |
| :--------: | :--: | :----------: | :---------: | :----: |
|   redis    | 5.0  | 15e36694d7df | 12 days ago | 98.4MB |

Jika kita melakukan pulling images redis tanpa memberikan tag maka secara default versi terakhir dari **images redis** yang akan di **pull** :

```bash
$ docker pull redis
```

Jikakita cek **images redis** yang telah kita **pull** maka akan terdapat dua versi :

```bash
$ docker images
```

Perintah di atas akan menampilkan **output** sebagai berikut :

| Repository |  Tag   |   Image ID   |   Created   |  Size   |
| :--------: | :----: | :----------: | :---------: | :-----: |
|   redis    |  5.0   | 15e36694d7df | 12 days ago | 98.4 MB |
|   redis    | latest | ddcca4b8a6f0 | 12 days ago | 105 MB  |

----



### Interactive Mode

Kita dapat menggunakan mode **interative mode** agar bisa berinteraksi dengan **container** :

```bash
$ docker run -it <your-image>
```



----



### Volume Mapping

Di bawah ini adalah contoh penerapan **Volume Mapping** dalam **MySQL Container** :

```bash
$ docker run -v /opt/mysqldata:/var/lib/mysql mysql
```



----



### Inspect Container

Untuk melakukan inspeksi pada suatu **Container** eksekusi perintah di bawah ini :

```bash
$ docker inspect zan_kodok
[
    {
        "Id": "7476e104a25c9e6fc197bcdd7348f8620072a3cd509d29e8440a9696cb87b4a2",
        "Created": "2021-08-30T08:59:24.123835663Z",
        "Path": "python",
        "Args": [
            "app.py"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            
....
```



---



Disini terdapat dua **lifecycle** : 

1. **Operator**

   Bagian **operator** akan melakukan **download image (Docker Image)**, menjalankan **container**, mengelola **container** sampai akhirnya melakukan operasi **destroy container** ketika sudah tidak digunakan.

2. **Developer**

   Bagian **developer** akan lebih fokus melakukan pengembangan aplikasi, explorasi **containerized apps**, kloning dan modifikasi **containerized apps**, dan menjalankannya sebagai **container**.



---



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
