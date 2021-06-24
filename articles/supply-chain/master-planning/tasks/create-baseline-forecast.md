---
title: 'Vejledning: Oprette et prognosegrundlag'
description: En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223956"
---
# <a name="guide-create-a-baseline-forecast"></a>Vejledning: Oprette et prognosegrundlag

[!include [banner](../../includes/banner.md)]

En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel. Denne procedure viser, hvordan du kopierer den historiske efterspørgsel for at oprette et prognosegrundlag for alle produkter ved brug af en varefordelingsnøgle.

## <a name="set-up-an-item-allocation-key"></a>Oprette en varefordelingsnøgle

1. Gå til **Varedisponering > Opsætning > Interne planlægningsgrupper**.
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet *Navn* med værdien *10*.
    * Behovsprognose kører på tværs af juridiske enheder. Derfor skal du konfigurere alle firmaer, som du generere prognoser for, i en intern planlægningsgruppe.  
3. Find og vælg den ønskede post på listen.
4. Vælg **Varefordelingsnøgler**.
    * Vælg alle de varefordelingsnøgler, hvortil du vil oprette prognoser.  
5. Markér den valgte række på listen.
    * Vælg D_Aloc-varefordelingsnøgle.  
6. Vælg **>**.
7. Luk siden.
8. Luk siden.

## <a name="set-up-the-demand-forecasting-parameters"></a>Konfigurere parametre til behovsprognoserne

1. Gå til **Varedisponering > Opsætning > Behovsprognose > Parametre til behovsprognoser**.
2. Udvid sektionen **Parametre til prognosealgoritme**.
3. Vælg **Kopiér over historisk efterspørgsel** i feltet **Strategi for generering af prognose**.
4. Vælg **Gem**.

## <a name="create-a-baseline-forecast"></a>Oprette et prognosegrundlag

1. Gå til **Varedisponering > Prognose > Behovsprognose > Generér statistisk budgetgrundlag**.
2. Indtast en dato i feltet **Fra dato**.
    * Hvis du har salgsordrer med start fra 1. januar 2015, skal du angive denne dato. Hvis du ikke har det, kan du angive den tidligste dato for salgsordrer.  
3. Indtast en dato i feltet **Til dato**.
    * Angiv den sidste dato for dine salgsordrer, f.eks. *31-03-2015*.  
4. Indtast en dato i feltet **Fra dato**.
    * Indtast *01-04-2015*. Denne dato beregnes automatisk som startdatoen for det næste prognosegruppe.  
5. Udvid sektionen **Poster, der skal indgå**.
6. Vælg **Filter**.
7. Markér den valgte række på listen.
    * Markér rækken, hvor **Felt** = *Intern planlægningsgruppe*.  
8. Skriv en værdi i feltet **Kriterier**.
    * Indtast den interne planlægningsgruppe (f.eks. *10*), som du brugte i den første opgave.  
9. Find og vælg den ønskede post på listen.
    * Markér rækken, hvor **Felt** = *Varefordelingsnøgle*.  
10. Skriv en værdi i feltet **Kriterier**.
11. Vælg **OK**.
12. Udvid sektionen **Avancerede parametre**.
13. Vælg **Måned** i feltet *Prognosegruppe*.
14. Angiv **3** i feltet *Prognosehorisont*.
15. Angiv **1** i feltet *Låsningstidshorisont*.
16. Vælg **OK**.

## <a name="visualize-the-demand-forecast"></a>Visualiser behovsprognosen

1. Gå til **Varedisponering > Prognose > Behovsprognose > Justeret behovsprognose**.
2. Vælg cellen i række 1, kolonne 2 i tabellen for aggregeret visning. Dette er den anden måned, du har oprettet budget for.
3. Angiv **QtyCell** til *400*.
    * Angiv et andet tal i cellen end det, der blev prognosticeret, f.eks. 400.  
4. Du har foretaget en manuel regulering af prognosen. Bemærk den grafiske indikator i næste trin.
5. Vælg **Prognoselinjedetaljer**.
    * Du kan se de nøjagtige værdier, historisk efterspørgsel og prognose på denne side. Du kan også foretage ændringer af prognosen.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]