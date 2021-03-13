---
title: Aktiver og arbejdsordrer
description: I dette emne beskrives aktiver og arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cddb0a25286c8ce9d72aef0b835809705ad577a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020933"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="dca1d-103">Aktiver og arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="dca1d-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="dca1d-104">I dette emne beskrives aktiver og arbejdsordrer i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="dca1d-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="dca1d-105">Aktiver og arbejdsordrer er de centrale dele af Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="dca1d-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="dca1d-106">Et *Aktiv* er en maskine eller en maskindel, der kræver kontinuerlig vedligeholdelse og service.</span><span class="sxs-lookup"><span data-stu-id="dca1d-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="dca1d-107">Aktiver kan oprettes i en hierarkisk struktur, og de kan relateres til arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="dca1d-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="dca1d-108">Vedligeholdelsesjob kan planlægges på alle niveauer i aktivstrukturen.</span><span class="sxs-lookup"><span data-stu-id="dca1d-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="dca1d-109">Der oprettes forskellige data, såsom produktoplysninger og aktivspecifikation samt påkrævede vedligeholdelsesplaner, for hvert aktiv.</span><span class="sxs-lookup"><span data-stu-id="dca1d-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="dca1d-110">I følgende illustration vises en oversigt over aktivdata og tilknytningen af aktiver til jobtyper.</span><span class="sxs-lookup"><span data-stu-id="dca1d-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="dca1d-111">Rød tekst bruges til eksempler, der viser nedarvning og afhængigheder.</span><span class="sxs-lookup"><span data-stu-id="dca1d-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Diagram, der viser aktivdata vedrørende jobtyper](media/05-overview-image.png)

<span data-ttu-id="dca1d-113">Hver arbejdsordre har en arbejdsordretype, såsom forebyggende vedligeholdelse, korrigerende vedligeholdelse eller inspektion.</span><span class="sxs-lookup"><span data-stu-id="dca1d-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="dca1d-114">Arbejdsordren indeholder et eller flere arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="dca1d-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="dca1d-115">Alle arbejdsordrejob definerer et job, der skal udføres på et aktiv og en relateret jobtype.</span><span class="sxs-lookup"><span data-stu-id="dca1d-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="dca1d-116">Eksempler på relaterede jobtyper omfatter 10.000 km, 50.000 km, 1 års eftersyn og sikkerhedsinspektion.</span><span class="sxs-lookup"><span data-stu-id="dca1d-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="dca1d-117">En arbejdsordre kan relateres til flere aktiver.</span><span class="sxs-lookup"><span data-stu-id="dca1d-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="dca1d-118">I følgende illustration vises en oversigt over nøgledataene i en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="dca1d-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Diagram, der viser nøgledata i en arbejdsordre](media/06-overview-image.png)

<span data-ttu-id="dca1d-120">En arbejdsordre kan relateres til en anden arbejdsordre, og jobtyper kan indeholde efterfølgende job, der opretter en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="dca1d-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="dca1d-121">Generelt er der ingen afhængigheder mellem arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="dca1d-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="dca1d-122">Derfor kan arbejdsordrene ændre deres livscyklustilstand og planlægges uafhængigt af hinanden.</span><span class="sxs-lookup"><span data-stu-id="dca1d-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="dca1d-123">Arbejdsordrer kan oprettes på forskellige måder, der er relateret til korrigerende, forebyggende eller proaktiv vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="dca1d-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="dca1d-124">Du kan også oprette arbejdsordre manuelt.</span><span class="sxs-lookup"><span data-stu-id="dca1d-124">You can also create work orders manually.</span></span> <span data-ttu-id="dca1d-125">I følgende illustration vises en oversigt over processen for automatisk eller manuel oprettelse af arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="dca1d-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Diagram, der viser automatisk eller manuel oprettelse af arbejdsordrer](media/07-overview-image.png)

<span data-ttu-id="dca1d-127">Adskillige trin skal fuldføres, når du vil planlægge og køre et vedligholdelsesjob på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="dca1d-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="dca1d-128">I følgende illustration vises en oversigt over processen for en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="dca1d-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Diagram, der viser oversigt over behandling af en arbejdsordre](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="dca1d-130">Når du generelt arbejder i Dynamics 365 Supply Chain Management og modulet **Styring af aktiver**, skal du vælge **Ny** for at oprette en ny post, **Rediger** for at opdatere en eksisterende post og **Gem** for at gemme nye eller redigerede data.</span><span class="sxs-lookup"><span data-stu-id="dca1d-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
