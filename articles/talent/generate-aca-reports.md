---
title: Generere Affordable Care Act (ACA)-indberetninger
description: "Funktionen kan hjælpe arbejdsgivere med at spore de oplysninger, der indberettes i blanketterne 1095-B og C 1095, som et led i Employer Mandate-delen af Affordable Care Act. Bemærk, at denne funktion er kun aktiveret for juridiske enheder i USA."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 25d2b8326bba69ac627f3fa7e05a6c850bd04c91
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="generate-affordable-care-act-aca-reports"></a>Generere Affordable Care Act (ACA)-indberetninger

[!include [banner](includes/banner.md)]

Funktionen kan hjælpe arbejdsgivere med at spore de oplysninger, der indberettes i blanketterne 1095-B og C 1095, som et led i **Employer Mandate**-delen af Affordable Care Act. Bemærk, at denne funktion er kun aktiveret for juridiske enheder i USA.

## <a name="getting-started"></a>Kom godt i gang
Når du begynder at spore oplysninger, som skal indberettes i blanketterne 1095-B og C-1095, skal du først oprette en eller flere Affordable Care-dækningsgrupper. Disse dækningsgrupper under Affordable Care bruges til at angive det tilbud om dækning, der er givet til en medarbejder, medarbejderens andel af den månedlige præmie med de laveste omkostninger (hvis omkostningen overstiger den føderale fattigdomsgrænse) samt Safe Harbor, der bruges af arbejdsgiveren, hvis det er relevant. Brug af grupper under Affordable Care Act gør det muligt for dig at administrere oplysningerne for disse felter uden at skulle åbne alle medarbejderposter, hvor betingelserne er ens. Desuden kan Affordable Care-dækningsgrupper nemt tildeles til en eller flere medarbejdere ved hjælp af massetildelingsfunktionerne på siden.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Vedligeholde flere versioner af en dækningsgruppe
Du kan vedligeholde flere versioner af en dækningsgruppe, så du kan foretage ændringer, der ajourfører gruppens oplysninger, uden at skulle oprette en ny gruppe og tildele medarbejdere til den, når noget ændres i din organisation eller i de frynsegoder, der tilbydes. 

Når du har oprettet de dækningsgrupper til Affordable Care, du skal bruge, kan du vælge at massetildele grupperne til medarbejderne ved hjælp af funktionen **Massetildeling** på siden, eller du kan gå til den enkelte medarbejder og angive, om ACA-oplysninger skal spores og rapporteres for denne medarbejder, samt tildele medarbejderen til en Affordable Care-dækningsgruppe.

Hvis oplysninger om Affordable Care-dækning ikke skal spores eller rapporteres for en medarbejder, f.eks. hvis medarbejderen arbejder på deltid, kan feltet **Indberet dækning** være indstillet til Nej. Selvom hver medarbejder, hvis ACA-oplysninger skal spores, skal tildeles til en Affordable Care-dækningsgruppe, kan du stadig ændre indstillingerne **Tilbud om dækning**, **Medarbejderens andel af omkostningen** og **Safe Harbor** for enhver måned – eller måneder – hvor der skal bruges andre værdier end dem, der er angivet i Affordable Care-dækningsgruppen.

Hvis du vil angive undtagelser til nogen af værdierne i Affordable Care-dækningsgrupper, skal du klikke på linket Affordable Care Coverage, der er findes på siden Detaljer om arbejder. Det er under afsnittet Flere oplysninger under fanen Ansættelse.

## <a name="reporting-health-care-coverage"></a>Indberetning af dækning af sygeforsikring
Udover at spore, hvad der ville ske, hvis en sygeforsikringsdækning blev tilbudt til en fuldtidsmedarbejder, hvis arbejdsgiveren tilbyder en arbejdsgiver-sponsoreret sygesikringsordning med egendækning, som medarbejderen er tilmeldt (uanset om vedkommendes ansættelsesstatus er fuldtid eller deltid), skal yderligere oplysninger rapporteres i 1095-C. Hver medarbejder (inklusive deres afhængige parter), der er omfattet af arbejdsgiver-sponsorerede frynsegodeplaner, skal medtages i indberetningen for de måneder, hvor de var dækket. 

Du kan angive, om hver frynsegodeplan skal indberettes, ved at markere afkrydsningsfeltet **Skal indberettes til det amerikanske skattevæsen (ACA)**.

Hvis medarbejdere derudover har valgt, at en eller flere afhængige parter skal være omfattet af et frynsegode, kan du angive de datoer, hvor disse afhængige har været dækket, for hver medarbejder på siden Vedligehold frynsegoder. Du kan angive, at den afhængige part er dækket af frynsegoden, ved at vælge knappen Rediger i handlingsruden i oversigtspanelet Afhængige.

På siden **Håndtering af dækningsdato for den afhængige** kan du angive de datoer, hvor den afhængige part er dækket af frynsegodet. Når du angiver datoer på denne side, markeres afkrydsningsfeltet **Disponeret** automatisk på siden **Vedligehold frynsegoder**.

## <a name="generate-1095b-and-1095c-forms"></a>Generere 1095B- og 1095C-blanketter
Du kan også generere 109-B- og 1095-C-blanketter fra produktet og distribuere dem til hver af dine medarbejdere. Elektronisk generering af 1095 C, og de tilsvarende 1094 C-filer, der kan bruges til at sende til det amerikanske skattevæsen (IRS), kan også genereres fra systemet.  

Når du genererer 1095-C-blanketten, skal du angive den relevante kalender- eller skatteåret også, hvis du vil udskrive blanketten med to eller tre sider. Den tresidede blanket er kun nødvendigt, hvis arbejdsgiverens sygesikringsordning med egendækning og en medarbejder har mere end seks dækkede afhængige, herunder sig selv. Når systemet genererer den tosidede blanket, registrerer det automatisk, hvis en medarbejder har mere end 6 dækkede afhængige, og vedkommende medtages ikke, når blanketten genereres. Når systemet genererer den tresidede blanket, medtager det desuden kun de medarbejdere, der har mere end seks dækkede afhængige.

## <a name="viewing-information"></a>Visning af oplysninger
Du kan bruge siden **Arbejderens dækning under Affordable Care** til at se, hvilke medarbejdere der er tildelt til hver dækningsgruppe, hvilke medarbejderne der ikke skal medtages i en rapport, og hvilke medarbejdere der ikke er tildelt.

Hvis nogen af standardværdier fra Affordable Care-dækningsgruppen er blevet tilsidesat, vises en stjerne ud for den værdi, der er ændret. Hvis værdierne for alle 12 måneder er de samme og ikke er blevet tilsidesat, udskrives værdien i kolonnen **Alle 12 måneder**.

Du kan også bruge forespørgselsvinduet til at få en forståelse af, hvilke medarbejdere der er markeret som ikke-ACA- indberetningspligtige, hvilket betyder, at du ikke behøver at spore, om de er blevet tilbudt dækning, og at du ikke behøver at udstede en 1095-C til dem i slutningen af året. Ved at vælge **Skal ikke indberettes til det amerikanske skattevæsen (ACA)** i feltet **Filtrer efter** kan du generere en liste over alle medarbejdere, hvor det er markeret, at de ikke skal modtage en 1095-C-blanket.

Udover at få vist en liste over medarbejdere, der ikke er omfattet af ACA-indberetningspligten, kan du også få vist alle medarbejdere, der ikke er tildelt (feltet **Indberet ACA-dækning** er tomt), eller som er tildelt til en Affordable Care-dækningsgruppe, der er udløbet for det år, der er valgt i feltet **År**.

Du kan eksportere lister over medarbejdere, som er genereret ved hjælp af filtreringsindstillingerne, til Excel.

Hvis du skal rapportere dækkede enkeltpersoner, fordi du som arbejdsgiver tilbyder sygesikring med egendækning, kan du også få vist alle afhængige, der er omfattet af frynsegodeplaner, der er markeret som **Skal indberettes til det amerikanske skattevæsen (ACA)**, ved at vælge handlingen Vis dækning af afhængig part i handlingsrudestriben.

**Bemærk!** Kun frynsegoder, hvis plan er markeret som **Skal indberettes til det amerikanske skattevæsen (ACA)** vises i forespørgselsvinduet.

