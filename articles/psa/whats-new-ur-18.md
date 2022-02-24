---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 18, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147207"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation Pembaruan Rilis 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365. Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan. Rilis ini kompatibel dengan Dynamics 365 9. x. Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan. Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 18. Versi ini memiliki nomor pembuatan V3.10.8.12 dan umumnya tersedia melalui pembaruan mandiri pada April 2020.

## <a name="update-release-18"></a>Pembaruan rilis 18

### <a name="bug-fixes"></a>Perbaikan bug

**Waktu dan Pengeluaran**

- Diperbaiki: aliran **penarikan**, **permintaan**, dan **membatalkan persetujuan** menghasilkan pengecualian dengan pesan kesalahan tidak jelas.
- Diperbaiki: saat **membatalkan persetujuan** gagal untuk pengeluaran, kesalahan pengecualian yang relevan tidak dihasilkan.
- Diperbaiki: kisi waktu entri salah menangani hari non-kerja di Australia setelah beralih ke Daylight Savings Time (DST) di Oktober.
- Diperbaiki: logika default yang salah mencegah pengajuan pengeluaran.
- Diperbaiki: bila persetujuan entri waktu gagal, persetujuan tetap dalam status **tertunda**.
- Diperbaiki: kesalahan SQL pada persetujuan massal (kemacetan/batas waktu).
- Diperbaiki: masalah kinerja yang signifikan dalam pengalaman pengguna yang disebabkan oleh memperbarui anggota tim saat menyetujui entri waktu.

**Manajemen proyek**

- Diperbaiki: pemberitahuan zona waktu dipindahkan dari tampilan **rekonsiliasi** ke formulir utama **proyek**.
- Diperbaiki: template kalender tidak dengan benar disetel ke format otomatis saat formulir proyek baru terbuka.
- Diperbaiki: untuk browser berbasis Chromium, pengguna tidak dapat dengan mudah memilih tugas pendahulu untuk dihapus.
- Diperbaiki: membuat atau menyalin **proyek dari template kosong** mengambil tugas yang tidak terkait.
- Diperbaiki: di kasus tepi tertentu, membuat tugas baru dari kisi tugas menyebabkan rekaman duplikat dibuat.
- Diperbaiki: dalam mode manual, pengguna tidak dapat memperbarui tanggal mulai tugas agar lebih belakangan dari tanggal saat ini yang disimpan.

**Manajemen sumber daya**

- Diperbaiki: baris subtotal tampilan **rekonsiliasi** salah menghitung Pemesanan setelah memperpanjang Pemesanan.
- Diperbaiki: tampilan **rekonsiliasi** salah menampilkan tugas sumber daya saat sumber daya dapat dipesan memiliki kalender yang tidak cocok dengan kalender proyek.

**Sales**

- Diperbaiki: bila entri waktu disetujui ulang (**setujui > Batalkan >** setujui lagi), nilai aktual tidak dikenai biaya duplikat dibuat.
