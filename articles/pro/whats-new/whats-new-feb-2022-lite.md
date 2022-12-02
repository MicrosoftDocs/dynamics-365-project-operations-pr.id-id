---
title: Apa yang baru Februari 2022 - penyebaperan Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di penyebaran Project Operations lite Februari 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922824"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Apa yang baru Februari 2022 - penyebaperan Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.28.0.120

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Pada rilis ini, Anda dapat menambahkan hingga 300 anggota tim ke satu proyek. Sebelumnya, batas jumlah anggota tim adalah 150. Untuk informasi selengkapnya, lihat [batas proyek](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan harga | 2497369 | Koreksi bahan harus mengikuti nilai tanggal dalam parameter **Koreksi**. |
| Penagihan dan harga | 2498697 | Meningkatkan konfigurasi keamanan untuk **penarikan entri waktu**. |
| Penagihan dan harga | 2517455 | Tindakan **transaksi baris faktur yang di-refresh** tidak boleh dibolehkan dipicu beberapa kali bersamaan untuk faktur yang sama. |
| Penagihan dan harga | 2517465 | Tindakan **Nonaktifkan rincian baris faktur** diblokir karena tidak didukung. |
| Penagihan dan harga | 2556660 | Memperbaiki pemeriksaan efektivitas tanggal yang dilakukan pada daftar harga yang dilampirkan ke rekaman parameter proyek. |
|   Manajemen peluang | 2369202 | Mengoreksi logika bisnis yang memverifikasi bahwa daftar harga yang memiliki tanggal efektivitas tumpang tindih dapat dilampirkan ke kontrak proyek yang sama. |
|   Manajemen peluang | 2385965 | Mengoreksi perilaku pada tab **Pelanggan** pada halaman **kontrak proyek** saat Anda memilih **Simpan dan tutup**. |
