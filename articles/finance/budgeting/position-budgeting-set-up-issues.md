---
title: Fejlfinding af stillingsbudgettering
description: Denne artikel giver svar på spørgsmål, som du kan have, når du konfigurerer stillingsbudgettering. Emnet omhandler ofte stillede spørgsmål om, hvordan man opretter budgetomkostningselementer, kompensationsgrupper og kompensationsgitre.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afddc9815ee3864236f93c8400bcf116d5b6cc89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441649"
---
# <a name="position-budgeting-troubleshooting"></a>Fejlfinding af stillingsbudgettering

[!include [banner](../includes/banner.md)]

Denne artikel giver svar på spørgsmål, som du kan have, når du konfigurerer stillingsbudgettering. Emnet omhandler ofte stillede spørgsmål om, hvordan man opretter budgetomkostningselementer, kompensationsgrupper og kompensationsgitre. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Hvorfor kan jeg ikke finde Siden Budgetteret stilling i Personale?
---------------------------------------------------------------

Budgetpositioner er flyttet til Budgetlægning.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Hvorfor kan jeg ikke slette et budgetomkostningselement?
Du kan ikke slette et budgetomkostningselement, der er tildelt en budgetteret stilling. Før du kan slette et budgetomkostningselement, skal du fjerne det fra alle budgetterede stillinger. **Tip!** For at finde alle de stillinger, som et budgetomkostningselement er tildelt til, skal du vælge omkostningselementet på siden **Budgetomkostningselementer** og derefter klikke på **Opdater stillinger**. De stillinger, der bruger omkostningselementet, vises i det øverste gitter.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Hvordan fjerner jeg et omkostningselement fra flere budgetterede stillinger uden at åbne hver enkelt?
Du kan ikke fjerne et omkostningselement. Men hvis du ændrer start- og slutdatoerne, så de ligger uden for datoerne for budgetplanlægningscyklussen, bliver omkostningselementet ikke længere tildelt til de budgetterede stillinger i denne budgetplanlægningscyklus. For at foretage denne ændring skal du åbne budgetomkostningselementet, og på oversigtspanelet **Omkostningsberegning** skal du derefter klikke på **Ret datoer** og ændre ikrafttrædelsesdatoen eller udløbsdatoen. Klik derefter på **OK** for automatisk at opdatere alle budgetterede stillinger, som omkostningselement er tildelt til. **Tip!** Hvis du bruger denne metode, skal du være opmærksom på, at budgetomkostningselementet fjernes fra **alle** budgetterede stillinger, hvor start- og slutdatoen ikke længere ligger inden for det relevante interval. Hvis det ikke er det, du ønsker, skal du åbne hver budgetterede stilling, som du vil fjerne budgetomkostningselementet fra, og manuelt foretage ændringen.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Hvorfor kan jeg ikke angive et årligt beløb i oversigtspanelet Omkostningsberegning for budgetomkostningselementet?
Du kan ikke angive et årligt beløb, hvis der er budgetomkostningselementer i oversigtspanelet **Beregningsbasis**, da systemet kræver en procentsats, for at værdien kan beregnes. Du kan ændre værdien ved at fjerne alle budgetomkostningselementer fra oversigtspanelet **Beregningsbasis**.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Hvorfor kan jeg ikke ændre budgetomkostningstypen fra indtægt til en anden budgetomkostningstype?
Nogle budgetomkostningselementer bruge omkostningselementet indtægt som udgangspunkt for beregningen. For at ændre feltet **Budgetomkostningstype** skal du fjerne indtjeningsomkostningselementet fra **Beregningsbasis** oversigtspanelet for alle budgetomkostningselementer.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Hvorfor kan jeg ikke ændre datoen på budgetomkostningselementlinjer for et budgetomkostningselement?
Du kan ikke ændre den dato på budgetomkostningselementlinjen, når et budgetomkostningselement benyttes af en budgetteret stilling. Denne begrænsning hjælper med at sikre, at de budgetterede stillinger altid er i overensstemmelse med retningslinjerne for budgetomkostningselementet. For at ændre datoen skal du på oversigtspanelet **Omkostningsberegning** klikke på **Ret datoer** og angive de nye datoer. Klik derefter på **OK** for at opdatere de stillinger, som omkostningselement er tildelt til.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Hvorfor kan jeg ikke ændre omkostningerne for et budgetomkostningselement på siden Kompensationsgruppe?
Du kan kun oprette og ændre budgetomkostningselementer på siden **Budgetomkostningselementer**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Hvorfor får jeg en fejlmeddelelse, når jeg ændrer datoerne for et omkostningselement for en budgetteret stilling?
Datoerne på omkostningselementlinjen for den budgetterede stilling skal være inden for følgende intervaller:

-   Datoen for aktivering og ophør for stillingen.
-   Datoerne for aktivering og udløb for budgetomkostningselementet.
-   Start- og slutdatoer for budgetcyklussen, der er tilknyttet budgetplanlægningsprocessen til den budgetterede stilling.




