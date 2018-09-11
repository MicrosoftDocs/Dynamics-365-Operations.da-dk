--- 
title: Oprette et organisationshierarki
description: "Brug følgende procedure for at oprette et organisationshierarki."
author: sericks007
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 99819a2bff8d002721397c084babc07ebc070a37
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="66654-103">Oprette et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="66654-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66654-104">Brug følgende procedure for at oprette et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="66654-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="66654-105">Du kan bruge organisationshierarkier for at få vist og rapportere om forskellige perspektiver i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="66654-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="66654-106">Du kan f.eks. oprette et hierarki til skattemæssig, juridisk eller lovpligtig rapportering.</span><span class="sxs-lookup"><span data-stu-id="66654-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="66654-107">Derefter kan du oprette et andet hierarki for at afrapportere økonomiske oplysninger, der ikke er juridisk påkrævet, men bruges til interne afrapportering.</span><span class="sxs-lookup"><span data-stu-id="66654-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="66654-108">Før du opretter et organisationshierarki, skal du oprette organisationer.</span><span class="sxs-lookup"><span data-stu-id="66654-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="66654-109">Yderligere oplysninger finder du i opgaverne "Oprette en juridisk enhed" eller "Oprette en driftsenhed".</span><span class="sxs-lookup"><span data-stu-id="66654-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="66654-110">Du kan også oprette afdelinger og team.</span><span class="sxs-lookup"><span data-stu-id="66654-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="66654-111">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="66654-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="66654-112">Opret et hierarki</span><span class="sxs-lookup"><span data-stu-id="66654-112">Create a hierarchy</span></span>
1. <span data-ttu-id="66654-113">Gå til Virksomhedsadministration > Organisationer > Organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="66654-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="66654-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="66654-114">Click New.</span></span>
3. <span data-ttu-id="66654-115">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="66654-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="66654-116">Klik på Tildel formål.</span><span class="sxs-lookup"><span data-stu-id="66654-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="66654-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="66654-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66654-118">Vælg det formål, du vil tildele til organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="66654-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="66654-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="66654-119">Click Add.</span></span>
7. <span data-ttu-id="66654-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="66654-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="66654-121">Find det hierarki, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="66654-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="66654-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="66654-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="66654-123">Føje organisationer til hierarkiet</span><span class="sxs-lookup"><span data-stu-id="66654-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="66654-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="66654-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66654-125">Vælg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="66654-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="66654-126">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="66654-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="66654-127">Tilføj organisationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="66654-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="66654-128">Klik på Rediger og derefter Indsæt for at tilføje en organisation.</span><span class="sxs-lookup"><span data-stu-id="66654-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="66654-129">Når du er færdig med at foretage ændringer, kan du gemme en kladde og/eller udgive ændringerne.</span><span class="sxs-lookup"><span data-stu-id="66654-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  


