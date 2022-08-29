---
title: Sinkronkan Status Proyek untuk mencegah masuk terhadap proyek yang ditutup
description: Artikel ini menjelaskan cara menyinkronkan Status Proyek untuk mencegah masuk terhadap proyek yang tidak aktif atau tertutup.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinkronkan Status Proyek untuk mencegah masuk terhadap proyek yang ditutup

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

## <a name="scenario"></a>Skenario

Contoso aktif dengan Microsoft Dynamics 365 Project Operations untuk skenario sumber daya/tidak tersedia. Sebagai bagian dari kegiatan bisnis normal, proyek dapat diselesaikan atau ditunda. Anda dapat menonaktifkan proyek untuk memastikan tidak ada pengeluaran atau faktur yang dihasilkan.

## <a name="solution"></a>Solusi

### <a name="prerequisites"></a>Prasyarat

-   Microsoft Dynamics 365 Keuangan 10.0.29 atau yang lebih baru harus diinstal.
-   1.0.0.3 peta Tulis Ganda untuk Proyek V2 (proyek msdyn\_) harus diinstal atau dikonfigurasi secara manual seperti yang dijelaskan di bawah ini.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Membuat versi terbaru dari peta tulis ganda Project Operations Integration Projects V2

Untuk memperbarui peta tulis ganda Project Operations Projects V2:

1. Buka Ruang **kerja manajemen** data dan pilih **Tulis ganda**.
2. Pilih ubin **Tulis** ganda.
3. Dari kolom peta Tabel T **, temukan dan pilih** Proyek V2 (proyek msdyn **)\_, lalu pilih** Berhenti.
4. Pilih nama peta untuk membuka peta lalu pilih **[Tidak Ada]**.
5. Dari kotak dialog Pilih kolom, pilih **status \[Status\]** Proyek lalu pilih OK. Anda bisa mengetikkan **status** dalam nilai filter untuk mempersempit daftar.
6.  Pilih **Tambahkan atau edit transformasi** di **kolom jenis** peta untuk mengedit transformasi.
7.  Dari **Transform type** pilih **ValueMap**.
8.  Pilih **Tambahkan pemetaan** nilai, lalu tambahkan Kunci **dan** Nilai **berikut**:

   Tombol       | Nilai 
   ----------|-------
   Dalam Proses | 0     
   selesai | 1     

![Cuplikan layar memperlihatkan pemetaan tulis ganda](media/projectstage-dw-mapping.png)

9. Pilih **Simpan**.
10. Dari bagian atas **halaman Dual-write > Projects V2 (msdyn_projects),** pilih **Save As**.
11. Dari **Tambahkan tabel** di **bidang Publisher**, pilih **Publisher** Default CDS.
12. Atur bidang **Versi** ke 1.0.0.3.
13. Ketik **Deskripsi**, lalu pilih **Simpan**.
14. Dari bagian atas **halaman Dual-write > Projects V2 (msdyn_projects),** pilih **Run** untuk memulai peta, lalu sekect **Yes** jika diminta untuk mengonfirmasi sebelum dijalankan. 

### <a name="close-a-newly-completed-project"></a>Menutup proyek yang baru selesai

Dynamics 365 Finance menggunakan **bidang tahap** proyek untuk membedakan antara proyek **dalam proses** atau **selesai**. **Proyek yang sudah selesai** tidak dapat menimbulkan biaya atau ditagihkan kepada pelanggan.

1. Buka proyek untuk menonaktifkan.
2. Dari pita, pilih **Nonaktifkan**.

> [!NOTE]
> Anda dapat menonaktifkan atau menutup proyek karena keduanya akan berperilaku sama dalam konteks Keuangan.

3. Di Keuangan, buka halaman **Daftar** semua proyek.
4. Konfirmasikan bahwa proyek yang dinonaktifkan tidak muncul dalam daftar.
5. **Dalam filter perlihatkan proyek** di atas daftar, ubah nilai dari **Aktif** ke **Semua**.
6. Anda sekarang akan melihat proyek yang dinonaktifkan.

Jika Anda mencoba mencatat waktu atau pengeluaran terhadap proyek ini di Keuangan, Anda seharusnya tidak melihat proyek untuk dipilih. Jika Anda memasukkan nomor proyek secara manual dengan biaya tertentu, Anda akan melihat pesan seperti "Tahap proyek selesai tidak mengizinkan perekaman dalam proyek". Faktur dan fungsi penagihan lainnya harus dinonaktifkan karena akan berada dalam konteks proyek tertutup.

