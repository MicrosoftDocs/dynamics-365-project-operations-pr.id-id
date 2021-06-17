---
title: Mengonfigurasikan kategori proyek
description: Topik ini menyediakan informasi tentang pengaturan kategori proyek.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995175"
---
# <a name="configure-project-categories"></a>Mengonfigurasikan kategori proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Project Operations menawarkan kemampuan kuat untuk mengkategorikan pendapatan dan pengeluaran dalam proyek. Kategori memberikan kemampuan untuk melaporkan dan menganalisis transaksi proyek, dan mendorong posting ke buku besar.

Diagram berikut mengilustrasikan korelasi antara kategori transaksi, kategori bersama, dan kategori proyek. 

Kategori transaksi adalah pengelompokan dasar untuk transaksi proyek. Dalam pengelompokan tersebut, ada seperangkat kategori bersama yang dapat dibagikan di seluruh aplikasi dan modul. Menyelami lebih jauh ke yang spesifik, kategori proyek adalah tingkat kategori yang paling rinci. Kategori proyek dikhususkan untuk badan hukum, modul, dan aplikasi.

![Korelasi antara kategori transaksi, kategori bersama, dan kategori proyek](media/project-categories.png)

## <a name="transaction-categories"></a>Kategori Transaksi

Kategori transaksi mewakili pengelompokan dasar untuk transaksi proyek dan bukan spesifik perusahaan atau jenis transaksi. Misalnya, Contoso Robotics menggunakan kategori Desain, Perjalanan, Penginstalan, dan Transaksi Layanan untuk mengelompokkan transaksi Proyek.

Kategori transaksi ditentukan dalam modul Project Operations. 
1. Buka **pengaturan** \> **Kategori Transaksi** untuk membuka formulir. 
2. Buat kategori transaksi baru baik dengan memilih **baru** atau dengan memilih **impor dari Excel**.

## <a name="shared-categories"></a>Kategori bersama

Dynamics 365 menggunakan konsep Kategori bersama untuk mengkategorikan pengeluaran dalam aplikasi yang berbeda, seperti Dynamics 365 Finance, Dynamics 365 Supply Chain, dan Dynamics 365 Project Operations. Untuk setiap kategori transaksi yang dibuat, Project Operations secara otomatis membuat empat kategori bersama terkait: jam, pengeluaran, ongkos, dan item. Anda dapat meninjau dan menyesuaikan kategori bersama dengan membuka kategori **manajemen proyek dan akuntansi** \> **penataan** \> **kategori** \> **Kategori bersama**.

## <a name="project-categories"></a>Kategori proyek

Kategori proyek mewakili tingkat konfigurasi kategori yang paling rinci dan harus dikonfigurasi secara terpisah, dan untuk setiap perusahaan, oleh akuntan proyek.

1. Buka **manajemen Proyek dan Akuntansi** \> **Penyiapan** \> **kategori** \> **Kategori proyek**.
2. Pilih **baru**.
3. Pilih **id kategori** dari kategori bersama yang Anda buat di bagian sebelumnya. Project Operations hanya memungkinkan menggunakan kategori bersama yang terkait dengan kategori transaksi.
4. Pilih grup kategori.

## <a name="category-groups"></a>Grup kategori

Grup kategori digunakan untuk berbagi properti, terutama profil posting, antara kategori proyek terkait. Harus ada minimal satu grup kategori untuk setiap jenis transaksi dan setiap kategori proyek diberi grup.

Spesifikasi posting dalam Project Operations ditentukan berdasarkan aturan profil biaya proyek dan pendapatan, kategori proyek, dan grup kategori. Anda dapat mengkonfigurasi grup kategori dengan membuka **manajemen proyek dan akuntansi** \> **Penyiapan** \> **Kategori** \> **Grup kategori**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]