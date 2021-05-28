---
title: Opsætning af fragtstatus
description: I dette emne beskrives, hvordan du kan fastlægge de statusværdier, som brugerne kan tildele fragt.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022102"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="9b0d8-103">Opsætning af fragtstatus</span><span class="sxs-lookup"><span data-stu-id="9b0d8-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b0d8-104">På siden **Fragtstatusser** skal du oprette det sæt statusværdier, som brugerne kan tildele fragt.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="9b0d8-105">Brugerne kan tildele fragtstatusværdier til alle niveauer af en fragt: fragt, forsendelsescontainer, folio, indkøbsordre og vare (indkøbslinjer og flytteordrelinjer).</span><span class="sxs-lookup"><span data-stu-id="9b0d8-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="9b0d8-106">De bruges til to formål:</span><span class="sxs-lookup"><span data-stu-id="9b0d8-106">They are used for two purposes:</span></span>

- <span data-ttu-id="9b0d8-107">Oplyse brugeren om status for fragten, forsendelsescontainer, folio, indkøbsordre eller vare (indkøbslinjer og flytteordrelinjer).</span><span class="sxs-lookup"><span data-stu-id="9b0d8-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="9b0d8-108">Begrænse brugen af omkostningsområdet ved at forhindre ændringer eller sletninger.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="9b0d8-109">Du kan konfigurere fragtstatusserne ved at gå til **Landingsomkostninger \> Opsætning \> Fragtstatusser**.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="9b0d8-110">Her kan du tilføje, fjerne og redigere statusser ved at bruge knapperne i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="9b0d8-111">Hvert omkostningsområde har sit eget sæt og hierarki over fragtstatusser.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="9b0d8-112">På siden **Fragtstatusser** skal du derfor først vælge det omkostningsområde, du vil se eller oprette fragtstatusser for, i feltet **Kostprisområde**.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="9b0d8-113">Angiv derefter de felter, der er beskrevet i følgende tabel, efter behov for hver fragtstatus.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="9b0d8-114">Bemærk, at status for en fragt også kan ændres automatisk af systemhændelser, f.eks. regler, der er oprettet ved hjælp af sporingskontrolcenteret.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="9b0d8-115">Felt</span><span class="sxs-lookup"><span data-stu-id="9b0d8-115">Field</span></span> | <span data-ttu-id="9b0d8-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9b0d8-116">Description</span></span> |
|---|---|
| <span data-ttu-id="9b0d8-117">Fragtstatus</span><span class="sxs-lookup"><span data-stu-id="9b0d8-117">Voyage status</span></span> | <span data-ttu-id="9b0d8-118">Angiv navnet på fragtstatus.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="9b0d8-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9b0d8-119">Description</span></span> | <span data-ttu-id="9b0d8-120">Indtast en beskrivelse af fragtstatussen.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="9b0d8-121">Rediger</span><span class="sxs-lookup"><span data-stu-id="9b0d8-121">Modify</span></span> | <span data-ttu-id="9b0d8-122">Markér dette afkrydsningsfelt, hvis brugere skal have tilladelse til at redigere fragt, der har denne status.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="9b0d8-123">Delete</span><span class="sxs-lookup"><span data-stu-id="9b0d8-123">Delete</span></span> | <span data-ttu-id="9b0d8-124">Markér dette afkrydsningsfelt, hvis brugere skal have tilladelse til at slette fragt, der har denne status.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="9b0d8-125">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="9b0d8-125">Mandatory</span></span> | <span data-ttu-id="9b0d8-126">Markér dette afkrydsningsfelt for at gøre fragtstatus obligatorisk, så den ikke kan springes over.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="9b0d8-127">Overordnet</span><span class="sxs-lookup"><span data-stu-id="9b0d8-127">Parent</span></span> | <span data-ttu-id="9b0d8-128">Brug dette felt til at oprette et hierarki mellem statusværdierne.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="9b0d8-129">Fragtstatusser kan kun ændres (enten manuelt eller automatisk) nedad i hierarkiet, fra en overordnet status til en af dets underordnede statusser.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="9b0d8-130">Du skal kun konfigurere de specifikke fragtstatusser, som din organisation bruger.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="9b0d8-131">Af typiske fragtstatusser kan nævnes *Bekræftet*, *Varer i transit*, *Modtaget*, *Klar til efterkalkulation* og *Efterkalkuleret*.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="9b0d8-132">Der kan dog være andre statusser.</span><span class="sxs-lookup"><span data-stu-id="9b0d8-132">However, other statuses might be present.</span></span>
