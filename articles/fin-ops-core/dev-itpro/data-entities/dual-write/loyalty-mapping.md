---
title: Fordelskundekort og belønningspoint
description: I dette emne beskrives integrationen af data om fordelskundekort og belønningspoint mellem Finance and Operations-apps og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998008"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="4b6c8-103">Fordelskundekort og belønningspoint</span><span class="sxs-lookup"><span data-stu-id="4b6c8-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="4b6c8-104">Virksomheder klassificerer kunder og leverer avancerede tjenester baseret på kundens indkøbs- og forbrugsmønstre.</span><span class="sxs-lookup"><span data-stu-id="4b6c8-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="4b6c8-105">I Microsoft Dynamics 365-programpakken har Dynamics 365 Commerce infrastrukturen og funktionerne til at oprette og håndtere fordelskundekort, belønningspoint, loyalitetsbaseret prissætning og belønningsbaserede indkøbsoplevelser.</span><span class="sxs-lookup"><span data-stu-id="4b6c8-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="4b6c8-106">Når oplysninger om fordelskundekort og belønningspoint i Commerce synkroniseres til Common Data Service, kan disse data bruges af modelbaserede apps i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4b6c8-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="4b6c8-107">Dynamics 365 Customer Service-brugere kan f.eks. bruge dataene til at levere de samme avancerede tjenester via helpdesk.</span><span class="sxs-lookup"><span data-stu-id="4b6c8-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="4b6c8-108">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="4b6c8-108">Templates</span></span>

| <span data-ttu-id="4b6c8-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="4b6c8-109">Finance and Operations apps</span></span> | <span data-ttu-id="4b6c8-110">Modelstyrede apps i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4b6c8-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="4b6c8-111">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="4b6c8-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="4b6c8-112">Fordelskundekort</span><span class="sxs-lookup"><span data-stu-id="4b6c8-112">Loyalty card</span></span>                | <span data-ttu-id="4b6c8-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="4b6c8-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="4b6c8-114">Denne skabelon synkroniserer oplysninger om fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="4b6c8-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="4b6c8-115">Fordelskundebelønningspoint</span><span class="sxs-lookup"><span data-stu-id="4b6c8-115">Loyalty reward points</span></span>       | <span data-ttu-id="4b6c8-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="4b6c8-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="4b6c8-117">Denne skabelon synkroniserer oplysninger om kunders belønningspoint.</span><span class="sxs-lookup"><span data-stu-id="4b6c8-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
