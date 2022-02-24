---
title: Mengonfigurasi kebijakan pengeluaran
description: Anda dapat membuat kebijakan pengeluaran yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan di Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271267"
---
# <a name="set-up-expense-policies"></a>Mengonfigurasi kebijakan pengeluaran

Anda dapat menentukan kebijakan yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan.         
Mengimplementasikan kebijakan pengeluaran dapat membantu Anda mengelola pengeluaran secara efektif.         

Misalnya, Anda dapat mengatur kebijakan untuk pengeluaran Hotel di New York City, yang menyatakan bahwa pengeluaran per malam tidak dapat melebihi USD 250.       
Jika pekerja mengirimkan laporan pengeluaran atau permintaan perjalanan dengan tarif kamar melebihi jumlah ini, sistem akan memberi tahu        
Pekerja bahwa jumlah kebijakan untuk pengeluaran telah terlampaui. Anda dapat mengkonfigurasi pesan yang akan diterima oleh pekerja        
menentukan kebijakan.      
        
Anda dapat menentukan tiga jenis kebijakan:         
        
- Peringatan – memungkinkan pekerja untuk mengirimkan laporan pengeluaran atau permintaan perjalanan namun pengeluarannya akan ditandai untuk semua pemberi izin dan        
  Untuk pelaporan selanjutnya.        

- Kesalahan – mengharuskan pekerja untuk merevisi biaya untuk mematuhi kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.       
 
 - Pembenaran – memerlukan pekerja atau manajer untuk memasukkan pembenaran untuk melampaui jumlah kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.        

## <a name="policy-tips"></a>Tips kebijakan
Berikut adalah beberapa saran yang dapat membantu Anda ketika membuat kebijakan baru untuk manajemen pengeluaran. 
* Kebijakan adalah tanggal efektif dan tidak akan berlaku jika kebijakan dibuat dengan tanggal setelah tanggal pengeluaran terjadi. Misalnya, jika Anda membuat kebijakan baru hari ini untuk memberlakukan biaya makan maksimum $50, maka setiap biaya yang ada yang dimasukkan kemarin tidak akan diperiksa terhadap kebijakan ini.
* Saat membuat kebijakan untuk kategori pengeluaran yang dapat diperinci, pertimbangkan menambahkan kondisi untuk jenis baris pengeluaran. Beberapa kebijakan seperti memerlukan tanda terima mungkin tidak masuk akal untuk baris yang diperinci dan hanya dapat diterapkan ke baris header atau baris non-rinci. 
* Kebijakan manajemen pengeluaran dievaluasi terhadap entitas sumber secara default. Untuk skenario antarperusahaan, Anda dapat mengatur kebijakan untuk dievaluasi terhadap entitas tujuan (entitas peminjam) sebagai gantinya. Untuk menjalankan kebijakan terhadap entitas tujuan, Aktifkan fitur "Evaluasi kebijakan pengeluaran terhadap entitas hukum peminjaman" di ruang kerja **manajemen fitur**.

## <a name="when-to-evaluate-policies"></a>Kapan mengevaluasi kebijakan

Dalam parameter manajemen pengeluaran, ada opsi untuk mengevaluasi kebijakan manajemen pengeluaran bila baris disimpan atau saat laporan pengeluaran diajukan. Jika Anda memilih untuk mengevaluasi bila baris disimpan, ini memastikan pengguna memiliki visibilitas sebelumnya ke apa yang perlu mereka lakukan untuk menyelesaikan laporan pengeluaran mereka sekaligus. Jika tidak, Anda dapat menunda evaluasi kebijakan dan menghemat waktu jika Anda memiliki validasi yang terjadi di akhir, selama pengajuan ke alur kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]