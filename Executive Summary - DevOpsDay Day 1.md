# Executive Summary - DevOpsDay Day 1

> #### DevOpsDay Jakarta, Birawa Hall Assembly, Menteng Dalam, Jakarta Selatan

> **Date:** Wed, 24 Jul 2024 8.30 - 17.00

> **Author:** [Haydar Dzaky](craftdocs://users?id=9902b343-5a8a-dfea-2f1e-3daa7db80360) [Muhammad Priandani Nur Ikhsan](craftdocs://users?id=df06ebfc-3d9d-fd44-ce7d-545f82c2614d)

## Sesi 1 : Cloud Native - Fordigi

Speaker : Ari Pratiwi, BNI (Representative)

![Image.png](https://www.pagerduty.com/wp-content/uploads/2021/03/image1-2-1024x612.png)

Fig 1. Lifecycle DevSecOps

![Photo from Library.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/E32BCA8D-C38E-41B6-9417-786CD0F4785F_2/8WM6egkfu9rmBrYrsRXFLHLAhR9cBwDVrdC8dbxEQy0z/Photo%20from%20Library.jpeg)

Fig 2. Lifecycle DevSecOps BNI

#### Balancing workload

- Public cloud

   Cloud yang digunakan untuk komputasi tinggi seperti AI

- Private/Hybrid cloud

   Sebuah prefered strategy untuk semua workload dan sesuai dengan Perlindungan Data Pribadi (PDP)

- On premise

**Microservices & DevSecOps (Best Practices)**

![image.png](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/e1962d91-82a4-429e-b53f-483508a8fe76)

Fig 3. Microservices & DevSecOps Best Practice

**Manfaat DevSecOps untuk BNI**

1. Mampu 3x lebih cepat untuk melakukan deployment
2. Zero downtime.
3. Enchanced Security

---

## Sesi 2: Building a Resiliant IT with DevOps - Narada Code

Speakers: Made Mulia Indrajaya & Christian Hermanus

![images.png](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/DF5CEE8E-6A5B-418B-9782-6DCB920E0A3C_2/sdWtMJaTSgK5eyk849AYIyTPfSwROnvKyrI3Fju6i0Qz/images.png)

Fig 4. The DevOps core model focuses on balancing workloads between public, private, and hybrid clouds, with a preference for on-premise solutions.

![image.png](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/fdb8f9c2-1a5b-405f-9cdb-ef7e86cd556f)

Fig 5. DevOps In a Nutshell

*Engineer the resiliency, failures are to tests, not avoided.*

- Dengan adanya DevOps dapat meningkatkan segala aspek yang ada diantara Dev & Ops
- Terdapat beberapa hal yang harus dipahami dalam melakukan DevOps
   - Resilience Engineering
   - AWS Fail Injection Service
   - Self Healing Infrastructure

---

## Sesi 3: Integrating Backup Into Your CI/CD Pipeline - VEEAM

Speakers: Newin Atmarumeksa & Kelvin Mun

![IMG_4891.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/1073EC18-5E1D-4520-94FE-5693D58BE4BF_2/Ojx8wR03Qe8AWmO1t2cNuuvbRhcuJK4KgTShJSwiLDwz/IMG_4891.jpeg)

Fig 6. CI/CD Overview

DevOps engineer terkadang melakukan kesalahan seperti tidak sengaja menghapus database, miskonfigurasi, atau ketika melakukan migrasi berpotensi gagal.

Kasten dari Veeam menawarkan solusi untuk melakukan backup db secara native secara otomatis ketika dilakukan git commit. Sehingga, ketika terjadi insiden cukup ke restore point dan direcover.

Ketika melakukan migrasi, kasten akan melakukan backup sebelum akhirnya disync ke kubernetes.

![IMG_4892.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/532513BC-7C5C-47B4-9F33-1DE247AE50A1_2/u3oaM9ysmxfJSCKTaVQvx2l2bjUMxsmnhH5lkLgzs6oz/IMG_4892.jpeg)

Fig 7. Protection in Kubernetes

#### Tech Stack:

- ArgoCD
- Kasten K10
- Kubernetes

#### Ada beberapa hal yang harus diperhatikan dalam melakukan CI/CD:

1. Accidents
2. Compliance Requests
3. App Mobility
4. Recovery Experience

---

## Sesi 6: Ensuring Data Privacy & Protection in Continuous Deployment - Opentext

Speaker: Malik Abdul Jabbar, Consultant

"Zero trust = Security strategy that never assume trust, always verifies who's accessing."

#### Jenis Data

- General: name, age, birthday
- Specific: DNA, fingerprint, height
- Enterprise: confidental data

#### *Misconception*

*Data Security != Database security, Database firewall, Database encryption*

![IMG_4896.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/E8AB01A8-401C-4DF0-B976-839F2CF9F5D0_2/XFpKVQc6ZwrfnTaFixtjCNZ4pvUaUDKe5jefZbTLYx0z/IMG_4896.jpeg)

Fig 8. Pada skala enterprise, umumnya database dibagi menjadi beberapa bagian.

#### Jenis database:

- Production merupakan database yang digunakan oleh pengguna
- Data Recovery (DR) / Failover merupakan database replika sebagai backup jika production mengalami gangguan
- Test merupakan database untuk testing
- Routine Backups merupakan database yang rutin dibackup

Pada implementasi sistem, seringkali ditemukan bahwa database mengekspos data plain ketika dilakukan fetching melalui API (lihat warna merah). Sehingga, jika hacker berhasil masuk melalui celah pada endpoint" ini, database dapat terancam.

#### Tipe data yang harus diproteksi:

- **Data-in-Transit**

   Data dalam proses untuk ditransfer atau dikirim dari satu ke lokasi lainnya.

- **Data-in-Use**

   Data yang secara aktif digunakan atau diproses oleh sistem atau user.

- **Data-at-Rest**

   Data yang disimpan pada media storage.

![IMG_4897.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/0F61AA44-DC82-4FB0-9B0D-7A6AAC5F5B3B_2/oyx5elhZngpnDik6bQtSDQ52wjyYTwlbJoa7MUx2JBIz/IMG_4897.jpeg)

Fig 9. Perhatikan bahwa tiap jenis data berpotensi untuk dibajak ditandai oleh warna merah.

### ::Lalu, mengapa tidak kita enkripsi saja semua yang ada di database?::

Encryption atau hashing biasanya dilakukan dalam format base64 dimana ini dapat merubah size data.

*Misal menggunakan **::base64::** hash:*

Vince → VmluY2U=

18 → MTg=

Dapat dilihat size data dan formatnya berubah. Akibatnya, ketika mengatur jumlah nilai maksimum pada kolom tabel di database akan terjadi inkonsistensi dan jenis data menjadi sulit terprediksi karena dapat berubah.

Jadi, bagaimana kita dapat melakukan enkripsi tanpa perlu mengubah data size dan format? Pada standar industri saat ini, digunakan Hyper Format Preserving Encryption (FPE) yang memungkinkan enkrikpsi tanpa perlu merubah format.

![IMG_4898.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/640B5088-0F42-4BD9-974D-5CD5C9189F4C_2/HZ4x9z2UaxFzKTnafeOoqBOst13wfzh7ykYzMFoyCyoz/IMG_4898.jpeg)

Fig 10. FPE dikenalkan melalui paper yang dipublish tahun 2019 silam mengenai enkripsi yang tetap mempertahankan format upper/lower case, jenis data, bahkan special karakter seperti -,_,*,& akan dipertahankan.

![IMG_4899.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/E007F734-E103-4824-AEDC-6B0E8A354DA5_2/BJOMtkSC5bzvvJHhUAd4ZKLsk0OPoxit3xVZ5yP8hDwz/IMG_4899.jpeg)

Fig 10. Post implementation dari FPE memungkinkan proteksi pada seluruh data state

Lebih lanjut, bagaimana kita dapat mengelola siapa saja yang dapat mengakses data. Voltage SecureData dari Opentext memungkinkan kita untuk ngeshare data ke siapa aja, dengan company memegang key untuk mengizinkan person mana yang dapat mengakses porsi dari decrypted data.

![IMG_4900.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/A5B1C093-3554-47F1-B952-DE0785200578_2/nJtF7g8zSTOtH9PUPxhJUCSPjHcRWmANZRczoJPTVeAz/IMG_4900.jpeg)

Fig 11. Zero Trust implementation oleh Voltage SecureData

Gambaran lebih lanjut implementasi dari Voltage dalam skala Enterprise. Tiap endpoint dilengkapi oleh Voltage guna memastikan keamanan end-to-end dari request oleh edge hingga response yang sampai ke edge.

![IMG_4901.jpeg](https://res.craft.do/user/full/604ead3b-1bd5-781b-0dc5-e076e7b9fcdf/doc/FF13AAFF-8D40-4717-AE7E-2B2E7761CF8D/C0B7EC6E-E0FB-44DD-A5DC-D430C5DD4D8B_2/AcNiafRGyzN0bOddddKp4ZOEwEYxMk6it7R2LtqlIoEz/IMG_4901.jpeg)

Fig 12. Voltage Enterprise Scale Implementation

---

### People we met and introduce Safebox to

Mas Didik, Sr. Technical Success Manager @ Snyk, Singapore

Sebian, Sr. Fullstack Dev @ BCA, Jakarta Pusat

Fahri, Frontend Dev @ BCA, Jakarta Pusat

