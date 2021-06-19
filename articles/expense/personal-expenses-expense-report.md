---
title: Menangani Pengeluaran pribadi pada laporan pengeluaran
description: Informasi topik ini berisi informasi tentang cara menangani pengeluaran pribadi yang ditanggung oleh karyawan saat bepergian untuk keperluan bisnis.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025688"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="4f786-103">Menangani Pengeluaran pribadi pada laporan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="4f786-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="4f786-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="4f786-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4f786-105">Selama perjalanan bisnis, karyawan dapat membebankan biaya pribadi ke kartu kredit perusahaan mereka.</span><span class="sxs-lookup"><span data-stu-id="4f786-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="4f786-106">Jika proses belum ditentukan untuk menangani pengeluaran pribadi, proses persetujuan laporan pengeluaran mungkin terganggu saat karyawan mengirimkan laporan pengeluaran terperinci mereka.</span><span class="sxs-lookup"><span data-stu-id="4f786-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="4f786-107">Ada dua metode yang dapat Anda gunakan untuk menangani pengeluaran pribadi karyawan:</span><span class="sxs-lookup"><span data-stu-id="4f786-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="4f786-108">**Dibayar oleh karyawan**: organisasi Anda tidak membayar pengeluaran pribadi yang muncul pada tagihan untuk kartu kredit perusahaan.</span><span class="sxs-lookup"><span data-stu-id="4f786-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="4f786-109">Sebaliknya, karyawan membayar vendor kartu kredit secara langsung untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4f786-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="4f786-110">**Dibayar oleh perusahaan**: Organisasi Anda membayar tagihan penuh untuk kartu kredit korporasi, kemudian mendebit akun pekerja untuk pengeluaran pribadi.</span><span class="sxs-lookup"><span data-stu-id="4f786-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="4f786-111">Anda dapat memilih metode yang digunakan organisasi pada halaman **parameter manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="4f786-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="4f786-112">Mengaktifkan fungsi pengeluaran terpisah bila bidang jumlah pribadi telah ditentukan nilainya</span><span class="sxs-lookup"><span data-stu-id="4f786-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="4f786-113">Fitur, **Aktifkan fungsi pengeluaran terpisah bila bidang jumlah pribadi telah ditentukan nilainya** hanya berlaku untuk laporan pengeluaran yang disetujui menggunakan alur kerja tingkat baris.</span><span class="sxs-lookup"><span data-stu-id="4f786-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="4f786-114">Laporan disetujui dengan membuka **Proses Laporan pengeluaran** > **Laporan pengeluaran yang ditetapkan kepada saya** > **Buka laporan pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="4f786-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="4f786-115">Untuk mengaktifkan fitur ini, buka **Ruang Kerja** > **Manajemen Fitur**, pilih **Aktifkan fungsi pengeluaran terpisah bila bidang jumlah pribadi memiliki nilai yang ditentukan**, lalu pilih **Aktifkan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="4f786-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="4f786-116">Bila fitur diaktifkan, baris pengeluaran yang menggunakan fungsi ini akan menghasilkan dua baris saat laporan dikirim.</span><span class="sxs-lookup"><span data-stu-id="4f786-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="4f786-117">Dua baris dibuat sehingga pemberi izin dapat menyetujui setiap baris secara terpisah.</span><span class="sxs-lookup"><span data-stu-id="4f786-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
