---
title: Ikhtisar proses pemfakturan
description: Laporan topik ini memberikan ikhtisar proses pemfakturan di Project Operations untuk skenario berbasis sumber daya/non-stok.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089256"
---
# <a name="invoicing-process-overview"></a>Ikhtisar proses pemfakturan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Project Operations untuk skenario berbasis sumber daya/non-stok menawarkan kemampuan komprehensif yang disesuaikan dengan kebutuhan manajer proyek dan akuntan piutang/akuntan proyek. Untuk proses penagihan, manajer proyek mengelola backlog penagihan proyek dan akuntan piutang/proyek membuat dokumen faktur yang sesuai dan akurat untuk pelanggan.

![Diagram alur faktur](./media/invoicing-flow.png)

Baris kontrak proyek menentukan metode penagihan untuk transaksi proyek yang terkait. Ketika manajer proyek menyetujui waktu dan transaksi pengeluaran, sistem merekam transaksi di entitas **Aktual Proyek** dan mengirimkan informasi tersebut ke modul **manajemen Proyek dan akuntansi** di Dynamics 365 Finance. Akuntan proyek kemudian melihat dan memposting rekaman menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Jurnal ini mencakup rincian akuntansi penting untuk aktual proyek, seperti penagihan, grup pajak penjualan, grup pajak penjualan item penagihan, dan dimensi keuangan.

Manajer proyek dapat memeriksa transaksi penjualan belum tertagih menggunakan metode penagihan waktu dan material pada [backlog penagihan Waktu dan material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) serta penagihan harga tetap dalam [tahapan harga tetap](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Tampilan ini memungkinkan Anda memfilter dan memilih transaksi yang harus disertakan dalam siklus penagihan berikutnya, lalu menandainya sebagai **Siap Ditagih**.

Anda dapat [membuat faktur proforma secara manual](../proforma-invoicing/create-manual-proforma-invoice.md) atau menggunakan [proses periodik](../proforma-invoicing/configure-automated-invoice-creation.md). Manajer proyek dapat [menyesuaikan faktur proforma draf](../proforma-invoicing/manage-proforma-invoice.md) jika diperlukan, lalu mengkonfirmasikannya.

Faktur proforma terkonfirmasi dikirim ke **modul manajemen proyek dan akuntansi di** Finance. Akuntan proyek memformat dan memperbarui proposal faktur proyek, kemudian memposting dan mencetak dokumen. Faktur proyek yang diposting direkam dalam buku besar umum, serta buku besar pembantu Pelanggan dan Proyek.
