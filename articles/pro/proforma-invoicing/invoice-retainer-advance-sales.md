---
title: Menagih uang muka atau panjar
description: Artikel ini memberikan informasi tentang cara menagih retainer atau uang muka dalam Operasi Proyek.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 044186d5c7759866dec3883103acec19cb571c11
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914498"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Menagih uang muka atau panjar

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mendukung kontrak berbasis uang muka dan panjar. Pada kontrak proyek, Anda dapat merekam jadwal panjar atau uang muka satu kali. Namun, rekaman pada tingkat kontrak proyek tidak segera membuat panjar atau uang muka tersedia untuk digunakan. Untuk menggunakan panjar atau uang muka pada faktur yang sebenarnya menagih pelanggan, panjar atau uang muka harus ditagih terlebih dulu.

Selesaikan langkah berikut untuk menagih panjar atau uang muka.

1. Pilih **penjualan** > **Penagihan** > **Panjar atau uang muka**. 
2. Di halaman **Panjar atau uang muka**, gunakan filter untuk memilih panjar atau uang muka untuk ditagih dan tandai **siap faktur**.
3. Buat faktur baik secara manual dari Daftar **kontrak proyek** atau halaman rincian. Panjar atau uang muka ditampilkan pada draf faktur di Bagian **panjar atau uang muka** di halaman **faktur**.
4. Konfirmasikan Faktur. Ini akan membuat panjar atau uang muka tersedia untuk digunakan. Anda dapat memverifikasi faktur pada halaman daftar **Panjar atau uang muka**. Untuk Panjar atau uang muka yang ditagih, jumlah yang tersedia akan ditampilkan di kisi.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Membuat panjar atau uang muka dari kisi faktur

Anda dapat membuat panjar atau uang muka langsung pada faktur.

1. Pada faktur draf, pada subkisi **panjar atau uang muka**, pilih **baru** untuk membuat panjar atau uang muka baru. 
2. Pada halaman **Buat cepat**, tambahkan informasi yang diperlukan, lalu pilih **Simpan**. Panjar atau uang muka dibuat pada kontrak proyek yang terkait dengan faktur. Panjar atau uang otomatis ditandai sebagai **siap faktur** lalu ditambahkan ke subkisi **Panjar atau uang muka** di halaman **faktur**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Rekonsiliasi uang muka atau panjar yang ditagih

Setelah panjar atau uang muka ditagih, mereka dapat digunakan, atau didamaikan direkonsiliasi pada faktur dengan waktu, pengeluaran, tonggak waktu, atau biaya berbasis proyek lainnya. Pelanggan akan melihat jumlah faktur yang dikurangi dengan jumlah panjar atau uang muka yang digunakan pada faktur ini.

Pada setiap faktur yang dibuat untuk kontrak proyek yang telah ditagih panjar atau uang mukanya, Project Operations secara otomatis menerapkan panjar atau uang muka ke faktur.

Hal ini dapat dilihat di kisi **panjar atau uang muka yang diterapkan** di halaman **faktur**. Tabel berikut menyediakan informasi tentang bidang pada kisi **panjar atau uang muka yang diterapkan** pada halaman **faktur** proyek.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| KETERANGAN | Kisi **panjar atau uang muka yang diterapkan** di halaman **faktur proyek** |Bidang hanya baca ini memberikan deskripsi panjar atau uang muka yang digunakan pada faktur ini. Nilai ini tidak dapat diubah di faktur. Nilai ini dapat diperbarui pada subkisi pada halaman **kontrak proyek**. | Bidang ini dapat ditampilkan kepada pelanggan pada faktur tercetak untuk menunjukkan panjar atau uang muka mana yang diterapkan pada faktur. |
| Dikirim Pada | Kisi **panjar atau uang muka yang diterapkan** di halaman **faktur proyek**  | Bidang hanya baca ini memberikan tanggal faktur panjar atau uang muka yang digunakan pada faktur ini. Nilai ini tidak dapat diubah di faktur. Nilai ini dapat diperbarui pada subkisi pada halaman **kontrak proyek**. | Bidang ini dapat ditampilkan kepada pelanggan pada faktur tercetak untuk menunjukkan tanggal ketika panjar atau uang muka pertama kali ditagih ke pelanggan. |
| Jumlah | Kisi **panjar atau uang muka yang diterapkan** di halaman **faktur proyek**  | Bidang hanya baca ini memberikan jumlah panjar atau uang muka yang digunakan pada faktur ini. Nilai ini tidak dapat diubah di faktur. Nilai ini dapat diperbarui pada subkisi pada halaman **kontrak proyek**. | Bidang ini dapat ditampilkan kepada pelanggan pada faktur tercetak untuk menunjukkan jumlah asli panjar atau uang muka yang dibayar oleh pelanggan. |
| Jumlah Digunakan | Kisi **panjar atau uang muka yang diterapkan** di halaman **faktur proyek**  | Bidang hanya baca ini memberikan nilai yang dihitung yang merangkum berapa banyak panjar atau uang muka telah digunakan. | Bidang ini dapat ditampilkan kepada pelanggan pada faktur tercetak untuk menunjukkan jumlah dari panjar atau uang muka yang telah digunakan. |
| Jumlah Kelipatan | Kisi **panjar atau uang muka yang diterapkan** di halaman **faktur proyek**  | Bidang yang bisa diedit ini memberikan jumlah panjar atau uang muka yang digunakan pada faktur proyek ini. Jumlah ini tidak dapat lebih dari yang tersedia di uang muka. Sistem secara otomatis mengkalkulasi ini sebagai perbedaan antara bidang **jumlah** dan **jumlah yang digunakan** pada kisi. Anda dapat mengurangi jumlah ini untuk menggunakan kurang dari yang tersedia, namun Anda tidak dapat meningkatkan jumlah untuk menggunakan lebih dari yang tersedia. | Bidang ini dapat ditampilkan kepada pelanggan pada faktur tercetak untuk menunjukkan jumlah dari panjar atau uang muka yang digunakan di faktur. |
| Jumlah Panjar Saldo. | Kisi **panjar atau uang muka yang diterapkan** di halaman **faktur proyek**  | Bidang hanya baca ini memberikan nilai berapa banyak panjar atau uang muka akan tersisa setelah faktur dikonfirmasi. | Bidang ini dapat ditampilkan kepada pelanggan pada faktur tercetak untuk menunjukkan jumlah yang akan tersisa dari panjar atau uang muka setelah fakturdikonfirmasi dan dibayar. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]