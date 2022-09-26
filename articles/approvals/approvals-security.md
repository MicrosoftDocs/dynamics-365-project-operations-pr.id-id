---
title: Keamanan dan persetujuan
description: Artikel ini menyediakan informasi tentang pengaturan keamanan untuk bekerja dengan persetujuan di Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525406"
---
# <a name="security-and-approvals"></a>Keamanan dan persetujuan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Microsoft Dynamics 365 Project Operations menggunakan dua peran keamanan untuk memungkinkan persetujuan waktu, biaya, dan entri material:

- Pemberi Persetujuan Proyek
- Admin Pemberi Persetujuan Proyek

## <a name="project-approver"></a>Pemberi Persetujuan Proyek

Anda harus memiliki **Pemberi Persetujuan** Proyek peran keamanan untuk menyetujui waktu proyek, pengeluaran, dan entri materi. Anda juga harus memiliki akses ke entitas terkait yang relevan, seperti **Project**. Akses tersebut **dapat ditetapkan oleh seseorang yang memiliki peran Manajer** Proyek. Selain itu, Anda harus menjadi anggota tim proyek dan ditandai sebagai pemberi persetujuan.

Untuk menyetujui entri non-proyek, Anda harus menjadi manajer pengirim.

## <a name="project-approver-admin"></a>Admin Pemberi Persetujuan Proyek

> [!NOTE]
> Fitur [Kumpulan](approval-sets.md) persetujuan harus diaktifkan sebelum Anda dapat menggunakan fungsionalitas Admin Pemberi Persetujuan Proyek.

**peran keamanan Admin** Pemberi Persetujuan Proyek memungkinkan pengguna untuk melewati kebijakan dan memungkinkan persetujuan entri di semua proyek. Penetapan peran ini akan melewati logika validasi yang memerlukan keanggotaan tim dan ditandai sebagai pemberi persetujuan. Anda harus memiliki akses ke entitas terkait yang relevan, seperti **Project**. Akses tersebut **dapat ditetapkan oleh seseorang yang memiliki peran Manajer** Proyek.

Konteks pengguna SYSTEM melewati validasi dengan cara yang sama seperti peran keamanan Admin Pemberi Persetujuan Proyek.
