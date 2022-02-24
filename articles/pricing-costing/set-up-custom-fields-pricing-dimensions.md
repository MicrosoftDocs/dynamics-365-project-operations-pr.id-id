---
title: Mengonfigurasikan bidang kustom sebagai dimensi harga
description: Topik ini menyediakan informasi tentang bagaimana mengkonfigurasi dimensi harga menggunakan bidang kustom .
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 744c561d023d7ef5ed79947e69f2de8a3902fb41
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650218"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Mengonfigurasikan bidang kustom sebagai dimensi harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Sebelum memulai, topik mengasumsikan bahwa anda telah menyelesaikan prosedur dalam topik, [membuat bidang kustom dan entitas](create-custom-fields-entities-pricing-dimensions.md), serta [menambahkan bidang kustom yang diperlukan untuk penyiapan harga dan entitas transaksi](add-custom-fields-price-setup-transactional-entities.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan selesaikan dan kemudian kembali ke topik ini. 

Topik ini menyediakan informasi tentang cara mengkonfigurasi dimensi harga kustom. Pada halaman **parameter**, tab **Dimensi harga berbasis jumlah** menampilkan entitas dimensi harga. Secara default, ada dua baris di kisi pada tab ini:

- **msdyn_resourcecategory** (Peran)
- **msdyn_OrganizationalUnit** (unit organisasi)

> [!IMPORTANT]
> Jangan hapus baris ini. Namun, jika Anda tidak memerlukannya, Anda dapat membuatnya tidak berlaku dalam konteks tertentu dengan menetapkan **berlaku untuk biaya**, **berlaku untuk penjualan**, dan **berlaku untuk pembelian** semua ke **tidak**. Mengatur nilai atribut ke **tidak** memiliki efek yang sama dengan tidak memiliki bidang sebagai dimensi harga.

Agar bidang menjadi dimensi harga, harus:

- Dibuat sebagai bidang di entitas **harga peran** dan entitas **markup harga peran**. Untuk informasi lebih lanjut tentang cara melakukannya lihat [Tambahkan bidang kustom ke pengaturan harga dan entitas transaksi](add-custom-fields-price-setup-transactional-entities.md).

- Dibuat sebagai baris di tabel **dimensi harga**. Misalnya, tambahkan baris dimensi harga seperti yang ditunjukkan dalam grafik berikut. 

![Baris Dimensi Harga Berdasarkan Jumlah](media/Amt-based-PD.png)

Jam kerja sumber daya (**msdyn_resourceworkhours**) telah ditambahkan sebagai dimensi berbasis markup dan telah ditambahkan ke kisi pada tab **Dimensi harga berdasarkan markup**.

![Baris Dimensi Harga Berdasarkan Markup](media/Markup-based-PD.png)


> [!IMPORTANT]
> Setiap perubahan pada data dimensi harga dalam tabel ini, yang ada atau yang baru, disebarkan ke logika bisnis harga hanya setelah cache diperbarui. Waktu refresh cache dapat berlangsung hingga 10 menit. Berikan waktu tersebut untuk melihat perubahan harga logika default yang harus dihasilkan dari perubahan pada data dimensi harga.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atribut tabel dimensi harga
Bagian berikut ini menyediakan informasi tentang atribut yang berbeda dalam tabel **dimensi harga**.

### <a name="pricing-dimension-name"></a>Nama Dimensi Harga
Nilai ini harus sama persis dengan nama skema bidang yang ditambahkan ke tabel **harga peran** untuk dimensi harga kustom. Untuk informasi lebih lanjut tentang menambahkan bidang ke tabel **harga peran**, lihat [menambahkan bidang kustom untuk pengaturan harga dan entitas transaksi](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Jenis dimensi
Ada dua jenis dasbor di dimensi harga:
  
  - **Di mana pun berbasis jumlah**: nilai dimensi dari konteks input disesuaikan dengan nilai dimensi pada baris **harga peran** dan harga/biaya akan di-default langsung dari tabel **harga peran**.
  - **Dimensi berbasis markup**: ini adalah dimensi di mana ketiga proses langkah berikut untuk mendapatkan harga/biaya digunakan:
 
    1. Nilai dimensi berbasis non-markup dari konteks input dicocokkan ke baris harga peran untuk mendapatkan tingkat dasar.
    2. Nilai dimensi dari konteks input dicocokkan ke baris **markup harga peran** untuk mendapatkan persentase markup.
    3. Persentase markup dari langkah kedua dicocokkan ke tingkat dasar yang Diperoleh dari tabel **harga peran** pada langkah pertama untuk mencapai harga/biaya akhir.
   
   Tabel berikut ini menunjukkan penghitungan markup harga.
  
| Peran        | Unit Organisasi    |Lokasi Kerja      |Jabatan standar      |Jam Kerja Sumber daya      |  Mark up|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Aswono India|Di Lokasi            |                    |Lembur                 |15     |
|             | Aswono India|Lokal             |                    |Lembur                 |10     |
|             | Contoso AS   |Lokal             |                    |Lembur                 |20     |


Jika sumber daya dari Aswono India yang tingkat dasarnya adalah 100 USD bekerja di lokasi, dan mereka mencatat 8 jam waktu reguler, dan 2 jam lembur pada saat entri waktu, Mesin harga akan menggunakan tingkat dasar 100 selama 8 jam untuk merekam 800 USD. Untuk lembur 2 jam, markup 15% akan diterapkan ke tingkat dasar 100 untuk mendapatkan harga unit 115 USD dan akan merekam total biaya 230 USD.

### <a name="applicable-to-cost"></a>Berlaku untuk Biaya 
Jika ini diatur ke **ya**, ini menunjukkan bahwa nilai dimensi dari konteks input harus digunakan untuk mencocokkan dengan **harga peran** dan **markup harga peran** saat mengambil biaya dan tingkat markup.

### <a name="applicable-to-sales"></a>Berlaku untuk Penjualan
Jika ini diatur ke **ya**, ini menunjukkan bahwa nilai dimensi dari konteks input harus digunakan untuk mencocokkan dengan **harga peran** dan **markup harga peran** saat mengambil tagihan dan tingkat markup.

### <a name="applicable-to-purchase"></a>Berlaku untuk Pembelian
Jika ini diatur ke **ya**, ini menunjukkan bahwa nilai dimensi dari konteks input harus digunakan untuk mencocokkan dengan **harga peran** dan **markup harga peran** saat mengambil harga pembelian. Skenario subkontrak tidak didukung, sehingga bidang ini tidak digunakan. 

### <a name="priority"></a>Prioritas
Pengaturan prioritas dimensi akan membantu harga menghasilkan harga bahkan saat tidak dapat menemukan kecocokan yang sama persis antara nilai dimensi input dan nilai dari tabel **harga peran** atau **markup harga peran**. Dalam skenario ini, nilai null digunakan untuk nilai dimensi yang tidak cocok dengan menimbang dimensi dalam urutan prioritasnya.

- **Prioritas biaya**: nilai prioritas biaya dimensi akan menunjukkan bobot dimensi saat mencocokkan dengan penyiapan harga biaya. Nilai **prioritas biaya** harus unik di seluruh dimensi yang **berlaku untuk biaya**.
- **Prioritas penjualan**: nilai prioritas biaya dimensi penjualan akan menunjukkan bobot dimensi saat mencocokkan dengan penyiapan harga penjualan atau tingkat tagihan. Nilai **prioritas penjualan** harus unik di seluruh dimensi yang **berlaku untuk penjualan**.
