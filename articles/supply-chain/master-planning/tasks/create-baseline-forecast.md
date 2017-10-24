--- 
title: Oprette en baselineprognose
description: "En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e6363ee48c0d13c79a6c623205dfa10f50d6070f
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-baseline-forecast"></a>Oprette en baselineprognose

[!include[task guide banner](../../includes/task-guide-banner.md)]

En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel. Denne procedure viser, hvordan du kopierer den historiske efterspørgsel for at oprette et prognosegrundlag for alle produkter ved brug af en varefordelingsnøgle. 


## <a name="set-up-an-item-allocation-key"></a>Oprette en varefordelingsnøgle
1. Gå til Overordnet planlægning > Opsætning > Interne planlægningsgrupper.
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien '10'.
    * Behovsprognose kører på tværs af juridiske enheder. Derfor skal du konfigurere alle firmaer, som du generere prognoser for, i en intern planlægningsgruppe.  
3. Find og vælg den ønskede post på listen.
4. Klik på Vis varefordelingsnøgler.
    * Vælg alle de varefordelingsnøgler, hvortil du vil oprette prognoser.  
5. Markér den valgte række på listen.
    * Vælg D_Aloc-varefordelingsnøgle.  
6. Klik på >.
7. Luk siden.
8. Luk siden.

## <a name="set-up-the-demand-forecasting-paramters"></a>Konfigurer parametre til behovsprognoserne
1. Gå til Overordnet planlægning > Opsætning > Behovsprognose > Parametre til behovsprognoser.
2. Udvid sektionen Parametre til prognosealgoritme.
3. Vælg "Kopiér over historisk efterspørgsel" i feltet Strategi for generering af prognose.
4. Klik på Gem.

## <a name="create-a-baseline-forecast"></a>Oprette en baselineprognose
1. Gå til Overordnet planlægning > Prognose > Behovsprognose > Generér statistisk budgetgrundlag.
2. Indtast en dato i feltet Fra dato.
    * Hvis du har salgsordrer med start fra 1. januar 2015, skal du angive denne dato. Hvis du ikke har det, kan du angive den tidligste dato for salgsordrer.  
3. Indtast en dato i feltet Til dato.
    * Angiv den sidste dato for dine salgsordrer, f.eks. '31-03-2015'.  
4. Indtast en dato i feltet Fra dato.
    * Indtast '01-04-2015'. Denne dato beregnes automatisk som startdatoen for det næste prognosegruppe.  
5. Udvid posterne for at inkludere sektion.
6. Klik på Filtrér.
7. Markér den valgte række på listen.
    * Markér rækken, hvor feltet = intern planlægningsgruppe.  
8. Skriv en værdi i feltet Kriterier.
    * Indtast den interne planlægningsgruppe, f.eks. 10, som du brugte i den første opgave.  
9. Find og vælg den ønskede post på listen.
    * Markér rækken, hvor feltet = varefordelingsnøgle.  
10. Skriv en værdi i feltet Kriterier.
11. Klik på OK.
12. Udvid sektionen Avancerede parametre.
13. Vælg "Måned" i feltet Prognosegruppe.
14. Angiv "3" i feltet Prognosehorisont.
15. Angiv "1" i feltet Låsningstidshorisont.
16. Klik på OK.

## <a name="visualize-the-demand-forecast"></a>Visualiser behovsprognosen
1. Gå til Overordnet planlægning > Prognose > Behovsprognose > Justeret behovsprognose.
2. Vælg cellen i række 1, kolonne 2 i tabellen for aggregeret visning. Dette er den anden måned, du har oprettet budget for.
3. Angiv QtyCell til "400".
    * Angiv et andet tal i cellen end det, der blev prognosticeret, f.eks. 400.  
4. Du har foretaget en manuel regulering af prognosen. Bemærk den grafiske indikator i næste trin.
5. Klik på Prognoselinjedetaljer.
    * Du kan se de nøjagtige værdier, historisk efterspørgsel og prognose på denne side. Du kan også foretage ændringer af prognosen.  


