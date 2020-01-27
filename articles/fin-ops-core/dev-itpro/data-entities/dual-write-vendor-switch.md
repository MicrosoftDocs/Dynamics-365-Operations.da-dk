---
title: Skifte mellem kreditordesign
description: I dette emne beskrives det, hvordan du kan skifte mellem integrationen af leverandørdata mellem Finance and Operations-programmer og Common Data Service.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902719"
---
# <a name="switch-between-vendor-designs"></a>Skifte mellem kreditordesign

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Kreditordataflow 

Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du vil adskille leverandøroplysningerne fra kundernes, kan du bruge dette grundlæggende leverandørdesign.  

![Grundlæggende leverandørflow](media/dual-write-vendor-data-flow.png)
 
Hvis du bruger andre Dynamics 365-apps til leverandørhåndtering, og du fortsat vil bruge enheden **Konto** til at gemme leverandøroplysninger, kan du bruge dette udvidede leverandørdesign. I dette design gemmes udvidede leverandøroplysninger som f.eks. leverandørers på hold-status og leverandørprofil i enheden **leverandører** i Common Data Service. 

![Udvidet leverandørflow](media/dual-write-vendor-detail.jpg)
 
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
    5. Aktiver de arbejdsgange, du har oprettet på enhederne **Konto** og **Leverandør** for at påbegynde anvendelsen af enheden **Konto** til lagring af leverandøroplysninger. 
 
