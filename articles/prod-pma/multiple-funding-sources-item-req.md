---
title: Persyaratan item untuk kontrak proyek dengan beberapa sumber pendanaan
description: Ini topik memberikan informasi tentang cara mengkonfigurasi dan menggunakan persyaratan item dengan beberapa sumber pendanaan.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728087"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Persyaratan item untuk kontrak proyek dengan beberapa sumber pendanaan

_**Berlaku untuk:** Project Operations untuk skenario berbasis stok/produksi_

Beberapa perjanjian kontraktual untuk kiriman berbasis proyek mungkin memerlukan banyak sumber pendanaan. Ini topik menjelaskan cara memilih dan mengkonfigurasi sumber pendanaan yang diinginkan ketika beberapa sumber diperlukan untuk proyek atau kontrak proyek.

## <a name="terminology"></a>Terminologi

- **Sumber pendanaan** – Entitas yang mendanai pekerjaan kontrak proyek. Entitas ini dapat berupa organisasi internal atau akun faktur eksternal (pelanggan atau hibah).
- **Pelanggan** proyek – Entitas tempat pekerjaan proyek dikirim.
- **Akun** faktur – Entitas eksternal yang membayar untuk pekerjaan proyek.

## <a name="example"></a>Contoh

Contoso telah memenangkan kontrak perpanjangan peralatan dengan dua pelanggannya: Adatum US dan Adatum Corporate. Kontrak tersebut mencakup layanan perangkat keras dan instalasi yang akan dikirimkan ke Adatum US (pelanggan proyek). Perangkat keras akan dibiayai oleh Adatum Corporate (akun faktur 1), dan pekerjaan instalasi akan dibiayai oleh Adatum US (akun faktur 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Menyiapkan aturan default akun faktur untuk persyaratan item

### <a name="prerequisites"></a>Prasyarat

- Microsoft Dynamics 365 Keuangan dan Operasi **versi 10.0.27 atau yang lebih baru** diharuskan menggunakan persyaratan item yang memiliki beberapa akun faktur.
- Administrator sistem Anda harus mengaktifkan **fitur Izinkan Item dengan beberapa sumber pendanaan untuk skenario** operasi proyek yang ditebar/berbasis produksi di **ruang kerja manajemen** fitur.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Menyiapkan aturan default akun faktur

Untuk menyiapkan aturan default untuk akun faktur, ikuti langkah-langkah berikut.

1. Buka **manajemen proyek dan akuntansi** \> **konfigurasi** \> **parameter manajemen proyek dan akuntansi**.
1. **Pada tab Umum**, di **bagian Pesanan penjualan dan persyaratan** Item, atur **opsi Izinkan untuk proyek dengan beberapa sumber** pendanaan menjadi **Ya**.
1. **Di bidang Pelanggan** default, tentukan dari mana pelanggan pengiriman proyek pada persyaratan item berasal secara default:

    - **Dari sumber** pendanaan – Pelanggan pengiriman proyek default berasal dari sumber pendanaan. Jika beberapa sumber pendanaan dikaitkan dengan kontrak proyek, sumber pendanaan pertama dalam daftar akan digunakan.
    - **Dari proyek** – Pelanggan pengiriman proyek default berasal dari pelanggan yang dipilih di **bidang akun** catatan Proyek.

1. Opsional: Mengatur atau mengubah akun faktur default pada catatan proyek:

    1. **Buka Proyek manajemen proyek dan proyek** \> **akuntansi** \> **Semua proyek**, dan buka detail catatan proyek.
    2. **Pada tab Umum**, atur atau perbarui **bidang Akun** faktur default. Akun yang Anda tentukan akan digunakan sebagai akun faktur default untuk persyaratan item baru yang dibuat untuk proyek. Jika Anda membiarkan bidang kosong, akun faktur dari sumber pendanaan kontrak proyek pertama akan digunakan secara default. Namun, pengguna akan dapat mengubah akun saat mereka menyimpan catatan.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Pilih akun faktur yang akan digunakan saat Anda membuat persyaratan item

Untuk memilih akun faktur yang akan digunakan saat Anda membuat persyaratan item, ikuti langkah-langkah berikut.

1. **Buka Proyek manajemen proyek dan proyek** \> **akuntansi** \> **Semua proyek**, dan pilih catatan proyek.
1. Pada tab **Paket**, pilih **Persyaratan item**.
1. Buat catatan persyaratan item baru.

    - Secara default, **bidang Akun** faktur dalam catatan diatur ke akun faktur yang ditetapkan untuk proyek. Anda dapat mengubah nilai **bidang Akun** faktur lalu menyimpan catatan. Setelah catatan disimpan, Anda tidak dapat lagi memperbarui **nilai akun** Faktur. Jika Anda harus memperbarui **nilai akun** Faktur untuk persyaratan item, hapus persyaratan item yang ada, lalu buat yang baru yang memiliki nilai yang diinginkan.
    - Secara default, **bidang Pelanggan** untuk persyaratan item diatur berdasarkan **nilai pelanggan** Default yang ditetapkan pada **halaman parameter** manajemen proyek dan akuntansi.

    Saat catatan persyaratan item disimpan, sistem mengaitkannya dengan **catatan header pesanan** penjualan persyaratan Item. Jika tidak ada header pesanan penjualan terbuka yang memiliki akun faktur yang dipilih, sistem akan membuatnya dan mengaitkan baris persyaratan item dengannya.

> [!NOTE]
> Persyaratan item selalu ditagih sepenuhnya ke akun faktur yang diatur dalam catatan. Sistem saat ini tidak mendukung aturan alokasi dana yang memiliki persyaratan item, dan tidak akan membagi posting berdasarkan pengaturan aturan alokasi pendanaan.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Membuat persyaratan item dari catatan perkiraan item

Untuk membuat persyaratan item dari catatan perkiraan item, ikuti langkah-langkah berikut.

1. **Buka Proyek manajemen proyek dan akuntansi** \> **Semua** \> **proyek** dan pilih catatan proyek.
1. Pada tab **Paket**, pilih **Perkiraan item**.
1. Buat catatan perkiraan item baru.
1. Opsional: Pada **tab Proyek**, di **bidang Sumber pendanaan**, pilih akun faktur yang diinginkan.
1. Pilih **Buat persyaratan** item, dan konfirmasikan pesan yang Anda terima.

    > [!NOTE]
    > Sistem menyalin **nilai sumber** Pendanaan dari catatan perkiraan item ke catatan persyaratan item yang baru dibuat.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Akun faktur default saat sistem secara otomatis membuat persyaratan item dari baris pesanan pembelian

**Jika opsi Buat persyaratan** item diatur ke **Ya** pada **halaman Parameter** manajemen proyek dan akuntansi, sistem secara otomatis membuat persyaratan item saat baris pesanan pembelian proyek baru disimpan. Secara default, **bidang akun** Faktur dan **persyaratan** item diatur ke nilai **bidang Akun** faktur default dalam catatan proyek. Sistem saat ini tidak mendukung pembaruan atau perubahan akun faktur untuk catatan jenis ini.
