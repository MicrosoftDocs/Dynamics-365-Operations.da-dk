---
title: Skift mellem leverandørdesign
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772358"
---
# <a name="switch-between-vendor-designs"></a>Skift mellem leverandørdesign

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Kreditordataflow 

Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du vil adskille leverandøroplysningerne fra kundernes, kan du bruge dette grundlæggende leverandørdesign.  

![Grundlæggende leverandørflow](media/dual-write-switch-1.png)
 
Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du fortsat vil bruge enheden **Konto** til at gemme leverandøroplysninger, kan du bruge dette udvidede leverandørdesign. I dette design gemmes udvidede leverandøroplysninger som f.eks. leverandørers på hold-status og leverandørprofil i enheden **leverandører** i Common Data Service. 

![Udvidet leverandørflow](media/dual-write-switch-2.png)
 
Følg nedenstående fremgangsmåde for at bruge det udvidede leverandør design: 
 
1. Løsningspakken **SupplyChainCommon** indeholder skabeloner for arbejdsgangsproces som vist i følgende billede.
    > [!div class="mx-imgBorder"]
    > ![Skabeloner for arbejdsgangsprocesser](media/dual-write-switch-3.png)
2. Opret nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner: 
    1. Opret en ny arbejdsgangsproces for enheden **Leverandør** ved hjælp af skabelonen for arbejdsgangsprocessen **Opret leverandører i Kontoenheden**, og tryk dernæst på **OK**. Denne arbejdsgang håndterer leverandøroprettelsesscenariet for enheden **Konto**.
        > [!div class="mx-imgBorder"]
        > ![Opret Leverandører i Kontoenhed](media/dual-write-switch-4.png)
    2. Opret en ny arbejdsgangsproces for enheden **Leverandør** ved hjælp af skabelonen for arbejdsgangsprocessen **Opdater Kontoenheder**, og tryk dernæst på **OK**. Denne arbejdsgang håndterer opdateringsscenariet for leverandører for enheden **Konto**. 
        > [!div class="mx-imgBorder"]
        > ![Opdater Kontoenheder](media/dual-write-switch-5.png)
    3. Opret nye arbejdsgangsprocesser ud fra de skabeloner, der blev oprettet på enheden **Konti**. 
        > [!div class="mx-imgBorder"]
        > ![Opret leverandører i leverandørenheder](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Opdater leverandørenheder](media/dual-write-switch-7.png)
    4. Du kan konfigurere arbejdsprocesser som realtids- eller baggrundsarbejdsgange, der er baseret på dine krav. 
        > [!div class="mx-imgBorder"]
        > ![Konverter til en baggrundsarbejdsgang](media/dual-write-switch-8.png)
    5. Aktiver de arbejdsgange, du har oprettet på enhederne **Konto** og **Leverandør** for at påbegynde anvendelsen af Customer Engagement-enheden **Konto** til lagring af leverandøroplysninger. 
 
