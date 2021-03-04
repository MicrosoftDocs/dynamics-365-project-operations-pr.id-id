---
title: Konfigurasi Manajemen Pengeluaran
description: Artikel ini menjelaskan pertimbangan dan keputusan yang harus Anda buat selama proses perencanaan sebelum mengkonfigurasi manajemen pengeluaran di Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960341"
---
# <a name="configure-expense-management"></a>Konfigurasi Manajemen Pengeluaran

Topik ini menjelaskan pertimbangan dan keputusan yang harus Anda buat selama proses perencanaan sebelum mengkonfigurasi manajemen pengeluaran. Di manajemen pengeluaran, Anda dapat menyimpan informasi tentang metode pembayaran, permintaan perjalanan, laporan pengeluaran, kebijakan, dan sebagainya.

Karena banyak keputusan yang Anda buat saat merencanakan konfigurasi untuk manajemen pengeluaran berdasarkan hierarki dan struktur keuangan organisasi Anda, Anda harus merujuk ke dokumen perencanaan untuk area tersebut.

## <a name="intercompany-expenses"></a>Pengeluaran antarperusahaan

Bila Anda mengaktifkan biaya antarperusahaan, Anda mengizinkan entitas hukum dan karyawan untuk mengeluarkan biaya atas nama entitas hukum lain, dan menagih pembayaran dari badan hukum kerja dalam organisasi Anda. Contohnya, seorang karyawan di entitas hukum A menyelesaikan proyek untuk badan hukum B, dan proyek ini menimbulkan pengeluaran terkait perjalanan. Jika pengeluaran antarperusahaan diaktifkan, karyawan kemudian dapat mengajukan laporan pengeluaran yang akan memposting pengeluaran ke badan hukum B, dan pengeluaran kemudian harus dibayar oleh entitas hukum A. Jika organisasi Anda tidak memiliki beberapa entitas hukum, Anda tidak perlu mengaktifkan biaya antarperusahaan.

**Keputusan:** Apakah Anda ingin mengaktifkan biaya Antarperusahaan?

## <a name="financial-management"></a>Manajemen keuangan

Manajemen pengeluaran terintegrasi erat dengan manajemen keuangan organisasi Anda. Banyak konfigurasi Anda untuk manajemen pengeluaran akan didasarkan pada keputusan yang telah Anda buat tentang keuangan organisasi Anda. Bagian berikut menjelaskan berbagai area yang memerlukan perencanaan dan keputusan, berdasarkan keputusan keuangan organisasi Anda dan bimbingan dari tim kepemimpinan Anda.

### <a name="per-diems"></a>Pembayaran harian

Anda harus menentukan uang saku karyawan yang disediakan organisasi Anda. Karena setiap uang saku biasanya digunakan untuk mencakup pengeluaran seperti makanan, penginapan, dan biaya insidental lainnya, Anda dapat membuat aturan untuk tunjangan uang saku yang ditawarkan oleh organisasi Anda. Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya. Saat menentukan aturan uang saku, Anda dapat menentukan bahwa persentase tingkat uang saku diabaikan jika pekerja menerima makanan, atau layanan gratis. Anda juga dapat menetapkan tingkat tarif uang saku untuk mengatur jumlah jam minimum dan maksimum yang dapat diterapkan dalam tarif uang saku untuk perjalanan pekerja.

**Keputusan:**

- Aturan default uang saku untuk hari pertama dan terakhir:

    - Berapakah jumlah jam minimum yang dapat diklaim karyawan selama satu hari dan tetap menerima uang saku?
    - Apakah ada pengurangan dalam jumlah yang ditawarkan untuk makanan untuk hari pertama dan hari terakhir? Jika ada pengurangan, berapa persentase pengurangan?
    - Apakah ada pengurangan dalam jumlah yang ditawarkan untuk hotel untuk hari pertama dan hari terakhir? Jika ada pengurangan, berapa persentase pengurangan?
    - Apakah ada pengurangan dalam jumlah yang ditawarkan untuk pengeluaran lain yang ditanggung pada hari pertama dan hari terakhir? Jika ada pengurangan, berapa persentase pengurangan?

- Default aturan uang saku:

    - Apakah ada pengurangan persentase pada penyisihan uang saku untuk setiap makanan jika, misalnya, makanan gratis? Jika ada pengurangan, berapa persentase pengurangan untuk setiap makanan?
    - Apakah pengurangan makanan dihitung per hari, per perjalanan, atau dengan jumlah makanan per hari?
    - Haruskah jumlah uang saku dibulatkan dalam cara biasa atau dibulatkan ke atas?
    - Apakah uang saku dihitung dalam periode 24 jam atau pada hari kalender?

- Aturan uang saku yang didasarkan pada lokasi:

    - Apakah tarif uang saku bervariasi sesuai lokasi? Lokasi apa yang disertakan?
    - Jika tarif uang saku bervariasi menurut lokasi, untuk setiap lokasi, berapa jumlah persentase yang diberikan untuk jenis pengeluaran berikut:

        - Makan
        - Hotel
        - Pengeluaran lain

### <a name="expense-management-journals-and-accounts"></a>Jurnal dan akun manajemen pengeluaran

Manajemen pengeluaran mengharuskan Anda menggunakan beberapa jurnal dan akun. Anda harus memutuskan, misalnya, Apakah akun yang sama digunakan untuk uang muka dan perselisihan kartu kredit.

**Keputusan:**

- Jurnal pembukuan manakah yang merupakan laporan pengeluaran disetujui untuk diposting?
- Akun yang digunakan untuk kasbon?
- Apakah kasbon harus segera diposting?

### <a name="payment-methods"></a>Metode Pembayaran

Bila Anda mengizinkan karyawan untuk mengeluarkan pengeluaran atas nama bisnis Anda, Anda harus menentukan metode pembayaran yang diizinkan untuk digunakan karyawan. Misalnya, Anda dapat mengizinkan karyawan menggunakan uang tunai atau kartu kredit perusahaan. Anda juga dapat mengizinkan karyawan menggunakan kartu kredit pribadi, dan kemudian meminta penggantian kepada karyawan. Anda harus membuat keputusan berikut untuk setiap metode pembayaran yang Anda Izinkan.

**Keputusan:**

- Metode pembayaran apa saja yang diizinkan?
- Siapa yang bertanggung jawab atas pengeluaran metode pembayaran?
- Apakah ada jenis akun offset? Jika ada jenis akun offset, apakah itu?
- Jika ada jenis akun offset, apakah akunnya?
- Jika metode pembayaran adalah kartu kredit, Apakah metode pembayaran hanya digunakan dengan transaksi impor?

### <a name="expense-categories-and-shared-categories"></a>Kategori pengeluaran dan kategori bersama

Bila karyawan membuat laporan pengeluaran, setiap biaya yang direkam harus dikaitkan dengan kategori pengeluaran. Kategori pengeluaran berasal dari kategori bersama yang dapat dibagikan di seluruh entitas hukum di organisasi Anda. Kategori ini juga dapat dibagikan dalam manajemen proyek dan akuntansi, tergantung pada cara yang organisasi Anda tentukan. Berdasarkan definisi organisasi dan panduan dari tim penerapan, tentukan apakah kategori yang digunakan dalam manajemen pengeluaran hanya akan digunakan di manajemen pengeluaran, atau apakah harus dibagikan di antara manajemen proyek dan akuntansi serta manajemen pengeluaran. Ingat, kategori ini dapat dibagi antara proyek dan pengeluaran atau proyek dan produksi, bukan antara pengeluaran dan produksi. Anda harus membuat keputusan berikut untuk setiap kategori pengeluaran.

**Keputusan:**

- Apa itu kategori pengeluaran? Contohnya mencakup kategori untuk penerbangan, Hotel, atau jarak tempuh.
- Dapatkah kategori pengeluaran juga dapat digunakan dalam manajemen proyek dan akuntansi?
- Apa itu jenis pengeluaran?
- Apa yang dimaksud dengan metode pembayaran default untuk kategori pengeluaran?
- Apakah pengeluaran dalam kategori pengeluaran harus diitemkan?
- Apa yang dimaksud akun default utama untuk kategori pengeluaran?
- Apa yang dimaksud dengan grup pajak penjualan item default untuk kategori pengeluaran?
- Apakah metode pembayaran tambahan diizinkan untuk kategori pengeluaran? Jika metode pembayaran tambahan diizinkan, apakah itu?
- Apakah ada subkategori dalam kategori pengeluaran ini? Jika ada subkategori, Anda juga harus membuat keputusan berikut:

    - Apakah ada subkategori yang dikecualikan dari pemulihan pajak?
    - Apa yang dimaksud dengan grup pajak penjualan item dari subkategori?

Jika kategori pengeluaran juga digunakan dalam manajemen proyek dan akuntansi, Jawablah pertanyaan yang tersisa. Atau, lanjutkan ke bagian berikutnya.

- Biaya akun apa yang akan digunakan untuk biaya berikut?

    - Biaya
    - Alokasi penggajian
    - WIP-Nilai biaya
    - Item biaya
    - Item-Nilai biaya-WIP
    - Rugi akrual
    - Rugi akrual-WIP

- Akun pendapatan mana yang akan digunakan untuk yang berikut?

    - Pendapatan yang ditagih
    - pendapatan akrual – nilai penjualan
    - WIP-nilai penjualan
    - Pendapatan akrual-produksi
    - WIP-Produksi
    - Pendapatan akrual-laba
    - WIP-Laba
    - Pendapatan akrual-langganan
    - WIP-Langganan

### <a name="taxes"></a>Pajak

Untuk pajak terkait pengeluaran, Anda harus menentukan apa yang disertakan atau diaktifkan pada laporan pengeluaran.

**Keputusan:**

- Apakah pajak penjualan termasuk dalam jumlah pengeluaran?
- Haruskah pemulihan pajak diaktifkan pada pengeluaran?

    > [!NOTE]
    > Saat Anda merencanakan buku besar, jika Anda memutuskan untuk menerapkan pajak penjualan AS dan aturan pajak penggunaan, Anda tidak dapat mengaktifkan pemulihan pajak pada pengeluaran. (Untuk menerapkan pajak penjualan AS dan menggunakan aturan pajak, atur **Terapkan pilihan aturan perpajakan pajak penjualan** ke **ya**.)

## <a name="policies"></a>Kebijakan

Dengan membuat kebijakan laporan pengeluaran, Anda dapat membantu organisasi menghemat waktu dan uang saat karyawan memiliki pengeluaran atas namanya. Kebijakan membantu menjamin bahwa karyawan tetap dalam anggaran, menyediakan semua informasi yang diperlukan, dan membelanjakan uang hanya saat mereka memerlukannya. Anda harus membuat keputusan berikut untuk setiap kebijakan laporan pengeluaran dan setiap kebijakan persetujuan laporan pengeluaran yang Anda buat.

**Keputusan:**

- Apa nama kebijakan?
- Apa yang dimaksud dengan kebijakan pengeluaran?
- Jika Anda sebelumnya memutuskan untuk mengaktifkan pengeluaran antarperusahaan, perusahaan mana yang akan diterapkan kebijakan ini dalam organisasi Anda?
- Kapan kebijakan menjadi efektif?
- Kapan kebijakan berakhir?
- Apa aturan kebijakan?
- Apa hasil dari aturan kebijakan?
