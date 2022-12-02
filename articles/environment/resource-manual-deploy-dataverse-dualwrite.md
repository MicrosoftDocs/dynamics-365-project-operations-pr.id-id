---
title: Terapkan aplikasi Project Operations Dataverse secara manual dengan dukungan penulisan ganda
description: Artikel ini menjelaskan cara menyebarkan aplikasi Project Operations Dataverse secara manual sehingga mendukung penulisan ganda.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a25e2a59f1c069057c6689825ce52b13d842af71
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028568"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Terapkan aplikasi Project Operations Dataverse secara manual dengan dukungan penulisan ganda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini menjelaskan cara menyebarkan Microsoft Dynamics 365 Project Operations di Microsoft Dataverse secara manual sehingga mendukung penulisan ganda. Project Operations mendeteksi konfigurasi lingkungan dan menambahkan dukungan tambahan untuk penulisan ganda jika prasyarat terpenuhi.

Selama penyebaran Microsoft Dynamics melalui Lifecycle Services (LCS), jika Anda telah mengikuti petunjuk di artikel ini, Anda dapat melewatkan penyebaran integrasi Microsoft Power Platform (sebelumnya dikenal sebagai lingkungan Common Data Service).

Proses penyebaran Project Operations di Dataverse sehingga mendukung penulisan ganda memiliki empat langkah utama:

1. [Membuat lingkungan baru di Dataverse yang mendukung penulisan ganda](#create).
2. [Menambahkan prasyarat penulisan ganda ke lingkungan](#prerequisites).
3. [Tambahkan aplikasi Project Operations Dataverse](#dataverse).
4. [Tautkan lingkungan Anda](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Membuat lingkungan baru di Dataverse yang mendukung penulisan ganda

Untuk menyelesaikan prosedur ini, Anda harus masuk sebagai administrator.

1. Buka [pusat admin Power Platform](https://admin.powerplatform.com), lalu masuk sebagai administrator.
2. Buat lingkungan baru dan beri nama.
3. Pilih jenis lingkungan. Jika Anda mendaftar penawaran uji coba, pilih **Uji Coba (berbasis langganan)**.
4. Konfirmasikan kawasan penyebaran.
5. Aktifkan pilihan **Buat database untuk lingkungan ini**. 
6. Konfirmasikan bahasa, lalu konfirmasikan bahwa mata uang sesuai dengan mata uang untuk aplikasi keuangan dan operasi Anda.
7. Aktifkan pilihan **aplikasi Dynamics 365**, dan konfirmasikan bahwa bidang **Terapkan aplikasi ini secara otomatis** diatur ke **Tidak Ada**.
8. Tambahkan grup keamanan, jika grup keamanan diperlukan.
9. Pilih **Simpan** untuk membuat lingkungan.
10. Tunggu selama penyebaran selesai dan lingkungan mencapai status **Siap**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Menambahkan prasyarat penulisan ganda ke lingkungan

Dukungan penulisan ganda mencakup bidang tambahan yang ditambahkan ke entitas utama, seperti entitas **Perusahaan**. Jika Anda menambahkan dukungan penulisan ganda ke lingkungan yang ada, Anda harus memperbarui data untuk mengaktifkan dukungan. Untuk informasi tentang cara meng-klik data, lihat [data perusahaan Bootstrap](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Untuk informasi lebih lanjut tentang penulisan ganda, lihat [persyaratan sistem Penulisan ganda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Selesaikan prosedur ini untuk menambahkan prasyarat penulisan ganda ke lingkungan Anda.

1. Buka lingkungan yang baru saja Anda buat, lalu buka **Sumber daya** \> **aplikasi Dynamics 365**.
2. Pilih **solusi inti penulisan ganda** dalam daftar aplikasi, lalu instal.
3. Tunggu hingga penginstalan selesai. Lalu Pilih **solusi orkestrasi aplikasi penulisan ganda** dalam daftar aplikasi, lalu instal.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Tambahkan aplikasi Project Operations Dataverse

Anda dapat menyelesaikan prosedur ini hanya jika Anda telah menyelesaikan prosedur sebelumnya sebelum menginstal Project Operations. Selama penginstalan, sistem akan menganalisis konfigurasi lingkungan dan menambahkan dukungan untuk penulisan ganda jika diperlukan.

1. Buka lingkungan yang Anda buat tadi, lalu buka **Sumber daya** \> **aplikasi Dynamics 365**.
2. Pilih **Microsoft Dynamics 365 Project Operations** dalam daftar aplikasi, lalu instal.

## <a name="link-your-environments"></a><a name="link"></a>Tautkan lingkungan Anda

Setelah lingkungan Dataverse disebarkan, Anda dapat mengkonfigurasi tautan di aplikasi keuangan dan operasi Anda. Ikuti langkah-langkah dalam [Gunakan wizard penulisan ganda untuk menautkan lingkungan Anda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
