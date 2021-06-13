# Belajar Dengan Jenius DevOps

## Outline

<img src="/asset/DevOps-Outline.png" style="zoom:100%;" />

## What You Will Learn

**Programming Languages & Modules** :  

Node.js | Python | Boto3

**Amazon Web Resources** :

IAM | VPC | EC2 |  EBS | RDS | SNS | CloudWatch | Elasticsearch | DLM | S3 | CloudFormation | EKS | ECR

**Source Code Manager :**

Git

**Artifact Source Code Manager :**

Nexus | Docker Hub

**Containerization :**

Docker

**Continuous Integration :**

Jenkins

**Orchestration :**

Kubernetes

**Provisioning** : 

Terraform

## Content Tables

1. Introduction to DevOps
   - DevOps, FinTech, & Banking Industry
     - Wise (Transferwise)
     - Stripe
     - Robinhood
     - Grab
     - CBDC
     - Cryptocurrency
     - Facebook
     - Paypal
     - Bank Challenges
       - Cobol Applications
       - Mainframe Computer
   - So What is DevOps?
   - DevOps As Emerging Role
     - Traditional Software Development
   - DevOps Way
     - Culture
     - Tools
     - Processes
       - Continuous Integration (CI)
       - Continuous Delivery (CD)
       - Continuous Deployment
   - Agile Software Development
     - Quick Understanding Market
   - Release Management

# Introduction to DevOps

## DevOps, FinTech & Banking Industry

Okay karena mas Gun seneng banget dengan dunia **FinTech** dan teknologi perbankan, ini jadi pembahasan awal menarik. Sebagai generasi yang lahir tahun 90an mas Gun melihat perusahaan di bidang **FinTech** melakukan disrupsi besar-besaran di dunia perbankan. 

Tahun 1994, **Microsoft Founder Bill Gates** membuat **statement** menarik : 

*“Banking is necessary, banks are not”*

**FintTech** atau **Financial Technology** adalah perusahaan yang memberikan layanan keuangan sama seperti **bank**. Kecepatan mereka untuk akuisisi **customer** bersifat disruptif untuk perbankan, meskipun begitu jangkauan disrupsi **FinTech** masih terbatas regulasi. Terdapat regulasi yang membatasi jumlah dana yang dapat di transaksikan.

**Startup** dan perusahaan tersebut diantaranya adalah :

### **Wise (Transferwise)**

Startup ini fokus membangun layanan transfer uang antar negara dengan biaya rata-rata 0,7%, sangat jauh sekali jika menggunakan layanan perbankan di amerika yang menekankan biaya sebesar 3-4%. **Wise** menyediakan layanan **Debit Card** untuk menyimpan dana, transfer dana dan pengunaan dana yang dapat dibelanjakan di 55 negara. 

Valusi terakhir **Wise** mencapai **$ 5 Billion**, dengan 10 juta pengguna.

### **Stripe**

**Startup** ini fokus membangun layanan **payment processor** yang dapat membantu para **web developer** untuk integrasi sistem pembayaran pada **web application** yang mereka buat. Layanan mereka sudah digunakan di 100 negara. Kini mereka menyediakan **BaaS** (**Banking as a Service**). 

Layanan **BaaS Stripe** membantu setiap **customer** untuk bisa menyimpan uang, melakukan pembayaran, hingga mendapatkan bunga. Kini valusi **stripe** mencapai **$ 95 Billion**, dengan pendapatan pada tahun 2020 mencapai 1 Trilliun USD. 

### **Robinhood**

Perusahaan ini yang awalnya berfokus pada **stockbroker** kini menyediakan layanan trading untuk **cryptocurrency**, selain **stock** dan **ETFs**. Dengan pengguna yang mereka klaim kini sudah mencapai 13 juta pengguna, pendapatan mereka pada **Q1 2021** mencapai **$ 331 Million**.

Kini mereka juga menyediakan layanan **Debit Card** diseluruh dunia selama tempat tersebut mendukung **Mastercard**.

### **Grab**

Tidak ada yang akan mengira di masa depan saat startups **ride-hailing**, yang bertransformasi menjadi **Super Apps** akhirnya juga menyediakan layanan **financial** seperti pinjaman, asuransi, pembayaran dan investasi melalui **mobile application** yang mereka sediakan.

Di Asia, **Grab** telah mendapatkan dukungan dari **Monetary Authority of Singapore** (**MAS**) untuk membangun bank digital. Masyarakat dapat melakukan deposit pada bank digital dan mendapatkan layanan perbankan seperti pada umumnya, **Bank Digital** akan mulai beroperasi pada tahun 2022.

### **CBDC (Central Bank Digital Currency)**

Selain tantangan dari **FinTech**, perbankan juga harus berhadapan dengan tantangan untuk berinovasi dan beradaptasi dengan regulasi. Pada tanggal 8 Juni 2021 **Hong Kong Monetary Authority (HKMA)** meluncurkan strategi **FinTech 2025**. Dalam strategi tersebut terdapat [5 Fokus Area](https://www.hkma.gov.hk/eng/news-and-media/press-releases/2021/06/20210608-4/) diantaranya adalah :

- **All Bank Go to Fintech**

  **HKMA** menekan **Traditional Bank** untuk melakukan transformasi menjadi **Smart Bank** dengan melakukan adopsi **FinTech**, proses digitalisasi harus dilakukan secara keseluruhan operasi perbankan. **HKMA** sendiri yang akan memberikan **guideline** untuk perbankan. 

- **CBDC (Central Bank Digital Currency)**

  Eksistensi sistem keuangan terdesentralisasi menjadi ancaman perbankan, untuk itu **central bank** secara global mulai melakukan perlawanan dengan cara menerbitkan mata uang digital mereka sendiri. Langkah ini juga didukung oleh **IMF** (**International Monetary Fund**)

### **Cryptocurrency**

Selain **fintech** juga terdapat **alternative financial channel** lain yang mendisrupsi perbankan salah satunya adalah **cryptocurrency**. Tingkat **confidence** masyarakat pada uang kertas (**Fiat**) bisa menurun, masyarakat bisa cenderung lebih senang menyimpannya dalam bentuk **crypto** daripada di **bank**.

Saking sulitnya diprediksikan perbankan di Texas mencoba untuk beradaptasi dengan cara mengizinkan perbankan untuk bisa mengadopsi **virtual currency**, seperti **bitcoin** dan sebagainya.

<img src="/asset/BankBitcoin.jpg" style="zoom:80%;" />

Izin tersebut muncul setelah Negara El Savador mendeklarasikan bahwa **Bitcoin** diperbolehkan sebagai alat transaksi pembayaran yang sah di negaranya. 

### **Facebook** 

Selain itu perbankan juga di hantui perusahaan-perusahaan raksasa seperti **Facebook**, **Google**, **Amazon** dan **Apple**, kompetitor-kompetitor dengan skala rivalitas yang sangat sulit ditandingi. 

**Facebook** juga kini mengembangkan **Diem** sebuah **stablecoin**, dengan kemampuan skalabilitas yang bisa membangun milyaran akun disertai kemampuan transaksi dengan kecepatan tinggi.

### **Paypal**

Selain perusahaan-perusahaan raksasa tersebut, perusahaan **Paypal** juga kini mendukung **cryptocurrency** pada layanan mereka. Terdapat dukungan untuk pengelolaan **bitcoin** dalam perusahaan tersebut.

### **Bank Challenges**

Banyak dan besar sekali ya tantangan perbankan?

Kalau diamati secara detail penyebabnya adalah **bank** sebagai pemain besar kehilangan kemampuan untuk membangun sistem IT yang **cost-effective**. Wajar saja untuk ukuran perbankan pasti berhadapan dengan penyakit **Corporate Inefficiency**, semakin besar semakin lamban perkembangannya.

<img src="/asset/DevOps-Intro-0.png" style="zoom:100%;" />

Bank juga mengalami **struggling** di lini :

- **Legacy IT System** 

  Tantangan resiko keamanan (**security risk**) pada **Legacy IT System** masih menjadi tantangan untuk melakukan **Digital Transformation**.

- **Lack of DevOps Skill**

  Berdasarkan riset yang dibangun oleh **Avanade**, secara mayoritas permasalahan perbankan adalah kesulitan mengakuisisi **DevOps Engineer** dan menerapkan **DevOps Culture**.

#### **Cobol Applications**

Terlebih mayoritas perbankan secara global saat ini masih menggunakan teknologi 90an, **Mainframe Computing** dan Aplikasi yang ditulis menggunakan bahasa tahun 50an, bahasa pemrograman **Cobol**. Berdasarkan laporan [thomsonreuters](http://fingfx.thomsonreuters.com/gfx/rngs/USA-BANKS-COBOL/010040KH18J/index.html) di USA 43% sistem perbankan dibangun menggunakan bahasa Cobol :

<img src="/asset/DevOps-Mainframe1.png" style="zoom:100%;" />

Begitupun saat kita melakukan penarikan atau belanja menggunakan **ATM** terdapat 95% kode **Cobol** yang dieksekusi. Sistem perpajakan yang dibangun pemerintahan **USA**, yaitu **IRS** juga masih mengandalkan **Mainframe Computer** dan aplikasi **Cobol**. 

<img src="/asset/DevOps-Mainframe2.png" style="zoom:100%;" />

Tahun ini tepatnya saat buku ini ditulis usia bahasa pemrograman **Cobol** sudah mencapai 60 tahun, dengan versi terakhir **Cobol 6.3.0**. Bahasa ini lebih tua dari bahasa pemrograman C & C++.

**Mainframe & Cobol** adalah **Legacy IT System** perbankan yang menjadi tantangan untuk melakukan inovasi berkelanjutan. Permasalahan serius yang bisa timbul dalam Legacy IT System ini dapat dipelajari dari kejadian **shortage** **Cobol Programmer** yang menimpa pemerintahan **New Jersey** :

<img src="/asset/DevOps-Mainframe3.png" style="zoom:100%;" />

Terdapat pengesahan regulasi terbaru di new jersey yang baru di sahkan pada tahun 2020, yaitu pemberian uang sebesar  600 dollar perminggu untuk 362 ribu warganya. Namun tantangan yang harus dihadapi pemerintah New Jersey adalah melakukan perubahan kode pemrograman pada sistemnya.

Permasalahannya adalah sistem **Unemployment Insurance Software System** mereka berusia 40 tahun dan ditulis menggunakan bahasa pemrograman **Cobol**. **Software** tersebut telah dioptimasi selama beberapa dekade dan diprogram ulang, namun tidak ada yang sanggup melakukannya sehingga pemerintah **New Jersey** harus mencari jasa pihak ke 3.

Ahli pemrograman **Cobol**, berkomentar **software** tersebut telah dikembangkan sejak lama kemungkinan para ahli yang memeriksa kode pemrograman tersebut akan berakhir menjadi **Reverse Engineering Project** dimana mereka akan menjadi seorang arkeologis disana. wkwk medoq sekali ya.

<img src="/asset/DevOps-Mainframe4.png" style="zoom:100%;" />

Tantangan terbesar dari **Cobol Programmer** selanjutnya bukan hanya dari bahasa pemrograman **Cobol** itu sendiri tetapi kemampuan untuk memahami teknologi di infrastruktur sebelumnya. Sebab saat menyentuh Aplikasi **Cobol** di **production** tanpa memahami latar belakang dan sejarahnya hanya akan menambahkan resiko.

Itu sebabnya para ahli Cobol berkata :

"*If all the COBOL programs stopped working, the US economy would collapse.*"

#### Mainframe Computer

**Mainframe Computer** adalah teknologi komputer tahun 60an yang kehadirannya menandai revolusi digital di era revolusi industri ke 3, sampai saat ini 92 dari 100 bank terbaik didunia masih menggunakan **Mainframe Computer**. Mainframe adalah monster ketika berhadapan dengan masalah **computation** dan **transaction processing**.

**Mainframe Computer** didesain untuk bisa menangani jutaan transaksi secara **conccurent**, Pada **Mainframe Computer IBM z13** terdapat kapabilitas untuk memproses **2.5 billion transactions/day**, Sementara pada **Mainframe Computer IBM z15** memiliki kapabilitas untuk memproses **1 trillion transactions/day.**

**Mainframe Computing** masih dianggap lebih **Reliable**, karena akurasinya untuk menyelesaikan komputasi pada **decimal arithmetic**. Juga kemampuan **Mainframe Computing** memproses jutaan transaksi perdetik, masalah **Availability** mendikte perbankan untuk tidak boleh mengalami **downtime**.

Selain dukungan **cryptography** di level **hardware**, kecepatan analitik juga menjadi tuntutan utama agar sistem **ATM**, **Credit Card** dan internal perbankan yang memerlukan respon dengan kecepatan **instant**. Namun kecanggihan **mainframe computer** tetap tidak mengubah statusnya sebagai **Legacy IT System**.

Pengembangan **applications** pada **Mainframe Computer** masih menggunakan **Traditional Software Development**. Pemanfaatan **DevOps** juga seringkali dianggap tidak **reliable**, padahal menurut **Jonathan Webster**, Former **CIO Lloyd Banking Group Digital** :

"**Bank** memiliki banyak **engineer** dengan talenta yang dapat diandalkan untuk mendukung **mainframe computer** dalam sistem perbankan mereka. Tim tersebut dapat digunakan untuk mengembangkan kembali **legacy system** yang telah dibangun, namun kebanyakan tim tersebut tidak digunakan karena terdapat miskonsepsi bahwa praktek **DevOps** tidak dapat diterapkan dalam **mainframe computer** dan **legacy system**. Anda bisa dan harus melakukannya."

Terdapat inisiatif untuk menerapkan **DevOps** pada **Mainframe Computer** yang di gagas oleh **[Open Mainframe Project](https://www.openmainframeproject.org/about)** di bawah payung **[The Linux Foundation](https://www.linuxfoundation.org/projects)**. Inisiatif itu diwujudkan dengan membuat sebuah **Open Source Framework** yang diberi nama dengan **Zowe**.

<img src="/asset/openmainframeproject-color.svg" style="zoom:30%;" />

Jika dikaji lebih serius penggunaan **Mainframe Computing** memiliki beban biaya yang mahal dan gak **economies of scale**, berdasarkan laporan yang dibuat oleh **Accenture** dengan judul **Reframe your Mainframe** dikatakan bahwa **Mainframe Computing** dikatakan tidak **sustainable** untuk jangka panjang (**Long Term**)



Disisi lain **startup FinTech** dengan skala kecil sampai menengah mulai mendisrupsi perbankan. Kapabilitas mereka yang bisa dengan cepat membangun **High Impact IT System** dan **Break Things Faster** jadi andalannya di pasar. 

Inilah yang menjadikan peran **DevOps** dibalik kesuksesan perusahaan **FinTech** mendisrupsi perbankan yaitu kemampuan mereka untuk **break things faster**, peran **DevOps** sangat bersahabat dengan **FinTech** startup skala kecil.

<img src="/asset/DevOps-Intro.png" style="zoom:100%;" />

Pada akhirnya agar bisa bertahan perbankan harus mengakuisisi **FinTech** dan **DevOps** itu sendiri ke dalam ekosistemnya agar bisa bertahan. Peran **DevOps** memberikan perubahan besar pada **landscape** Industri IT.

Saat acara virtual [Devops World](https://www.cloudbees.com/devops-world), **Julienne McLean** konsultan perbankan **JPMorgan Chase** berkata :

“*When I look at disruptors in the financial services space, they exploit speed. That is the cheat code to survive*” 

Dalam 



## So What is DevOps?

**DevOps** adalah peran baru yang kini eksistensinya vital dalam industry IT, mulai dari sektor perbankan, keuangan, **e-commerce** dan sebagainya. Sekali lagi kenapa figur **DevOps** di anggap sangat vital? karena figur **DevOps** dapat membantu **To Break things faster** mempercepat **delivery business value** untuk user. 

Figur **DevOps** membuat, perusahaan atau startup bisa berkompetisi dengan baik dipasar, sehingga pasar menjadi lebih kompetitif. Eksistensi **DevOps** membuat perusahaan yang tidak mampu bersaing secara kompetitif memiliki resiko kegagalan yang lebih besar.

<img src="/asset/DevOps-Faster-Delivery.png" style="zoom:100%;" />

Figur **DevOps** mulai lahir karena problema **corporate inefficiency** mulai menjadi masalah serius, sebab semakin besar suatu perusahaan maka semakin lama potensi perusahaan tersebut menyelesaikan sebuah **task**. Sehingga peluang perusahaan atau startup skala kecil sampai menengah bisa melakukan disrupsi dengan cepat.

Industri skala besar seperti perbankan atau **e-commerce** mereka mungkin memiliki dana yang mumpuni, namun jika anda berada dalam sebuah startup kecil maka anda harus mereduksi biaya dengan cara melakukan **automation**. Terdapat mantra dalam **DevOps** : *Anything that can be automated must be automated*.

<img src="/asset/DevOps-Advantage.png" style="zoom:100%;" />

**Julienne McLean** konsultan perbankan **JPMorgan Chase** juga berkata dengan menerapkan **DevOps**, **CI/CD**, dan **Automations** mereka bisa mempercepat rilis product secara signifikan. Manfaat besar lainnya **developer** bisa menjadi lebih fokus mengerjakan hal-hal yang mereka sukai untuk lebih kreatif dan inovatif.

Jadi peran akhir seorang **DevOps** untuk **enterprise**, dapat dilihat dari seberapa besar **cost** yang bisa ditekan dan kualitas **IT System** yang sangat mumpuni (**High Impact**). 

<img src="/asset/DevOps-Advantage-2.png" style="zoom:100%;" />

## DevOps As Emerging Role

Terminologi ini sempat muncul sekitar tahun 2007 yang merepresentasikan dua istilah yaitu **Development (Dev)** dan **Operations (Ops)**. 

Pertama kali diperkenalkan oleh **Patrick Debois** seorang figur di bidang **Software Engineer** yang frustasi dalam memanajemen permasalahan **Traditional Software Development** yang dihadapi tim **developer** dan tim dibagian **operations**.

Tahun 2009 istilah **DevOps** mulai populer setelah **Patrick Debois** membuat sebuah **conference** dengan nama **DevOpDays**. Event tersebut sukses menjadi perbincangan di kalangan para **software engineer**, gagasan Patrick dianggap solutif karena ternyata banyak juga **software engineer** menghadapi permasalahan yang sama.

<img src="/asset/DevOps-Problem.png" style="zoom:100%;" />

Saat proses **Release Management** :

**Problem** disini adalah **developer** ingin terus dan tertuntut tantangan berinovasi dalam ekosistemnya sendiri. **Developer** juga ingin pekerjaan segera cepat selesai. Jika organisasi perusahaan tersebut besar dan kompleks program yang dirilis **developer** akan diuji terlebih dahulu oleh **tester** sebelum diberikan kepada bagian **operations**.

Bagian **Operations** memiliki tanggung jawab terhadap **Scalability** jangan sampai terjadi **downtime** dan **back-end server** mampu mengatasi **huge traffic**.

<img src="/asset/DevOps-Problem2.png" style="zoom:100%;" />

**Developer** biasanya memberikan beberapa instruksi dan konfigurasi untuk **Operator**, jika terdapat instruksi dan konfigurasi yang tidak tercatat atau terlewat oleh **Operator** karena dilakukan secara manual maka seringkali menimbulkan masalah.

Buat yang tahu bagaimana rumitnya **develop**, **test**, **build** sebuah **source code** diberbagai **environment** atau **os** yang berbeda pasti sering berhadapan dengan **dependency problem**. Setiap sistem boleh jadi memiliki versi **tools**, **interpreter**, **compiler** yang berbeda-beda.

Saat uji coba berjalan dengan baik namun ternyata tidak berjalan saat sudah masuk **production**. Inilah kenyataanya sulit sekali membangun **Consistent Configuration Management** jika kita masih menggunakan **Traditional Software Development**.

### Traditional Software Development

Kurang lebih di bawah ini adalah figur-figur yang ada dalam **Traditional Software Development** :

<img src="/asset/DevOps-Traditional-Software-Management.png" style="zoom:100%;" />

Pada proses **Software Development Life Cycle (SDLC)** di atas umumnya :

**Business Analysts** akan menyusun sebuah **Business Requirement**, selanjutnya **Developers** akan menerjemahkan **Business Requirement** ke dalam kode pemrograman, dan **QA** melakukan **Testing**. Sampai akhirnya tim **SysAdmin** membantu melakukan **Deployment** dan **Monitoring** di **Production**.

Pada perusahaan dan organisasi yang lebih besar sering kali terjadi **Silo Working**, beberapa **departments**, **groups** atau perorangan tidak mau berbagi informasi satu sama lain. Di tambah kompleksitas masing-masing entitas mungkin memiliki preferensi yang berbeda-beda.

**Problem** yang paling sering dan populer disini - **It's Not Works On My Machine Syndrome**

<img src="/asset/DevOps-Silo.png" style="zoom:100%;" />

Jika **problem** komunikasi ini terus berlanjut, maka impaknya adalah produk yang dihasilkan memiliki resiko kegagalan yang lebih tinggi. Biaya yang sangat tinggi, waktu pengerjaan molor dan **performance** yang tidak sesuai ekspektasi **stakeholder**.

Pengembangan dalam **Traditional Software Developmen**t biasanya menggunakan metode **Waterfall**, kelemahan paling menonjol dalam metode **waterfall** adalah pada sebagian besar kasus kurang **adaptable** dan **slow** sehingga memberikan **rate survival** yang sangat kecil. 

![SDLC Model Waterfall | Diaz Astizar](https://astizardiaz.files.wordpress.com/2016/12/waterfall.jpg?w=772)

Terlebih **cost** untuk **fixing bug** berpotensi **deadly** untuk perusahaan, banyaknya **steps** yang harus dilakukan bisa membuat perusahaan kehilangan **revenue**. Malah totoz, bukanya untung malah buntung.

Secara garis besar, hal yang membuat frustasi dalam **Traditional Software Development** adalah :

<img src="/asset\DevOps-Traditional-Software-Development-Problem.png" style="zoom:100%;" /> 

Sebagaimana dikatakan **Lord** **Dogecoin**, **Elon musk** "***Any Product That Needs A Manual is Broken***". Mas Gun sepakat sekali di era otomasi saat ini kalau masih dikerjakan secara manual ya produk gagal.

## DevOps Way

<img src="/asset/DevOps-Problem3.png" style="zoom:100%;" />

Peran seorang **DevOps** berada di antara **Developments** dan **Operations** terlibat secara penuh dalam **Software Development Life Cycle (SDLC)**. Menyelesaikan seluruh permasalahan dalam **Traditional Software Development** menggunakan prinsip-prinsip **Agile** yang radikal.

Dalam beberapa kasus seorang **DevOps** dapat ikut serta dalam proses **development**, namun fokus utamanya tetap menjamin operasi bisnis perusahaan.

<img src="/asset/DevOps-Focus.png" style="zoom:100%;" />

Seorang **DevOps Engineer** juga memperkenalkan bahwa **DevOps** bukan hanya sekedar **roles** tetapi sebuah gagasan yang lebih luas :

<img src="/asset/DevOps-Way.png" style="zoom:100%;" />

**DevOps** adalah gabungan dari sebuah **culture**, **tools** dan **processes** dengan tujuan agar dapat memberikan **business value** lebih cepat. 

### Culture

**Culture** yang membangun kolaborasi antar entitas, melepaskan **silo working** yang terjadi pada **Traditional Software** **Development**. Sebuah **culture** yang membangun tim dengan kemampuan multidisiplin, bukan hanya individu dengan kemampuan multidisiplin ilmu. 

### Tools

Komitmen untuk menentukan **tools** yang akan digunakan dalam perusahaan sangat penting. Jika bagian **Development**, **DevOps engineer** dan **Operations** masih menggunakan ego sektoralnya dalam pengunaan **tools**, maka problema **silo working** akan terjadi lagi. 

**DevOps Engineer** merekomendasikan **tools** yang harus diketahui bagian **development** dan **operations**, **DevOps Engineer** merekomendasikan **tools** yang dapat mempermudah keduanya untuk menyelesaikan pekerjaan. Penggunaan **tools** yang sama agar dapat dengan mudah difahami oleh semua tim.

Dari permasalahan sebelumnya **Traditional Software Development** kita harus berterima kasih untuk mereka yang berjuang dalam gerakan **Open Source**, mereka para pejuang yang menjadi akar keberhasilan karena kini banyak sekali **tools** untuk **DevOps**. 

Kini **DevOps** mulai banyak diakuisisi institusi dan tingkat adopsinya semakin meningkat. Di bawah ini adalah beberapa **DevsOps Open Source Tools** yang terus dikembangkan komunitas :

<img src="/asset/DevOps-Open-Source-Tools.png" style="zoom:100%;" />

Banyak sekali kan? jangan khawatir kita akan mempelajarinya, jika kita bisa menggunakan salah satu **tools** maka kita juga akan memiliki model mental untuk memahami **tools** lainnya.

### Processes

Ketika **Culture** sudah di bangun, komitmen pada **Tools** yang akan digunakan selanjutnya adalah **process** yang harus dilakukan agar kita dapat membangun **High Impact IT System**. Ada beberapa fase yang harus dilalui dimulai dari perencanaan dan kegiatan menentukan prioritas :

<img src="/asset/DevOps-Way2.png" style="zoom:100%;" />

Untuk bisa memahami **CI/CD** kita perlu memahami beberapa **stack technologies** minimum seperti :
**Source Code Management** seperti **git**, **Continuous Integration** seperti **jenkins**, **Cloud Computing** seperti **EC2** pada **Amazon Web Services (AWS)**, **Containerization** seperti **Docker** dan **Artifact Repository Management** seperti **Nexus**.

#### Continuous Integration (CI)

Untuk melakukan **Continuous Integration (CI)**, diperlukan **Source Code Manager** dan **CI Tools** :

<img src="/asset/DevOps-CI.png" style="zoom:100%;" />

Pada **Continuous Integration** **(CI)** kita dapat melakukan otomasi **testing**, **compilation**, atau **build** sebuah **artifact** dan kegiatan otomasi lainnya seperti **static code analysis** yang bermanfaat untuk memeriksa kerentanan dalam **source code application**.

<img src="/asset/DevOps-CI2.png" style="zoom:100%;" />

Selanjutnya dalam **CI Tools** kita dapat membaca seluruh kegiatan otomasi apakah berhasil atau terdapat kegagalan didalamnya :

<img src="/asset/Report.png" style="zoom:30%;" />

Manfaat dari kegiatan ini adalah kita dapat mendeteksi sebuah **issue** yang tidak diinginkan lebih awal, dan terhindar dari masalah **integration hell** yang sering terjadi dalam sebuah **startup**.

#### Continuous Delivery (CD)

Jika seluruh kegiatan yang dibutuhkan telah selesai pada **Continuous Integration (CI)** selanjutnya adalah melakukan **deployment application** kedalam sebuah **non-production environments**, biasanya di sebut dengan **staging**. Kegiatan ini disebut dengan **Continuous Delivery (CD)**.

<img src="/asset/DevOps-CD.png" style="zoom:80%;" />

**Continuous Delivery (CD)** akan menggunakan **application** yang telah disiapkan **Continuous Integration (CI)** untuk di otomasi lebih lanjut. Seperti kegiatan eksekusi **Functional** dan **Acceptance Testing**, baik itu **alpha** atau **beta testing**. 

Untuk menyelesaikan proses **CI/CD** ini kita memerlukan sebuah **Artifact Repository Management** seperti **Nexus**, kita akan mempelajarinya nanti. Pada **Continuous Delivery (CD)** proses **deployment** dilakukan secara manual untuk lingkungan yang sensitif seperti **production environment**. (Manual karena biasanya ada proses **approval** tertentu)

#### Continuous Deployment

**Continuous Deployment** adalah ekstensi tambahan dari **Continuous Delivery (CD)**, statusnya bisa dipertimbangkan sebagai opsi. Setiap perusahaan memiliki **maturity** dan **complexity** yang berbeda-beda. Perbedaanya dengan **Continuous Delivery (CD)** pada **Continuous Deployment** otomasi dilakukan secara **end-to-end**.

<img src="/asset/DevOps-ContinuousDeployment.png" style="zoom:100%;" />

Pada **Continuous Deployment** otomasi **deployment application** terjadi semenjak **Developer** melakukan **code commit**, semuanya akan diotomasi sampai **production**. Karena proses ini cukup **advance**, untuk bisa otomasi sampai **production** diperlukan **wide coverage** dan kemampuan **testing** yang mumpuni mulai dari :

<img src="/asset/DevOps-Deployment.png" style="zoom:100%;" />

Sehingga jarang sekali dilakukan oleh perusahaan-perusahaan yang menganut **devops**, hanya perusahaan-perusahaan yang sudah memiliki para **engineers** dengan kemampuan seperti pasukan **avengers** biasanya melakukan ini.

Pada **Continuous Deployment** tipe **deployment** yang digunakan biasanya **Blue/Green Deployment**. Kita akan membangun sebuah replikasi infrastruktur untuk periode jangka pendek. 

Terdapat Infrastruktur baru yang juga sudah menyediakan aplikasi terbaru yang sedang berjalan, juga mempertahankan infrastruktur lama dengan aplikasi sebelumnya yang tetap berjalan sampai uji coba dianggap selesai. Jika sudah selesai infrastruktur lama akan diberhentikan, infrastruktur terbaru dengan aplikasi versi terbaru digunakan.

Sebelum era **cloud computing** metode ini sangat memakan biaya, namun era **cloud computing** mempermudah dan memperkecil biaya metode **Blue/Green Deployment**.

## Agile Software Development

Gagasan tentang **DevOps** memiliki akar yang kuat dengan prinsip dalam **Agile Software Development**, dengan tujuan improvisasi **software development cyle** yang lebih baik dari sebelumnya (**Traditional Software Development**). Di bawah ini adalah The Agile Manifesto yang ditulis pada tahun 2001 :

- *"Individuals and interactions over processes and tools*
- *Working software over comprehensive documentation*
- *Customer collaboration over contract negotiation*
- *Responding to change over following a plan*
- *That is, while there is value in the items on the right, we value the items on the left more."*

**Agile Software Development** memecahkan permasalahan komunikasi dan pekerjaan repetitif, **error-prone** yang sangat kronis dalam **Traditional Software Development**. 

**Stakeholder** diikut sertakan dalam manajemen **software** **development** dari awal sampai **testing**, sehingga terhindar dari pembuatan fitur yang ternyata tidak dibutuhkan atau memberikan manfaat signifikan.

Pada **Traditional Software Development** jika berhadapan dengan **deadline**, biasanya akan berakhir seperti ini :

<img src="/asset/Meme-Project.jpg" style="zoom:100%;" />

**Agile Software Development** lebih **adaptable** dari **Traditional Software Development**. Saat berhadapan dengan **deadline**, **agile software development** akan mereduksi target pada **final product** dengan mengorbankan beberapa fungsionalitas, bukan mengorbankan kualitas.

### Quick Understanding Market

Salah satu mantra yang menarik dalam **Agile Software Development** adalah :

"*Deliver early and deliver often*"

Jika perusahaan kita bisa melakukan **delivery value** dengan cepat untuk **customer**, kita bisa mendapatkan respon dari **customer** lebih awal pula. Ini sangat penting saat mode validasi atau kompetisi sehingga kita bisa memahami **product** dipasar lebih cepat dibandingkan kompetitor.

<img src="/asset/DevOps-Agile-Mantra.png" style="zoom:100%;" />

Jika anda pernah membaca buku karya **Dan Olsen** yang berjudul **The Lean Product Playbook**, mayoritas kegagalan produk suatu perusahaan adalah tidak tercapainya **Product Market-Fit**. 

<img src="/asset/Product Market Fit.png" style="zoom:100%;" />

## Release Management

Untuk mewujudkan hal tersebut **Delivery Early, Delivery Often**, biasanya kita akan membuat sebuah **Sprint**. Sebuah **Sprint** terdiri dari sekumpulan fungsionalitas yang harus tersedia di dalam **production** dengan periode waktu biasanya per 2 minggu. Manfaat dari aktivitas ini adalah :

1. **Customer** lebih sering mendapatkan **value** dari **product** yang kita buat
2. **Feedback** sampai pada tim **development** per 2 minggu
3. Tim memiliki kemampuan lebih untuk mengukur dan memprediksikan pekerjaan

**Story** adalah sekumpulan fungsionalitas dengan seluruh detil informasi yang dapat difahami oleh t**im development** sebelum **sprint** dimulai. Kumpulan **story** di sebut dengan **product backlogs**, setiap **story** memiliki **story point** yang digunakan sebagai **measure unit** tingkat kompleksitasnya. 

**Story Point** membantu tim **development** untuk bisa melakukan kalkulasi seberapa banyak **story point** yang dapat mereka berikan sampai **sprint** berakhir. 

Inti dari semua kegiatan ini adalah satu bagaimana caranya setiap orang dalam tim harapannya terpenuhi dengan komunikasi yang terbuka, prediksi waktu apa yang sedang kita **delivery**, dan apa saja yang kita butuhkan untuk melakukannya.

Ada banyak **Agile Methodologies** untuk pengembangan **software development**, salah satunya adalah **scrum**. Jika kita bandingkan dengan metodologi lainnya semuanya sama saja fokus pada konsep yang sama, yaitu : 

Peningkatan kualitas komunikasi dan koordinasi antar aktor dalam tim yang sama.

Jika menggunakan metode **agile**, dimana kita akan melakukan **delivery product** versi terbaru yaitu setiap 2 minggu (bi-weekly) maka pola kerja kita sangat konsumtif. Apalagi jika dibandingkan dengan model **release management quarter release** :

1. **Quarter Release** : Rilis 4x selama setahun, belum termasuk **hotfix, emergency release** jika terdapat masalah di production.
2. **Bi-weekly Release** : Rilis selama 1x setiap 2 minggu, belum termasuk **hotfix, emergency release** jika terdapat masalah di **production**. Maka selama setahun terdapat 24 rilis.

Jika kita asumsikan, persiapan untuk rilis memerlukan waktu 10 jam maka :

 <img src="/asset/DevOps-Release-Management.png" style="zoom:100%;" />

Jika kita perhatikan **bi-weekly releases** mengkonsumsi banyak waktu dan energi, apalagi jika terdapat **hotfix problem** yang harus diselesaikan. Solusi dari problema ini adalah **Automation**.

Sekitar tahun 2015-an **tools** untuk melakukan **automation** belum cukup matang, **bash scripting** masih dianggap kurang ideal untuk melakukan perubahan **state** pada **production server**. Namun kini perubahan besar telah datang semenjak **Docker** dan **platform** untuk **orchestration** muncul seperti **kubernetes** atau **Docker Swarm**.

Jika kita menggunakan **kubernetes** untuk proses **deployment time** kita bisa mereduksi pekerjaan berjam-jam atau di atas 10 jam hanya dengan beberapa klik saja. Dengan begitu konsumsi 240 jam selama setahun dapat direduksi kedalam hitungan menit. 

Kita sudah memasuki masa dimana rilis **patch** dalam hitungan menit, atau ternyata kita malah merilis sebuah **bug** yang impaknya cukup serius kita dapat melakukan **rollback** dalam hitungan menit pula.

Dunia sudah berubah guys, **DevOps** tamvan macam kita eksistensinya seksi untuk perusahaan. ea.

## Interesting Notes :

1. Usia **Mainframe** lebih tua dari sistem operasi **linux**, **mainframe** hadir pada tahun 1940an dan pada tahun 1960an **mainframe** sudah mendominasi dunia bisnis. **Linux kernel** hadir tahun **1991**. 
2. IBM membuat **OS** sendiri khusus untuk **mainframe**, **OS/360** dan **OS/390** adalah **OS** untuk **mainframe IBM** sebelum akhirnya diganti dengan penerusnya **z/OS** pada awal tahun 2000an.
3. Tahun 2001 **IBM** yang sudah mengalami keuntungan besar-besaran dari penjualan **mainframe computer** untuk perbankan, penerbangan, pemerintah hingga dunia kesehatan melakukan Investasi **1 Billion US Dollar** untuk pengembangan **OS Linux**.
4. **Mainframe Computer** pertama didesain untuk Departemen Pertahanan Amerika menghadapi perang dingin (**cold war**).
5. Pada **Commodity Server** meskipun memiliki infrastruktur yang bagus terdapat **issue** pada **database**, **special case** pada **SQL Server 2005** memiliki kemampuan untuk memproses **1,379 transactions/sec** dengan total **119 million transactiond/day**.
6. **IBM z13** memiliki kapabilitas untuk memproses **2.5 billion transaction/day**, **IBM z13** di desain untuk **mobile app economy** yang sedang **booming**.  **IBM z13** memiliki kemampuan untuk **encrypt mobile transaction** secara **real-time** dan memberikan insight seluruh transaksi sekaligus, pemerintah & perusahaan dapat membaca **Fraud Detection** saat itu juga.
7. **IBM z15** memiliki kapabilitas untuk memproses **1 trillion web transaction/day** dan menjalankan 2.4 juta **Docker containers** sekaligus.

