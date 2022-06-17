---
title: Metode biaya penyelesaian
description: Artikel ini memberikan informasi tentang metode yang digunakan untuk menghitung biaya untuk menyelesaikan proyek.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920294"
---
# <a name="cost-to-complete-methods"></a>Metode biaya penyelesaian

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini memberikan informasi tentang metode yang digunakan untuk menghitung biaya untuk menyelesaikan proyek. Ada beberapa metode yang dapat Anda gunakan untuk menghitung biaya penyelesaian satu proyek. 

Saat Anda membuat perkiraan untuk proyek, di halaman **Buat perkiraan**, di bidang **Metode biaya penyelesaian**, Anda dapat memilih salah satu biaya berikut untuk menyelesaikan metode.

| Metode biaya penyelesaian    | KETERANGAN                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Biaya total - aktual            | Masukkan biaya estimasi secara manual di bidang **Biaya total** atau **Jumlah total** menggunakan tombol **Perkiraan biaya** pada halaman **Perkiraan**. Sistem akan mengurangi biaya aktual dari total yang Anda masukkan. Total adalah biaya untuk menyelesaikan proyek. Metode ini tidak menggunakan perkiraan pengeluaran dan penugasan sumber daya yang dimasukkan di Project Operations yang dibuat di dalam Microsoft Dataverse. Total biaya atau jumlah total dapat diperbarui secara manual sesuai kebutuhan.  |
| Total prakiraan - aktual        | Penetapan sumber daya dan perkiraan biaya digunakan untuk menentukan total jumlah prakiraan proyek. Biaya aktual dibandingkan dengan prakiraan ini untuk menghitung biaya penyelesaian.                                                                                                                                                                                                                                                                          |
| Seperti estimasi sebelumnya         | Metode estimasi yang sama yang digunakan pada periode sebelumnya digunakan di sini. Metode ini memerlukan model perkiraan jika periode sebelumnya memerlukan model perkiraan.                                                                                                                                                                                                                                                                                                                           |
| Atur biaya penyelesaian ke nol | Biasanya digunakan sebelum proyek estimasi dihilangkan, metode ini sesuai dengan estimasi total dengan transaksi aktual yang diposting dan menghapus **Biaya penyelesaian**. Setelah selesai, hasilnya selalu bernilai 100 persen. Untuk setiap lini biaya yang Anda buat, kotak centang **Prakiraan** dikosongkan dan estimasi total disalin dari estimasi biaya sebelumnya. Konsumsi aktual untuk periode estimasi dikurangi dari biaya untuk menyelesaikan proyek.              |
| Dari template biaya           | Metode biaya penyelesaian yang diatur dalam template biaya yang terkait dengan proyek estimasi yang dipilih.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]