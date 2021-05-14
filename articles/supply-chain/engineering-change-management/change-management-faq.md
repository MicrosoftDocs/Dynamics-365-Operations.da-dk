---
title: Ofte stillede spørgsmål om styring af tekniske ændringer
description: Dette emne indeholder svar på ofte stillede spørgsmål om funktionen til styring af tekniske ændringer.
author: t-benebo
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ed48c694cec42b86fb3b3908dc608a97979944f6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920175"
---
# <a name="engineering-change-management-faq"></a>Ofte stillede spørgsmål om styring af tekniske ændringer

[!include [banner](../includes/banner.md)]

Dette emne indeholder svar på ofte stillede spørgsmål om funktionen til styring af tekniske ændringer.

## <a name="should-i-track-the-version-in-transactions"></a>Skal jeg spore versionen i transaktioner?

Når du opretter en ændringskategori for teknikere, indeholder siden **Kategoridetaljer om tekniske ændringer** indstillingen **Spor version i transaktioner**. Hvad er denne indstilling, og hvad gør den?

- Hvis du angiver indstillingen **Spor version i transaktioner** til *Ja*, filtreres feltet **Dimensionsgruppe**, så det kun viser de dimensionsgrupper, hvor versionen er en aktiv dimension.
- Hvis du angiver indstillingen **Spor version i transaktioner** til *Nej*, filtreres feltet **Dimensionsgruppe**, så det kun viser de dimensionsgrupper, hvor versionen **ikke** er en aktiv dimension.

### <a name="if-you-track-the-version-in-transactions"></a>Hvis du sporer versionen i transaktioner

I forbindelse med tekniske kategorier, hvor du har valgt en dimensionsgruppe, hvor versionen er en aktiv dimension, kan du spore versioner i transaktioner for produkter i den pågældende kategori. I så fald vil det tekniske produkt være en produktmaster, og hver version af produktet er en produktvariant, der bruger versionsdimensionen. Andre dimensioner kan bruges sammen med versionsdimensionen.

I så fald behandles hver enkelt teknisk version som en variant i alle processer. Hvis du har en bestemt variant i en transaktion (så du kan bestemme, hvilken variant der blev solgt eller købt), skal du derfor administrere lagerbeholdningen for hver version, mens varedisponeringen planlægger levering for hver version osv. Hvis du trækker en version tilbage fra markedet, skal du manuelt justere start- og slutdatoerne, så de afspejler ændringen. Du skal også styre lageret for at sikre, at du ikke har ubrugte vareversioner på dine lagersteder.

Selvom denne indstilling kræver mere administration, anbefales den, hvis du har brug for høj sporbarhed for de specifikke versioner, der bruges i de enkelte transaktioner.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Hvis du ikke sporer versionen i transaktioner

I forbindelse med tekniske kategorier, hvor du har valgt en dimensionsgruppe, hvor versionen **ikke** er en aktiv dimension, kan du **ikke** spore versioner i transaktioner for produkter i den pågældende kategori. Hvis du ikke bruger en anden dimension i dette tilfælde, vil det tekniske produkt være et særskilt produkt. Produktet bliver stadig versioneret, og du kan administrere oplysninger om bestemte versioner (f.eks. stykliste og rute), men du vil ikke kunne spore, hvilken specifik version der er brugt i de enkelte transaktioner. Start- og slutdatoerne angiver gyldigheden af hver version.

Denne indstilling er meget nemmere at administrere, for hvis du vil skifte fra én version til en anden, skal du blot foretage de nødvendige ændringer i en ændringsrækkefølge og derefter opdatere start- og slutdatoerne i den tekniske version. Produktionsprocesserne henter derefter den nødvendige stykliste og rute for produktet (og dets specifikke version).

De fleste organisationer vælger denne indstilling, fordi den indeholder versions- og ændringsstyring, men ikke giver de ekstra faste omkostninger til sporing af versionen i de enkelte transaktioner, på lageret og under varedisponeringen.

## <a name="which-fields-are-copied-to-the-released-item-template"></a>Hvilke felter kopieres til den frigivne vareskabelon?

Når en teknisk virksomhed opretter et teknisk produkt, oprettes dette produkt som et frigivet produkt i den tekniske virksomhed. Det frigivne produkt, der oprettes, er baseret på den valgte *skabelon for frigivne varer*. (Skabelonen til frigivne varer er i sig selv et frigivet produkt). Skabelonen for frigivne varer bruges også, når produktet frigives til en driftsvirksomhed. I alle tilfælde definerer skabelonen for frigivne varer de fleste feltværdier for det frigivne produkt, og disse værdier hentes fra den tilknyttede side **Oplysninger om frigivne produkter**.

Følgende tabeller viser de felter, der kopieres under disse processer.

| Oversigtspanel | Felter, der kopieres ved produktets oprettelse i den tekniske virksomhed | Felter, der kopieres ved frigivelse til en driftsvirksomhed |
|---|---|---|
| **Almindelig** | Alle felter i afsnittet **Administration** | De samme felter, som er kopieret til den tekniske virksomhed |
| **Indkøb** | Alle felter | Alle felter med undtagelse af **Enhed** |
| **Sælg** | Alle felter i følgende afsnit: **Salgsordre**, **Administration**, **Moms**, **Prisopdatering**, **Basissalgspris**, **Gebyrer**, **Rabatter** og **Alternativt produkt** | Alle de felter, der er kopieret til den tekniske virksomhed, undtagen **Enhed** |
| **Udenrigshandel** | Alle felter | Alle felter |
| **Styr lager** | Alle felter og sektioner *undtagen* **Fysiske dimensioner** og **Fastvægt** | Alle de felter, der er kopieret til den tekniske virksomhed, undtagen **Enhed** |
| **Tekniker**, **Plan**, **Administrer omkostninger**, **Administrer projekter**, **Økonomiske dimensioner** og **Lagersted** | Alle felter | Alle felter undtagen **Styklisteenhed** |
| **Produktvarianter** | Alle felter i sektionen **Standardproduktvariant** | De samme felter, som er kopieret til den tekniske virksomhed |

Ud over de felter, der vises i den forrige tabel, kopieres alle standardordreindstillinger fra den frigivne vareskabelon, både når produktet oprettes i den tekniske virksomhed, og når det frigives til en driftsvirksomhed. (Hvis du vil have vist standardordreindstillingerne for en skabelon for frigivne varer, skal du åbne den relevante side **Oplysninger om frigivne produkter** og derefter vælge **Standardordreindstillinger** under fanen **Administrer lager** i handlingsruden.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Skal jeg oprette en separat juridisk enhed for tekniske produkter eller bruge en eksisterende juridisk enhed?

Din virksomheds behov afgør, om du skal oprette en ny juridisk enhed til tekniske produkter.

Når du opretter en separat teknisk virksomhed, kan du adskille de tekniske data og derefter tilføje ændringer, efterhånden som det kræves af dine lokale driftsvirksomheder. På den måde kan du opfylde følgende målsætninger:

- Bevare en separat enhed, hvor de tekniske produkter oprettes og administreres.
- Undgå, at tekniske produkter vises sammen med resten af dine frigivne produkter, før de er klar og frigivet.
- Skelne klart mellem henholdsvis tekniske data og lokale data.

På den anden side skal du sandsynligvis bruge en eksisterende juridisk enhed som teknisk virksomhed, hvis følgende betingelser gælder for dig:

- Du har kun én juridisk enhed i systemet, og/eller du behøver ikke have en klar adskillelse mellem de produkter, der konstrueres.
- Du ønsker ikke at duplikere visse data, f.eks. ressourcegrupper, ressourcer, operationer og (måske) lokationer.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Hvad er nomenklaturen for tekniske versioner og varianter?

Nomenklaturen for tekniske produkter og produktvarianter fungerer på følgende måde:

- For det tekniske produkt (dvs. det specifikke produkt, når der ikke anvendes dimensioner, eller produktmasteren, når der anvendes en dimension) defineres nomenklaturen i kategorien for det tekniske produkt. Her kan du bruge en nummerserie, tekstkonstanter samt attributnavne og værdier.
- For hver variant af et teknisk produkt (hvis det pågældende tekniske produkt er en produktmaster, oprettes der varianter i den tekniske produktkategori, hvor du angiver dimensionsgruppen) defineres nomenklaturens nummereringsregel for hver variant i dimensionsgruppen. I så fald kan du bruge produkt-id'et for masteren samt dimensionsværdier og -navne.
