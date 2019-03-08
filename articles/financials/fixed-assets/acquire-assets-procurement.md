---
title: Anskaffe aktiver via indkøb
description: I dette emne beskrives det, hvordan du kan konfigurere integration mellem Anlægsaktiver og Kreditor, så der automatisk oprettes anlægsaktiver ud fra indkøbsordrer eller kreditorfakturaer, eller så der automatisk bogføres posteringer med anskaffelser eller anskaffelsesreguleringer for anlægsaktiver.
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef69de1c93de5c19b9f197838f1f2d3eb2e7645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "355788"
---
# <a name="acquire-assets-through-procurement"></a>Anskaffe aktiver via indkøb

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan konfigurere integration mellem Anlægsaktiver og Kreditor, så der automatisk oprettes anlægsaktiver ud fra indkøbsordrer eller kreditorfakturaer, eller så der automatisk bogføres posteringer med anskaffelser eller anskaffelsesreguleringer for anlægsaktiver.

 Følgende metoder er tilgængelige til integration mellem Anlægsaktiver og Kreditor, og du skal bruge samme metode for alle anlægsaktiver:
-   Du opretter et anlægsaktiv manuelt, før du føjer anlægsaktivnummeret til linjen på indkøbsordren eller kreditorfakturaen. Der bogføres automatisk en anskaffelsespostering for aktivet, når du bogfører kreditorfakturaen. Dette er standardmetoden.
-   Du opretter et anlægsaktiv manuelt, før du føjer anlægsaktivnummeret til linjen på indkøbsordren eller kreditorfakturaen. Der bogføres ikke en anskaffelsespostering for aktivet, når du bogfører kreditorfakturaen.
-   Der oprettes automatisk et anlægsaktiv, når du bogfører en produktkvittering eller en kreditorfaktura, hvor afkrydsningsfeltet Opret et nyt anlægsaktiv er markeret. Der bogføres automatisk en anskaffelsespostering for aktivet, når du bogfører kreditorfakturaen.
-   Der oprettes automatisk et anlægsaktiv, når du bogfører en produktkvittering eller en kreditorfaktura, hvor afkrydsningsfeltet Opret et nyt anlægsaktiv er markeret. Der bogføres ikke en anskaffelsespostering for aktivet, når du bogfører kreditorfakturaen.

Vælg en af de første to metoder, hvis du foretrækker at oprette anlægsaktiver manuelt, og tildel derefter anlægsaktivnummeret til indkøbsordren eller kreditorfakturaen. Vælg en af de to sidste metoder, hvis du foretrækker en fleksibel tilgang: Nogle gange opretter du måske anlægsaktiver manuelt, og nogle gange opretter du måske automatisk et nyt anlægsaktiv på baggrund af oplysningerne om anlægsaktiver i linjevaredetaljerne. 

Uanset om du opretter anlægsaktiver manuelt eller bruger en mere fleksibel tilgang, skal du også beslutte, om en anskaffelsespostering kun kan bogføres i Anlægsaktiver, eller om den kan bogføres, når du bogfører en kreditorfaktura. Visse organisationer foretrækker, at brugere opretter anskaffelser og anskaffelsesposteringer manuelt i Anlægsaktiver ved hjælp af manuelle kladdeposteringer eller forslag. 

I dette emne beskrives detaljerne ved de enkelte metoder.

## <a name="methods-for-manually-creating-fixed-assets"></a>Metoder til manuel oprettelse af anlægsaktiver
Når du bogfører en kreditorfaktura, hvor der er angivet et anlægsaktivnummer på linjerne, og indstillingen Tillad aktivanskaffelse fra Indkøb er markeret på siden Anlægsaktivparametre, bogføres anskaffelsen automatisk, og anlægsaktivets status ændres til Åben. 

Hvis en anskaffelse ikke kan bogføres, kan du enten angive en anskaffelsespostering i Anlægsaktiver manuelt eller bruge et anskaffelsesforslag i kladden Anlægsaktiver til at oprette flere anskaffelsesposteringer samtidigt.

> [!NOTE]                                                                                                                              
> Hvis Anlægsaktiver er konfigureret til at begrænse bogføring af anskaffelsesposteringer til en bestemt brugergruppe, skal du være medlem af den pågældende brugergruppe for at bogføre anskaffelsesposteringer fra fakturaer.

## <a name="methods-for-automatically-creating-fixed-assets"></a>Metoder til automatisk oprettelse af anlægsaktiver
Når du bogfører en produktkvittering, hvor indstillingen Opret et nyt anlægsaktiv er markeret for en linje, oprettes der et nyt anlægsaktiv med statussen Endnu ikke anskaffet. Når du derefter bogfører en kreditorfaktura med et nyt anlægsaktiv, bogføres der en anskaffelsespostering for det nye aktiv, og status ændres til Åben, hvis Anlægsaktiver er konfigureret til at tillade anskaffelser af aktiver fra Kreditor, og du er medlem af en brugergruppe, der kan bogføre anskaffelsesposteringer. 

Hvis indstillingen Nyt anlægsaktiv? ikke er markeret på indkøbslinjen, når du bogfører produktkvitteringen, men det er markeret, når du bogfører kreditorfakturaen, oprettes det nye anlægsaktiv, og det anskaffes med statussen Åben, hvis Anlægsaktiver er konfigureret til at tillade oprettelse og anskaffelse. Der oprettes ikke et ekstra aktiv, når du bogfører en kreditorfaktura, hvis der allerede blev oprettet ét, da du bogførte produktkvitteringen.

### <a name="capitalization-threshold"></a>Grænse for kapitalisering

Når du bruger en metode, hvor aktivet oprettes og anskaffes automatisk, kan du angive, at systemet skal kontrollere, om indkøbsbeløbet for anlægsaktivet overholder en bestemt grænse for kapitalisering for afskrivning af aktiver. Hvis det er tilfældet, er indstillingen Afskrivning valgt i bogen for aktivet, når det oprettes fra Kreditor. 

En grænse for kapitalisering er et beløb, der bestemmer, om aktiver afskrives, hvis de overholder det bestemte beløb. En grænse for kapitalisering er et beløb, der bestemmer, om aktiver afskrives, hvis de overholder det bestemte beløb. Hvis du f.eks. køber et aktiv, og indkøbsprisen er mindre end grænsen for kapitalisering, angives aktivet ikke til afskrivning. Hvis indkøbsprisen overholder eller overskrider grænsen, angives aktivet til afskrivning. 

Du kan konfigurere grænsen for kapitalisering på siden Anlægsaktivgrupper.

## <a name="scenario"></a>Scenarie
I følgende scenario beskrives hele integrationscyklussen for Anlægsaktiver og Kreditor. Der vises en eksempelopsætning, og brugen af anskaffelsesforslaget beskrives også. 

I dette scenario er systemet konfigureret på følgende måde:

-   Der oprettes automatisk aktiver, når produktkvitteringer eller kreditorfakturaer bogføres, men Anlægsaktiver er konfigureret til at forhindre, at der bogføres anskaffelsesposteringer fra Kreditor.
-   Konti er angivet i feltet Kontotype til kontotyper for Kvittering for anlægsaktiv og Anlægsaktivafgang på siden Varegrupper.
-   Grænsen for kapitalisering for computergruppen (COMP) er 1.500.
-   Din opgave består i at indtaste en indkøbsordre på en ny bærbar computer, som en medarbejder skal bruge, bogføre indkøbsordren, kontrollere, at kontorassistenten bogfører en produktkvittering, bogføre kreditorfakturaen og derefter kontrollere, at bogholderen opdaterer status for det bærbare computeraktiv til Åben.

Når du starter, skal du bruge siden Indkøbsordre til at angive detaljer om den bærbare computer, som koster 1.600. Du markerer indstillingen Nyt anlægsaktiv? i oversigtspanelet Anlægsaktiver på indkøbsordrelinjerne, vælger COMP som anlægsaktivgruppe og gemmer indkøbsordren. 

Når den bærbare computer modtages, indtaster og bogfører kontorassistenten en produktkvittering for at registrere modtagelsen af computeren. Computeraktivet oprettes og har statussen Endnu ikke anskaffet. Beløbet overskrider grænsen for kapitalisering. Derfor er indstillingen Afskrivning valgt i bøgerne for computeraktivet. Følgende posteringer forekom.

| Beskrivelse                               | Konto             | Debet    | Kredit   |
|-------------------------------------------|---------------------|----------|----------|
| Køb, produktkvitteringskøb        | Ikke-fakturerede tilgange | 1.600,00 |          |
| Køb, modkonto for produktkvitteringskøb | Periodiserede køb   |          | 1.600,00 |

Derefter skal du bogføre kreditorfakturaen for den bærbare computer. Status for computeren ændres ikke, da Anlægsaktiver er konfigureret til at forhindre, at der bogføres en postering af en aktivanskaffelse, når der bogføres en kreditorfaktura. Indstillingen Opret et nyt anlægsaktiv blev markeret, da kreditorfakturaen er bogført. Derfor blev kontoen Kvittering for anlægsaktiv brugt. Kontoen Anlægsaktivafgang blev ikke brugt, da der ikke blev bogført en anskaffelse. Den bruges senere, når organisationens bogholder bogfører en anskaffelsespostering i Anlægsaktiver ved hjælp af anskaffelsesforslag. 

Følgende posteringer forekom.

| Beskrivelse                               | Konto             | Debet    | Kredit   |
|-------------------------------------------|---------------------|----------|----------|
| Køb, modkonto for produktkvitteringskøb | Periodiserede køb   | 1.600,00 |          |
| Kreditorsaldo                            | Kreditor    |          | 1.600,00 |
| Køb, kvittering for anlægsaktiv             | Computerudgift    | 1.600,00 |          |
| Køb, produktkvitteringskøb        | Ikke-fakturerede tilgange |          | 1.600,00 |

Til sidst gennemser bogholderen alle anlægsaktiver med statussen Endnu ikke anskaffet. Det nye computeraktiv gennemses således. Bogholderen åbner derefter siden Anskaffelsesforslag fra kladdelinjerne Anlægsaktiver og opretter anskaffelsesposteringer for alle de aktiver, der har en faktura, men som stadig har statussen Endnu ikke anskaffet. Når kladden bogføres, ændres status for computeraktivet til Åben. Kontoen for Anlægsaktivafgang krediteres, og kontoen for aktivanskaffelse debiteres. 

Der findes bl.a. følgende variationer for dette scenario:

-   Hvis Anlægsaktiver er konfigureret til at tillade, at anskaffelsesposteringer for aktiver bogføres, når kreditorfakturaer bogføres, behøver bogholderen ikke at bruge anskaffelsesforslag i Anlægsaktiver, da anskaffelsesposteringen er oprettet. Forskellige konti opdateres også, når du bogfører kreditorfakturaen. I stedet for udgiften Computer debiteres beholdningskontoen Kvittering for anlægsaktiv, og to ekstra posteringer forekommer: Kontoen for aktivanskaffelse debiteres, og beholdningskontoen for Anlægsaktivafgang krediteres.
-   Hvis indstillingen Opret et nyt anlægsaktiv ikke er markeret, når produktkvitteringen bogføres, oprettes der ikke samtidig et aktiv. Hvis du markerer indstillingen Opret et nyt anlægsaktiv, før du bogfører kreditorfakturaen, oprettes aktivet og har statussen Endnu ikke anskaffet eller statussen Åben, hvis du også bogfører anskaffelsesposteringer, når der oprettes kreditorfakturaer.
-   Hvis omkostningerne for den bærbare computer er 1.400 i stedet for 1.600, nås grænsen for kapitalisering ikke. Aktivet oprettes derfor, og markeringen i indstillingen Afskrivning fjernes.
-   Hvis der bruges en indgangsbog, skal du bruge siden Godkendelseskladde, når indgangsbogen er bogført, for at hente bilaget, knytte indkøbsordren til kreditorfakturaen, markere indstillingen Opret et nyt anlægsaktiv og derefter bogføre kreditorfakturaen. Hvis du er medlem af en brugergruppe, der kan oprette anskaffelsesposteringer, oprettes anskaffelsen, og aktivet har statussen Åben.
-   Hvis der kun er modtaget en delmængde, oprettes der ikke en anskaffelse af aktiv for den første kreditorfaktura på grund af brugergruppebegrænsninger. Den eneste måde, anskaffelsen kan bogføres på for den anden kreditorfaktura, der afslutter det bestilte antal, er, hvis der allerede er registreret en anskaffelsespostering for den første kreditorfaktura, og du er medlem af en brugergruppe, der kan bogføre anskaffelser.


Du kan finde flere oplysninger under [Integration af anlægsaktiver](fixed-asset-integration.md).



