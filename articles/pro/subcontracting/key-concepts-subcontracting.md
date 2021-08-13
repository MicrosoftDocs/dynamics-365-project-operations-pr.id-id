---
title: Konsep penting dalam subkontrak
description: Topik Ini menjelaskan beberapa konsep utama yang berlaku untuk subkontrak di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994280"
---
# <a name="key-concepts-in-subcontracting"></a>Konsep penting dalam subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Topik ini menjelaskan beberapa konsep utama yang harus Anda ketahui sebelum Anda mulai menggunakan fungsionalitas subkontrak di Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unit kontrak pada subkontrak

Unit kontrak mewakili divisi atau praktik yang memiliki pengiriman proyek akhirnya. Unit kontrak juga merupakan divisi yang masuk ke dalam hubungan kontrak dengan vendor.

## <a name="purchase-currency"></a>Mata Uang pembelian

Dalam Project Operations, mata uang pembelian adalah mata uang tempat subkontrak dibuat. Ini juga mata uang pencatatan biaya subkontraktor pada proyek. Mata uang pembelian dapat berbeda dari mata uang proyek, dan mata uang proyek dapat, pada gilirannya, berbeda dari mata uang penjualan.

## <a name="billing-methods-on-subcontract-lines"></a>Metode penagihan pada baris subkontrak

Untuk proyek, biasanya ada model kontrak biaya tetap dan berbasis konsumsi. Project Operations mendukung metode penagihan ini dalam konteks penjualan dan pembelian. Untuk pembelian, metode penagihan berfungsi dengan cara berikut:

- **Waktu dan Bahan** - Ketika baris subkontrak menggunakan metode penagihan **Waktu dan Bahan**, biaya waktu dicatat pada proyek saat subkontraktor mengerjakan proyek itu dan mencatat waktu. Transaksi biaya ini dari subkontraktor kemudian dicocokkan dengan item baris pada faktur vendor. Dalam model ini, manajer proyek yang menggunakan Project Operations dapat mencocokkan dan memverifikasi baris faktur vendor dengan waktu subkontraktor yang direkam dan disetujui. Setelah verifikasi selesai, aktual biaya sebelumnya yang dicatat setelah persetujuan dibalik, dan aktual biaya baru yang didasarkan pada faktur vendor dibuat pada proyek.
- **Harga Tetap** - Dalam model kontrak biaya tetap ini, faktur vendor didasarkan pada pencapaian tetap. Namun, sumber daya subkontraktor juga dapat melaporkan waktu. Waktu kemudian ditinjau dan disetujui oleh manajer proyek. Ketika disetujui, Project Operations menciptakan aktual biaya sementara pada proyek. Setelah vendor mengirim faktur untuk pencapaian, manajer proyek dapat mencocokkan aktual biaya yang dicatat sebelumnya terhadap pencapaian. Ketika verifikasi selesai, biaya aktual dibalik, dan biaya berbasis pencapaian dicatat.

## <a name="project-price-lists-on-subcontracts"></a>Daftar harga proyek pada subkontrak

Daftar harga proyek adalah daftar harga yang digunakan untuk menyiapkan harga pembelian untuk waktu, pengeluaran, dan komponen terkait proyek lainnya. Mungkin ada beberapa daftar harga, yang masing-masing dapat memiliki subkontrak yang efektif tanggal dalam Project Operations. Project Operations tidak mendukung tanggal efektif yang tumpang tindih pada daftar harga proyek untuk subkontrak.

## <a name="transaction-classes-on-subcontracts"></a>Kelas transaksi pada subkontrak

Project Operations mendukung empat jenis kelas transaksi:

- Waktu
- Pengeluaran
- Materi
- Biaya

Biaya pembelian dapat diperkirakan dan dikeluarkan hanya pada kelas transaksi **Waktu**, **Pengeluaran**, dan **Bahan**. **Biaya** adalah kelas transaksi khusus pendapatan dan tidak tersedia dalam konten pembelian.

## <a name="purchase-pricing-dimensions"></a>Dimensi harga pembelian

Dimensi harga memungkinkan Anda memutuskan atribut apa yang digunakan untuk pengaturan harga pembelian dan default pada transaksi waktu. Sehubungan dengan pembelian, Project Operations hanya mendukung set dimensi tetap untuk penyiapan harga pembelian dan default. Untuk penyiapan harga pembelian dan default pada jalur subkontrak dan transaksi waktu subkontrak, atributnya adalah **Peran** dan **Sumber daya yang dapat dipesan**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
