---
title: Mengkonfigurasi akuntansi untuk proyek yang bisa ditagih
description: Topik ini menyediakan informasi tentang pilihan akuntansi untuk proyek yang dapat ditagih.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 32031742b1a9580b9ebdbaf6952a998733be5e8f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896142"
---
# <a name="configure-accounting-for-billable-projects"></a>Mengkonfigurasi akuntansi untuk proyek yang bisa ditagih

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations mendukung berbagai pilihan akuntansi untuk proyek yang dapat ditagih yang mencakup waktu dan materi, serta transaksi harga tetap.

- **Transaksi waktu dan material**: transaksi ini ditagih sebagai kemajuan kerja berdasarkan konsumsi jam, biaya, item, atau biaya pada proyek. Biaya transaksi ini dapat disesuaikan dengan pendapatan pada setiap transaksi dan proyek ditagih seiring pekerjaan berlangsung. Pendapatan proyek juga dapat diperoleh pada saat transaksi terjadi. Selama faktur, pendapatan diakui dan jika berlaku, pendapatan yang diperoleh akan dibalik.
- **Transaksi harga tetap**: Transaksi ini ditagih berdasarkan jadwal penagihan yang didasarkan pada kontrak proyek. Pendapatan transaksi harga tetap dapat dikenali pada faktur atau dihitung dan diposkan secara berkala, berdasarkan **kontrak yang telah diselesaikan** atau **metode persentase yang telah selesai**.

Proyek dianggap dapat ditagih saat dikaitkan dengan satu atau beberapa baris kontrak. Baris kontrak proyek menentukan sendiri metode penagihan dan jenis transaksi yang diizinkan.

Sebagai contoh, fabrikam robotik telah memenangkan kontrak proyek dengan Adatum Corporation untuk pengoptimalan peralatan. Adatum akan membayar sejumlah $10.000 USD untuk menanggung pengeluaran proyek yang terjadi. Ini adalah metode penagihan harga tetap. Waktu dan biaya proyek akan ditagih per penggunaan. Ini adalah metode penagihan untuk waktu dan material. Semua pekerjaan akan dilacak dalam satu proyek bernama, Optimalisasi peralatan Adatum.

Anggota tim proyek mengajukan delapan jam kerja pada proyek pengoptimalan peralatan Adatum. Saat manajer proyek menyetujui waktu ini, sistem menggunakan metode tagihan waktu dan bahan untuk membuat transaksi aktual, faktur, dan akun. Transaksi ini tidak akan disertakan dalam perhitungan perkiraan Pendapatan harga tetap.

Anggota tim proyek lainnya mengirimkan biaya perjalanan untuk $2000,00 USD terhadap proyek pengoptimalan peralatan Adatum, Saat manajer proyek menyetujui pengajuan ini, sistem menggunakan metode tagihan harga tetap untuk membuat transaksi aktual dan akun untuk peluang proyek ini. Pelanggan tidak akan ditagih berdasarkan transaksi ini. Namun, mereka akan ditagih dengan menggunakan tonggak penagihan yang dikonfigurasi secara terpisah. Transaksi pengeluaran, bersama dengan estimasi pengeluaran, akan disertakan dalam perhitungan perkiraan Pendapatan harga tetap.

Prinsip akuntansi untuk transaksi proyek ditentukan dalam profil biaya dan pendapatan proyek. Untuk setiap transaksi proyek, sistem menentukan profil biaya dan pendapatan proyek yang sesuai dengan menggunakan aturan biaya proyek dan profil pendapatan yang telah dikonfigurasi.

## <a name="define-project-cost-and-revenue-profiles"></a>Menentukan profil biaya dan pendapatan proyek 

Profil biaya dan pendapatan proyek menentukan aturan akuntansi untuk transaksi proyek. Profil ini dikonfigurasi dalam manajemen proyek dan akuntansi. 

Selesaikan langkah-langkah berikut untuk membuat profil biaya dan pendapatan proyek baru. 

1. Buka **manajemen proyek dan akuntansi** > **konfigurasi** > **posting** > **profil biaya proyek dan pendapatan**. 
2. Pilih **baru** untuk membuat biaya proyek baru dan profil pendapatan.
3. Di bidang **nama**, masukkan nama dan deskripsi singkat tentang profil.
4. Di bidang **metode penagihan**, pilih **waktu dan bahan** atau **harga tetap**.
5. Perluas fasttab **buku besar**. Bidang pada tab ini menentukan prinsip akuntansi yang digunakan saat transaksi proyek dijurnalkan menggunakan jurnal integrasi Project Operations dan kemudian ditagih melalui proposal faktur proyek.
6. Pilih informasi yang sesuai di bidang berikut di fasttab **buku besar**:

    - **posting Biaya-jam**:

       - *tidak ada Buku besar*: biaya untuk waktu transaksi tidak akan dikirim ke buku besar saat jurnal integrasi Project Operations dikirim. Namun, akuntan dapat mengirimkan biaya menggunakan fungsi posting biaya di lain waktu.
       - **Saldo**: biaya untuk waktu transaksi akan didebet ke jenis akun buku besar, *nilai WIP-biaya* dan dikreditkan ke *akun alokasi gaji* di konfigurasi posting buku besar. Akuntan akan menggunakan fungsi biaya posting untuk memindahkan biaya ini dari akun saldo ke akun laba-rugi secara periodik.
       - **Keuntungan dan kerugian**: saat posting jurnal integrasi operasi proyek, biaya transaksi waktu akan didebet ke biaya jenis akun buku besar *Biaya*, dan dikreditkan ke *akun alokasi penggajian* yang ditetapkan pada tab **biaya** pada halaman **penataan posting Buku besar** (**manajemen proyek dan akuntansi** \> **penataan** \> **posting** \> **penataan posting buku besar**). Konfigurasi ini paling umum untuk transaksi waktu dan material.
        - *Tidak pernah di buku besar*: biaya untuk waktu transaksi tidak akan diposting ke buku besar.

    - **Memposting biaya - pengeluaran**:

         - **Keseimbangan**: ketika memposting jurnal integrasi Project Operations, biaya transaksi pengeluaran akan didebet ke tipe akun buku besar *nilai WIP-biaya* sebagaimana ditetapkan pada tab **biaya** pada halaman **penataan posting buku besar** dan dikreditkan ke akun offset pada baris jurnal. Akun offset default untuk pengeluaran ditentukan dalam **manajemen proyek dan akuntansi** > **penataan** \> **posting** \> **Akun offset default untuk pengeluaran**. Akuntan akan menggunakan fungsi **posting biaya** untuk memindahkan biaya ini dari akun saldo ke akun laba-rugi secara periodik.
        - **Laba dan rugi**: ketika memposting jurnal integrasi Project Operations, biaya transaksi pengeluaran akan didebet ke tipe akun buku besar *Biaya* sebagaimana ditetapkan pada tab **biaya** pada halaman **penataan posting buku besar** dan dikreditkan ke akun offset pada baris jurnal. Akun offset default untuk pengeluaran ditentukan dalam **manajemen proyek dan akuntansi** \> **penataan** \> **posting** \> **Akun offset default untuk pengeluaran**.
       
    - **Tentang memfaktur akun**:

        - **Saldo**: saat posting proposal faktur proyek, transaksi pada akun (tonggak penagihan) akan dikreditkan ke akun buku besar jenis *WIP ditagih - pada akun yang* sebagaimana ditetapkan pada tab **pendapatan** pada halaman **penataan posting Buku besar**, dan didebet ke akun saldo pelanggan.
         - **Laba-rugi**: saat posting proposal faktur proyek, transaksi pada akun (tonggak penagihan) akan dikreditkan ke akun buku besar jenis *pendapatan ditagih - pada akun yang* sebagaimana ditetapkan pada tab **pendapatan** pada halaman **penataan posting Buku besar**, dan didebet ke akun saldo pelanggan. Akun saldo Pelanggan yang ditentukan dalam **piutang dagang** \> **Penataan** \> **profil posting pelanggan**.

   Bila Anda menentukan profil posting untuk metode penagihan waktu dan material, Anda memiliki pilihan untuk mengumpulkan pendapatan per jenis transaksi (jam, pengeluaran, dan ongkos). Jika opsi **akumulasikan pendapatan** diatur ke **ya**, transaksi penjualan yang belum ditagih di jurnal integrasi Project Operations akan direkam ke buku besar. Nilai penjualan didebet ke **WIP - akun nilai penjualan** dan dikreditkan ke akun **pendapatan akrual-nilai penjualan** yang dikonfigurasi pada halaman **pengaturan posting buku besar**, pada tab **pendapatan**. 
  
  > [!NOTE]
  > Pilihannya, **Akumulasi pendapatan** tersedia hanya bila masing-masing jenis transaksi **biaya** diposkan ke akun laba-rugi.
    
7. Perluas fasttab **Estimasi**. Bidang pada tab ini menentukan pengaturan penghitungan untuk estimasi pendapatan harga tetap. Bidang pada tab ini hanya berlaku untuk biaya proyek dan profil pendapatan dengan metode penagihan **harga tetap**.
8. Pilih informasi yang sesuai di bidang berikut di fasttab **Estimasi**:

    - **Prinsip yang digunakan untuk perhitungan penyelesaian proyek**:

        - **Kontrak selesai**: kecocokan biaya dan pengakuan pendapatan tidak terjadi hingga akhir proyek. Biaya menunjukkan WIP dalam saldo hingga proyek selesai.
        - **Persentase yang telah selesai**: pendapatan yang diperoleh dihitung dan diposting ke buku besar setiap periode berdasarkan persentase penyelesaian proyek. Ada beberapa metode yang tersedia untuk menghitung penyelesaian persentase. Metode ini dapat secara otomatis berdasarkan konfigurasi, atau manual.
        - **Tidak ada WIP**: konfigurasi ini digunakan untuk proyek harga tetap dengan rentang waktu singkat dan di mana faktur dan biaya terjadi pada periode yang sama. Dalam kasus ini, nilai bidang **pemfakturan pada akun** pada fasttab **buku besar** secara otomatis diatur ke **Laba-rugi** untuk memastikan pendapatan diakui pada faktur. Proses estimasi pendapatan tidak akan digunakan untuk biaya proyek ini dan profil pendapatan.

    - **Prinsip pencocokan**: bidang ini menentukan cara kerja penghitungan nilai penjualan (pendapatan yang ditambahkan) akan diposting ke buku besar.

        - Menggunakan prinsip **nilai penjualan**, sistem akan menghitung nilai penjualan dengan mencocokkan biaya dan pendapatan, lalu mengirimkannya sebagai satu jumlah.
        - Menggunakan prinsip **produksi dan laba**, sistem akan membagi nilai penjualan menjadi biaya yang direalisasikan dan laba yang dihitung. Ini diposting secara terpisah.

    - **Template biaya**: memungkinkan transaksi proyek dikelompokkan berdasarkan jenis transaksi dan kategori proyek dan menentukan aturan penghitungan penyelesaian persentase untuk grup ini.
    - **Kode periode**: menentukan frekuensi dengan taksiran pendapatan yang dihitung untuk biaya proyek dan profil pendapatan tertentu.
    - **Kategori untuk estimasi**: digunakan untuk posting nilai penjualan (pendapatan akrual) ke transaksi proyek. Pertama, konfigurasikan kategori proyek khusus untuk jenis transaksi **Ongkos**, lalu Atur peringatan, **Estimasi** untuk kategori proyek ini. Selanjutnya, tergantung pada prinsip pencocokan yang dipilih, pilih kategori proyek ini di nilai **penjualan** atau bidang **Laba** di profil biaya proyek dan pendapatan.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Konfigurasi sampel untuk biaya proyek dan profil pendapatan

Waktu dan Material – tidak ada WIP

![Profil biaya dan pendapatan: waktu dan material-tanpa WIP](media/time-material-no-wip.png)

Waktu dan material– WIP (Pendapatan)

![Profil biaya dan pendapatan: waktu dan material-WIP](media/time-material-with-wip.png)

Harga tetap – Tanpa WIP

![profil Biaya dan pendapatan: harga tetap-tidak ada WIP](media/fixed-price-no-wip.png)

Harga tetap – kontrak selesai

![profil Biaya dan pendapatan: harga tetap- Kontrak yang selesai](media/fixed-price-completed-contract.png)

Harga tetap – persentase penyelesaian

![profil Biaya dan pendapatan: harga tetap- Persentase penyelesaian](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Contoh aktivitas akuntansi untuk sampel profil biaya proyek dan pendapatan.

| Aktivitas akuntansi                  | Waktu dan bahan – Tanpa WIP                       | Waktu dan bahan – WIP                                                                                           | Harga tetap – Tanpa WIP                                            | Harga tetap – kontrak selesai                                                                            | Harga tetap – persentase penyelesaian                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Jurnalisasi transaksi waktu    | Debit – biaya <br>Kredit-alokasi penggajian          | Debit – biaya <br>Kredit-alokasi penggajian <br>Debit – nilai penjualan WIP <br>Kredit – nilai penjualan pendapatan akrual                | Debit – biaya <br>Kredit-alokasi penggajian                         | Debit – biaya <br>Kredit-alokasi penggajian                                                                    | Debit – biaya <br>Kredit-alokasi penggajian                       |
| Jurnalisasi transaksi pengeluaran | Debit – biaya <br>Kredit-akun offset untuk pengeluaran | Debit – biaya <br>Kredit-akun offset untuk pengeluaran <br>Debit – nilai penjualan WIP <br>Kredit – nilai penjualan pendapatan akrual      | Debit – biaya <br>Kredit-akun offset untuk pengeluaran                 | Debit – biaya<br> Kredit-akun offset untuk pengeluaran                                                            | Debit – biaya <br>Kredit-akun offset untuk pengeluaran               |
| Memfaktur Pelanggan                | Debit – saldo pelanggan <br>Kredit-pendapatan yang ditagih | Debit – saldo pelanggan <br>Kredit-pendapatan yang ditagih <br>Kredit-debit nilai penjualan WIP – nilai penjualan pendapatan akrual | Debit – saldo pelanggan <br>Kredit-pendapatan yang ditagih-pada akun | Debit – saldo pelanggan <br>Kredit- WIP – Difaktur pada akun                                                  | Debit – saldo pelanggan <br>Kredit- WIP – Difaktur pada akun    |
| Posting Estimasi Pendapatan             | Tidak berlaku                                   | Tidak berlaku                                                                                                    | Tidak Berlaku                                                  | Debit – nilai biaya WIP <br>Kredit –Biaya                                                                         | Debit – WIP – nilai penjualan <br>Kredit – nilai penjualan pendapatan akrual |
| Hapus                         | Tidak berlaku                                   | Tidak berlaku                                                                                                    | Tidak Berlaku                                                  | Kredit – nilai biaya WIP <br>Debit – biaya <br>Kredit – pendapatan akrual – nilai penjualan <br>Debit - WIP Difaktur pada akun | Debit - WIP – Difaktur pada akun <br>Kredit – nilai penjualan WIP     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurasikan aturan profil biaya dan pendapatan proyek

Aturan profil biaya dan pendapatan proyek menentukan profil pendapatan dan biaya proyek yang harus digunakan saat memproses transaksi proyek yang dapat ditagih. Tentukan aturan dengan membuka **manajemen proyek dan akuntansi** \> **Penataan** \> **Posting** \> **Aturan profil biaya dan pendapatan proyek**.

Aturan dapat didefinisikan berdasarkan kontrak proyek, grup proyek, atau proyek tertentu. Sistem akan selalu memilih aturan perincian tertinggi terlebih dahulu.
