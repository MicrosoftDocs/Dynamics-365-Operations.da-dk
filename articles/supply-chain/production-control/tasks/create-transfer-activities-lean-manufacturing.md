---
title: Oprette overførselsaktiviteter for lean manufacturing
description: Opret en overførselsaktivitet for lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 04cb0afa74cb95acf4007e9292f9fb88d4c86f87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837728"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Oprette overførselsaktiviteter for lean manufacturing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Opret en overførselsaktivitet for lean manufacturing. 

Forudsætninger: 

1. Der skal oprettes et produktionsflowet og en version, der ikke er aktive.

2. Lokaliteterne fra og til lagersted skal oprettes. Du kan også vælge at oprette genopfyldningsarbejdscellen eller den genopfyldte arbejdscelle.


## <a name="find-the-production-flow-version"></a>Find produktionsflowversionen
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
    * Bemærk, at produktionsflowet skal have en version i kladdestatus.  
3. Klik op linket i den valgte række på listen.

## <a name="create-a-new-activity"></a>Opret en ny aktivitet
1. Klik på Aktiviteter.
    * Kontroller, at det valgte produktionsflow har en version i udkast, og vælg den version.  
2. Klik på Opret ny planaktivitet.
3. Klik på Næste.
4. Skriv en værdi i feltet Navn.
5. Vælg"Overfør" i feltet Aktivitetstype.
6. Skriv et tal i feltet Procesantal.
7. Klik på Næste.

## <a name="select-the-work-cells"></a>Vælg arbejdscellerne.
1. Klik på rullelisten i feltet Genopfyldning for at åbne opslaget.
    * Vælg en arbejdscelle for at bruge arbejdscellens udlagringslokalitet som fra-lokalitet i overførselsaktiviteten. Det samme kan gøres med den genopfyldte arbejdscelle, som angiver mållokaliteten for overførselsaktiviteten.  
2. Klik op linket i den valgte række på listen.

## <a name="define-the-inventory-updates"></a>Definer lageropdateringerne
1. Vælg en indstilling i feltet Produkt.
    * Bemærk, at en overførsel ikke ændrer produkttypen. Du kan overføre færdige produkter eller halvfabrikata (overførsel mellem to aktiviteter i et produktionsflow og eventuelt en kanban-proces).     Når du overfører færdige produkter, kan du vælge plukning eller modtagelse af resultaterne i en lagertransaktion.  

## <a name="define-the-transfer-locations"></a>Definer overførselslokaliteterne
1. Klik på Næste.
2. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Klik på rullelisten i feltet Lokation for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
7. Vælg "Afsender" i feltet Fragtet af.
    * Indstillingerne omfatter: Afsender - den organisation, som driver forsendelseslagerstedet, Modtager - den organisation, som driver tilgangslagerstedet, Fragtmand - en tredjepartsforhandler. Hvis driftsorganisationen er en kreditor, kræver overførselsaktiviteten en aftale for underleverandørarbejde.  
8. Klik på Næste.

## <a name="define-the-activity-times"></a>Definer aktivitetstiderne
1. Find og vælg den ønskede post på listen.
    * Definitionen af en Kørsel er obligatorisk. Kørslen bruges til at beregne omkostninger og procestider for kanban-job. Kørsler bruges ikke til at beregne kapacitetsbelastninger og forbrug, som beregnes ud fra procestid, afledt fra produktionsflowversion-opgaven.  
2. Angiv et tal i feltet Tid.
3. Skriv en værdi i feltet Enhed.
4. Vælg Tidsenhed.
5. Skriv et tal i feltet Pr. antal.
6. Find og vælg den ønskede post på listen.
    * Køtider er valgfri.  
7. Angiv et tal i feltet Tid.
8. Skriv en værdi i feltet Enhed.
9. Vælg Tidsenhed.
10. Skriv et tal i feltet Pr. antal.
11. Klik på Næste.
12. Klik på Finish.
13. Luk siden.

