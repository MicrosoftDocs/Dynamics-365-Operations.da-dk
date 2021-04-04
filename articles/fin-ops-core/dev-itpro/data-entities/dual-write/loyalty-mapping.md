---
title: Fordelskundekort og belønningspoint
description: I dette emne beskrives integrationen af data om fordelskundekort og belønningspoint i dobbeltskrivning.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568022"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="2b8cc-103">Kundefordelskundekort og -belønningspoint</span><span class="sxs-lookup"><span data-stu-id="2b8cc-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2b8cc-104">Virksomheder klassificerer kunder og leverer avancerede tjenester baseret på kundens indkøbs- og forbrugsmønstre.</span><span class="sxs-lookup"><span data-stu-id="2b8cc-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="2b8cc-105">Dynamics 365 Commerce har f.eks. infrastrukturen og funktionerne til at oprette og håndtere fordelskundekort, belønningspoint, loyalitetsbaseret prissætning og belønningsbaserede indkøbsoplevelser.</span><span class="sxs-lookup"><span data-stu-id="2b8cc-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="2b8cc-106">Når oplysninger om fordelskundekort og belønningspoint i Commerce synkroniseres med Dataverse, kan disse data bruges af Customer Engagement-apps.</span><span class="sxs-lookup"><span data-stu-id="2b8cc-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="2b8cc-107">Dynamics 365 Customer Service-brugere kan f.eks. bruge dataene til at levere de samme avancerede tjenester via helpdesk.</span><span class="sxs-lookup"><span data-stu-id="2b8cc-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="2b8cc-108">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="2b8cc-108">Templates</span></span>

| <span data-ttu-id="2b8cc-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="2b8cc-109">Finance and Operations apps</span></span> | <span data-ttu-id="2b8cc-110">Modelstyrede apps i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2b8cc-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="2b8cc-111">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="2b8cc-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="2b8cc-112">Fordelskundekort</span><span class="sxs-lookup"><span data-stu-id="2b8cc-112">Loyalty card</span></span>                | <span data-ttu-id="2b8cc-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="2b8cc-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="2b8cc-114">Denne skabelon synkroniserer oplysninger om fordelskundekort.</span><span class="sxs-lookup"><span data-stu-id="2b8cc-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="2b8cc-115">Fordelskundebelønningspoint</span><span class="sxs-lookup"><span data-stu-id="2b8cc-115">Loyalty reward points</span></span>       | <span data-ttu-id="2b8cc-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="2b8cc-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="2b8cc-117">Denne skabelon synkroniserer oplysninger om kunders belønningspoint.</span><span class="sxs-lookup"><span data-stu-id="2b8cc-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]