---
title: Harga proyek
description: Topik ini menyediakan informasi tentang cara kerja harga di Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000580"
---
# <a name="project-pricing"></a>Harga proyek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation memperluas entitas daftar harga di Dynamics 365 Sales. 

## <a name="key-entities"></a>Entitas utama

Daftar Harga mencakup informasi yang disediakan oleh empat entitas yang berbeda:

- **Daftar harga** - entitas ini menyimpan informasi tentang konteks, mata uang, efektivitas tanggal, dan unit waktu untuk waktu harga. Konteks menunjukkan apakah daftar harga mengungkapkan tingkat biaya atau tingkat penjualan. 
- **Mata uang** - entitas ini menyimpan mata uang harga pada daftar harga. 
- **Tanggal** -entitas ini digunakan saat sistem mencoba memasukkan harga default pada transaksi. Harga PSA memilih daftar harga yang memiliki efektivitas tanggal yang mencakup tanggal transaksi. Jika penentuan harga PSA menemukan lebih dari satu daftar harga yang efektif untuk tanggal transaksi yang dilampirkan ke kuotasi, kontrak, atau unit organisasi terkait, maka tidak ada harga yang dijadikan default. 
- **Waktu** -entitas ini menyimpan unit waktu yang dinyatakan harga, seperti tarif harian atau per jam. 

Entitas daftar harga memiliki tiga tabel terkait yang menyimpan harga:

  - **Harga peran** - tabel ini menyimpan tingkat kombinasi peran dan nilai unit organisasi dan digunakan untuk mengkonfigurasi harga berbasis peran untuk sumber daya manusia.
  - **Harga kategori transaksi** - tabel ini menyimpan harga berdasarkan Kategori transaksi dan digunakan untuk mengkonfigurasi harga kategori pengeluaran.
  - **Item daftar harga** - tabel ini menyimpan harga untuk produk Katalog.

> ![Mengonfigurasikan harga dengan daftar harga.](media/basic-guide-12.png)
 
Daftar Harga adalah kartu tarif. kartu tarif adalah kombinasi dari entitas daftar harga dan baris terkait pada harga peran, harga kategori transaksi, dan tabel item daftar harga.

## <a name="resource-roles"></a>Peran Sumber Daya

Istilah *peran sumber daya* merujuk pada seperangkat keterampilan, kompetensi, dan sertifikasi yang harus dimiliki oleh seseorang untuk melakukan serangkaian tugas tertentu pada suatu proyek.

Waktu sumber daya manusia biasanya dikutip berdasarkan peran yang diisi sumber daya pada proyek tertentu. Untuk waktu sumber daya manusia, PSA mendukung penetapan biaya dan penagihan yang didasarkan pada peran sumber daya. Waktu dapat dihargai di unit mana pun dalam grup unit **waktu**.

Grup unit **waktu** dibuat saat PSA diinstal. Ia memiliki unit default **jam**. Anda tidak dapat menghapus, mengubah nama, atau mengedit atribut untuk grup unit **waktu** atau unit **jam**. Namun, Anda dapat menambahkan unit lain ke grup unit **waktu**. Jika Anda mencoba untuk menghapus Grup unit **waktu** atau unit **jam**, Anda dapat menyebabkan kegagalan dalam logika bisnis PSA.

> ![Mengkonfigurasi harga berdasarkan peran.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Kategori transaksi dan kategori pengeluaran

Biaya perjalanan dan biaya lain yang dikenakan oleh konsultan proyek biasanya ditagihkan kepada pelanggan. PSA mendukung penetapan harga kategori pengeluaran dengan menggunakan daftar harga. Tiket pesawat, Hotel, dan Penyewaan Mobil adalah contoh kategori pengeluaran. Setiap baris daftar harga untuk pengeluaran menentukan harga untuk kategori pengeluaran tertentu. Untuk harga kategori pengeluaran, PSA mendukung tiga metode harga berikut:

- **Pada Biayanya** -biaya pengeluaran ditagihkan kepada pelanggan, dan tidak ada markup yang diterapkan.
- **Persentase markup** -persentase terhadap biaya aktual yang ditagihkan kepada pelanggan. 
- **Harga per unit** -harga penagihan diatur untuk setiap unit dari kategori pengeluaran. Jumlah tagihan yang ditagihkan pada pelanggan dihitung berdasarkan jumlah unit pengeluaran yang dilaporkan oleh konsultan. Jarak tempuh menggunakan metode harga per unit. Misalnya, kategori pengeluaran jarak tempuh dapat dikonfigurasi untuk 30 dolar AS (USD) per hari atau 2 USD per mil. Bila konsultan melaporkan jarak tempuh pada suatu proyek, jumlah tagihan dihitung berdasarkan jumlah mil yang dilaporkan oleh konsultan.

> ![Mengkonfigurasi harga untuk kategori pengeluaran.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Harga penjualan proyek dan penggantian

Untuk kuotasi dan kontrak proyek, daftar harga proyek memiliki pola penggantian harga yang berbeda dari daftar harga produk. Pada baris kuotasi Katalog Produk, Anda dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi, karena setiap baris kuotasi mengarah ke satu item Katalog. Namun, pada baris kuotasi berbasis proyek, Anda tidak dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi. Untuk mendukung dua pola pengabaian yang berbeda, PSA telah memperkenalkan Asosiasi daftar harga baru, daftar harga proyek.

> [!NOTE]
> Sebaiknya Anda memiliki daftar harga terpisah untuk sumber daya proyek dan item Katalog Anda, karena perbedaan perilaku antara keduanya saat Anda mengganti harga.

Setiap entitas berikut dapat memiliki satu atau beberapa daftar harga penjualan terkait untuk harga proyek:

- Pelanggan (Akun) 
- Peluang 
- Kuotasi 
- Kontrak Proyek

Asosiasi entitas ini dengan daftar harga ditunjukkan oleh daftar harga proyek. Anda dapat mengaitkan satu atau beberapa daftar harga dengan entitas pelanggan, peluang, kuotasi, dan entitas penjualan kontrak proyek.

Daftar harga proyek default tidak secara otomatis dimasukkan ke rekaman pelanggan. Namun, Anda dapat melampirkan daftar harga proyek secara manual ke rekaman pelanggan. Namun demikian, Anda harus melampirkan daftar harga proyek secara manual hanya bila Anda memiliki perjanjian harga kustom dengan pelanggan. 

Bila daftar harga proyek dilampirkan ke entitas penjualan, PSA memvalidasi informasi berikut:

- Daftar harga memiliki konteks **penjualan**. 
- Mata uang daftar harga cocok dengan mata uang pelanggan. 

Pada kontrak proyek, PSA menggunakan urutan prioritas berikut untuk secara otomatis mengatur daftar harga proyek yang terkait:

1. Kuotasi
2. Peluang
3. Pelanggan 
4. Pengaturan global untuk PSA

Bila daftar harga proyek dimasukkan secara default, PSA memvalidasi bahwa mata uang cocok dengan mata uang pelanggan, dan bahwa daftar harga default yang telah dimasukkan memiliki konteks **penjualan**.

Anda dapat mengaitkan beberapa daftar harga proyek dengan entitas pelanggan, peluang, kuotasi, dan entitas kontrak proyek. Kemampuan ini mendukung harga default spesifik tanggal untuk kontrak proyek berjalan lama, di mana Anda memerlukan lebih dari satu daftar harga untuk menjelaskan pembaruan harga yang terjadi karena inflasi. Namun, jika daftar harga yang Anda kaitkan dengan pelanggan, peluang, kuotasi, atau entitas kontrak proyek memiliki efektivitas tanggal tumpang tindih, harga default mungkin salah. Oleh karena itu, Anda harus memastikan bahwa daftar harga proyek yang memiliki efektivitas tanggal tumpang tindih tidak terkait dengan entitas tersebut.

### <a name="deal-specific-price-overrides"></a>Penimpaan harga spesifik transaksi

Dalam PSA, Anda dapat membuat penimpaan spesifik transaksi untuk harga yang dipilih pada daftar harga proyek yang dimasukkan secara default pada kuotasi atau kontrak proyek.

Secara default, kontrak proyek selalu mendapatkan salinan dari daftar harga penjualan induk, bukan link langsung ke sana. Perilaku ini membantu menjamin bahwa perjanjian harga yang dibuat dengan pelanggan untuk pernyataan pekerjaan (SOW) tidak berubah jika daftar harga Master diubah.

Namun, pada kuotasi, Anda dapat menggunakan daftar harga Master. Atau, Anda dapat menyalin daftar harga Master dan mengeditnya untuk membuat daftar harga kustom yang berlaku hanya untuk kuotasi tersebut. Untuk membuat daftar harga baru yang spesifik untuk kuotasi, pada halaman **kuotasi**, pilih **buat harga kustom**. Anda dapat mengakses daftar harga proyek spesifik kesepakatan hanya dari kuotasi. 

Bila Anda membuat daftar harga proyek kustom, hanya komponen proyek dari daftar harga yang akan disalin. Dengan kata lain, daftar harga baru dibuat sebagai salinan dari daftar harga proyek yang ada yang dilampirkan pada kuotasi, dan daftar harga baru ini hanya memiliki harga peran yang terkait dan harga kategori transaksi.

> ![Melihat dan mengkonfigurasi harga kustom untuk kontrak proyek.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Pelacakan Biaya

PSA melacak biaya untuk penggunaan waktu sumber daya manusia dalam proyek. Ia juga melacak biaya untuk pengeluaran lain yang tidak dapat diperoleh selama proyek, seperti biaya perjalanan.

Seperti tarif tagihan, tingkat biaya untuk sumber daya manusia juga diatur menggunakan daftar harga. Berikut adalah perbedaan utama dalam perilaku daftar harga biaya dan daftar harga penjualan:

- Tingkat biaya sumber daya tidak dapat ditimpa pada proyek, kontrak, atau kuotasi tertentu. Namun, tarif tagihan dapat diganti secara per transaksi jika perubahan dibuat yang khusus untuk sifat transaksi. 

- Urutan berikut digunakan untuk menangani daftar harga biaya:

    1. Daftar harga biaya yang dilampirkan ke unit organisasi.
    2. Daftar harga biaya yang dilampirkan ke parameter Project Service. Karena daftar harga biaya dalam banyak mata uang yang berbeda dapat dilampirkan ke parameter Project Service, PSA melakukan pencocokan mata uang antara mata uang unit organisasi kontrak proyek, kontrak, atau kuotasi, dan mata uang dari daftar harga biaya.
    3. Untuk pengeluaran, metode harga pada biaya dan markup terhadap biaya tidak berlaku pada daftar harga biaya. Meskipun metode harga ini digunakan pada baris daftar harga biaya untuk menyiapkan biaya kategori transaksi, sistem akan mengabaikan, dan tidak ada harga default yang dimasukkan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]