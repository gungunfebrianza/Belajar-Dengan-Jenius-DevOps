# Belajar Dengan Jenius DevOps

## Author : Gun Gun Febrianza



# AWS EC2 (Elastic Cloud Computing)

Fitur **Amazon** **EC2** :

1. **Virtual Computing Environment**

   Lingkungan untuk melakukan komputasi virtual yang disebut dengan **instance**.

2. **Preconfigured Templates**

   Kita dapat membangun sebuah template untuk **instance** menggunakan **Amazon Machine Images (AMIs)**  

3. **Secure Login Information**

   Sistem untuk melakukan login yang aman, **AWS** akan menyimpan **public-key** dan kita akan menyimpan **private-key** untuk melakukan **login** ke dalam **instance**.

4. **Firewall Configuration**

   Pengaturan **Protocol**, **Ports** dan **Source IP Ranges** yang dapat mengakses **instances** milik kita.

5. **Instance Store Volumes**

   Tempat penyimpanan sementara yang akan dihapus jika perintah **stop**, **hibernate** atau **terminate** dieksekusi pada **instances**. 

6. **Amazon Elastic Block Store (EBS) Integration**

   Tempat penyimpanan permanen menggunakan layanan **Amazon Elastic Block Store (EBS)**.

7. **Amazon Elastic IP Integration** 

   Dukungan penerapan **Static IPv4 Addresses** menggunakan layanan **Amazon Elastic IP**.

8. **Virtual Private Clouds (VPCs)**

   Kita dapat membuat jaringan komputer virtual secara terisolasi.

   

## General Purpose Instance 

## Compute Optimized Instance 

## Memory Optimized Instance 

## Accelerated Computing



# AWS EC2 Dashboard

## Instances 

## Images 

## Elastic Block Store 

## Network & Security 

## Load Balancing 

## Auto Scaling

---



# EC2 Introduction

## Create EC2



-------



## Example Running Instance

Di bawah ini adalah contoh informasi dari running instance dalam **Amazon EC2** :



|    Instance Info    |                          Value                          | Description |
| :-----------------: | :-----------------------------------------------------: | ----------- |
|        Name         |                 Server A - Development                  |             |
|     Instance ID     |                   i-0d06ceabb68b31c80                   |             |
|   Instance State    |                         Running                         |             |
|    Instance Type    |                       t3a.2xlarge                       |             |
|    Status Check     |                    2/2 Checks Passed                    |             |
|    Alarm Status     |                        No Alarm                         |             |
|  Availability Zone  |                     ap-southeast-1c                     |             |
|   Public IPv4 DNS   | ec2-13-212-226-211.ap-southeast-1.compute.amazonaws.com |             |
| Public IPv4 Address |                     13.212.226.211                      |             |
|     Elastic IP      |                            -                            |             |
|      IPv6 IPs       |                            -                            |             |
|     Monitoring      |                         Enabled                         |             |
|   Security Group    |                     launch-wizard-1                     |             |
|      Key Name       |                      X-Development                      |             |
|     Launch Time     |                 2021/08/25 16:06 GMT+7                  |             |

Terdapat informasi tambahan lainnya :

|    Instance Info     |             Value             |   Description   |
| :------------------: | :---------------------------: | :-------------: |
|        VPC ID        |         vpc-893ee9ef          |                 |
|      Subnet ID       |        subnet-74cdba2d        |                 |
|       IAM Role       | EC2-Call-All-AWS-Services-Gun | Manual Creation |
|       Platform       |            Ubuntu             |                 |
| Credit Specification |           Unlimited           |                 |
| Virtualization Type  |              HVM              |                 |
|   Number of vCPUs    |               8               |                 |
|       Tenancy        |            Default            |                 |

## Storage

### Root Device Details

Dibawah ini adalah informasi **Root Device Details Storage** yang digunakan dari **Running Instance** di atas :

|   Storage Info   |   Value   | Description |
| :--------------: | :-------: | :---------: |
| Root device name | /dev/sda1 |             |
| Root device type |    EBS    |             |
| EBS Optimization |  enabled  |             |

### Block Device Details

|      Storage Info      |                            Value                             | Description |
| :--------------------: | :----------------------------------------------------------: | :---------: |
|          Name          |                                                              |             |
|       Volume ID        |                    vol-00fbee6da3f467e4a                     |             |
|          Size          |                            60 GiB                            |             |
|      Volume Type       |                             gp2                              |             |
|          IOPS          |                             180                              |             |
|       Throughput       |                              -                               |             |
|        Snapshot        |                    snap-0c83907cbff0eb0fb                    |             |
|        Created         |             August 25, 2021 at 4:06:54 PM UTC+7              |             |
|   Availability Zone    |                       ap-southeast-1c                        |             |
|         State          |                            in-use                            |             |
|      Alarm Status      |                            *None*                            |             |
| Attachment Information | [i-0d06ceabb68b31c80 (Server A - Development)](https://ap-southeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-1#Instances:search=i-0d06ceabb68b31c80;sort=instanceId):/dev/sda1 (attached) |             |
|       Monitoring       |                                                              |             |
|     Volume Status      |                                                              |             |
|       Encryption       |                        Not Encrypted                         |             |
|       KMS Key ID       |                                                              |             |
|  Multi-attach Enabled  |                              No                              |             |



----



## Create EC2 Template



-----





# [EC2 API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html)









# [EC2 Auto Scaling API Reference](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/Welcome.html) 

