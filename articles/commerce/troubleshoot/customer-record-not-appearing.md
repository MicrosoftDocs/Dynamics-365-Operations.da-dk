---
title: Debitorposter vises ikke i Commerce Headquarters
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018476"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="67b74-103">Debitorposter vises ikke i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="67b74-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67b74-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="67b74-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="67b74-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="67b74-105">Description</span></span>

<span data-ttu-id="67b74-106">Når du opretter en ny kundepost ved hjælp af tilmeldingsflowet i e-commerce storefronten, vises den tilsvarende debitorpost ikke med det samme i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="67b74-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="67b74-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="67b74-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="67b74-108">Deaktivere kundeoprettelse i async-tilstand</span><span class="sxs-lookup"><span data-stu-id="67b74-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67b74-109">Hvis du deaktiverer asynkron oprettelse af kunder, kan det påvirke systemets ydeevne, da oprettelsen af hver post vil medføre en anmodning i realtid til Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="67b74-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="67b74-110">Hvis Commerce Headquarters er nede (f.eks. under servicering af flow), vil nye kundeoprettelsesflow desuden give fejl.</span><span class="sxs-lookup"><span data-stu-id="67b74-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="67b74-111">Hvis du vil deaktivere kundeoprettelse i async-tilstand i Commerce Headquarters, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="67b74-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="67b74-112">Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="67b74-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="67b74-113">Hvis du ikke allerede bruger en funktionalitetsprofil til din onlinekanal, skal du oprette en.</span><span class="sxs-lookup"><span data-stu-id="67b74-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="67b74-114">Sørg for, at indstillingen **Opret debitor i async-tilstand** er angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="67b74-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="67b74-115">Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.</span><span class="sxs-lookup"><span data-stu-id="67b74-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="67b74-116">Vælg den onlinebutik, der skal deaktiveres asynkron oprettelse af kunder for.</span><span class="sxs-lookup"><span data-stu-id="67b74-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="67b74-117">Under fanen **Generelt** skal du kontrollere, at feltet **Funktionalitetsprofil** er angivet til den funktionalitetsprofil, du bruger til din onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="67b74-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67b74-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="67b74-118">Additional resources</span></span>

[<span data-ttu-id="67b74-119">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="67b74-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
