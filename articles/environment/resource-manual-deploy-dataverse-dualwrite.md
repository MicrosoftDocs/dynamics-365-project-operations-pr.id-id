---
title: Terapkan aplikasi Project Operations Dataverse secara manual dengan dukungan penulisan ganda
description: Topik ini menjelaskan cara menyebarkan aplikasi Project Operations Dataverse secara manual sehingga mendukung penulisan ganda.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591224"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Terapkan aplikasi Project Operations Dataverse secara manual dengan dukungan penulisan ganda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini menjelaskan cara menyebarkan Microsoft Dynamics 365 Project Operations di Microsoft Dataverse secara manual sehingga mendukung penulisan ganda. Project Operations mendeteksi konfigurasi lingkungan dan menambahkan dukungan tambahan untuk penulisan ganda jika prasyarat terpenuhi.

Selama penyebaran Microsoft Dynamics melalui Lifecycle Services (LCS), jika Anda telah mengikuti petunjuk di topik ini, Anda dapat melewatkan penyebaran integrasi Microsoft Power Platform (sebelumnya dikenal sebagai lingkungan Common Data Service).

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
6. Konfirmasikan bahasa tersebut, lalu konfirmasikan bahwa mata uang tersebut cocok dengan mata uang untuk aplikasi Keuangan dan Operasi Anda.
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

Dataverse Setelah lingkungan disebarkan, Anda dapat mengatur tautan di aplikasi Keuangan dan Operasi Anda. Ikuti langkah-langkah dalam [Gunakan wizard penulisan ganda untuk menautkan lingkungan Anda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
