---
title: "Masseansættelsesprojekter"
description: "Masseansættelsesprojekter tillader personalespecialister at oprette flere stillinger og effektivt ansætte arbejdere til disse stillinger."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 538733c2b3453ad928f42dafb618303d9964452f
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="mass-hire-projects"></a>Masseansættelsesprojekter

[!include[banner](includes/banner.md)]


Masseansættelsesprojekter tillader personalespecialister at oprette flere stillinger og effektivt ansætte arbejdere til disse stillinger.

<a name="overview"></a>Overblik
--------

Brug masseansættelsesprojekter, når du ansætter flere arbejdere på én gang, f.eks når du ansætter pga. sæsonbestemt efterspørgsel. Det er nyttigt at oprette et masseansættelsesprojekt, fordi kan du oprette stillingsposter, poster for arbejdere og arbejdertildelinger på samme tid. Når du opretter stillinger til et masseansættelsesprojekt, kan du angive følgende oplysninger:
-   Antallet af stillinger, der skal oprettes
-   De arbejdstyper, du vil ansætte i stillingerne
-   Afdelingen og det job, der er tilknyttet stillingerne.
-   Værdien af den tilsvarende fuldtidsstilling

## <a name="example"></a>Eksempel
Om sommeren ansætter du normalt 15-20 studerende på deltid i de turnusstillinger, der findes i virksomheden. I år vil du ansætte fem bogholdere, fem medarbejdere til ordrebehandling og fem kasserer. I stedet for at oprette hver stillingspost og arbejderpost særskilt, opretter du ét masseansættelsesprojekt, der kaldes "Sommermedarbejdere". Projektets start- og slutdatoer samkøres med start- og slutdatoerne for varigheden af de stillinger, du opretter til dette masseansættelsesprojekt. 

På siden **Masseansættelsesprojekter** skal du vælge projektet "Sommermedarbejdere" og derefter klikke på **Åbn projekt**. I det åbne masseansættelsesprojekt skal du klikke på **Opret stillinger** og angive oplysninger om bogholderstillingen. Du kan angive, at fem bogholderstillinger bør oprettes med de samme oplysninger for hver stilling, og derefter kan du klikke på OK. Gentag denne proces for stillingerne til medarbejdere til ordrebehandling og kasserere. 

Når du har fundet studerende, der skal ansættes i praktikantstillingerne, indtaster du den enkelte studerendes oplysninger i **Detaljer for stilling** for stillingen, som du vil ansætte dem i. Når du har angivet alle stillingsoplysningerne, skal du vælge stillingen på siden Masseansættelsesprojekter og derefter klikke på **Ansæt**. Der oprettes en stillingspost for hver stilling, og der oprettes og tildeles en arbejderpost til den relevante stilling for hver person, du ansætter.

## <a name="mass-hire-project-statuses"></a>Statusser for masseansættelsesprojekter
Et masseansættelsesprojekt kan have følgende statusser.
-   Oprettet
-   Åbnet
-   Lukket

På siden **Masseansættelsesprojekt** skal du klikke på **Åbn projekt** eller **Luk projekt** for at ændre status for et masseansættelsesprojekt. I følgende tabel beskrives, hvad du kan gøre med et projekt i henhold til projektets status.

<table>
<thead>
<tr class="header">
<th>Status</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Oprettet</td>
<td>Du kan oprette og redigere oplysninger, men du kan ikke oprette stillinger til projektet. Det er standardstatus for nye projekter.</td>
</tr>
<tr class="even">
<td>Åbnet</td>
<td>Du kan ændre projektoplysninger, oprette stillinger til masseansættelsesprojektet og ansætte personer i stillingerne. Det er status for aktive projekter.</td>
</tr>
<tr class="odd">
<td>Lukket</td>
<td>Du kan ikke føje stillinger til projektet. Hvis du vil føje stillinger til masseansættelsesprojektet, skal du åbne projektet igen. Det er status for færdige projekter.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Bemærk! </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Før du kan lukke et masseansættelsesprojekt, skal alle stillinger i projektet være tildelt statussen Oprettet eller Lukket.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 






