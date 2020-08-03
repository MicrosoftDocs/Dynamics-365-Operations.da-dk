---
title: Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management
description: I dette emne beskrives funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597110"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="7ad46-103">Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7ad46-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ad46-104">Dette emne opdateres, efterhånden som nye fjernede eller udfasede funktioner dokumenteres til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7ad46-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="7ad46-105">En *fjernet* funktion er ikke længere tilgængelige i produktet.</span><span class="sxs-lookup"><span data-stu-id="7ad46-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="7ad46-106">En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="7ad46-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="7ad46-107">Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="7ad46-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="7ad46-108">Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="7ad46-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="7ad46-109">Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="7ad46-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="7ad46-110">Fjernede eller udfasede funktioner i Supply Chain Management 10.0.11-udgaven</span><span class="sxs-lookup"><span data-stu-id="7ad46-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="7ad46-111">Brug af det indbyggede Supply Chain Management-varedisponeringsprogram til distributionsscenarier</span><span class="sxs-lookup"><span data-stu-id="7ad46-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="7ad46-112">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="7ad46-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7ad46-113">Med henblik på at forbedre ydeevnen og minimere SQL-databasebelastningen under varedisponeringskørsler erstattes det indbyggede Supply Chain Management-varedisponeringsprogram med Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="7ad46-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="7ad46-114">Planlægningsoptimering giver mulighed for kørsler af hurtig planlægning, der også kan udføres inden for kontorets åbningstider.</span><span class="sxs-lookup"><span data-stu-id="7ad46-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="7ad46-115">Dette giver planlæggere mulighed for straks at reagere på behovsmæssige ændringer eller planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="7ad46-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="7ad46-116">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="7ad46-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7ad46-117">Ja, Planlægningsoptimering erstatter det eksisterende indbyggede Supply Chain Management-varedisponeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="7ad46-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="7ad46-118">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="7ad46-118">**Product areas affected**</span></span>         | <span data-ttu-id="7ad46-119">Supply Chain Management – varedisponering</span><span class="sxs-lookup"><span data-stu-id="7ad46-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="7ad46-120">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="7ad46-120">**Deployment option**</span></span>              | <span data-ttu-id="7ad46-121">Kun skybaseret.</span><span class="sxs-lookup"><span data-stu-id="7ad46-121">Cloud only.</span></span> <span data-ttu-id="7ad46-122">Bemærk, at Planlægningsoptimering ikke understøttes med lokale installationer.</span><span class="sxs-lookup"><span data-stu-id="7ad46-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="7ad46-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="7ad46-123">**Status**</span></span>                         | <span data-ttu-id="7ad46-124">Forældet.</span><span class="sxs-lookup"><span data-stu-id="7ad46-124">Deprecated.</span></span> <span data-ttu-id="7ad46-125">Fra april 2021 vil distributionsscenarier ikke længere være understøttet med det indbyggede Dynamics 365 Supply Chain Management-varedisponeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="7ad46-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="7ad46-126">For distributionsscenarier skal kunderne bruge Planlægningsoptimering til varedisponeringsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7ad46-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="7ad46-127">Du kan finde flere oplysninger under [Dokumention til Planlægningsoptimering](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="7ad46-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="7ad46-128">Kunder med lokale installationer af Dynamics 365 Supply Chain Management kan fortsætte med at bruge Supply Chain Management-varedisponeringsprogrammet til distributionsscenarier efter april 2021.</span><span class="sxs-lookup"><span data-stu-id="7ad46-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="7ad46-129">Der kommer dog ikke flere funktionsforbedringer.</span><span class="sxs-lookup"><span data-stu-id="7ad46-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="7ad46-130">Tidligere meddelelser om fjernede eller udfasede funktioner</span><span class="sxs-lookup"><span data-stu-id="7ad46-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="7ad46-131">Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="7ad46-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
