---
title: Menentukan kebijakan pengeluaran
description: Anda dapat menentukan kebijakan pengeluaran yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001880"
---
# <a name="define-expense-policies"></a>Menentukan kebijakan pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat menentukan kebijakan yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan.         
Mengimplementasikan kebijakan pengeluaran dapat membantu Anda mengelola pengeluaran secara efektif.         

Misalnya, Anda dapat mengatur kebijakan untuk pengeluaran Hotel di New York City, yang menyatakan bahwa pengeluaran per malam tidak dapat melebihi USD 250.       
Jika pekerja mengirimkan laporan pengeluaran atau permintaan perjalanan dengan tarif kamar melebihi jumlah ini, sistem akan memberi tahu         
Pekerja bahwa jumlah kebijakan untuk pengeluaran telah terlampaui. Anda dapat mengkonfigurasi pesan yang akan diterima oleh pekerja        
menentukan kebijakan.      
        
Anda dapat menentukan tiga jenis kebijakan:         
        
- **Peringatan**: memungkinkan pekerja untuk mengirimkan laporan pengeluaran atau permintaan perjalanan namun pengeluarannya akan ditandai untuk semua pemberi izin dan         
  Untuk pelaporan selanjutnya.        

- **Kesalahan**: mengharuskan pekerja untuk merevisi biaya untuk mematuhi kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.        
 
 - **Pembenaran**: memerlukan pekerja atau manajer untuk memasukkan pembenaran untuk melampaui jumlah kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.        

## <a name="policy-tips"></a>Tips kebijakan
Berikut adalah beberapa saran yang dapat membantu Anda ketika membuat kebijakan baru untuk manajemen pengeluaran: 

- Kebijakan adalah tanggal efektif yang berarti kebijakan tidak akan berlaku jika dibuat dengan tanggal setelah tanggal pengeluaran terjadi. Misalnya, Anda membuat kebijakan baru hari ini untuk memberlakukan pengeluaran makan maksimum $50. Pengeluaran yang ada yang dimasukkan sebagai kemarin tidak akan diperiksa terhadap kebijakan ini.
- Saat membuat kebijakan untuk kategori pengeluaran yang dapat diperinci, pertimbangkan menambahkan kondisi untuk jenis baris pengeluaran. Beberapa kebijakan, seperti memerlukan tanda terima, mungkin tidak masuk akal untuk baris terperinci. Dalam situasi ini, kebijakan hanya diterapkan ke baris header atau baris non-itemisasi. 
- Kebijakan manajemen pengeluaran dievaluasi terhadap entitas sumber secara default. Untuk skenario antarperusahaan, Anda dapat mengatur kebijakan untuk dievaluasi terhadap entitas tujuan (entitas peminjam) sebagai gantinya. Untuk menjalankan kebijakan terhadap entitas tujuan, Aktifkan fitur **Evaluasi kebijakan pengeluaran terhadap entitas hukum peminjaman** di ruang kerja **manajemen fitur**.

## <a name="when-to-evaluate-policies"></a>Kapan mengevaluasi kebijakan

Dalam parameter manajemen pengeluaran, Anda dapat memilih untuk mengevaluasi kebijakan manajemen pengeluaran bila baris disimpan atau saat laporan pengeluaran diajukan. Jika Anda memilih untuk mengevaluasi bila baris disimpan, pengguna akan memiliki visibilitas sebelumnya ke apa yang perlu mereka lakukan untuk menyelesaikan laporan pengeluaran mereka sekaligus. Jika tidak, Anda dapat menunda evaluasi kebijakan dan menghemat waktu dengan memvalidasi di akhir, selama pengajuan ke alur kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]