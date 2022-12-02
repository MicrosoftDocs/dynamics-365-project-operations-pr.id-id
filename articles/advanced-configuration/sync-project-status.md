---
title: Menyinkronkan Status Proyek untuk mencegah entri terhadap proyek tertutup
description: Artikel ini menjelaskan cara mensinkronisasi Status Proyek untuk mencegah entri terhadap proyek tidak aktif atau ditutup.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348114"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Menyinkronkan Status Proyek untuk mencegah entri terhadap proyek tertutup

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

## <a name="scenario"></a>Skenario

Contoso melakukan publikasi dengan Microsoft Dynamics 365 Project Operations untuk skenario sumber daya/non-persediaan. Sebagai bagian dari aktivitas bisnis biasa, proyek dapat diselesaikan atau ditahan. Anda dapat menonaktifkan proyek untuk memastikan tidak ada pengeluaran atau faktur yang dihasilkan.

## <a name="solution"></a>Solusi

### <a name="prerequisites"></a>Prasyarat

-   Microsoft Dynamics 365 Finance 10.0.29 atau yang lebih baru harus diinstal.
-   Peta penulisan ganda 1.0.0.3 untuk Proyek V2 (msdyn\_projects) harus diinstal atau dikonfigurasi secara manual seperti dijelaskan di bawah.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Membuat versi terbaru dari peta penulisan ganda Project Operations integration Projects V2

Untuk memperbarui peta Penulisan Ganda Project Operations Projects V2:

1. Buka ruang kerja **manajemen Data**, pilih **Tulis ganda**.
2. Pilih ubin **penulisan ganda**.
3. dari kolom **peta Tabel** T, cari dan pilih **Project V2 (msdyn\_projects)**, lalu pilih Berhenti.
4. Pilih nama peta untuk membuka peta, lalu pilih **[Tidak Ada]**.
5. Dari kotak dialog Pilih kolom, pilih status **statecode \[Project Status\]**, lalu pilih OK. Anda dapat mengetik **state** di nilai filter untuk mempersempit daftar.
6.  Pilih **Tambah atau edit transformasikan** di kolom **jenis peta** untuk mengedit transformasi.
7.  Dari **Jenis Transformasi**, pilih **ValueMap**.
8.  Pilih **Tambah pemetaan nilai**, lalu tambahkan **Kunci** dan **Nilai** berikut:

   Tombol       | Nilai 
   ----------|-------
   InProcess | 0     
   selesai | 1     

![Tangkapan layar yang menampilkan pemetaan penulisan ganda](media/projectstage-dw-mapping.png)

9. Pilih **Simpan**.
10. Dari bagian atas halaman **Penulisan ganda > Project V2 (msdyn_projects)**, pilih **Simpan Sebagai**.
11. Dari **Tambah tabel**, di bidang **Penerbit**, pilih **penerbit Default CDS**.
12. Atur bidang **Versi** ke 1.0.0.3.
13. Ketik **Deskripsi**, lalu pilih **Simpan**.
14. Dari bagian atas halaman **Penulisan ganda > Projects V2 (msdyn_projects)**, pilih **Jalankan** untuk memulai peta, lalu pilih **Ya** jika diminta mengkonfirmasikan sebelum dijalankan. 

### <a name="close-a-newly-completed-project"></a>Menutup proyek yang baru saja selesai

Dynamics 365 Finance menggunakan bidang **tahapan proyek** untuk membedakan antara proyek yang **sedang diproses** atau **selesai**. Proyek yang telah **selesai** tidak dapat menimbulkan pengeluaran atau ditagihkan ke pelanggan.

1. Buka proyek untuk dinonaktifkan.
2. Pilih **Nonaktifkan** dari pita atas.

> [!NOTE]
> Anda dapat menonaktifkan atau menutup proyek karena keduanya akan berperilaku sama dalam konteks Keuangan.

3. Di Finance, buka halaman **Semua daftar proyek**.
4. Konfirmasikan proyek yang dinonaktifkan tidak akan muncul dalam daftar.
5. Dalam filter **tampilkan proyek** di atas daftar, ubah nilai dari **Aktif** ke **Semua**.
6. Anda sekarang akan melihat proyek yang dinonaktifkan.

Jika Anda mencoba mencatat waktu atau pengeluaran terhadap proyek ini di Finance, maka seharusnya Anda tidak melihat proyek yang akan dipilih. Jika Anda memasukkan nomor proyek secara manual pada pengeluaran, Anda akan melihat pesan seperti "Tahapan proyek selesai tidak memungkinkan perekaman di proyek". Faktur dan fungsi penagihan lainnya harus dinonaktifkan karena akan berada dalam konteks proyek tertutup.

