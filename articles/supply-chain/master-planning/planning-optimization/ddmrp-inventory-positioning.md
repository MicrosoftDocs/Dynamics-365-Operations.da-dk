---
title: Lagerpositionering
description: Denne artikel indeholder oplysninger om strategisk lagerplacering, som omfatter identifikation af afkoblingspunkter i forsyningskæden, hvor du kan opbygge den tilgængelige lagerbeholdning for at hjælpe med at komprimere leveringstider og nedbryde leveringstiderne for forsyningskæden.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bec36b5b51b937782afdb78d7009a58dcd0942f0
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186682"
---
# <a name="inventory-positioning"></a>Lagerpositionering

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Strategisk lagerplacering omfatter identifikation af afkoblingspunkter i forsyningskæden, hvor du kan opbygge lagerbeholdning. Denne indfaldsvinkel bruges først og fremmest til at komprimere leveringstider og sikre forsyningskæden. Det giver dig mulighed for at reducere "effekten af efterspørgsel", fordi tilpasningen af behovet ikke har passeret hele forsyningskæden. (Denne *effekt af efterspørgsel* refererer til, hvor lille efterspørgselsudsving på detailniveau kan medføre progressivt større efterspørgsel hos engros-, distributør-, producent- og råvareleverandørniveauerne.)

Lagerpositionering er det første trin i DDMRP (Demand Driven Materials Resource Planning).

## <a name="inventory-positioning-for-manufacturing"></a>Lagerpositionering til produktion

Dette afsnit indeholder et eksempel på, hvordan du foretager lagerplaceringsbeslutninger, hvis du fremstiller et typisk produkt. Et arbejde har en stykliste på flere niveauer, som vist i følgende illustration.

![Eksempel på styklister med flere niveauer for et produkt, der bruger flere produkter.](media/ddmrp-bom-example.png "Eksempel på styklister med flere niveauer for et produkt, der bruger flere produkter")

### <a name="choose-your-decoupling-points"></a>Vælge dine afkoblingspunkter

Når du vælger, hvor du vil placere dine afkoblingspunkter, skal du overveje alle følgende aspekter af hver vare i styklisten som et kriterium:

- Ekstern variability
- Lagerstyring og fleksibilitet
- Beskyttelse af kritisk operation
- Kundetolerancetid
- Synlighed af salgsordrer
- Potentiel markedstid

I eksemplet her kan du placere dit første afvænningspunkt hos *foam billets* af følgende årsager:

- Det er svært at finde de materialer, der bruges til at lave styklisterne, og tilgængeligheden er vigtig. Det *eksterne variationskriterium* er derfor opfyldt.
- De forskellige produkter kan skæres ud i mange forskellige former og størrelser, så der ud over produktet fremstilles indsætninger til andre produkter, som du producerer. Kriterierne for *lagerstyring og fleksibilitet* er derfor opfyldt.

Derefter kan du placere dit næste aftrækspunkt i *materialesættet*, der er forudindstillet materiale. Du kan vælge dette punkt, fordi du kun har én materialeskæringsmaskine. Det kritiske kriterium for *beskyttelse af operationer* er derfor opfyldt.

Til sidst kan du eventuelt placere dit sidste afkoblingspunkt på det færdige vareelement. Du kan vælge dette punkt, fordi du har en meget lav *kundetolerancetid* på salg, og fordi *synligheden af salgsordrer* er rimelig kort. Du vil derfor sikre dig, at du har den lagerbeholdning, der er til rådighed, så du kan opfylde indgående ordrer. Du kan også angive en højere pris ved at holde leveringstiden så kort, hvilket er det, som kriteriet for den *potentielle markedstid* refererer til.

Baseret på denne analyse viser følgende illustration, hvad pillow-styklisten ser ud. De gule lagersymboler fremhæves ved udfyldningspunkter.

![Eksempel på stykliste med fremhævede punkter.](media/ddmrp-bom-decoupling-example.png "Eksempel på stykliste med fremhævede punkter")

### <a name="calculate-your-decoupled-lead-time"></a>Beregn din afkoblede gennemløbstid

I dette afsnit vises, hvordan du kan beregne de nye leveringstider, efter du har indført afkoblingspoint.

I følgende illustration af eksemplet ovenfor, der blev startet i forrige afsnit, vises leveringstiderne i grå felter øverst til venstre for hver styklistekomponent. Felter med rød omrids angiver varer, der kører den akkumulerede leveringstid (summen af de længste gennemløbstider på hvert niveau i styklisten). Denne gennemløbstid er 21 dage, hvor du starter fra bunden.

![Eksempel på stykliste med leveringstider.](media/ddmrp-bom-lead-times-example.png "Eksempel på stykliste med leveringstider")

Hvis du anvender de afkoblingspunkter, du tidligere har valgt, vil de afkoblede varer dog altid være på lager. De vil derfor have en gennemløbstid på 0 (nul). Den nye gennemløbstid for kunden er nu kun fem dage: To dage til at købe tråden og tre dage til at producere en pillow. Denne gennemløbstid kaldes den *mislykkede gennemløbstid*.

![Eksempel på afkoblet gennemløbstid.](media/ddmrp-bom-decoupled-lead-time-example.png "Eksempel på afkoblet gennemløbstid")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strategisk lagerplacering i en detailmodel

Da detailforretninger kun opbevarer lagervarer, er styklisterne ikke et problem. Detailhandlende kan dog stadig bruge DDMRP ved at angive strategiske lagerplaceringer og bufferniveauer baseret på lagerplaceringer i distributionsnetværket.

I følgende illustration vises et eksempel på et firma, der har et distributionscenter i Seattle, og butikker i Boston, Atlanta og Portland.

![Afkoblingspunkter, der er baseret på lokation i en detailmodel.](media/ddmrp-retail-decoupl-points-example.png "Afkoblingspunkter, der er baseret på lokation i en detailmodel")

Du bestemmer måske, at overførselstiden for flytningen af et rammeprodukt mellem distributionscenteret og butikkerne overtræder *kundetolerancetiden*, da kunderne forventer, at blanketter er på lager, når de besøger lageret. I dette tilfælde skal du oprette et kontaktpunkt for rammeelementet i hver af de tre butikker. Der er forskellige bufferniveauer for hver enkelt butik, afhængigt af dens leveringstider, efterspørgselsmønstre osv.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Implementere lagerplacering i Dynamics 365 Supply Chain Management

I dette afsnit beskrives, hvordan du implementerer lagerplaceringsstrategien i Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Konfigurere varedisponeringsgrupper, der opretter disponeringspunkter

Varer bliver til efterposteringspunkter, når de tilhører en disponeringsgruppe, der er konfigureret med **disponeringskodeværdien** med *Afkoblingspunkt*. Det første trin i opsætningen af DDMRP er derfor at beslutte, hvilke disponeringsgrupper du skal implementere for DDMRP-strategien, og derefter oprette dem ved at følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Dækningsgrupper**.
1. Vælg **Ny** i handlingsruden for at oprette en dækningsgruppe.
1. Angiv oplysninger, der identificerer disponeringsgruppen og vælg derefter den kalender, der skal bruges.
1. Angiv feltet **Afkoblingspoint** i feltet **Dækningskode** på fanen *Generelt*. Denne indstilling bevirke, at alle varer, der tilhører denne disponeringsgruppe, behandles som dDMRP-point. Den aktiverer også alle DDMRP-indstillinger for denne gruppe som beskrevet senere i denne procedure.
1. Angiv følgende felter i afsnittet **DDMRP-parametre** under fanen **Andet**.

    - **Gennemløbstidsfaktor** – Angiv en faktor (som en decimalværdi mellem 0 og 1) for at styre den virkning, som gennemløbstiden skal have, når der beregnes minimum- og maksimumlagerniveauer for varer i denne disponeringsgruppe. Jo længere leveringstiden for en vare er, jo lavere skal dens gennemløbstidsfaktor være. En lavere gennemløbstidsfaktor medfører lavere minimums- og maksimumlagerniveauer og medfører derfor mindre og mere hyppige ordrer. DDMRP-metoden anbefaler en værdi mellem 0,20 og 0,40 for varer med lange gennemløbstider mellem 0,41 og 0,60 for varer med mellemfristede leveringstider og mellem 0,61 og 1,00 for varer med korte leveringstider. Du kan finde flere oplysninger i [Bufferprofil og niveauer](ddmrp-buffer-profile-and-levels.md).
    - **Variabilitetsfaktor** – Angiv en faktor (som en decimalværdi mellem 0 og 1) for at styre den virkning, som gennemløbstiden skal have, når der beregnes minimum- og maksimumlagerniveauer for varer i denne disponeringsgruppe. Jo mere variabel varebehovet er, jo højere skal dens variationsmuligheder være. En højere variationsfaktor medfører et højere minimumslagerniveau. DDMRP-metoden anbefaler en værdi mellem 0,00 og 0,40 for varer med lave gennemløbstider mellem 0,41 og 0,60 for varer med mellemfristede variabilitet og mellem 0,61 og 1,00 for varer med høj variabilitet. Du kan finde flere oplysninger i [Bufferprofil og niveauer](ddmrp-buffer-profile-and-levels.md).
    - **Min., maks. og re-ordre-pointperiode** – Angiv, hvor ofte der skal beregnes bufferværdier (*Dagligt* eller *Ugentligt*).

1. Angiv følgende felter i afsnittet **Gennemsnitlig dagligt brug** under fanen **Andet**.

    - **Gennemsnitlig daglig brug baseret på** – Vælg, hvilke tidsperioder beregningen af den gennemsnitlige daglige brug (ADU) skal baseres på. Vælg en af følgende værdier:

        - *Tidligere* – Se kun på tidligere brug af det antal dage, der er angivet i feltet **Tidligere periode (dage)**. ADU beregnes som den samlede efterspørgsel efter en vare i beregningsperioden (i lagerenheder) divideret med antallet af dage i beregningsperioden.
        - *Fremadrettet* – Se kun på planlagt fremtidig brug (herunder prognoser) for antallet af dage, der er angivet i feltet **Fremadrettet periode (dage)**. ADU beregnes som den samlede efterspørgsel efter en vare i beregningsperioden (i lagerenheder) divideret med antallet af dage i beregningsperioden. 
        - *Blandet* - Se på både tidligere og fremtidig brug. Indstillinger for feltet **Tidligere periode (dage)**, feltet **Fremadrettet periode (dage)** og blandingsindstillingerne gælder alle. 

            *Blandet ADU* = (\[*Tidligere vægtning* × *Past ADU*\] + \[*Fremadrettet vægtning* × *Fremadrettet ADU*\]) ÷ (*Tidlig vægtning* + *Fremadrettet vægtning*)

    - **Tidligere periode (dage)** – Angiv det antal tidligere dage (op til og med dags dato), som systemet skal tage højde for, når det beregner det ADU for varer i denne disponeringsgruppe. Denne indstilling gælder kun, når brugen af **Daglig gennemsnit baseret på**-feltet er angivet til *Tidligere* eller *Blandet*.
    - **Fremadrettet periode (dage)** – Angiv det antal fremtidige dage (fra i dag og op til en bestemt dag), som systemet skal tage højde for, når det beregner det ADU for varer i denne disponeringsgruppe. Denne indstilling gælder kun, når brugen af **Daglig gennemsnit baseret på**-feltet er angivet til *Fremadrettet* eller *Blandet*.
    - **Relativ vægt af tidligere periode for daglig brug af blandet gennemsnit** – Angiv den vægt (som en procent), der skal anvendes i den sidste periode, når den blandet ADU beregnes. Denne indstilling gælder kun, når brugen af **Daglig gennemsnit baseret på**-feltet er angivet til *Blandet*.
    - **Relativ vægt af fremadrettet periode for daglig brug af blandet gennemsnit** – Angiv den vægt (som en procent), der skal anvendes i den fremtidige periode, når den blandede ADU beregnes. Denne indstilling gælder kun, når brugen af **Daglig gennemsnit baseret på**-feltet er angivet til *Blandet*.

1. For alle andre faner og felter skal du angive detaljerede oplysninger, der bruges til at beregne behovene for de varer, der er tilknyttet disponeringsgruppen.

### <a name="set-an-item-as-a-decoupling-point"></a>Angive en vare som et afkoblingspunkt

Hvis du vil angive en vare som et afkoblingspunkt, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Find og vælg en frigivet vare, som du vil konfigurere til DDMRP.
1. Vælg **Plan** i handlingsruden, og vælg derefter **Varedisponering**.
1. På siden **Varedisponering** er der måske allerede angivet flere varedisponeringsposter, som hver især gælder for en forskellig kombination af lagrings- og produktdimensioner. Du kan vælge en eksisterende varedisponeringspost, der gælder for de dimensioner, hvor du vil oprette et udligningspunkt. Du kan også vælge **Ny** i handlingsruden for at oprette en ny varedisponeringspost.
1. Konfigurer varedisponeringsposten som sædvanligt. Du skal som minimum angive den lokation og det lagersted, hvor afkoblingspunktet skal anvendes.
1. Mens den relevante post stadig er valgt, skal du vælge fanen **Generelt**.
1. Marker afkrydsningsfeltet **Brug specifikke indstillinger**.
1. Indstil feltet **Disponeringsgruppe** til en disponeringsgruppe, der er konfigureret til at oprette disponeringspunkter (som beskrevet i forrige afsnit).
1. Varen er nu konfigureret som et afkoblingspunkt. Når du bruger DDMRP, kan du normalt også konfigurere indstillinger her, der påvirker bufferstørrelser og restordreantallet. Du kan dog fuldføre konfigurationen senere. Du kan finde flere oplysninger i indstillinger i [Oprette buffere for en vare til udfyldningspunkt](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Hvis du vil planlægge varer, der ikke er afkoblingspunkter, skal du følge samme trin, som du skal følge, når der bruges mrp (standard material requirements planning).
