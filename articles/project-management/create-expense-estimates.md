---
title: Perkiraan pengeluaran
description: Topik ini memberikan informasi tentang mendefinisikan atau memperkirakan biaya berdasarkan proyek.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078406"
---
# <a name="expense-estimates"></a><span data-ttu-id="4600e-103">Perkiraan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="4600e-103">Expense estimates</span></span>
<span data-ttu-id="4600e-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="4600e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4600e-105">Seiring dengan mendefinisikan perkiraan berbasis sumber daya, Dynamics 365 Project Operations memungkinkan manajer proyek untuk menentukan biaya berbasis proyek untuk setiap proyek.</span><span class="sxs-lookup"><span data-stu-id="4600e-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="4600e-106">Setiap item biaya dapat dikaitkan dengan tugas proyek atau kategori pengeluaran tertentu.</span><span class="sxs-lookup"><span data-stu-id="4600e-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="4600e-107">Kategori pengeluaran biasanya ditentukan pada tingkat organisasi.</span><span class="sxs-lookup"><span data-stu-id="4600e-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="4600e-108">Harga untuk setiap kategori pengeluaran biasanya didefinisikan dalam hierarki berikut:</span><span class="sxs-lookup"><span data-stu-id="4600e-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="4600e-109">Organisasi</span><span class="sxs-lookup"><span data-stu-id="4600e-109">Organization</span></span>
- <span data-ttu-id="4600e-110">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="4600e-110">Customer</span></span>
- <span data-ttu-id="4600e-111">Kuotasi/Kontrak</span><span class="sxs-lookup"><span data-stu-id="4600e-111">Quote/contract</span></span>

<span data-ttu-id="4600e-112">Selesaikan langkah berikut untuk melihat, menambah, atau menghapus biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="4600e-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="4600e-113">Buka **proyek** , dan pilih proyek yang ingin Anda kerjakan.</span><span class="sxs-lookup"><span data-stu-id="4600e-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="4600e-114">Pilih tab **estimasi proyek** dan lihat daftar pengeluaran proyek.</span><span class="sxs-lookup"><span data-stu-id="4600e-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="4600e-115">Pilih **pengeluaran baru** untuk menambahkan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4600e-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="4600e-116">Atau, pilih pengeluaran untuk dihapus, lalu pilih **Hapus pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="4600e-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="4600e-117">Atribut berikut ditentukan untuk setiap item baris pengeluaran:</span><span class="sxs-lookup"><span data-stu-id="4600e-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="4600e-118">**Kategori** : pengelompokan umum yang digunakan untuk menjelaskan semua pengeluaran yang terjadi pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="4600e-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="4600e-119">**Tanggal mulai** : tanggal saat pengeluaran diperkirakan akan dikeluarkan.</span><span class="sxs-lookup"><span data-stu-id="4600e-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="4600e-120">**Kuantitas** : perkiraan jumlah item pengeluaran untuk kategori tertentu.</span><span class="sxs-lookup"><span data-stu-id="4600e-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="4600e-121">**Harga unit biaya** : harga unit yang digunakan untuk menghitung biaya pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4600e-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="4600e-122">**Harga unit penjualan** : harga unit yang digunakan untuk menghitung harga penjualan dari pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4600e-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

