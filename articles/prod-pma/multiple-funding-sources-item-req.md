---
title: Persyaratan item untuk kontrak proyek dengan beberapa sumber dana
description: Artikel ini berisi informasi tentang cara mengkonfigurasi dan menggunakan persyaratan item dengan beberapa sumber dana.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028477"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Persyaratan item untuk kontrak proyek dengan beberapa sumber dana

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Beberapa perjanjian kontraktual untuk hasil berbasis proyek mungkin memerlukan beberapa sumber dana. Artikel ini menjelaskan cara memilih dan mengkonfigurasi sumber dana yang diinginkan bila diperlukan beberapa sumber untuk proyek atau kontrak proyek.

## <a name="terminology"></a>Terminologi

- **Sumber dana** – Entitas yang dananya digunakan untuk pekerjaan kontrak proyek. Entitas ini dapat merupakan organisasi internal atau akun faktur eksternal (pelanggan atau hibah).
- **Pelanggan proyek** – Entitas yang menerima pekerjaan proyek.
- **Akun faktur** – Entitas eksternal yang membayar untuk pekerjaan proyek.

## <a name="example"></a>Contoh

Contoso telah memenangkan kontrak perpanjangan perlengkapan dengan dua pelanggannya: Adatum AS dan Adatum Corporate. Kontrak mencakup layanan perangkat keras dan penginstalan yang akan dikirim ke Adatum AS (pelanggan proyek). Perangkat keras akan didanai oleh Adatum Corporate (faktur akun 1), dan pekerjaan penginstalan akan didanai oleh Adatum AS (akun faktur 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Mengkonfigurasikan aturan default akun faktur untuk persyaratan item

### <a name="prerequisites"></a>Prasyarat

- Microsoft Dynamics 365 Finance **versi 10.0.27 atau yang lebih baru** harus menggunakan persyaratan item yang memiliki beberapa akun faktur.
- Administrator sistem Anda harus mengaktifkan persyaratan fitur **Izinkan Item dengan beberapa sumber dana untuk skenario berbasis produksi/stok Project Operations** di ruang kerja **manajemen Fitur**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Mengkonfigurasi aturan default akun faktur

Untuk mengkonfigurasi aturan default untuk akun faktur, ikuti langkah-langkah ini.

1. Buka **manajemen proyek dan akuntansi** \> **konfigurasi** \> **parameter manajemen proyek dan akuntansi**.
1. Pada tab **Umum**, di bagian **Pesanan penjualan dan Persyaratan Item**, atur pilihan **izinkan untuk proyek dengan beberapa sumber dana** ke **Ya**.
1. Di bidang **pelanggan Default**, tentukan lokasi pelanggan pengiriman proyek pada persyaratan item yang berasal dari default:

    - **Dari sumber dana** – Pelanggan pengiriman proyek default berasal dari sumber dana. Jika lebih dari satu sumber dana terkait dengan kontrak proyek, maka sumber dana pertama dalam daftar akan digunakan.
    - **Dari proyek** – Pelanggan pengiriman proyek default berasal dari pelanggan yang dipilih pada bidang **akun rekaman Proyek**.

1. Opsional: Atur atau ubah akun faktur default pada rekaman proyek:

    1. Buka **Manajemen proyek dan akuntansi** \> **Proyek** \> **Semua proyek**, lalu buka detail rekaman proyek.
    2. Pada tab **Umum**, atur atau perbarui bidang **akun faktur Default**. Akun yang Anda tentukan akan digunakan sebagai akun faktur default untuk persyaratan item baru yang dibuat untuk proyek. Jika Anda membiarkan bidang kosong, akun faktur dari sumber dana kontrak proyek pertama akan digunakan secara default. Namun, pengguna akan dapat mengubah akun saat mereka menyimpan rekaman.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Pilih akun faktur yang akan digunakan saat Anda membuat persyaratan item

Untuk memilih akun faktur yang akan digunakan saat Anda membuat persyaratan item, ikuti langkah-langkah ini.

1. Buka **Manajemen proyek dan akuntansi** \> **Proyek** \> **Semua proyek**, lalu pilih rekaman proyek.
1. Pilih **Persyaratan item** pada tab **rencana**.
1. Membuat rekaman persyaratan item baru.

    - Secara default, bidang **Akun faktur** di rekaman diatur ke akun faktur yang ditetapkan untuk proyek. Anda dapat mengubah nilai bidang **akun Faktur**, lalu menyimpan rekaman. Setelah rekaman disimpan, Anda tidak dapat lagi memperbarui nilai **akun Faktur**. Jika Anda harus memperbarui nilai **akun Faktur** untuk persyaratan item, hapus persyaratan item yang ada, lalu buat item baru yang memiliki nilai yang diinginkan.
    - Secara default, bidang **Pelanggan** untuk persyaratan item diatur berdasarkan nilai **pelanggan Default** yang diatur pada halaman **parameter manajemen proyek dan akuntansi**.

    Ketika rekaman persyaratan item disimpan, sistem mengaitkannya dengan rekaman header **pesanan penjualan persyaratan Item**. Jika tidak ada header pesanan penjualan yang memiliki akun faktur yang dipilih, sistem akan membuat satu dan mengaitkan baris persyaratan item dengannya.

> [!NOTE]
> Persyaratan item selalu sepenuhnya ditagih ke akun faktur yang diatur di rekaman. Sistem saat ini tidak mendukung aturan alokasi dana yang memiliki persyaratan item dan tidak akan memecah posting berdasarkan konfigurasi aturan alokasi dana.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Membuat persyaratan item dari rekaman perkiraan item

Untuk membuat persyaratan item dari rekaman perkiraan item, ikuti langkah-langkah berikut ini.

1. Buka **Manajemen proyek dan akuntansi** \> **Proyek** \> **Semua proyek**, lalu pilih rekaman proyek.
1. Pilih **Perkiraan item** pada tab **Rencana**.
1. Membuat rekaman perkiraan item baru.
1. Opsional: Pada tab **Proyek**, pada bidang **sumber Dana**, pilih akun faktur yang diinginkan.
1. Pilih **Buat persyaratan item**, dan konfirmasikan pesan yang Anda terima.

    > [!NOTE]
    > Sistem menyalin nilai **sumber Dana** dari rekaman perkiraan item ke rekaman persyaratan item yang baru dibuat.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Akun faktur default saat sistem secara otomatis membuat persyaratan item dari baris pesanan pembelian

Jika pilihan **Buat persyaratan item** diatur ke **Ya** di halaman **parameter manajemen proyek dan akuntansi**, sistem secara otomatis membuat persyaratan item saat baris pesanan pembelian proyek baru disimpan. Secara default, bidang **Akun faktur** dan **persyaratan item** dan diatur ke nilai bidang **akun faktur Default** di rekaman proyek. Sistem saat ini tidak mendukung pembaruan atau mengubah akun faktur untuk rekaman jenis ini.
