---
title: Oprette leasingkladdenavne
description: Dette emne forklarer, hvordan du kan definere navne på leasingkladder. Navne på leasekladder angiver de kladder, som poster, der stammer fra aktivleasing, bogføres på.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e45475530ae56ec51bbfb5642d351822c9abfd7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822993"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="b0d4d-104">Oprette leasingkladdenavne</span><span class="sxs-lookup"><span data-stu-id="b0d4d-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0d4d-105">Navne på leasingkladder angiver de kladder, som transaktioner fra aktivleasing, bogføres på.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="b0d4d-106">Kun de kladdenavne, der er tildelt **Aktivleasing** kladdetypen, vises i felterne **Oprindelig genkendelse** og **Månedlig kladdenavn** på siden **Parametre til aktivleasing**.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="b0d4d-107">Kun kladdetypen **Kreditorfakturaregistrering** kan tildeles til feltet **Fakturakladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="b0d4d-108">Benyt følgende fremgangsmåde for at konfigurere leasingkladdenavne.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="b0d4d-109">Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="b0d4d-110">Under fanen **Generelt** i feltet **Første genkendelseskladdenavn** og vælg en kladde.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="b0d4d-111">Alle posteringer i den første genkendelseskladde bogføres på dette kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="b0d4d-112">Vælg en kladde i feltet **Fakturakladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="b0d4d-113">Hvis indstillingen **Betal til kreditor** er angivet til **Ja** for leasingkartoteket, vil leasing- og udgiftsbetalingsfakturaer blive bogført på dette kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="b0d4d-114">Vælg en kladde i feltet **Leasingkladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="b0d4d-115">Alle poster for afskrivning, renter og kortfristede omposteringer bogføres på dette kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="b0d4d-116">Hvis indstillingen **Betal til kreditor** er angivet til **Nej** for leasingkartoteket, vil leasing- og udgiftsbetalingsbetalinger også blive bogført på dette kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="b0d4d-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]