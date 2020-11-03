---
title: Mengkonfigurasi akuntansi untuk proyek internal
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi praktik akuntansi untuk proyek internal dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078418"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="c1322-103">Mengkonfigurasi akuntansi untuk proyek internal</span><span class="sxs-lookup"><span data-stu-id="c1322-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="c1322-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="c1322-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c1322-105">Proyek internal memungkinkan perusahaan melacak biaya yang terkait dengan aktivitas yang tidak ditagihkan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="c1322-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="c1322-106">Contoh proyek internal mencakup:</span><span class="sxs-lookup"><span data-stu-id="c1322-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="c1322-107">Mengembangkan produk, seperti aplikasi seluler, dan melacak biaya yang terkait dengan pengembangan.</span><span class="sxs-lookup"><span data-stu-id="c1322-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="c1322-108">Mengelola waktu dan pengeluaran pra-penjualan.</span><span class="sxs-lookup"><span data-stu-id="c1322-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="c1322-109">Proyek internal pra-penjualan ini dapat dikonversi nanti ke proyek yang dapat ditagih jika kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c1322-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="c1322-110">Setiap proyek yang tidak terkait dengan kontrak dalam Dynamics 365 Project Operations diperlakukan sebagai internal.</span><span class="sxs-lookup"><span data-stu-id="c1322-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="c1322-111">Profil biaya dan pendapatan proyek tidak digunakan untuk menentukan aturan akuntansi untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="c1322-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="c1322-112">Biaya proyek internal selalu diposting menggunakan prinsip laba-rugi.</span><span class="sxs-lookup"><span data-stu-id="c1322-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="c1322-113">Akun buku besar untuk posting ditetapkan pada halaman **penataan posting buku besar**.</span><span class="sxs-lookup"><span data-stu-id="c1322-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="c1322-114">Transaksi waktu diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **alokasi gaji**.</span><span class="sxs-lookup"><span data-stu-id="c1322-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="c1322-115">Transaksi pengeluaran diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **akun pengimbang untuk pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="c1322-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="c1322-116">Setelah transaksi diposting ke proyek, jika proyek terkait dengan kontrak proyek, sistem akan membalikkan semua transaksi yang terkumpul dan membuat transaksi yang dapat ditagih baru.</span><span class="sxs-lookup"><span data-stu-id="c1322-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="c1322-117">Transaksi yang dapat ditagih mengikuti aturan akuntansi yang ditentukan di profil biaya dan pendapatan proyek masing-masing.</span><span class="sxs-lookup"><span data-stu-id="c1322-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


