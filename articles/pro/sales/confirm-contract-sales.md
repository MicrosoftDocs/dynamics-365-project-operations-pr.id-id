---
title: Konfirmasi Kontrak proyek
description: Topik ini menyediakan informasi topik cara mengonfirmasikan kontrak dalam Project operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128287"
---
# <a name="confirm-a-project-contract"></a>Konfirmasi Kontrak proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kontrak proyek dalam Dynamics 365 Project Operations dapat aktif dengan alasan **dikonfirmasi**, atau ditutup dengan alasan **Kalah**. Ketika anda mengkonfirmasi kontrak proyek, status diperbarui dari **draf** ke **aktif** dan alasan status **dikonfirmasi**. Kontrak aktif atau tertutup tidak dapat diedit atau dibuka kembali. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Dampak keuangan mengkonfirmasikan kontrak proyek

Setelah kontrak proyek dikonfirmasi, aplikasi akan menghitung ulang biaya dengan membalik aktual biaya yang lebih lama dan membuat aktual biaya baru. Aktual biaya baru lalu diproses berdasarkan metode penagihan pada baris kontrak proyek terkait. Jika aktual biaya merujuk pada baris kontrak waktu dan material, aplikasi akan secara otomatis membuat ulang aktual penjualan yang belum ditagih. Jika aktual biaya merujuk pada baris kontrak harga tetap, aplikasi akan berhenti memproses ulang aktual biaya.

Batas yang tidak boleh dilebihi, konfigurasi ketertagihan, serta penetapan harga dan biaya pada aktual dievaluasi dan kemudian diperbarui sebagai bagian dari proses konfirmasi.

## <a name="close-a-project-contract-as-lost"></a>Menutup kontrak proyek sebagai kalah

Saat anda menutup kontrak proyek sebagai kalah, status kontrak diperbarui menjadi **ditutup** dan alasan status adalah **Kalah**. Kontrak proyek menjadi baca-saja. Dialog konfirmasi diberikan sebelum perubahan selesai karena Anda tidak dapat membuka kembali kontrak proyek yang ditutup.

Jika kontrak proyek yang ditutup sebagai kalah merujuk pada suatu proyek pada barisnya, proyek itu juga ditandai sebagai tertutup. Setiap Pemesanan sumber daya dari waktu itu ke depan dibatalkan. Setiap aktual penjualan yang belum ditagih pada kontrak proyek yang belum ada di faktur, akan dibalik.

> [!NOTE]
> Dalam Dynamics 365 Project Operations, penutupan kontrak proyek sebagai kalah tidak akan memengaruhi status peluang terkait. Peluang akan tetap terbuka dan harus ditutup secara manual.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]