---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (15. november 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a571568850a675f3472f2b62df33c0c35d905af0
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551374"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="bdf67-103">Nyheder eller ændringer i Dynamics 365 Talent - Core HR (15. november 2018)</span><span class="sxs-lookup"><span data-stu-id="bdf67-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bdf67-104">**Build 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="bdf67-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="bdf67-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="bdf67-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="bdf67-106">Andre ændringer/rettelser</span><span class="sxs-lookup"><span data-stu-id="bdf67-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="bdf67-107">Det er ikke muligt at ændres medarbejderens aktuelle stilling til en fremtidig åben stilling</span><span class="sxs-lookup"><span data-stu-id="bdf67-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="bdf67-108">Der er foretaget en ændring, som giver mulighed for overførsler af stillinger, når stillingen først er tilgængelig på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="bdf67-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="bdf67-109">Stillingen vises ikke, når du opretter en ny medarbejder</span><span class="sxs-lookup"><span data-stu-id="bdf67-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="bdf67-110">Der er foretaget en ændring for at vise alle ledige stillinger, der er tilgængelige for tildeling ved ansættelse af nye medarbejdere i Talent.</span><span class="sxs-lookup"><span data-stu-id="bdf67-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="bdf67-111">Dette omfatter historiske stillinger, eller hvis stillingerne er dateret i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="bdf67-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="bdf67-112">Stillinger vises nu korrekt ud fra startdatoen for ansættelsen.</span><span class="sxs-lookup"><span data-stu-id="bdf67-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="bdf67-113">Fratrædelsesdatoen vises på grundlag af brugerindstillinger</span><span class="sxs-lookup"><span data-stu-id="bdf67-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="bdf67-114">Er der foretaget en ændring af listen over tidligere medarbejdere, som tager højde for eventuelle tidszoneforskydninger for medarbejderens foretrukne tidszone, når du får vist fratrædelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="bdf67-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="bdf67-115">Workflowopgaver, der er tildelt til mig-links viser ikke de korrekte oplysninger</span><span class="sxs-lookup"><span data-stu-id="bdf67-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="bdf67-116">Med denne ændring viser navigation til detaljerne i de enkelte arbejdselementer på listen de korrekte oplysninger for det valgte element.</span><span class="sxs-lookup"><span data-stu-id="bdf67-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="bdf67-117">Dette problem opstod kun med avancerede sikkerhedsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="bdf67-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="bdf67-118">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="bdf67-118">Known issue</span></span>

- <span data-ttu-id="bdf67-119">**Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet.</span><span class="sxs-lookup"><span data-stu-id="bdf67-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="bdf67-120">**Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket.</span><span class="sxs-lookup"><span data-stu-id="bdf67-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="bdf67-121">Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="bdf67-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="bdf67-122">(Dette problem vil blive løst i den næste platformsopdatering).</span><span class="sxs-lookup"><span data-stu-id="bdf67-122">(This issue will be fixed in the next platform update.)</span></span>
