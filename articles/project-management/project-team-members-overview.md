---
title: Anggota tim proyek
description: Topik ini menyediakan informasi tentang cara bekerja dengan informasi anggota tim proyek, atribut, dan penjadwalan.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078375"
---
# <a name="project-team-members"></a>Anggota tim proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anggota tim proyek adalah peserta proyek yang menyelesaikan pekerjaan pada proyek. Tujuan kisi anggota tim adalah menyediakan daftar sumber daya bernama yang berkomitmen terhadap keterlibatan, dan anggota tim umum yang merupakan sumber daya placeholder dan akan diisi nanti.

Dari kisi anggota tim, manajer proyek dan peserta proyek lainnya memiliki kemampuan untuk melihat siapa yang telah berkomitmen terhadap proyek. Mereka juga dapat melihat ringkasan Pemesanan mereka, upaya yang direncanakan, dan penetapan sumber daya individual. Kisi anggota tim memungkinkan manajer proyek menentukan persyaratan sumber daya untuk anggota tim Umum dan mengelola Pemesanan anggota tim yang ada.

Tabel berikut berisi daftar atribut kunci dari anggota tim proyek.

| Nama bidang          | KETERANGAN                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metode alokasi        | Metode alokasi yang digunakan untuk memesan sumber daya pada proyek.                                                                         |
| Jenis Penagihan             | Pilih apakah anggota tim diklasifikasikan sebagai dapat ditagih.                                                                                                                                       |
| Sumber Daya Dapat Dipesan        | Sumber daya dapat dipesan yang dipilih untuk menggantikan sumber daya umum.                                                                                                                   |
| Status Penghapusan            | Status penghapusan anggota tim untuk melacak apakah ada permintaan penghapusan yang dikirim ke PSS dan apakah PSS berhasil mengirim respons kembali dan dalam jendela waktu yang diperkirakan. |
| Upaya Total (Jam)     | Jumlah upaya anggota tim pada tugas mereka.                                                                                                                         |
| Upaya Selesai (Jam) | Pelacakan upaya yang dilakukan oleh anggota tim pada tugas mereka.                                                                                           |
| Upaya Tersisa (Jam) | Pelacakan upaya yang belum dilakukan oleh anggota tim pada tugas mereka.                                                                                    |
| Selesai                   | Tanggal akhir keanggotaan tim sumber daya.                                                                                                                                            |
| Jam Pasti Dipesan        | Jam yang dipesan secara definitif terhadap anggota tim.                                                                                                                                                                |
| Nama Posisi            | Nama yang digunakan untuk mengidentifikasi sumber daya umum.                                                                                                                                   |
| Unit Sumber Daya          | Unit organisasi sumber daya yang melakukan pekerjaan.                                                                                                                      |
| Pemberi Persetujuan Proyek         | Pilih apakah anggota tim dapat menyetujui waktu dan pengeluaran.                                                                                                                     |
| Jam yang Diperlukan           | Jam yang diperlukan oleh anggota tim dari persyaratan anggota tim.                                                                                                                       |
| Peran                     | Peran yang diisi anggota tim pada tim ini.                                                                                                                                |
| Deskripsi Posisi     | Masukkan keterangan peran untuk anggota tim ini.                                                                                                                             |
| Jam Sementara Dipesan        | Jam yang dipesan secara tentatif terhadap anggota tim.                                                                                                                                                                 |
| Pangkal                    | Tanggal mulai keanggotaan tim sumber daya.                                                                                                                                          |

Dari kisi anggota tim, tindakan berikut dapat diambil:

- **Pesan** : untuk organisasi yang mengeksekusi metodologi Pemesanan hibrid, tindakan pesan akan memungkinkan pengguna memesan sumber nama berdasarkan persyaratan yang diperlukan yang dihasilkan dari anggota tim generik
- **Membuat persyaratan** : tindakan ini menghasilkan persyaratan.
- **Tentukan pola** : memungkinkan manajer proyek menyesuaikan kontur kebutuhan sumber daya pada tingkat rinci. Manajer proyek dapat menyesuaikan kebutuhan spesifik proyek dalam kasus saat distribusi default tidak sesuai.
- **Ajukan permintaan** : untuk organisasi yang menggunakan metodologi Pemesanan pusat.
- **Edit** : atribut anggota tim dapat diedit termasuk unit organisasi, peran, dan nama posisi.
- **Memelihara Pemesanan** : bila Pemesanan sumber daya perlu diperbarui, pelihara Pemesanan memungkinkan manajer proyek menyesuaikan:

    - Pangkal
    - End
    - Alokasi usaha Total

- **Baru** Selain menambahkan sumber daya langsung dari jadwal, manajer proyek dapat menambahkan anggota tim baru bernama atau generik dari kisi anggota tim.
- **Hapus** : dengan memilih satu atau beberapa anggota tim, manajer proyek dapat menghapus sumber daya yang tidak lagi akan berpartisipasi dalam proyek. Menghapus anggota tim juga akan menghapus semua tugas sumber daya terkait dan membatalkan semua Pemesanan yang ada.
