---
title: Sekilas pengeluaran
description: Topik ini menyediakan informasi tentang fungsionalitas Pengeluaran dalam Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078364"
---
# <a name="expense-home-page"></a><span data-ttu-id="a3a64-103">Laman beranda pengeluaran</span><span class="sxs-lookup"><span data-stu-id="a3a64-103">Expense home page</span></span>

<span data-ttu-id="a3a64-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="a3a64-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a3a64-105">Dynamics 365 Project Operations mendukung kemampuan untuk memproses pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="a3a64-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="a3a64-106">Pemrosesan pengeluaran terjadi dengan atau tanpa proyek menggunakan alur kerja yang dapat disesuaikan kebijakan, kategori transaksi, dan persetujuan.</span><span class="sxs-lookup"><span data-stu-id="a3a64-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="a3a64-107">Dalam Project Operations, ada dua model penyebaran yang didukung untuk pengeluaran:</span><span class="sxs-lookup"><span data-stu-id="a3a64-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="a3a64-108">**Penuh** : penyebaran penuh tersedia untuk **Project Operations untuk skenario berbasis sumber daya/non-stok** atau **Project Operations untuk skenario berdasarkan pesanan produksi**.</span><span class="sxs-lookup"><span data-stu-id="a3a64-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="a3a64-109">**Dasar** : penyebaran dasar tersedia untuk **operasi proyek untuk skenario berbasis sumber daya/non-stok** dan **penyebaran sederhana– menangani faktur proforma**.</span><span class="sxs-lookup"><span data-stu-id="a3a64-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="a3a64-110">Penuh</span><span class="sxs-lookup"><span data-stu-id="a3a64-110">Full</span></span> 
<span data-ttu-id="a3a64-111">Penyebaran pengeluaran penuh memberikan penegakan kebijakan lengkap yang mencakup kemampuan untuk membuat kebijakan, seperti:</span><span class="sxs-lookup"><span data-stu-id="a3a64-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="a3a64-112">Batas kategori pengeluaran</span><span class="sxs-lookup"><span data-stu-id="a3a64-112">Expense category limits</span></span>
  - <span data-ttu-id="a3a64-113">Perjalanan</span><span class="sxs-lookup"><span data-stu-id="a3a64-113">Travel</span></span>
  - <span data-ttu-id="a3a64-114">Pembayaran harian</span><span class="sxs-lookup"><span data-stu-id="a3a64-114">Per diem</span></span>
  - <span data-ttu-id="a3a64-115">Impor kartu kredit</span><span class="sxs-lookup"><span data-stu-id="a3a64-115">Credit card imports</span></span>
  - <span data-ttu-id="a3a64-116">Pengenalan karakter optik tanda terima</span><span class="sxs-lookup"><span data-stu-id="a3a64-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="a3a64-117">Dasar</span><span class="sxs-lookup"><span data-stu-id="a3a64-117">Basic</span></span> 
<span data-ttu-id="a3a64-118">Skenario penyebaran pengeluaran dasar hanya memungkinkan Anda untuk merekam pengeluaran dasar terhadap proyek.</span><span class="sxs-lookup"><span data-stu-id="a3a64-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="a3a64-119">Untuk informasi lebih lanjut, lihat [entri pengeluaran (sederhana)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="a3a64-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="a3a64-120">Menentukan penyebaran pengeluaran Anda</span><span class="sxs-lookup"><span data-stu-id="a3a64-120">Determine your Expense deployment</span></span>
<span data-ttu-id="a3a64-121">Untuk menentukan apakah Anda menjalankan penyebaran manajemen pengeluaran dasar, Verifikasikan bahwa URL alamat diakhiri dengan **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="a3a64-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
