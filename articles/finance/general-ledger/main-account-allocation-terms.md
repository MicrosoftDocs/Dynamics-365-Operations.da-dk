---
title: Fordelingsbetingelser
description: I dette emne kan du finde oplysninger om, hvordan du bruger fordelingsbetingelser på en hovedkonto.
author: rachel-profitt
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60b995216eed2eda740cb4cd9be79d15d46789e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248921"
---
# <a name="allocation-terms"></a>Fordelingsbetingelser

[!include [banner](../includes/banner.md)]

I dette emne kan du finde oplysninger om, hvordan du bruger fordelingsbetingelser på en hovedkonto. Fordelingsbetingelser bruges til at fordele beløb på tværs af flere finanskontokombinationer. De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet.

Hver fordelingsbetingelse, du opretter på en hovedkonto, definerer procentdelen af et bilag, der skal fordeles fra en hovedkonto med en enkelt kilde og en kombination af økonomiske dimensioner. Desuden definerer du destinationens hovedkontoen og økonomiske dimensioner, hvor beløbet skal fordeles. 

Når du definerer kildens økonomiske dimension for tildelingen, kan du vælge, om hver enkelt dimension er specifik eller ikke-specifik. Specifik angiver, at den økonomiske dimension for kildetransaktionen skal stemme overens med den valgte dimension. Når du vælger ikke-specifik, angiver det, at alle værdier for den økonomiske dimension kan bidrage til et match.

Når du definerer destinationens finanskonto for en fordelingsbetingelse, skal du angive den hovedkonto, du allokerer beløbet til. Du kan bruge samme hovedkonto, hvor kildetransaktionen bogføres, eller en anden hovedkonto. Hvis den samme hovedkonto bruges, vises der en advarsel, når du gemmer posten. Ud over at angive hovedkontoen skal du også angive destinationsdimensionerne. For hver dimension kan du angive, om du vil bevare den økonomiske dimensionskildeværdi eller ændre den. Hvis du vælger Nej, skal du vælge en ny værdi for den økonomiske dimension. Hvis du vælger Ja, er der ikke angivet yderligere oplysninger, og systemet vil bevare de oprindelige økonomiske dimensioner, når du bogfører.

Der er ingen grænser for antallet af fordelingsbetingelser, som du kan føje til en hovedkonto, men summen af den procent, der skal fordeles på en fordelingsbetingelse, må dog ikke overstige 100. Du kan oprette fordelinger for mindre end 100 procent, hvis en del af det oprindelige bilagsbeløb skal forblive i kildens økonomiske dimensioner. Fordelingsbetingelser kan føjes til en hovedkonto som en tilsidesættelse for en juridisk enhed. Hvis du bruger en delt kontoplan, skal der defineres fordelingsbetingelser for hver juridiske enhed. Hvis du vil have adgang til knappen **Fordelingsbetingelser**, skal du først markere afkrydsningsfeltet **Fordeling** i tilsidesættelsen af en juridisk enhed .

## <a name="allocation-term-example"></a>Eksempel på fordelingsbetingelse
Du har defineret en bærer for din organisation, der hedder FIRMA, der er nummereret 000. Når fakturaer bogføres for forbrugsudgifter, kodes de til denne FIRMA-bærer. Dit firma har defineret en regel om, at alle forbrugsudgifter skal fordeles med en procentdel til hver af de enkelte bærere. De andre økonomiske dimensioner for afdeling og virksomhedsenhed er de samme.

I dette eksempel oprettes der en ny fordelingsbetingelse for hovedkontoen til forbrugsudgift. Der oprettes en række for hver bærer med den procent, der skal tildeles. **Udvælgelseskriterierne** for de økonomiske kildedimensioner for hver række vil være **Specifik** for **Bærer**, og værdien vil blive angivet til 000: FIRMA. Til afdeling og virksomhedsenhed er **Udvælgelseskriterier** **Ikke-specifikke**.

I oversigtspanelet **Destinationens finanskonto** er hovedkontoen den samme udgiftskonto for forbrug, og **Bevar økonomiske dimensioner i kilden** angives til **Ja** for **Virksomhedsenhed** og **Afdeling**. Indstillingen **Bevar økonomiske dimensioner i kilden** angives til **Nej** for **Bærer**, og den valgte værdi vil være hver enkelt bærer, du fordeler til. Hvis der er tre bærere, der skal fordeles til, oprettes der poster med tre fordelingsbetingelser. Den eneste forskel mellem de enkelte fordelingsbetingelser er den bærer, der er angivet på destinationens finanskonto.

## <a name="create-an-allocation-term-on-a-main-account"></a>Oprette en fordelingsbetingelse på en hovedkonto

1. Gå i **Navigationsrude** til **Moduler > Finans > Kontoplan > Konti > Hovedkonti**.
2. Find og vælg den ønskede post på listen.
3. I oversigtspanelet **Tilsidesættelser af juridisk enhed** skal du vælge **Tilføj**.
4. Vælg **Firma**, og vælg derefter **Tilføj**.
5. Marker afkrydsningsfeltet **Fordeling**.
6. Vælg **Fordelingsbetingelser**.
7. Vælg **Rediger** for at ændre standardposten, eller vælg **ny** for at tilføje en post.
8. Angiv procentdelen af de bilagsposteringer, du vil fordele, i feltet **Procent**.
9. Vælg en indstilling i **Udvælgelseskriterier** for de enkelte økonomiske dimensioner i oversigtspanelet **Økonomisk dimension i kilden**.
    - Hvis du vælger **Specifik**, skal du vælge den økonomiske dimensionsværdi på rullelisten til højre.
    - Hvis du vælger **Ikke-specifik**, kræves der ingen yderligere oplysninger for den økonomiske dimension.
10. I oversigtspanelet **Destinationens finanskonto** skal du i feltet **Til konto** vælge den hovedkonto, hvor du vil fordele procentsatsen af bilagstransaktionen.
11. Vælg en indstilling for hver økonomiske dimension i **Bevar økonomiske dimensioner i kilden**.
    - Hvis du vælger **Nej**, skal du vælge den økonomiske dimensionsværdi på rullelisten til højre, hvor du vil have, at bilagstransaktionen skal fordeles til.
    - Hvis du vælger **Ja**, er der ikke brug for yderligere oplysninger. Systemet vil beholde værdien på det oprindelige bilag, når du bogfører fordelingen.
12. Gentag trin 7 til 11 for hver ekstra fordeling. Summen af alle fordelinger er angivet i feltet **Samlet procent**. Dette beløb må ikke overstige 100.
13. Luk alle siderne.

>[!NOTE] 
> Du kan vælge at bruge knappen **Kopiér** til at duplikere den valgte fordeling.

Når der oprettes en fordelingsbetingelse for en hovedkonto, vil systemet automatisk bogføre et nyt bilag, når der bogføres et bilag, der svarer til de økonomiske dimensioner for kilden på fordelingsbetingelserne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]