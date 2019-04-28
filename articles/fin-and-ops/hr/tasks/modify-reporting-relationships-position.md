---
title: Redigere rapporteringsrelationerne for en stilling
description: Denne procedure viser, hvordan du ændrer rapporteringsrelation for en medarbejder.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a1afd2c1cdc2ebaa303030d01b3bbe5fd2af44f
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "857263"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="08ccd-103">Redigere rapporteringsrelationerne for en stilling</span><span class="sxs-lookup"><span data-stu-id="08ccd-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08ccd-104">Denne procedure viser, hvordan du ændrer rapporteringsrelation for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="08ccd-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="08ccd-105">Den rapporteringsrelationen kan bruges til at planlægge rute for dokumenter via arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="08ccd-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="08ccd-106">Proceduren viser også, hvordan medarbejderen tildeles til flere hierarkier.</span><span class="sxs-lookup"><span data-stu-id="08ccd-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="08ccd-107">En medarbejder kan eksempelvis være en del af et projektteam med en uformel rapporteringsrelation til en projektleder.</span><span class="sxs-lookup"><span data-stu-id="08ccd-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="08ccd-108">Yderligere rapporteringsrelationer kan defineres for stillingen for at imødekomme forskellige projekt- eller matrixscenarier.</span><span class="sxs-lookup"><span data-stu-id="08ccd-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="08ccd-109">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="08ccd-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="08ccd-110">Gå til Personale > Stillinger > Stillinger.</span><span class="sxs-lookup"><span data-stu-id="08ccd-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="08ccd-111">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="08ccd-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="08ccd-112">For eksempel kan du filtrere på feltet Stilling med værdien '000091'.</span><span class="sxs-lookup"><span data-stu-id="08ccd-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="08ccd-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="08ccd-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="08ccd-114">Udvid sektionen Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="08ccd-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="08ccd-115">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="08ccd-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="08ccd-116">Indtast eller vælg en værdi i feltet Rapportér til.</span><span class="sxs-lookup"><span data-stu-id="08ccd-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="08ccd-117">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="08ccd-117">Click Create.</span></span>
8. <span data-ttu-id="08ccd-118">Udvid eller skjul sektionen Relationer.</span><span class="sxs-lookup"><span data-stu-id="08ccd-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="08ccd-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="08ccd-119">Click Add.</span></span>
10. <span data-ttu-id="08ccd-120">Markér afkrydsningsfeltet til venstre for gitteret.</span><span class="sxs-lookup"><span data-stu-id="08ccd-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="08ccd-121">Indtast eller vælg en værdi i feltet Hierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="08ccd-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="08ccd-122">Eksempel: Projekt</span><span class="sxs-lookup"><span data-stu-id="08ccd-122">Example: Project</span></span>  
12. <span data-ttu-id="08ccd-123">Indtast eller vælg en værdi i feltet Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="08ccd-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="08ccd-124">Eksempel: 000437</span><span class="sxs-lookup"><span data-stu-id="08ccd-124">Example:  000437</span></span>
13. <span data-ttu-id="08ccd-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="08ccd-125">Click Save.</span></span>

