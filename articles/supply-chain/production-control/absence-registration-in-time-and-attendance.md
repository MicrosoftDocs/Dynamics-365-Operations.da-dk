---
title: Fraværsregistrering i Tid og fremmøde
description: I dette emne forklares, hvordan du håndterer fraværsregistreringer i Tid og fremmøde.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a076ade51ad295886bef747302c4874ef09d3fa7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203267"
---
# <a name="absence-registration-in-time-and-attendance"></a>Fraværsregistrering i Tid og fremmøde

[!include [banner](../includes/banner.md)]

I dette emne beskrives begreberne for fravær, og det forklares, hvordan du håndterer fravær i Tid og fremmøde.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Fravær, der er baseret på almindelig arbejdstid

Arbejdere betragtes som fraværende i alle timer, hvor de ikke arbejder i deres almindelig arbejdstid. Almindelig arbejdstid er defineret i en arbejders profil for normaltid.

En arbejder har f.eks. arbejde på en dagprofil, der har mødetid 7.00 og sluttid 15.00. Hvis arbejderen møder 9.00, betragtes han fraværende fra 7.00 til 9.00 på den pågældende dag.

I så fald bliver arbejderne bedt om at angive en årsag til deres fravær. De kan angive en årsag ved at vælge en fraværskode.

## <a name="absence-codes"></a>Fraværskoder

Fraværskoder definerer de forskellige typer fravær. Fraværskoder defineres af firmaet.

Forskellige regler kan anvendes til fraværskoder. F.eks. kan en fraværskode konfigureres til at trække eller give løn.

En virksomhed definerer f.eks. fraværskoden **For sent**, som arbejdere bruger, hvis de kommer sent og ikke har en god grund. Virksomheden definerer også fraværskoden **Internt kursus**, som arbejdere bruger for tid, som de bruger på at deltage i interne kurser. Disse fraværskoder kan konfigureres, så **For sent** trækker fra arbejderens løn, men **Internt kursus** ikke trækker fra en arbejders løn.

Du kan konfigurere automatiske fraværkskoder. Disse fraværskoder kan bruges til at beregne en arbejders tid, når der ikke er registreret noget fravær. Arbejderens arbejdstidsprofil bestemmer, om fraværskoden for normaltid eller flekstid bruges.

### <a name="set-up-standard-time-and-flex-time"></a>Opsætning af normaltid og flekstid

- Konfigurer parametrene for standardtid og flekstid ved hjælp af indstillingerne **Automatisk indsættelse af fravær** og **Automatisk indsættelse af fleks -** på siden **Parametre for tid og fremmøde**.

## <a name="absence-groups"></a>Fraværsgrupper

Fraværskoder er grupperet i fraværsgrupper. Du kan bruge fraværsgrupper til at gruppere fraværskoder, der har fælles karakteristika. Eksemplerne omfatter fraværskoderne for et gyldigt fravær eller fravær på grund af en lægeaftale, deltagelse i jury eller barns sygdom.

## <a name="planned-absence"></a>Planlagt fravær

Hvis du ved, at en arbejder vil være fraværende i en periode, f.eks. en kommende ferie, kan du bruge planlagt fravær. Du kan oprette planlagt fravær ved at konfigurere fraværskoden, så den tager højde for det planlagte fravær. Når du opretter et planlagt fravær, bliver du ikke bedt om en fraværskode i fraværsperioden, når tidsregistreringer for brugeren beregnes. Planlagt fravær kan defineres for en enkelt arbejder, eller du kan definere et batchjob til masseopdatering af planlagt fravær for arbejdere.

### <a name="set-up-planned-absence"></a>Konfigurer planlagt fravær

1. Vælg **Personale** &gt; **Arbejdere** &gt; **Medarbejdere**, og vælg en medarbejder.
2. Vælg **Tid** &gt; **Tidstildelinger** &gt; **Fraværsregistrering i tid**, og konfigurer det planlagte fravær.

## <a name="interrupted-planned-absence"></a>Afbrudt planlagt fravær

Hvis du anvender indstillingen **Afbryd**, når du opretter et planlagt fravær, afbrydes det planlagte fravær, hvis arbejderen logger på, under den planlagte fraværsperiode. Det planlagte fravær markeres som **Afbrudt** og har ingen indflydelse på fremtidige beregninger.

### <a name="set-up-a-planned-absence-for-interruption"></a>Konfigurere et planlagt fravær til afbrydelse

1. Åbn siden **Fraværsregistrering i tid**, som beskrevet i proceduren til opsætning af planlagt fravær.
2. Vælg **Afbryd**.

Indstillingen **Afbryd** gælder, når tiden registreres via produktionsterminalen eller produktionsenheden. Indstillingen gælder ikke, hvis registreringerne er angivet på beregnings- og godkendelsessiderne, eller på siden **Elektronisk timeseddel**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Eksempler på brugen af fravær i en fleksprofil

De følgende tre eksempler viser, hvordan fravær beregnes i en profil, der har fleksperioder.

Eksemplerne bruger følgende profil.

| Komme | Normaltid    | Pause             | Normaltid | Fleks-        | Gå | Fleks+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 8.00     | 9.00 til 11.30 | 11.30 til 12.00 | 12.00 til 15.00 | 15.00 til 16.00 | 16.00      | 16.00 til 18.00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>Eksempel 1: Logger af i en fleksperiode

Arbejderen stempler ind kl. 8.00 og stempler ud på kl. 15.30. Fordi arbejderen i dette tilfælde stempler ud i en fleksperiode, beregnes der intet fravær, og der trækkes en halv time fra arbejderens flekssaldo.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Eksempel 2: Logger af inden for perioden for normaltid

Arbejderen stempler ind kl. 8.00 og stempler ud på kl. 14.30. Fordi arbejderen i dette tilfælde stempler ud inden for perioden for normaltid, beregnes fravær fra 14.30 til 16.00, og der registreres en fraværsperiode på 1,5 timer. Der kræves en fraværskode for den pågældende periode.

### <a name="example-3-signing-out-during-a-flex-period"></a>Eksempel 3: Logger af under en fleks+-periode

Arbejderen stempler ind kl. 8.00 og stempler ud kl. 16.30. Fordi arbejderen i dette tilfælde stempler ud i en fleks+-periode, beregnes der intet fravær, og der lægges en halv time til arbejderens flekssaldo.

## <a name="absence-in-the-calculation-and-approval-process"></a>Fravær i processen til beregning og godkendelse

Tidsregistreringer for arbejderen skal beregnes og godkendes, før de kan overføres til et lønsystem som lønposter.

En godkender kan ændre en arbejders tidsregistreringer. Godkenderen kan desuden ændre ethvert fravær, som arbejderen har registreret. Hvis godkenderen manuelt angiver en tidsperiode, der har en fraværskode, tilsidesættes fraværskoden for den pågældende periode ikke af standardfraværskoden fra parametrene i Tid og fremmøde.

En arbejder stempler f.eks. ind 10.00 og vælger en fraværskode, der angiver, at hun er forsinket. Senere fortæller arbejderen sin arbejdsleder, at hun havde en lægeaftale fra 8.00 til 10.00. En lægeaftale bør ikke føre til et fradrag i arbejderens løn. I dette tilfælde kan arbejdslederen derfor justere to timers fravær fra 8.00 til 10.00 ved manuelt at angive en fraværskode, der angiver sygdom i to timer.

### <a name="calculate-and-approve-absence"></a>Beregne og godkende fravær

- Vælg **Tid og fremmøde** &gt; **Gennemse og godkend** &gt; **Godkend eller beregn**.
