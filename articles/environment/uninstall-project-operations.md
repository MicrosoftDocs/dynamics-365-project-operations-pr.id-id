---
title: Hapus instalan Dynamics 365 Project Operations
description: Artikel ini menyediakan informasi tentang cara hapus instalan Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911968"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Hapus instalan Dynamics 365 Project Operations 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menghapus instalan Dynamics 365 Project Operations, Anda harus mendapatkan peran Administrator.

1. Buka **Pengaturan** > **Solusi**.

    ![Halaman Pengaturan.](./media/uninstall-proj-ops-solutions.png)
  
2. Hilangkan solusi sesuai urutan yang tercantum dalam tabel berikut. 

    | Langkah | Nama solusi                                    | Catatan                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 2 | ProjectOperations_Anchor                           | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 5 | ProjectService                                     | Tidak ada Catatan tambahan.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Tidak ada Catatan tambahan.                                                                         |
    | 7 | ProjectServiceCore                                 | Tidak ada Catatan tambahan.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 9 | FieldServiceCommon                                 | Diperlukan untuk menulis dua kali dengan Dynamics 365 Finance atau Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Diperlukan untuk menulis dua kali dengan Dynamics 365 Finance atau Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 19 | Dynamics365Notes                                   | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 21 | DualWriteCore                                      | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 23 | Dynamics365AssetManagement                         | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 26 | HCMCommon                                          | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 28 | Pihak                                              | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 29 | Dynamics365Company                                 | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 30 | CurrencyExchangeRates                              | Jika tidak ditemukan, abaikan solusi ini.                                                            |
    | 31 | AssetCommon                                        | Jika tidak ditemukan, abaikan solusi ini.                                                            |
