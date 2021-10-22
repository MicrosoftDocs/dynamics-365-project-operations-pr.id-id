---
title: Yang baru di bulan Oktober 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia di penyebaran Project Operations lite oktober 2021 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5eb663f8b7450e4b7add6717aa717050ae94d571
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606774"
---
# <a name="whats-new-october-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Oktober 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

   - Project Operations dalam lingkungan Microsoft Dataverse versi 4.25.0.91
   - Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi version 10.0.21

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- [Pesanan pembelian proyek](../procurement/non-stocked-materials-project-purchase-orders.md) sekarang dapat digunakan untuk pengadaan yang dikelola/disentralisasi departemen pengadaan untuk proyek.
- [Retensi vendor](../procurement/vendor-retention-overview.md) memungkinkan Anda menahan sebagian pembayaran ke vendor.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada halaman Penulisan ganda pada kolom Versi. Untuk mengaktifkan versi baru peta, pilih versi peta tabel, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel yang tidak ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) pada panduan pemecahan masalah Penulisan Ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan harga | 2209402 | Mengoreksi validasi yang mencegah jumlah panjar ditagih saat kontrak proyek dikonfirmasi. |
|   Manajemen peluang | 2227414 | Bidang **Produk**, **Pilihan**, dan **IsProductOverriden** disalin ke detail baris kuotasi dan detail baris kontrak. |
| Penagihan dan harga | 2338357 | Mata uang pada log penggunaan bahan harus default dari mata uang proyek saat proyek dipilih. |
| Waktu dan pengeluaran | 2414777 | Membatalkan persetujuan bila pengeluaran atau entri waktu memiliki lebih dari satu persetujuan proyek terkait harus mungkin. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [412077](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D412077&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020681298%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JT2OvagELTPqep4rOiFTwGYF80KkgSHgBJmd%2BHBBgA8%3D&amp;reserved=0) | Mengizinkan akses peran manajer pembelian ke satu entitas hukum juga memfilter akses ke semua proyek di semua entitas hukum. |
| Manajemen proyek dan akuntansi | [555604](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D555604&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=NGAT/5r0sezqdisYP%2BDzyFDDi5f9gyrr5ZhJZaDLV0k%3D&amp;reserved=0) | Penghapusan estimasi gagal bila fitur, **Aktifkan mata uang kontrak proyek untuk perhitungan perkiraan** diaktifkan. |
| Manajemen proyek dan akuntansi | [564701](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564701&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IyhrFb59YBXjNpJdtPhlEDxoYiFCTrqzQtKZsBZk2DM%3D&amp;reserved=0) | [FRA] Pajak kondisional tidak dihitung dengan benar untuk pembayaran terakhir saat penyimpanan vendor dan pembayaran di muka diterapkan ke faktur pesanan pembelian. |
| Manajemen proyek dan akuntansi | [569250](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569250&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020741035%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YcB6z9MvvtiyT9d8g2GkHXDUcNfnPdxlYsHblbk%2BCXs%3D&amp;reserved=0) | Posting WIP ke buku besar umum di-posting dengan jumlah yang salah. |
| Manajemen proyek dan akuntansi | [581167](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D581167&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020989941%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=9UjX3lX/DOJOPiz%2BlYVge5F3Tpbb%2BUBaN7PVXkpwYJE%3D&amp;reserved=0) | Laporan faktur proyek melewatkan baris. |
| Manajemen proyek dan akuntansi | [598810](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598810&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021408104%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=f2oJYnmjpfUiIKvF6qfLsBcfTjoSOq955%2B87%2BSIh0Io%3D&amp;reserved=0) | Ada masalah dengan kumpulan posting faktur proyek di mana ia memproses dan memposting proposal faktur meskipun baris faktur belum dibuat. |
| Manajemen proyek dan akuntansi | [578970](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D578970&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021876048%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JMg%2BIRbLiSKeIXN/JArWC3hSGFhNhabERbuKzGBKCC8%3D&amp;reserved=0) | Perbarui pembuatan pekerjaan batch perkiraan proyek untuk mendukung pelaksanaan beberapa sub-tugas. |
| Manajemen proyek dan akuntansi | [586034](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586034&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021895962%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MRGsdBRM5spFKDJZ/IjrAoWy%2BGTyFVyUU7SCfFJSj6g%3D&amp;reserved=0) | Transaksi voucher tidak seimbang sebagai "XX/XX/XXXX" (mata uang akuntansi: 0,00 - mata uang pelaporan: 0,01). |
| Manajemen proyek dan akuntansi | [596669](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D596669&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021955698%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IpJrV7LW0CegdNrRXfDqBhLEsy8tlSvlaipvZBQFZVg%3D&amp;reserved=0) | Nomor pengecualian pajak untuk entitas hukum tidak ditampilkan pada faktur proyek cetak. |
| Manajemen proyek dan akuntansi | [598109](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598109&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021975611%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=erjkqXSdKwjU62xNiVEJomzc5JoiiC9U7f6ofrv4KGE%3D&amp;reserved=0) | Konfigurasi urutan angka kontinu saat memposting perkiraan tidak didukung setelah menerapkan KB 4619395. |
| Manajemen proyek dan akuntansi | [602677](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602677&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4TBJC6dKbgZxWQTlyDkTm%2BzHpL%2BJx5ZcueNWkMJfUK4%3D&amp;reserved=0) | Nilai WIP yang dikembalikan dari posting faktur berbeda dengan nilai WIP asli yang diposting dari entri waktu. |
| Manajemen proyek dan akuntansi | [602728](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Ux5tLxoBzA%2BJtbf5MhLB63/GNJqYcBg8PH4tncXLTsM%3D&amp;reserved=0) | Transaksi voucher tidak seimbang dengan benar karena terjadi masalah posting dengan pendapatan tertagih proyek dalam kasus panjar diterapkan. |
| Manajemen proyek dan akuntansi | [607324](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D607324&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022065219%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=I/SwbTsPpFvMkxLIK7JpligW%2B4nlObh3nCCSppVGvhE%3D&amp;reserved=0) | Estimasi proyek hanya dibuat untuk satu periode. |
| Perjalanan dan Pengeluaran | [551911](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D551911&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=fDFL3GM5jXJAzIzxwRlOIaq3/ytSHXnpIzGsC4Jjphg%3D&amp;reserved=0) | Kebijakan permintaan perjalanan diabaikan untuk menyetujui alur kerja tanpa kesalahan. |
| Perjalanan dan Pengeluaran | [563752](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D563752&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SVrkNdniaVfhOjc3Brf1gtrFv3SJpPNQ4JYOGnCOxlQ%3D&amp;reserved=0) | ID proyek baris pengeluaran, dapat ditagih, dan nomor aktivitas tidak disimpan dalam aplikasi pengeluaran seluler. |
| Perjalanan dan Pengeluaran | [569458](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569458&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020750990%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=cC33gCOlM8aa3jR5Hy1Hubf5bszsu2YWwraLLrIYCYk%3D&amp;reserved=0) | Bidang **Tanda Terima Terlampir** diatur ke **Ya** meskipun baris pengeluaran tidak memiliki tanda terima terlampir. |
| Perjalanan dan Pengeluaran | [571334](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D571334&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020760950%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Y6dd19CzWyWPa%2BItpWXBEgUuSx8evJxth6VslSRMYsg%3D&amp;reserved=0) | Pesan kesalahan terjadi saat Anda mencoba mengubah kategori pengeluaran ke **Pribadi**. |
| Perjalanan dan Pengeluaran | [572783](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D572783&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020770904%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=nugD/4Rj3d8CNanZf%2BY3vNm9aRqHoh5vF/bHFZD9UxE%3D&amp;reserved=0) | Setelah transaksi kartu kredit dipecah pada laporan pengeluaran, Anda tidak dapat mengedit pengeluaran induk atau melampirkan tanda terima. |
| Perjalanan dan Pengeluaran | [574252](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574252&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020790818%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=uKYIlgBpKju4jBH%2BK8GXVKCgi6kxSG1AxXVvF75WsbA%3D&amp;reserved=0) | Kebijakan pengeluaran untuk transaksi antar perusahaan dengan ID Proyek tidak berfungsi dengan benar. |
| Perjalanan dan Pengeluaran | [574489](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574489&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=ErBwfDvDtWWzEJP3STHd5kzPjTe7%2B4nCeG02kH64dWU%3D&amp;reserved=0) | Tanggal posting tidak ditemukan untuk laporan pengeluaran yang diposting. |
| Perjalanan dan Pengeluaran | [574504](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574504&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SeW6L68CNpJ86TJ2aNqLZoTMq5PHRfu3542mNkKqf%2Bg%3D&amp;reserved=0) | Ada masalah metode pembayaran dalam aplikasi seluler pengeluaran. |
| Perjalanan dan Pengeluaran | [584799](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D584799&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021129331%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4Q%2B/R9wPra2P/%2BEk63qgSenyNoJMa5OJsBv2Nn9s%2B%2Bo%3D&amp;reserved=0) | Permintaan perjalanan yang dibuat untuk satu pekerja dapat digunakan untuk laporan pengeluaran pekerja lain dan dapat menggunakan permintaan perjalanan sebelum tanggal delegasi. |
| Perjalanan dan Pengeluaran | [586023](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586023&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021169156%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=d9Kmf1ng415Uw0U4aQ5N%2B0RboRmjDW1S2lt91rG9ofc%3D&amp;reserved=0) | Saat pengeluaran dibuat, mengubah nilai dimensi keuangan tidak diperbarui dengan benar di tingkat distribusi akuntansi di ruang kerja **manajemen Pengeluaran**. |
| Perjalanan dan Pengeluaran | [586081](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586081&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021179116%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=LlWjcIANIl1gudmiD4WIsluKkF21w9EgVC5uDvBOzg4%3D&amp;reserved=0) | Status persetujuan baris pengeluaran utama tidak tersinkronisasi dengan status persetujuan alur kerja baris terperinci. |
| Perjalanan dan Pengeluaran | [590544](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D590544&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021318495%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MolkGywocB%2BG404npaOv7fcfunnlDUGgAYFOcw8OlKg%3D&amp;reserved=0) | Kesalahan terjadi saat posting laporan pengeluaran saat **pemulihan pajak** diaktifkan di parameter manajemen Pengeluaran. |
| Perjalanan dan Pengeluaran | [564851](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564851&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021856138%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YBsBJdzH%2BqbGzq07u7WILEs%2Bi5Ap6WYzqWnpGWcI4Ac%3D&amp;reserved=0) | Delegasi tidak dapat menghapus dokumen pengeluaran untuk karyawan yang diberhentikan. |
| Perjalanan dan Pengeluaran | [587306](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D587306&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021905919%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=TbWDuK1sHY//jTw%2BmehJG3M3N3feEl2oRkTMTkqWOVE%3D&amp;reserved=0) | Menghapus baris pengeluaran memerlukan waktu lama dan mempengaruhi kinerja. |
| Perjalanan dan Pengeluaran | [600455](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D600455&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021995524%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MH0sIRbAKhNNyAgYZzO9NovWHM7ZWKsoZYqXCIVHJ5A%3D&amp;reserved=0) | **TrvExpTrans** menyebabkan rekaman **TaxUncommitted** tanpa induk dengan hanya menghapus **SourceDocumentLine**. |