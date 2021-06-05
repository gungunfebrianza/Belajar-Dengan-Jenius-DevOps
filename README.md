# Belajar Dengan Jenius DevOps

## So What is DevOps?

Okay karena mas gun seneng banget dengan dunia FinTech dan teknologi perbankan, sebagai generasi yang lahir tahun 90an mas gun melihat perusahaan di bidang FinTech melakukan disrupsi besar-besaran di dunia perbankan. 

Kalau diamati secara detail penyebabnya adalah bank sebagai perusahaan besar kehilangan kemampuan untuk membangun sistem IT yang cost-effective. Wajar saja karena perbankan saat ini masih menggunakan teknologi 90an, **Mainframe Computing** dan Aplikasi yang ditulis menggunakan bahasa tahun 50an, bahasa pemrograman **Cobol**.



DevOps adalah peran baru yang kini eksistensinya vital dalam industry IT, mulai dari sektor perbankan, keuangan, e-commerce dan sebagainya. Kenapa figur **DevOps** di anggap sangat vital? karena figur **DevOps** dapat membantu **To Break things faster** mempercepat **delivery business value** untuk user. 

Figur **DevOps** membuat, perusahaan atau startup bisa berkompetisi dengan baik dipasar, sehingga pasar menjadi lebih kompetitif. 

<img src="/asset/DevOps-Faster-Delivery.png" style="zoom:100%;" />

Figur **DevOps** mulai lahir karena problema **corporate inefficiency** mulai menjadi masalah serius, karena semakin besar perusahaan maka semakin lama perusahaan tersebut menyelesaikan sebuah **task**. 

Industri skala besar seperti pebankan atau e-commerce mereka memiliki dana yang mumpuni, namun jika anda sebuah startup kecil maka anda harus mereduksi biaya dengan cara melakukan **automation**.

<img src="/asset/DevOps-Advantage.png" style="zoom:100%;" />

Terminologi ini sempat muncul sekitar tahun 2007 yang merepresentasikan dua istilah yaitu **Development (Dev)** dan **Operations (Ops)**. Pertama kali diperkenalkan oleh **Patrick Debois** seorang figur di bidang software engineer yang frustasi dalam memanajemen permasalahan yang dihadapi **developer** dan **operations**.

Tahun 2009 istilah DevOps mulai populer setelah Patrick Debois membuat sebuah **conference** dengan nama **DevOpDays**. Event tersebut sukses menjadi perbincangan di kalangan para **software engineer**, gagasan patrick dianggap solutif karena ternyata banyak juga software engineer menghadapi permasalahan yang sama.



**DevOps** membantu memecahkan permasalahan antara **developments** dan **operations**, **developments** cenderung ingin berinovasi dan memberikan delivery produk yang dirilis dengan cepat dan operations yang cenderung ingin bisa menjamin **production system** yang stabil dengan kualitas sistem yang terjaga.

Gagasan tentang **DevOps** memiliki akar yang kuat dengan prinsip dalam **Agile Software Development**, improvisasi **software development cyle** yang lebih baik dari sebelumnya. 

## Quick Understanding Market

Salah satu mantra yang menarik dalam **Agile Software Development** adalah :

"Deliver early and deliver often"

Jika perusahaan kita bisa melakukan delivery value dengan cepat untuk customer, kita bisa mendapatkan respon dari customer lebih awal. Ini sangat penting sehingga kita bisa memahami product kita dipasar lebih cepat dibandingkan kompetitor.

<img src="/asset/DevOps-Agile-Mantra.png" style="zoom:100%;" />

Jika anda pernah membaca buku karya **Dan Olsen** yang berjudul **The Lean Product Playbook**, mayoritas kegagalan produk suatu perusahaan adalah tidak tercapainya **Product Market-Fit**. 

<img src="/asset/Product Market Fit.png" style="zoom:100%;" />

Untuk mewujudkan hal tersebut kita akan membuat sebuah **Sprint** untuk memberikan sekumpulan fungsionalitas ke dalam **production** dengan periode waktu biasanya per 2 minggu. Manfaat dari aktivitas ini adalah :

1. **Customer** lebih sering mendapatkan value dari product yang kita buat
2. **Feedback** sampai pada tim development per 2 minggu
3. Tim memiliki kemampuan lebih untuk mengukur dan memprediksikan pekerjaan

**Story** adalah sekumpulan fungsionalitas dengan seluruh informasi yang dapat difahami oleh t**im development** sebelum **sprint** dimulai. Kumpulan **story** di sebut dengan **product backlogs**, setiap **story** memiliki **story point** yang digunakan sebagai **measure unit** tingkat kompleksitasnya. 

**Story Point** membantu tim **development** untuk bisa melakukan kalkulasi seberapa banyak **story point** yang dapat mereka berikan sampai **sprint** berakhir. 

Inti dari semua kegiatan ini adalah satu bagaimana caranya setiap orang dalam tim harapannya terpenuhi dengan komunikasi yang terbuka, prediksi waktu apa yang sedang kita **delivery**, dan apa saja yang kita butuhkan untuk melakukannya.

Ada banyak **Agile Methodologies** untuk pengembangan **software development**, salah satunya adalah **scrum**. Jika kita bandingkan dengan metodologi lainnya semuanya sama saja fokus pada konsep yang sama, yaitu : peningkatan kualitas komunikasi antar aktor dalam tim yang sama.

## Release Management

Jika menggunakan metode **agile** seperti sebelumnya, dimana kita akan melakukan **delivery product** versi terbaru yaitu setiap 2 minggu (bi-weekly) maka pola kerja kita sangat konsumtif. Apalagi jika dibandingkan dengan model release management quarter release :

1. **Quarter Release** : Rilis 4x selama setahun, belum termasuk hotfix, emergency release jika terdapat masalah di production.
2. **Bi-weekly Release** : Rilis selama 1x setiap 2 minggu, belum termasuk hotfix, emergency release jika terdapat masalah di production. Maka selama setahun terdapat 24 rilis.

Jika kita asumsikan, persiapan untuk rilis memerlukan waktu 10 jam maka :

 <img src="/asset/DevOps-Release-Management.png" style="zoom:100%;" />

Jika kita perhatikan **bi-weekly releases** mengkonsumsi banyak waktu dan energi, apalagi jika terdapat hotfix problem yang harus diselesaikan. Solusi dari problema ini adalah **Automation**.

Sekitar tahun 2015-an tools untuk melakukan automation belum cukup matang, bash scripting masih dianggap kurang ideal untuk melakukan perubahan state pada production server. Namun kini perubahan besar telah datang semenjak Docker dan platform untuk orchestration muncul seperti kubernetes atau docker swarm.

Jika kita menggunakan kubernetes untuk proses deployment time kita bisa mereduksi pekerjaan berjam-jam atau di atas 10 jam hanya dengan beberapa klik saja. Dengan begitu konsumsi 240 jam selama setahun dapat direduksi kedalam hitungan menit. 

Kita sudah memasuki masa dimana rilis patch dalam hitungan menit, atau ternyata kita malah merilis sebuah bug yang impaknya cukup serius kita dapat melakukan rollback dalam hitungan menit pula.

Dunia sudah berubah guys, devops tamvan macam kita eksistensinya seksi untuk perusahaan. ea.



Seorang 