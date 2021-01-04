---
title: Tilføje lokations- og partsrelationstyper
description: I dette emne beskrives, hvordan du tilføjer en ny lokations- og partsrelationstype.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e38d0bd75ad865b7885182f798beb43551576beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441589"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="9f924-103">Tilføje lokations- og partsrelationstyper</span><span class="sxs-lookup"><span data-stu-id="9f924-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="9f924-104">Tilføje lokationsroller</span><span class="sxs-lookup"><span data-stu-id="9f924-104">Add location roles</span></span>

<span data-ttu-id="9f924-105">Der er to måder at tilføje nye lokationsroller til adresse- og kontaktoplysninger:</span><span class="sxs-lookup"><span data-stu-id="9f924-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="9f924-106">Tilføj den via siden **Adresse- og kontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="9f924-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="9f924-107">Den nye rolle gemmes i tabellen **LogisticsLocationRole** med type = 0, hvilket angiver, at rollen ikke er en systemrolle, der er defineret i fastteksten **LogisticsLocationRoleType** og dens udvidelser.</span><span class="sxs-lookup"><span data-stu-id="9f924-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="9f924-108">En bruger kan bruge denne rolle, når han eller hun opretter adresse- eller kontaktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="9f924-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Formålet med adresse- og indholdsoplysninger](media/Address-Contact.PNG)

-  <span data-ttu-id="9f924-110">Føj oplysningerne til fasttekstudvidelsen **LogisticsLocationRoleType**, så de kan blive udfyldt via databasesynkroniseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="9f924-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="9f924-111">Opret en udvidelse til fastteksten **LogisticsLocationRoleType**, og tilføj den nye rolle i filtypenavnet.</span><span class="sxs-lookup"><span data-stu-id="9f924-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![Udvidelse til fasttekst LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="9f924-113">Opret en ny ressourcefil til den nye rolle, og tildel derefter en værdi til dens egenskaber.</span><span class="sxs-lookup"><span data-stu-id="9f924-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Ny ressourcefil](media/Resource.PNG)
        
    3.  <span data-ttu-id="9f924-115">Opret en datapopulationsklasse, og angiv en handlermetode for at udfylde den nye rolle.</span><span class="sxs-lookup"><span data-stu-id="9f924-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Datapopulation](media/Dirdata.PNG)

    4.  <span data-ttu-id="9f924-117">For at teste udfyldningen af den nye lokationsrolle kan du oprette en klasse, der kan køres, og kalde DirDataPopulation::insertLogisticsLocationRoles() i Main().</span><span class="sxs-lookup"><span data-stu-id="9f924-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="9f924-118">Når denne proces er fuldført, skal du se den nye rolle udfyldt i tabellen **LogisticsLocationRole** med typen \> 0.</span><span class="sxs-lookup"><span data-stu-id="9f924-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="9f924-119">Den nye rolle vises på siden **Adresse- og kontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="9f924-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Indsætte ny lokation](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="9f924-121">Tilføje partsrelationstyper</span><span class="sxs-lookup"><span data-stu-id="9f924-121">Add party relationship types</span></span> 

<span data-ttu-id="9f924-122">Der findes to måder at tilføje en ny relationstype på:</span><span class="sxs-lookup"><span data-stu-id="9f924-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="9f924-123">Føje den via siden **Relationstyper**.</span><span class="sxs-lookup"><span data-stu-id="9f924-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="9f924-124">Den nye relation gemmes i **DirRelationshipTypeTable** med systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="9f924-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Relationstyper](media/Relationship.PNG)

-  <span data-ttu-id="9f924-126">Føj den til udvidelsen af fastteksten **DirSystemRelationshipType** og lad den blive udfyldt via databasesynkroniseringsproces.</span><span class="sxs-lookup"><span data-stu-id="9f924-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="9f924-127">Opret en udvidelse af fastteksten **DirSystemRelationshipType**, og tilføj den nye relationstype.</span><span class="sxs-lookup"><span data-stu-id="9f924-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="9f924-128">Opret en initialisering for denne nye type.</span><span class="sxs-lookup"><span data-stu-id="9f924-128">Create an initializer for this new type.</span></span> <span data-ttu-id="9f924-129">Du kan finde flere eksempler i kernekoden, et af dem er **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="9f924-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="9f924-130">Dette er en initialiseringsklasse for partsrelationstypen "Underordnet".</span><span class="sxs-lookup"><span data-stu-id="9f924-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="9f924-131">Du kan starte din initialisering ved at kopiere og indsætte denne kode og derefter opdatere de fremhævede områder.</span><span class="sxs-lookup"><span data-stu-id="9f924-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild-initialisering](media/DirRelationship.PNG)

    3.  <span data-ttu-id="9f924-133">For at teste udfyldningen af den nye relationstype kan du oprette en klasse, der kan køres, og kalde DirDataPopulation::insertDirRelationshipTypes() i Main().</span><span class="sxs-lookup"><span data-stu-id="9f924-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="9f924-134">Den nye relationstype skulle nu vises i **DirRelationshipTypeTable**, og den nye relationstype er tilgængelig på siden **Relationstyper**.</span><span class="sxs-lookup"><span data-stu-id="9f924-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Kørbar klasse](media/Runnable.PNG)
