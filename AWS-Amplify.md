# Belajar Dengan Jenius DevOps

## Author : Gun Gun Febrianza



# Amazon Amplify



## Setup Custom Domain

Kita dapat menghubungkan **custom domain** dengan **application** yang di **deploy** pada **amazon amplify console**. Kita juga dapat membeli **custom domain** menggunakan **Domain Name System (DNS) Web Services** seperti **Amazon Route 53** atau menggunakan **godaddy** atau **google domains**.

Saat kita melakukan **deployment** pada **Amazon Amplify Console** kita akan mendapatkan alamat **domain** :

```
https://branch-name.d1m7bkiki6tdw1.amplifyapp.com
```

kita dapat menghubungkannya dengan sebuah **custom domain** misal :

```
https://masgun.io
```

**Amazon Console** akan menerbitkan sertifikat **SSL/TLS** untuk seluruh domain yang terhubung dengan aplikasi kita, sehingga seluruh **traffic** akan diamankan menggunakan **HTTPS/2**. **Certificate** di produksi menggunakan **AWS Certificate Manager (ACM)** yang akan valid selama 13 bulan dan dapat diperbaharui secara otomatis selama aplikasi terpasang di **AWS Amplify**.



### DNS Concepts
