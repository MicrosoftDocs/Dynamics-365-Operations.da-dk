--- 
title: Definere produktionsflowmodeller
description: Produktionsflowmodeller beskriver, hvordan kapaciteten af lean manufacturing-arbejdsceller beregnes og vedligeholdes.
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 3da0b5c4fc50136a98017e37b65afea9f8ec7b38
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="define-production-flow-models"></a>Definere produktionsflowmodeller

[!include[task guide banner](../../includes/task-guide-banner.md)]

Produktionsflowmodeller beskriver, hvordan kapaciteten af lean manufacturing-arbejdsceller beregnes og vedligeholdes. Definitionen af en produktionsflowmodel er derfor en forudsætning for definitionen af arbejdsceller. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="define-a-production-flow-model"></a>Definer en produktionsflowmodel. 
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflowmodeller.
2. Klik på Ny.
3. Angiv et id for produktionsflowmodellen i feltet Produktionsflowmodel.
4. Vælg en indstilling i feltet Modeltype.
    * Der er to typer af modellen: typen Gennemløb og typen Timer. For Gennemløbs-typen bliver kapaciteten for arbejdsceller, der bruger denne produktionsflowmodel, udtrykt og beregnet i produktantal. For Timer-typen bliver kapaciteten for arbejdsceller, der bruger denne produktionsflowmodel, udtrykt og beregnet i timer. Bemærk, at denne egenskab ikke kan ændres for en eksisterende produktionsflowmodel. Når en arbejdscelle har kapacitetsreservationer, kan produktionsflowmodeltypen ikke ændres.  
5. Angiv antallet af dage i feltet EPE-cyklus.
    * Intervallet beskriver den periode, hvor alle dele, der fremstilles af et produktionsflow eller en arbejdscelle, bliver produceret mindst én gang. Jo kortere EPE-cyklus jo mere fleksibel er produktionsprocessen. Hvis EPE-cyklus = 0, kan alle behov produceres på samme dag. EPE-cyklus bruges til at planlægge lean procesjob. Når du planlægger et job i en arbejdscelle med EPE-cyklus = 5, søger planlægningsprocessen efter kapacitet i arbejdscellen på Forfaldsdato – EPE-cyklus (5 dage før forfaldsdatoen) for at sikre, at produktet kan produceres i denne cyklus. Lagerleveringstiden for et produkt er normalt lig med eller større end EPE-cyklus for den relaterede produktionsproces.  
6. Vælg en indstilling i feltet Planlægningsperiodetype.
    * Når en arbejdscelle har kapacitetsreservationer, kan planlægningsperiodetypen ikke ændres. Du kan kun vælge produktionsflowmodeller med den samme periodetype for denne bestemte arbejdscelle.  
7. Angiv et tal i feltet Planlægningstidshorisont.
    * Planlægningstidshorisont beskriver antallet af dage, hvor der kan foretages kapacitetsreservationer for relaterede arbejdsceller. Angiv antal dage i Planlægningstidshorisont.   Kanban-procesjob, der falder uden for denne periode, planlægges ikke med automatisk planlægning. Planlægningstidshorisont er typisk to gange den gennemsnitlige lagerleveringstid for de produkter, der fremstilles i et produktionsflow eller en arbejdscelle. EPE-cyklus bør ikke være mere end halvdelen af den planlægningstidshorisonten.     
8. Vælg en indstilling i feltet Reaktion på manglende kapacitet.
    * Indstillingerne omfatter: Udskyd - Udskydelse af det fulde behov for planlægningshændelsen på den næste tilgængelige produktionsdag, med tilgængeligt gennemløb. Annuller - Afslutte den automatiske planlægning for planlægningshændelsen og ikke planlægge de relaterede job.   Føj til den ønskede dag – Planlægge de job, der blev anmodet om i den ønskede periode. Dette overbelaster cellen for den pågældende dag, og kræver planlæggerens gennemgang og manuelle indgriben.   Distribuere til tilgængelige perioder – Fordele de forskellige job i planlægningshændelsen på alle tilgængelige produktionsdage med start fra den første tilgængelige dag. Mimimumdistributionsmængden er kanban-jobmængden. Fordelingen tildeler minimumplanlægningsantal (kanban-mængde) til hver dag med tilstrækkeligt tilgængeligt gennemløb.  


