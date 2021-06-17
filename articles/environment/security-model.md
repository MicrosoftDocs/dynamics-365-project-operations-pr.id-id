---
title: Model keamanan
description: Topik ini memberikan informasi tentang model keamanan di Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ccca2f387ce3abef3b24cb96fdbcc69f3c0c075b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002248"
---
# <a name="security-model"></a>Model keamanan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations berisi model keamanan unik yang memungkinkan model keamanan bisnis berbasis peran yang berkolaborasi dengan Grup Microsoft Office. 


## <a name="security-roles"></a>Peran keamanan
Kemampuan Front-end Project Operations mencakup peran berikut:

| Peran                          | KETERANGAN                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Manajer praktik              | Mendukung pelaporan lintas-proyek.                                                                                                            | Unit bisnis              |
| Pemberi Persetujuan Proyek              | Menyetujui waktu dan pengeluaran proyek.                                                                                                                              | Unit bisnis |
| Administrator penagihan proyek | Membuat proposal faktur.                                                                                                                                                 | Unit bisnis |
| Manajer Proyek               | Membuat rencana proyek dan meminta sumber daya.                                                                                                                              | Unit bisnis |
| Sumber Daya Proyek              | Anggota tim yang dapat dipesan dan waktu laporan.                                                                                                          | Unit bisnis|
| Manajer Sumber Daya              | Semua fungsi manajemen sumber daya, seperti memenuhi permintaan sumber daya dan Pemesanan, dipisahkan untuk mendukung konfigurasi manajer proyek hibrida + manajer sumber daya dan peran Manajer sumber daya tunggal dan terpusat. | Unit bisnis |


Microsoft Project untuk web mencakup peran berikut:

| Peran           | KETERANGAN                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Pengguna proyek   | Pengguna kolaboratif proyek yang mampu membuat proyek mereka sendiri dan melihat proyek yang dibagikan dengan mereka. | Pengguna   |
| Sistem proyek | Peran yang digunakan untuk konteks aplikasi. Pelanggan tidak boleh menggunakan peran sistem ini.                                    | Global |

## <a name="security-enforcement"></a>Penegakan keamanan
Tindakan yang dilakukan di tingkat proyek dilakukan dalam konteks pengguna yang masuk. Ini berarti bahwa untuk membuat, membuka, atau menghapus suatu proyek, pengguna diharuskan memiliki akses yang tersedia dalam CDS. Akses dalam CDS dapat diberikan melalui salah satu mekanisme yang mungkin tercakup dalam platform. Misalnya, pengguna dengan cakupan yang lebih besar dapat mengakses proyek atau jika tindakan berbagi proyek eksplisit telah dilakukan yang memberikan akses kepada pengguna.

Penting untuk mempertimbangkan hal ini saat membuat proyek di Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Kolaborasi grup modern dengan Project Operations
Proyek untuk web dan Project Operations mendukung grup modern untuk kolaborasi. Pengguna yang ditambahkan ke proyek melalui Grup dapat mengedit rencana proyek.

Proyek untuk web menambahkan pengguna ke grup secara otomatis setelah penetapan.

Grup memungkinkan izin proyek dan mendukung artefak kolaborasi agar dapat dikerjakan secara kolaboratif. Diagram berikut menggambarkan peristiwa dan perubahan status yang terjadi selama proses penetapan grup.

Project Operations tidak membuat grup melalui tindakan implisit dan hanya melakukannya melalui tindakan eksplisit grup penekan.

Pencarian anggota grup di dialog **manajemen grup**, terbatas untuk mereka yang ditetapkan sebagai bagian dari grup keamanan lingkungan. Untuk informasi lebih lanjut, lihat [Mengontrol akses pengguna ke lingkungan: grup keamanan dan lisensi](/power-platform/admin/control-user-access).

![Mode grup](./media/groupsmode.png)

1. Proyek dibuat dan dimiliki oleh pengguna yang membuat.
2. Pemilik proyek diperbarui ke tim.
3. Tim pemilik dipetakan ke grup Office yang ditentukan atau dibuat.
4. Pemilik asli proyek ditambahkan ke Office Group.

## <a name="deployment-recommendation"></a>Rekomendasi penyebaran
Seiring model kolaborasi Office Group berkembang, fungsi akan ditambahkan untuk memberikan kontrol yang lebih rinci dari waktu ke waktu. Pelanggan yang menyebarkan Project Operations saat ini didorong untuk fokus pada model keamanan Microsoft Dynamics 365 tradisional.

Untuk informasi lebih lanjut, lihat [keamanan di Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Keamanan Microsoft Dynamics 365 Finance dan Project Operations
Operasi proyek mencakup peran berikut:

- Manajer Proyek
- Akuntan proyek

Untuk informasi lebih lanjut tentang peran keamanan di Finance, lihat [keamanan berbasis peran](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]