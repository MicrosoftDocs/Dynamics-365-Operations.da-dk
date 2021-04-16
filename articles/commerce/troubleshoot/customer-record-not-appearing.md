---
title: Debitorposter vises ikke i Commerce Headquarters
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801789"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="75cfb-103">Debitorposter vises ikke i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="75cfb-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75cfb-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kundeposter ikke omgående vises i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75cfb-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="75cfb-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="75cfb-105">Description</span></span>

<span data-ttu-id="75cfb-106">Når du opretter en ny kundepost ved hjælp af tilmeldingsflowet i e-commerce storefronten, vises den tilsvarende debitorpost ikke med det samme i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75cfb-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="75cfb-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="75cfb-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="75cfb-108">Deaktivere kundeoprettelse i async-tilstand</span><span class="sxs-lookup"><span data-stu-id="75cfb-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75cfb-109">Hvis du deaktiverer asynkron oprettelse af kunder, kan det påvirke systemets ydeevne, da oprettelsen af hver post vil medføre en anmodning i realtid til Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="75cfb-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="75cfb-110">Hvis Commerce Headquarters er nede (f.eks. under servicering af flow), vil nye kundeoprettelsesflow desuden give fejl.</span><span class="sxs-lookup"><span data-stu-id="75cfb-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="75cfb-111">Hvis du vil deaktivere kundeoprettelse i async-tilstand i Commerce Headquarters, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="75cfb-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="75cfb-112">Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af onlinebutik \> Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="75cfb-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="75cfb-113">Hvis du ikke allerede bruger en funktionalitetsprofil til din onlinekanal, skal du oprette en.</span><span class="sxs-lookup"><span data-stu-id="75cfb-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="75cfb-114">Sørg for, at indstillingen **Opret debitor i async-tilstand** er angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="75cfb-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="75cfb-115">Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.</span><span class="sxs-lookup"><span data-stu-id="75cfb-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="75cfb-116">Vælg den onlinebutik, der skal deaktiveres asynkron oprettelse af kunder for.</span><span class="sxs-lookup"><span data-stu-id="75cfb-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="75cfb-117">Under fanen **Generelt** skal du kontrollere, at feltet **Funktionalitetsprofil** er angivet til den funktionalitetsprofil, du bruger til din onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="75cfb-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75cfb-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="75cfb-118">Additional resources</span></span>

[<span data-ttu-id="75cfb-119">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="75cfb-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
