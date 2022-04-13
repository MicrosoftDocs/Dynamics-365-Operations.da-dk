---
title: Generere Affordable Care Act-indberetninger (ACA)
description: Affordable Care Act (ACA)-rapportering genererer blanketterne 1095-B og 1095-C som led i **Employer Mandate**-afsnittet af Affordable Care Act.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 6682a98bb7241060b035e7da1396ec8f8973bf09
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534147"
---
# <a name="generate-aca-reports"></a>Generere ACA-rapporter


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Affordable Care Act (ACA)-rapportering genererer blanketterne 1095-B og 1095-C som led i **Employer Mandate**-afsnittet af Affordable Care Act.

> [!NOTE]
> ACA-rapportering er kun aktiveret for juridiske enheder i USA.

## <a name="getting-started"></a>Kom godt i gang

Hvis du vil spore oplysninger, som skal indberettes i blanketterne 1095-B og C-1095, skal du først oprette en eller flere Affordable Care-dækningsgrupper. Affordable Care-dækningsgrupper angiver:

- Tilbuddet om dækning for en medarbejder
- Medarbejderens andel af det laveste månedlige løntillæg, hvis omkostningen ligger over den føderale fattigdomsgrænse
- Safe Harbor bruges af arbejdsgiveren, hvis det er relevant

Brug af dækningsgrupper under Affordable Care gør det muligt at administrere oplysningerne for disse felter uden at skulle ændre alle medarbejderposter, hvor betingelserne er ens. Desuden kan Affordable Care-dækningsgrupper nemt tildeles til en eller flere medarbejdere ved hjælp af indstillingen **Massetildeling** på siden.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Vedligeholde flere versioner af en dækningsgruppe

Du kan vedligeholde flere versioner af en enhver dækningsgruppe. Denne funktionalitet giver dig mulighed for at foretage ændringer uden at skulle oprette en ny gruppe og tildele medarbejdere til den igen. 

Når du har oprettet ACA-dækningsgrupper, kan du tildele medarbejderne flere grupper med indstillingen **Massetildeling**. Du kan også enkeltvist angive, om ACA-oplysninger skal spores og rapporteres, og knytte en medarbejder til dækningsgruppen Affordable Care for medarbejderne.

Du behøver ikke spore visse ACA-dækningsoplysninger, f.eks. for deltidsansatte. I dette tilfælde skal du angive feltet **Rapportdækning** til **Nej**. Selvom du skal tildele hver enkelt medarbejder med ACA-oplysninger, der kan spores, til en Affordable Care-dækningsgruppe, kan du stadig ændre følgende indstillinger for måneder med forskellige værdier:

- **Tilbud om dækning**
- **Medarbejderens andel af omkostningen**
- **Safe Harbor**

Hvis du vil angive undtagelser til værdier i Affordable Care-dækningsgrupper, skal du klikke på linket **Affordable Care Coverage** på siden **Detaljer om arbejder** under afsnittet **Flere oplysninger** under fanen **Ansættelse**.

## <a name="reporting-health-care-coverage"></a>Indberetning af dækning af sygeforsikring

Udover at spore en sygeforsikringsdækning, der blev tilbudt til fuldtidsmedarbejdere, hvis arbejdsgiveren tilbyder en arbejdsgiver-sponsoreret sygesikringsordning med egendækning, som medarbejderen er tilmeldt (uanset om vedkommendes ansættelsesstatus er fuldtid eller deltid), skal yderligere oplysninger rapporteres i 1095-C. Hver medarbejder (inklusive deres afhængige parter), der er omfattet af arbejdsgiver-sponsorerede frynsegodeplaner, skal medtages i indberetningen for de måneder, hvor de var dækket. 

Du kan angive, om hver frynsegodeplan skal indberettes, ved at markere afkrydsningsfeltet **Skal indberettes til det amerikanske skattevæsen (ACA)**.

Hvis medarbejdere derudover har valgt, at en eller flere afhængige parter skal være omfattet af et frynsegode, kan du angive de datoer, hvor disse afhængige har været dækket, for hver medarbejder på siden **Vedligehold frynsegoder**. Du kan angive, at den afhængige part er dækket af frynsegoden, ved at vælge knappen **Rediger** i handlingsruden i oversigtspanelet **Afhængige**.

På siden **Håndtering af dækningsdato for den afhængige** kan du angive de datoer, hvor den afhængige part er dækket af frynsegodet. Når du angiver datoer på denne side, markeres afkrydsningsfeltet **Dækket** automatisk på siden **Vedligehold frynsegoder**.

## <a name="generate-1095-b-and-1095-c-forms"></a>Generere 1095-B- og 1095-C-blanketter

Du kan også generere 1095-B- og 1095-C-blanketter fra produktet og distribuere dem til hver af dine medarbejdere. Systemet kan også generere 1095-C-blanketter elektronisk og 1094-C IRS-overførselsfilerne.  

Når du opretter blanketten 1095-C, skal du angive det relevante skatteår og angive, om social security-numre skal skjules. Hvis du udskriver 1095-C-blanketter for mere end 500 medarbejdere, modtager du mere end én PDF-fil. Det anbefales, at du øger **Maksimal filstørrelse** i vinduet **Dokumentstyringsparametre** til 150 MB.

## <a name="viewing-information"></a>Visning af oplysninger

Du kan bruge siden **Arbejderens dækning under Affordable Care** til at se, hvilke medarbejdere der er tildelt til hver dækningsgruppe, hvilke medarbejderne der ikke skal medtages i en rapport, og hvilke medarbejdere der ikke er tildelt.

Hvis nogen af standardværdier fra Affordable Care-dækningsgruppen er blevet tilsidesat, vises en stjerne ud for den værdi, der er ændret. Hvis værdierne for alle 12 måneder er de samme og ikke er blevet tilsidesat, udskrives værdien i kolonnen **Alle 12 måneder**.

Du kan også bruge forespørgselsvinduet til at forstå, hvilke medarbejdere der er markeret som ikke ACA-rapporterbare. Du behøver ikke at spore, om de har fået dækning, og derfor behøver du ikke udstede et 1095-C til dem ved udgangen af året. Vælg **Ikke ACA-rapporterbar** i feltet **Filtrer efter** for at generere en liste over alle medarbejdere, der ikke vil modtage 1095-C.

Derudover kan du se medarbejdere, der ikke er omfattet af ACA-indberetningspligten, kan du også få vist alle medarbejdere, der ikke er tildelt (feltet **Indberet ACA-dækning** er tomt), eller som er tildelt til en Affordable Care-dækningsgruppe, der er udløbet for det år, der er valgt i feltet **År**.

Du kan eksportere lister over medarbejdere, som er genereret ved hjælp af filtreringsindstillingerne, til Excel.

Hvis du har brug for at rapportere dækkede personer, fordi du giver dig selv forsikret dækning, kan du få vist alle afhængige, der er dækket af frynsegodeplaner, der er markeret som **ACA-rapporterbare**. Vælg **Vis afhængig dækning** i handlingsruden.

> [!NOTE]
> Kun frynsegodeplaner, der markeret som **ACA-rapporterbare**, vises i forespørgselsvinduet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
