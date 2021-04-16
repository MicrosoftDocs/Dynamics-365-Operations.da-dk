---
title: Oprette procesaktiviteter for lean manufacturing
description: Opret et procesaktivitet til lean manufacturing.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46d6b7696d606333a170eaa1c06b9e0503ae1e02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829012"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Oprette procesaktiviteter for lean manufacturing

[!include [banner](../../includes/banner.md)]

Opret et procesaktivitet til lean manufacturing. 

Forudsætninger: 

1. Der skal oprettes et produktionsflowet og en version, der ikke er aktive.

2. Der skal oprettes en arbejdscelle.


## <a name="find-the-production-flow-version"></a>Find produktionsflowversionen
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.

## <a name="create-a-new-activity"></a>Opret en ny aktivitet
1. Klik på Aktiviteter.
    * Kontroller, at det valgte produktionsflow har en version i udkast, og vælg den version.  
2. Klik på Opret ny planaktivitet.
3. Klik på Næste.
4. Skriv en værdi i feltet Navn.
5. Skriv en værdi i feltet Navn.
    * Bemærk, at navnet skal være entydigt for et givet produktionsflow for alle versioner.  
6. Skriv et tal i feltet Procesantal.
    * Bemærk, at uanset hvilket antal af job der skal behandles, er dette minimumantal pr. job til at beregne arbejdsomkostning. Hvis jobantal afviger fra dette antal, oprettes arbejdsomkostningsafvigelse.  
7. Klik på Næste.

## <a name="select-the-work-cell"></a>Vælg arbejdscellen
1. Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.
2. Klik op linket i den valgte række på listen.

## <a name="define-the-inventory-updates"></a>Definer lageropdateringerne
1. Marker eller fjern opdateringen i afkrydsningsfeltet Opdater lagertilgang.
    * Hvis Opdater lagerbeholdning = Nej, kan du definere aktiviteten for at modtage et halvfabrikataprodukt (aktiviteten ikke når op på det næste niveau i Styklisten).    Du kan også vælge for at forbruge halvfabrikata.  

## <a name="define-the-picking-activities"></a>Definer plukaktiviteterne
1. Klik på Næste.
2. Markér den valgte række på listen.
    * Der oprettes en standardplukaktiviteten for indlagringslokation af den valgte arbejdscelle.  
3. Klik på Tilføj.
    * Du kan oprette yderligere plukaktiviteter for specifikke produkter, der ikke opbevares på arbejdscellens inputaktivitet.  
4. Find og vælg den ønskede post på listen.
5. Indtast en værdi i feltet Varenummer.
6. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
    * Med denne definition plukkes alle materialer, der forbruges i aktiviteten, fra standardinputlagerstedet og lokaliteten med undtagelse af den vare, der er defineret i den anden plukaktivitet. Dette element vil blive plukket fra et andet lagersted og en anden lokalitet.  
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Vælg eller fjern markeringen i afkrydsningsfeltet Registrer spild.
10. Klik på Næste.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]