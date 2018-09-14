--- 
title: "Tilføje en eksisterende aktivitet til en produktionsflowversion"
description: "Når du opretter nye versioner af produktionsflow, kan du vælge at føje aktiviteter, der er oprettet for de ældre versioner, til den nye version."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 032855125ccd14fbdc1e1bdb735c92ce70853fb0
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="865a1-103">Tilføje en eksisterende aktivitet til en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="865a1-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="865a1-104">Når du opretter nye versioner af produktionsflow, kan du vælge at føje aktiviteter, der er oprettet for de ældre versioner, til den nye version.</span><span class="sxs-lookup"><span data-stu-id="865a1-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="865a1-105">Denne fremgangsmåde viser, hvordan du kan oprette en ny version for et eksisterende produktionsflow uden at kopiere aktiviteterne.</span><span class="sxs-lookup"><span data-stu-id="865a1-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="865a1-106">I næste trin føjes der en eksisterende aktivitet til den nye version.</span><span class="sxs-lookup"><span data-stu-id="865a1-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="865a1-107">Denne opgave kræver et produktionsflow, hvor version og aktiviteter allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="865a1-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="865a1-108">Opret en ny version af produktionsflowet</span><span class="sxs-lookup"><span data-stu-id="865a1-108">Create a new production flow version</span></span>
1. <span data-ttu-id="865a1-109">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="865a1-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="865a1-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="865a1-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="865a1-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="865a1-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="865a1-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="865a1-112">Click Edit.</span></span>
5. <span data-ttu-id="865a1-113">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="865a1-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="865a1-114">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="865a1-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="865a1-115">Bemærk, at før du opretter en ny produktionsflowversion, skal du sørge for at kontrollere udløbsdato og klokkeslæt for den aktive version.</span><span class="sxs-lookup"><span data-stu-id="865a1-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="865a1-116">Den nye version oprettes med en ikrafttrædelsesdato, som opretter knyttes til udløbsdatoen for den valgte version.</span><span class="sxs-lookup"><span data-stu-id="865a1-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="865a1-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="865a1-117">Click Add.</span></span>
8. <span data-ttu-id="865a1-118">Vælg Nej i feltet Kopier fra version.</span><span class="sxs-lookup"><span data-stu-id="865a1-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="865a1-119">Vælg Nej for at starte med en tom version, hvis de fleste af aktiviteterne i den kopierede version erstattes af nye aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="865a1-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="865a1-120">Tilføj de uændrede aktiviteter manuelt i formen Tilføj eksisterende funktion i aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="865a1-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="865a1-121">Vælg Nej i feltet Dupliker kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="865a1-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="865a1-122">Når aktiviteterne ikke kopieres til den nye version, er det ikke muligt at kopiere kanban-reglerne på tidspunktet for oprettelse af den nye version.</span><span class="sxs-lookup"><span data-stu-id="865a1-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="865a1-123">I stedet skal du bruge funktionen til udskiftning af kanban-regler senere i formen for kanban-regler til at erstatte kanban-regler i den gamle version af produktionsflowet med kanban-regler, der bruger aktiviteterne i den nye version.</span><span class="sxs-lookup"><span data-stu-id="865a1-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="865a1-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="865a1-124">Click OK.</span></span>
11. <span data-ttu-id="865a1-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="865a1-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="865a1-126">Tilføj en eksisterende aktivitet</span><span class="sxs-lookup"><span data-stu-id="865a1-126">Add an existing activity</span></span>
1. <span data-ttu-id="865a1-127">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="865a1-127">Click Activities.</span></span>
2. <span data-ttu-id="865a1-128">Klik på Tilføj eksisterende for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="865a1-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="865a1-129">Find og vælg en eksisterende aktivitet, der skal føjes til den nye produktionsflowversion.</span><span class="sxs-lookup"><span data-stu-id="865a1-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="865a1-130">Bemærk, at listen viser alle aktiviteter, der er oprettet for denne produktionsflow for alle tidligere versioner af flowet.</span><span class="sxs-lookup"><span data-stu-id="865a1-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="865a1-131">Indtast eller vælg en værdi i feltet Aktivitet.</span><span class="sxs-lookup"><span data-stu-id="865a1-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="865a1-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="865a1-132">Click OK.</span></span>


