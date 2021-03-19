---
title: Mengkonfigurasi akuntansi untuk proyek internal
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi praktik akuntansi untuk proyek internal dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287602"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="6898a-103">Mengkonfigurasi akuntansi untuk proyek internal</span><span class="sxs-lookup"><span data-stu-id="6898a-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="6898a-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="6898a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6898a-105">Proyek internal memungkinkan perusahaan melacak biaya yang terkait dengan aktivitas yang tidak ditagihkan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="6898a-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="6898a-106">Contoh proyek internal mencakup:</span><span class="sxs-lookup"><span data-stu-id="6898a-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="6898a-107">Mengembangkan produk, seperti aplikasi seluler, dan melacak biaya yang terkait dengan pengembangan.</span><span class="sxs-lookup"><span data-stu-id="6898a-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="6898a-108">Mengelola waktu dan pengeluaran pra-penjualan.</span><span class="sxs-lookup"><span data-stu-id="6898a-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="6898a-109">Proyek internal pra-penjualan ini dapat dikonversi nanti ke proyek yang dapat ditagih jika kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6898a-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="6898a-110">Proyek apa pun yang tidak terkait dengan kontrak di Dynamics 365 Project Operations ditangani sebagai internal.</span><span class="sxs-lookup"><span data-stu-id="6898a-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="6898a-111">Profil biaya dan pendapatan proyek tidak digunakan untuk menentukan aturan akuntansi untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="6898a-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="6898a-112">Biaya proyek internal selalu diposting menggunakan prinsip laba-rugi.</span><span class="sxs-lookup"><span data-stu-id="6898a-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="6898a-113">Akun buku besar untuk posting ditetapkan pada halaman **penataan posting buku besar**.</span><span class="sxs-lookup"><span data-stu-id="6898a-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="6898a-114">Transaksi waktu diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **alokasi gaji**.</span><span class="sxs-lookup"><span data-stu-id="6898a-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="6898a-115">Transaksi pengeluaran diposting dengan mendedebit akun **biaya** dan mengkreditkan akun **akun pengimbang untuk pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="6898a-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="6898a-116">Setelah transaksi diposting ke proyek, jika proyek terkait dengan kontrak proyek, sistem akan membalikkan semua transaksi yang terkumpul dan membuat transaksi yang dapat ditagih baru.</span><span class="sxs-lookup"><span data-stu-id="6898a-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="6898a-117">Transaksi yang dapat ditagih mengikuti aturan akuntansi yang ditentukan di profil biaya dan pendapatan proyek masing-masing.</span><span class="sxs-lookup"><span data-stu-id="6898a-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]