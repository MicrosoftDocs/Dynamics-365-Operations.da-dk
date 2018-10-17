--- 
title: Redigere rapporteringsrelationerne for en stilling
description: "Denne procedure viser, hvordan du ændrer rapporteringsrelation for en medarbejder."
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e779a337ff8f8e0199a60e094f4bec9eba49e701
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="fb50d-103">Redigere rapporteringsrelationerne for en stilling</span><span class="sxs-lookup"><span data-stu-id="fb50d-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb50d-104">Denne procedure viser, hvordan du ændrer rapporteringsrelation for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="fb50d-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="fb50d-105">Den rapporteringsrelationen kan bruges til at planlægge rute for dokumenter via arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fb50d-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="fb50d-106">Proceduren viser også, hvordan medarbejderen tildeles til flere hierarkier.</span><span class="sxs-lookup"><span data-stu-id="fb50d-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="fb50d-107">En medarbejder kan eksempelvis være en del af et projektteam med en uformel rapporteringsrelation til en projektleder.</span><span class="sxs-lookup"><span data-stu-id="fb50d-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="fb50d-108">Yderligere rapporteringsrelationer kan defineres for stillingen for at imødekomme forskellige projekt- eller matrixscenarier.</span><span class="sxs-lookup"><span data-stu-id="fb50d-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="fb50d-109">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="fb50d-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="fb50d-110">Gå til Personale > Stillinger > Stillinger.</span><span class="sxs-lookup"><span data-stu-id="fb50d-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="fb50d-111">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="fb50d-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fb50d-112">For eksempel kan du filtrere på feltet Stilling med værdien '000091'.</span><span class="sxs-lookup"><span data-stu-id="fb50d-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="fb50d-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fb50d-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fb50d-114">Udvid sektionen Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="fb50d-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="fb50d-115">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="fb50d-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="fb50d-116">Indtast eller vælg en værdi i feltet Rapportér til.</span><span class="sxs-lookup"><span data-stu-id="fb50d-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="fb50d-117">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="fb50d-117">Click Create.</span></span>
8. <span data-ttu-id="fb50d-118">Udvid eller skjul sektionen Relationer.</span><span class="sxs-lookup"><span data-stu-id="fb50d-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="fb50d-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fb50d-119">Click Add.</span></span>
10. <span data-ttu-id="fb50d-120">Markér afkrydsningsfeltet til venstre for gitteret.</span><span class="sxs-lookup"><span data-stu-id="fb50d-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="fb50d-121">Indtast eller vælg en værdi i feltet Hierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="fb50d-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="fb50d-122">Eksempel: Projekt</span><span class="sxs-lookup"><span data-stu-id="fb50d-122">Example: Project</span></span>  
12. <span data-ttu-id="fb50d-123">Indtast eller vælg en værdi i feltet Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="fb50d-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="fb50d-124">Eksempel: 000437</span><span class="sxs-lookup"><span data-stu-id="fb50d-124">Example:  000437</span></span>
13. <span data-ttu-id="fb50d-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="fb50d-125">Click Save.</span></span>


