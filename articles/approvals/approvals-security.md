---
title: Keamanan dan persetujuan
description: Artikel ini memberikan informasi tentang konfigurasi keamanan untuk bekerja dengan persetujuan di Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709401"
---
# <a name="security-and-approvals"></a>Keamanan dan persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Microsoft Dynamics 365 Project Operations menggunakan dua peran keamanan untuk memungkinkan persetujuan waktu, pengeluaran, dan entri bahan:

- Pemberi Persetujuan Proyek
- Admin Pemberi Persetujuan Proyek

## <a name="project-approver"></a>Pemberi Persetujuan Proyek

Anda harus memiliki peran keamanan **Pemberi Persetujuan Proyek** untuk menyetujui waktu, pengeluaran, dan bahan proyek. Anda juga harus memiliki akses ke entitas terkait yang relevan, seperti **Project**. Akses tersebut dapat ditetapkan oleh seseorang yang memiliki peran **Manajer Proyek**. Selain itu, Anda harus menjadi anggota tim proyek dan ditandai sebagai pemberi izin.

Untuk menyetujui entri non-proyek, Anda harus menjadi manajer pemohon.

## <a name="project-approver-admin"></a>Admin Pemberi Persetujuan Proyek

> [!NOTE]
> Fitur [Set Persetujuan](approval-sets.md) harus diaktifkan agar Anda dapat menggunakan fungsi Admin Pemberi Persetujuan Proyek.

Admin peran keamanan **Pemberi Persetujuan Proyek** memungkinkan pengguna memintas kebijakan dan memungkinkan persetujuan entri di seluruh proyek. Penugasan peran ini akan memintas logika validasi yang memerlukan keanggotaan tim dan ditandai sebagai pemberi persetujuan. Anda harus memiliki akses ke tabel terkait yang relevan, seperti **Proyek**, melalui peran keamanan yang ditetapkan kepada Anda.

Konteks pengguna SISTEM akan memintas validasi dengan cara yang sama seperti peran keamanan Admin Pemberi Persetujuan Proyek.
