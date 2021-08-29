# Belajar Dengan Jenius DevOps

# Author : Gun Gun Febrianza

# Docker

Untuk menggunakan **docker** pastikan anda terhubung dengan internet.

## Docker Installation

Untuk memastikan **docker** telah berjalan eksekusi perintah di bawah ini :

```bash
$ systemctl status docker
```

Untuk melihat versi **docker** yang digunakan :

```bash
$ docker version
```

## Images

**Images** atau **Docker Images** adalah sebuah **object** yang isinya dapat berubah **OS Filesystem**, **applications**, dan seluruh **application dependencies**. 

Untuk melihat **list images** dalam mesin komputer kita eksekusi perintah di bawah ini :

```bash
$ docker image ls
```

Jika kita baru pertama melakukan instalasi, maka belum terdapat **image** dalam mesin komputer kita.

### Pulling Images

Jika kita ingin mendapatkan sebuah **images** terdapat istilah **pulling**, artinya kita akan melakukan **download** sebuah **docker image** yang akan kita simpan dalam mesin komputer kita.

```bash
$ docker image pull ubuntu:latest
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
