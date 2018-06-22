---
title: "Tilføje lokations- og partsrelationstyper"
description: "I dette emne beskrives, hvordan du tilføjer en ny lokations- og partsrelationstype."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: bd8c5a18d69e1952d32675d759b8b2a997844822
ms.contentlocale: da-dk
ms.lasthandoff: 05/21/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a>Tilføje nye lokationsroller og partsrelationstyper 

## <a name="add-new-location-roles"></a>Tilføje nye lokationsroller

Der er to måder at tilføje nye lokationsroller til adresse- og kontaktoplysninger:

-  Tilføj den via siden **Adresse- og kontaktoplysninger**. Den nye rolle gemmes i tabellen **LogisticsLocationRole** med type = 0, hvilket angiver, at rollen ikke er en systemrolle, der er defineret i fastteksten **LogisticsLocationRoleType** og dens udvidelser. En bruger kan bruge denne rolle, når han eller hun opretter adresse- eller kontaktoplysninger.

    ![Formålet med adresse- og indholdsoplysninger](media/Address-Contact.PNG)

-  Føj oplysningerne til fasttekstudvidelsen **LogisticsLocationRoleType**, så de kan blive udfyldt via databasesynkroniseringsprocessen.

    1.  Opret en udvidelse til fastteksten **LogisticsLocationRoleType**, og tilføj den nye rolle i filtypenavnet. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Opret en ny ressourcefil til den nye rolle, og tildel derefter en værdi til dens egenskaber.
     
     ![Ny ressourcefil](media/Resource.PNG)
        
    3.  Opret en datapopulationsklasse, og angiv en handlermetode for at udfylde den nye rolle. 

        ![Datapopulation](media/Dirdata.PNG)

    4.  For at teste udfyldningen af den nye lokationsrolle kan du oprette en klasse, der kan køres, og kalde DirDataPopulation::insertLogisticsLocationRoles() i Main(). Når denne proces er fuldført, skal du se den nye rolle udfyldt i tabellen **LogisticsLocationRole** med typen \> 0. Den nye rolle vises på siden **Adresse- og kontaktoplysninger**.

        ![Indsætte ny lokation](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a>Tilføje nye partsrelationstyper 

Der findes to måder at tilføje en ny relationstype på:

-   Føje den via siden **Relationstyper**. Den nye relation gemmes i **DirRelationshipTypeTable** med systemtype = 0.

    ![Relationstyper](media/Relationship.PNG)

-  Føj den til udvidelsen af fastteksten **DirSystemRelationshipType** og lad den blive udfyldt via databasesynkroniseringsproces.

    1.  Opret en udvidelse af fastteksten **DirSystemRelationshipType**, og tilføj den nye relationstype.

    2. Opret en initialisering for denne nye type. Du kan finde flere eksempler i kernekoden, et af dem er **DirRelationshipTypeChildInitialize**. Dette er en initialiseringsklasse for partsrelationstypen "Underordnet". Du kan starte din initialisering ved at kopiere og indsætte denne kode og derefter opdatere de fremhævede områder.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  For at teste udfyldningen af den nye relationstype kan du oprette en klasse, der kan køres, og kalde DirDataPopulation::insertDirRelationshipTypes() i Main(). Den nye relationstype skulle nu vises i **DirRelationshipTypeTable**, og den nye relationstype er tilgængelig på siden **Relationstyper**.

        ![Kørbar klasse](media/Runnable.PNG)
