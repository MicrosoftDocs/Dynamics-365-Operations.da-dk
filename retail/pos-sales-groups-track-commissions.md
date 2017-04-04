---
title: Spore provisioner i POS bruge salgsgrupper
description: "Det er almindelig praksis at spore salg af den kollega, der har arbejdet med kunden retail – at yde bistand, op-salg, sælge på tværs og behandler bevægelsen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Spore provisioner i POS bruge salgsgrupper

Det er almindelig praksis at spore salg af den kollega, der har arbejdet med kunden retail – at yde bistand, op-salg, sælge på tværs og behandler bevægelsen.

Spore salg efter sælger er en måling af de associerede selskaber sælger evner, mens salg af kassereren er en måling af hastighed og effektivitet. Salg af sælger bruges også ofte til at beregne provision eller andre incitamenter.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfiguration af en arbejder skal en sælger i POS
Når en arbejder er føjet til en salgsgruppe, bliver berettiget til Kommissionen og kan identificeres som en sælger i systemet. En medarbejder, der ikke er i en salgsgruppe er ikke berettiget til Kommissionen og er angivet ikke som sælger punkt i salg (POS) program. Liste over sælgere er i POS afledt af alle salgsgrupper, der indeholder mindst én medarbejder, der er tildelt til butikken. Listen er vist i POS som en kombination af salgs-ID'ET og -navnet (ID: navn). En standard salgsgruppe kan tildeles til arbejdere til at understøtte scenarier, hvor forhandleren vælger at indstille den sælger på POS linjer automatisk. Brugerne kan vælge fra en salgsgruppe, som arbejderen er medlem af.

## <a name="functionality-profile-settings"></a>Funktioner Indstillinger
Der er en række funktioner profilindstillinger for en butik, der bestemmer strømmen og proces i POS, der vedrører sælgere.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Hvis denne indstilling er aktiveret, udfyldes POS automatisk posteringslinjer med den aktuelle kasserer standard-salgsgruppen. Hvis en kasserer ikke har en standard salgsgruppe, der er angivet, skal angives værdien ikke. En bruger kan angive salgsgruppen stadig manuelt ved hjælp af en POS knap gitter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Denne indstilling har tre mulige værdier: ** ikke **-hvis denne indstilling vælges, brugeren ikke bedt om at vælge en salgsgruppe. Værdien kan stadig angives ved hjælp af en kasserer standardgruppe for salg eller ved hjælp af en POS knappen manuelt gitter. **Starten af transaktionen** - Hvis denne indstilling er valgt, og enten den **kasserer som standard** indstilling er ikke aktiveret eller aktuelle kassereren har ikke en standard salgsgruppe, brugeren bliver bedt om at vælge en salgsgruppe i begyndelsen af hver transaktion. Hvis du vælger en salgsgruppe fra denne prompt som standard alle efterfølgende linjer til den valgte gruppe til salg. En bruger kan angive salgsgruppen stadig manuelt ved hjælp af en POS knap gitter. **For hver linje** - Hvis denne indstilling er valgt, og enten den **kasserer som standard** indstilling er ikke aktiveret eller aktuelle kassereren har ikke en standard salgsgruppe, brugeren bliver bedt om at vælge en salgsgruppe efter tilføjelse af hver linje. En bruger kan angive gruppen Salg stadig manuelt ved hjælp af en POS knap gitter. |
| **Kræver**                           | Denne indstilling gælder kun, når POS er konfigureret til at bede om en sælger. Hvis aktiveret, skal brugeren vælge en salgsgruppe, før du fortsætter. Ellers kan kan brugeren vil blive bedt om, men annullere og fortsætte uden at foretage et valg. Når linjen er tilføjet, kan en bruger med de nødvendige tilladelser stadig fjerne salgsgruppen fra linjen. "Kræv sælger" gennemtvinges ikke i denne situation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Vise de repræsentative oplysninger til salg på POS-skærmen transaktioner
POS-skærmlayout for transaktionen og indhold kan konfigureres ved hjælp af skærmlayout for layout designer og tildelte skærm til butikker, kasseapparater eller arbejdere. Den **sælger** feltet kan føjes til fanen linjer i kvitteringsruden.  Dette viser ID'ET for den angivne gruppe af salg for hver linje på skærmbilledet transaktion.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Tilføjelse af salg repræsentative handlinger på POS-knappen gitre
POS gør det muligt for brugerne at konfigurere knapmatricer, som indgår i skærmlayout giver adgang til POS-handlinger. Følgende POS-handlinger, der kan tildeles til gitteret knapper, der vedrører sælgere.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                             | **Description**                                                                                                                                                                                                                                                                              |
| Angiv sælger på linjen          | Handlingen POS viser en liste over støtteberettigede salg grupper (ID: navn) for butikken. At vælge en salgsgruppe fra denne liste angiver værdien på den aktuelle posteringslinje.                                                                                                            |
| Ryd sælger på linjen        | Handlingen POS fjerner den aktuelle værdi af salg gruppe fra den aktuelle posteringslinje.                                                                                                                                                                                                  |
| Sæt sælger på postering   | Handlingen POS viser en liste over støtteberettigede salg grupper (ID: navn) for butikken. At vælge en salgsgruppe på denne liste vil angive standardværdien for den aktuelle transaktion. Eksisterende linjer uden en salgsgruppe, der er tildelt bliver set, samt eventuelle senere tilføjede linjer. |
| Ryd sælger på postering | Handlingen POS fjerner den aktuelle standard gruppe salgsværdi fra den aktuelle postering. Det har ingen indflydelse på alle de linjer, der allerede eksisterer i transaktionen.                                                                                                                             |

## <a name="calculating-commissions"></a>Beregningen af provisioner
Provisionen beregnes for arbejderne i de angivne salgsgrupper på tidspunktet for bogføring af opgørelsen eller bogføring af salgsordrer. Provisionsbeløbet bestemmes baseret på arbejderens Kommissionen share, som defineret i salgsgruppen samt tilknyttede Kommissionen beregningsindstillinger for debitor og/eller produkter på posteringen.


