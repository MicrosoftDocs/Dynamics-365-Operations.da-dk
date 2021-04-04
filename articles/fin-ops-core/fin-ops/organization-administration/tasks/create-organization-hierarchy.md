---
title: Oprette et organisationshierarki
description: Brug følgende procedure for at oprette et organisationshierarki.
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d61d6eee3b55087d633a8416fbed3a6192e82b2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560573"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="d4ef9-103">Oprette et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="d4ef9-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4ef9-104">Brug følgende procedure for at oprette et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="d4ef9-105">Du kan bruge organisationshierarkier for at få vist og rapportere om forskellige perspektiver i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="d4ef9-106">Du kan f.eks. oprette et hierarki til skattemæssig, juridisk eller lovpligtig rapportering.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="d4ef9-107">Derefter kan du oprette et andet hierarki for at afrapportere økonomiske oplysninger, der ikke er juridisk påkrævet, men bruges til interne afrapportering.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="d4ef9-108">Før du opretter et organisationshierarki, skal du oprette organisationer.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="d4ef9-109">Yderligere oplysninger finder du i opgaverne "Oprette en juridisk enhed" eller "Oprette en driftsenhed".</span><span class="sxs-lookup"><span data-stu-id="d4ef9-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="d4ef9-110">Du kan også oprette afdelinger og team.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="d4ef9-111">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="d4ef9-112">Opret et hierarki</span><span class="sxs-lookup"><span data-stu-id="d4ef9-112">Create a hierarchy</span></span>
1. <span data-ttu-id="d4ef9-113">Gå til **Navigationsrude > Moduler > Virksomhedsadministration > Organisationer > Organisationshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="d4ef9-114">Klik på **Ny** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="d4ef9-115">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d4ef9-116">Klik på **Tildel formål** i sektionen **Formål**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="d4ef9-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="d4ef9-118">Vælg det formål, du vil tildele til organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="d4ef9-119">Klik på **Tilføj** i sektionen **Tildelte hierarkier**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="d4ef9-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-120">In the list, mark the selected row.</span></span> <span data-ttu-id="d4ef9-121">Find det hierarki, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="d4ef9-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="d4ef9-123">Føje organisationer til hierarkiet</span><span class="sxs-lookup"><span data-stu-id="d4ef9-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="d4ef9-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="d4ef9-125">Vælg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="d4ef9-126">Klik på **Vis hierarki** i sektionen **Tildelte hierarkier**.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="d4ef9-127">Tilføj organisationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="d4ef9-128">Klik på **Rediger** og derefter **Indsæt** for at tilføje en organisation.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="d4ef9-129">Når du er færdig med at foretage ændringer, kan du **gemme** en kladde og/eller **publicere** ændringerne.</span><span class="sxs-lookup"><span data-stu-id="d4ef9-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]