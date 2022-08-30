---
title: Lagerstedsallokering
description: Denne artikel indeholder oplysninger om lagerstedsallokering. Lagerstedsallokering gør det muligt at konsolidere efterspørgsel efter vare og måleenhed fra ordrer, der har statussen bestilt, reserveret eller frigivet. Den gør det lettere for lagerchefer at planlægge pluklokationer på en intelligent måde, før de frigiver ordrerne til lageret og opretter plukarbejde.
author: Mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: bb86800f1491e8cb9ad629ed6cc1c76e9393e945
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336029"
---
# <a name="warehouse-slotting"></a>Lagerstedsallokering

[!include [banner](../includes/banner.md)]

Der er flere tilgængelige funktioner for lagerstedsallokering, som gør det lettere for lagerchefer at planlægge pluklokationer på en intelligent måde, før de frigiver ordrerne til lagerstedet og opretter plukarbejde.

Funktionen *Lagerstedsallokering* gør det muligt at konsolidere efterspørgsel efter vare og måleenhed fra ordrer, der har statussen *Bestilt*, *Reserveret* eller *Frigivet*. Genereret efterspørgsel kan derefter anvendes på lokationer, der skal bruges til plukning, baseret på antal, enhed, fysiske dimensioner, faste lokationer mv. Når allokeringsplanen er blevet oprettet, kan genopfyldningsarbejdet oprettes for at bringe den korrekte lagermængde til hver lokation.

Med funktionen *Lagerstedallokering for flytteordrer* kan lagerchefer genopfylde plukpladser baseret på efterspørgsel fra flytteordrer, der endnu ikke er frigivet til lagerstedet. Det sikrer, at plukpladser indeholder alle de varer, der kræves til flytteordrerne, når de er frigivet til lagerstedet. Denne funktion kræver, at du også aktiverer funktionen *Lagerstedsallokering*.

Funktionen *Forbedringer af lagerstedsallokering* tilføjer en indstilling for de skabelonlinjer, der bruges af funktionen *Lagerstedsallokering*. Indstillingen gør det muligt for systemet at overveje den eksisterende disponible lagerbeholdning på en mållokation. Derfor kan der genereres færre genopfyldninger for allokering. Funktionen *Forbedringer af fordeling af lagerstedsallokering* kræver, at du også aktiverer funktionen *Lagerstedsallokering*. Den kan evt. bruges sammen med funktionen *Lagerstedsallokering for flytteordrer*.

## <a name="turn-on-the-warehouse-slotting-features"></a>Aktivere funktioner til lagerstedsallokering

Før du kan bruge disse funktioner, skal de være slået til for dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for funktionerne og aktivere dem, hvis de skal bruges. Aktivér følgende funktioner efter behov:

- Brug af slotfunktion på lagersted
- Lagerstedsallokering for flytteordrer

    > [!IMPORTANT]
    > Funktionen *Lagerstedsallokering* skal være aktiveret før denne funktion.

- Forbedringer af fordeling af lagerstedsallokering

    > [!IMPORTANT]
    > Funktionen *Lagerstedsallokering* skal være aktiveret før denne funktion.

## <a name="set-up-warehouse-slotting"></a>Konfigurere lagerstedsallokering

Hvis du vil bruge lagerstedsallokering, skal du konfigurere følgende elementer i dit system:

- Måleenhedsniveauer for allokering
- Vejledningskoder
- Allokeringsskabeloner
- Lokationsvejledninger

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Oprette måleenhedsniveauer for allokering

Måleenhedsniveauerne gør det muligt at gruppere flere måleenheder med henblik på allokering. Hvis der f.eks. plukkes flere størrelser af kasser fra det samme kasseplukområde, kan der oprettes ét niveau for alle størrelserne. **Der skal oprettes en linje for hver måleenhed, der skal være en del af niveauet.**

1. Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Måleenhedsniveauer til allokering**.
1. Vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Måleenhedsniveau:** *EaBoxPl*
    - **Beskrivelse:** *Hver kassepalle*

1. Vælg **Gem**.
1. Gå til oversigtspanelet **Måleenheder**, og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Enhed:** *Kasse*
    - **Beskrivelse:** Lad feltet være tomt. Det udfyldes automatisk, når du gemmer ændringerne.
    - **Enhedsklasse:** *Antal*

1. Vælg **Ny** for at føje en anden linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Enhed:** *Styk*
    - **Beskrivelse:** Lad feltet være tomt. Det udfyldes automatisk, når du gemmer ændringerne.
    - **Enhedsklasse:** *Antal*

1. Vælg **Ny** for at føje en tredje linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Enhed:** *PL*
    - **Beskrivelse:** Lad feltet være tomt. Det udfyldes automatisk, når du gemmer ændringerne.
    - **Enhedsklasse:** *Antal*

1. Vælg **Gem** for at gemme niveauet.

### <a name="create-a-directive-code-for-slotting"></a>Oprette en vejledningskode til allokering

Du skal vælge den vejledningskode, der skal knyttes til en skabelon.

1. Gå til **Lokationsstyring \> Opsætning \> Vejledningskoder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. I feltet **Vejledningskode** skal du angive *Allokering*.
1. I feltet **Vejledningsbeskrivelse** skal du angive *Allokering*.

### <a name="set-up-slotting-templates"></a>Konfigurere allokeringsskabeloner

Hver allokeringsskabelon styrer, hvordan lager tilknyttes lokationer for et bestemt lagersted. Hver skabelon skal indeholde en linje for hver allokeringsspecifikation. Brug procedurerne i dette afsnit til at konfigurere allokeringsskabeloner.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Genopfyldning \> Allokeringsskabeloner**.
1. Vælg **Ny** for at oprette en skabelon.

Derefter skal du konfigurere skabelonhovedet, allokeringsspecifikationerne og lokationsvejledningerne som forklaret i følgende under afsnit. Opsætningen af allokering af flytteordrer minder om opsætningen af allokering af salgsordrer, men feltet **Behovstype** er angivet til *Flytteordrer* i stedet for *Salgsordre*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Oprette en overskrift til en allokeringsskabelon for salgsordre

1. Angiv følgende værdier i overskriften for skabelonen:

    - **Allokeringsskabelon:** _61_
    - **Beskrivelse:** _61_
    - **Efterspørgselstype:** *Salgsordre*

        > [!NOTE]
        > I øjeblikket er *Salgsordrer* og *Flytteordrer* de eneste efterspørgselstyper, der understøttes. Du kan kun vælge *Flytteordrer*, hvis funktionen *Lagerstedsallokering for flytteordrer* er slået til.

    - **Efterspørgselsstrategi:** _Bestilt_

        Følgende værdier er tilgængelige i dette felt:

        - **Bestilt** – det fuldt bestilte antal på salgsordren skal betragtes som efterspørgsel.
        - **Reserveret** – det er kun de salgsordrelinjemængder, der er reserveret (fysisk og bestilt), som skal betragtes som efterspørgsel.
        - **Frigivet** – Det frigivne antal skal betragtes som efterspørgsel.

    - **Lagersted:** _61_
    - **Tillad bølgeefterspørgsel at bruge ikke-reserverede antal:** _Ja_

Du kan også angive en forespørgsel for at indsnævre omfanget af den efterspørgsel, der evalueres.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Konfigurere allokeringsspecifikationer for hver skabelon

For hver slagsordreskabelon, du opretter, skal du udføre disse trin for at tilføje en linje for hver allokeringsspecifikation.

1. Gå til oversigtspanelet **Detaljer om allokeringsskabelon**, og vælg **Ny** for at oprette en skabelonlinje.
1. Angiv følgende værdier på den nye linje:

    - **Sekvens:** _1_
    - **Beskrivelse:** _Fast lokation_
    - **Minimummængde:** _1_

        Dette felt definerer det mindste efterspørgselsantal, der kræves til linjen.

    - **Maksimummængde:** _1000000_

        Dette felt definerer det maksimale efterspørgselsantal, der er gyldig til linjen.

    - **Enhed:** Lad feltet være tomt.

        Dette felt definerer den måleenhed, som minimum- og maksimumantallet refererer til.

    - **Måleenhedsniveau:** _EaBoxPl_

        Dette felt definerer måleenheden for efterspørgsel, der er gyldig til linjen. (Få flere oplysninger i afsnittet i [Oprette måleenhedsniveauer for allokering](#unit-tiers) tidligere i denne artikel.)

    - **Tildel allokeringskriterier:** _Overvej antal_

        Følgende værdier er tilgængelige i dette felt:

        - **Antag tom** – dette system skal antage, at alle lokationer i plukområdet er tomme, og det skal ikke kontrollere disse lokationer med hensyn til lager.
        - **Overvej antal** – systemet skal kontrollere lokationerne i plukområdet for lager og skal springe lokationer over, der ikke er tomme.
        - **Overvej beholdningen** – Systemet skal kontrollere, om en bestemt lokation indeholder ikke-reserverede antal for varen på behovslinjen. Hvis antallet er stort nok til at opfylde mindst én enhed af behovslinjen, reduceres den genererede allokeringsplan med det disponible antal. Hvis behovet f.eks. er 10 kasser, og én kasse er disponibel, vil det fundne behov være ni kasser. Hvis behovet er 10 kasser, og én af hver er disponibel, vil det fundne behov være ti kasser. Denne værdi er kun tilgængelig, når funktionen *Forbedringer af fordeling af lagerstedsallokering* er slået til.

    - **Vejledningskode:** _Allokering_

        Dette felt definerer lokationsvejledningen, der bruges til at finde pluklokationen for genopfyldningsarbejdet.

    - **Overløbslokation:** Lad feltet være tomt.

        I dette felt defineres den lokation, som det lager, hvortil der lægges på lager, hvis der ikke kan findes en lokation for antallet, da linjen blev behandlet.

    - **Tillad brug:** _Ja_

        Når denne indstilling er angivet til *Ja*, og hvis det ikke muligt allokere noget efterspørgsel, vil der blive oprettet bevægelsesarbejde for at fjerne lager fra lokationer, hvor der er lager, men hvor der ikke er sket nogen allokering. Skabelonen køres derefter igen. Denne gang ignoreres lageret på lokationerne. Denne funktion fungerer bedst, når feltet **Tildel allokeringskriterier** er indstillet til at _Overvej antal_.

    - **Brug af fast lokation:** _Kun faste lokationer til produktet_

        Følgende værdier er tilgængelige i dette felt:

        - **Faste og ikke-faste lokationer** – systemet skal ikke være begrænset til kun at bruge faste lokationer.
        - **Kun faste lokationer til produktet** – systemet skal kun allokere til lokationer, der er faste lokationer for produktet.
        - **Kun faste lokationer til produktvarianten** – systemet skal kun allokere til lokationer, der er faste lokationer for produktvarianten.

> [!NOTE]
> Hvis allokeringsskabelonen indeholder mindst én linje, hvor feltet **Tildel allokeringskriterier** er angivet til *Overvej beholdning*, er afvigelser fra krav ikke længere tilladt for nogen af linjerne i skabelonen.

1. Vælg **Gem**.
1. Vælg **Ny** for at oprette en linje for anden skabelonlinje.
1. Angiv følgende værdier på den nye linje:

    - **Sekvens:** _2_
    - **Beskrivelse:** _Andet_
    - **Minimumantal:** _1_
    - **Maksimumantal:** _1000000_
    - **Enhed:** Lad feltet være tomt.
    - **Måleenhedsniveau:** _EaBoxPl_
    - **Tildel allokeringskriterier:** _Overvej antal_
    - **Vejledningskode:** _Allokering_
    - **Overløbslokation:** Lad feltet være tomt.
    - **Tillad brug:** _Ja_
    - **Brug faste lokationer:** _Faste og ikke-faste lokationer_

    I forespørgslen til den anden linje skal du nu angive de kriterier, der bruges til at bestemme, hvilke lokationer efterspørgslen for den linje kan allokeres til.

1. Vælg den linje, hvor feltet **Rækkefølge** er angivet til *2*.
1. Vælg **Rediger forespørgsel**.
1. Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Lokationer*
    - **Afledt tabel:** *Lokationer*
    - **Felt:** *Lokationsprofil-id*
    - **Kriterier:** *Pluk-06* (Vælg det dobbelte plustegn \[**++**\] i feltet for at udvide listen og vælg derefter *Pluk-06* - *Pluklokation 6*.)

1. Vælg **OK**.

#### <a name="set-up-location-directives"></a>Konfigurer lokationsvejledninger

Der skal oprettes mindst én lokationsvejledning, der understøtter allokeringspluk. Brug procedurerne i dette afsnit til at oprette en ny *lokationsvejledning for genopfyldning* til allokeringspluk.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I den venstre rude skal du i feltet **Arbejdsordretype** vælge *Genopfyldning*.
1. Gå til handlingsruden, og vælg **Ny**.
1. I overskriften for den nye lokationsvejledning skal du i feltet **Navn** angive *61 Allokeringspluk*.
1. Feltet **Løbenummer** accepterer standardværdien.

##### <a name="configure-the-location-directives-fasttab"></a>Konfigurere oversigtspanelet Lokationsvejledninger

1. I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier. Accepter standardværdierne for alle andre felter.

    - **Arbejdstype:** _Pluk_
    - **Lokation:** _6_
    - **Lagersted:** _61_
    - **Vejledningskode:** _Allokering_

1. Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.

##### <a name="configure-the-lines-fasttab"></a>Konfigurere oversigtspanelet Linjer

1. I oversigtspanelet **Linjer** skal du vælge **Ny** for at oprette en linje.
1. Angiv følgende værdier på den nye linje.

    - **Fra antal:** _0_
    - **Til antal:** _1000000_

1. Acceptér standardværdierne for alle de andre felter.
1. Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Konfigurere oversigtspanelet Handlinger i lokationsvejledninger

1. Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at oprette en linje.
1. Angiv følgende værdier på den nye linje. Accepter standardværdierne for alle andre felter.

    - **Løbenummer:** Accepter standardværdien.
    - **Navn:** _Masse_
    - **Strategi:** _Ingen_

1. Acceptér standardværdierne for alle de andre felter.
1. Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig.

##### <a name="edit-the-query"></a>Rediger forespørgslen

1. Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.
1. Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Tabel:** *Lokationer*
    - **Afledt tabel:** *Lokationer*
    - **Felt:** *Zone-id*
    - **Kriterier:** *Masse* (Vælg det dobbelte plustegn \[**++**\] i feltet for at udvide listen og vælg derefter *Masse*.)

1. Vælg **OK**.

## <a name="scenario"></a>Scenario

### <a name="set-up-the-scenario"></a>Konfigurere scenariet

I dette scenarie skal du bruge de indbyggede eksempeldata og oprette de poster, der er beskrevet i dette afsnit.

#### <a name="use-the-usmf-sample-data"></a>Brug af USMF-eksempeldata

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

#### <a name="create-demand"></a>Oprette efterspørgsel

Udfør følgende trin for at oprette den efterspørgsel, du vil anvende allokering på.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Gå til dialogboksen **Opret salgsordre**, og vælg **US-007** i feltet _Debitorkonto_.
1. Vælg _61_ i feltet **Lagersted**.
1. Vælg **OK**.
1. Den nye indkøbsordre åbnes. Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Vare:** _L0101_
    - **Antal:** _20_

1. Vælg **Tilføj linje** for at tilføje en ny linje, og angiv følgende værdier:

    - **Vare:** _T0100_
    - **Antal:** _8_

1. Vælg **Gem**.
1. Vælg **Ny** for at oprette en anden salgsordre.
1. Gå til dialogboksen **Opret salgsordre**, og vælg **US-008** i feltet _Debitorkonto_.
1. Vælg _61_ i feltet **Lagersted**.
1. Den nye indkøbsordre åbnes. Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Vare:** _T0100_
    - **Antal:** _1_

1. Vælg **Gem**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Gennemgå et typisk allokeringsscenarie

Når alle de nødvendige elementer er på plads, som beskrevet i forrige afsnit, er du klar til at afprøve funktionen ved at gå gennem hver enkelt øvelse i dette afsnit.

#### <a name="generate-demand"></a>Generér behov

1. Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Allokeringsskabeloner**, og vælg den allokeringsskabelon, du oprettede tidligere.
1. Vælg **Opret efterspørgsel** i handlingsruden. Denne kommando evaluerer al efterspørgsel, der findes i systemet, og som svarer til allokeringsskabelonforespørgslen. Den samlede efterspørgsel i alle ordrer konsolideres derefter til én linje pr. antal/måleenhed. Der vises en orienterende meddelelse, når processen er fuldført.

#### <a name="slotting-demand"></a>Allokeringsbehov

*Allokeringsefterspørgslen* viser resultater af efterspørgselsoprettelsen baseret på konfigurationen af allokeringsskabelonen.

- Vælg **Allokeringsefterspørgsel** i handlingsruden for at få vist resultaterne fra kommandoen **Opret efterspørgsel**. Linjerne i allokeringsbehovet kan redigeres. Du kan slette en linje, tilføje en ny linje eller redigere linjedetaljerne.

> [!NOTE]
> Du kan redigere efterspørgslen manuelt, eller du kan importere den fra et eksternt system ved hjælp af datastyring. Uanset hvad der er i allokeringsefterspørgslen bruges det i næste trin, uanset hvor den kommer fra.

#### <a name="locate-demand"></a>Find behov

Når efterspørgslen er oprettet, skal du bruge kommandoen **Find efterspørgsel** til at oprette *allokeringsplanen*.

- Vælg **Find efterspørgsel** i handlingsruden. Allokeringsprocessen kører. Der vises en orienterende meddelelse, når processen er fuldført.

#### <a name="slotting-plan"></a>Allokeringsplan

Allokeringsplan viser den lokation, som hver vare/hvert antal er tildelt til, om der er brugt overløb, om at der er oprettet et arbejde, og hvilken skabelonlinje der blev brugt. *Alle efterspørgsler, der ikke kunne allokeres, fremhæves med rødt.*

- I handlingsruden skal du vælge **Allokeringsplan** for at få vist resultaterne.

> [!NOTE]
> - Processerne **Generér efterspørgsel**, **Find behov** og **Kør genopfyldning** kører nu i en sandkasse. (Disse processer er tilgængelige i handlingsruden på siden **Allokeringsskabeloner**).
> - Processerne **Generér behov**, **Find behov** og **Kør genopfyldning** har en lås for at sikre, at de ikke kan udløses samtidig. Ellers kunne de data, der bruges, blive slettet.
> - Processerne **Generér behov** og **Find behov** viser en advarsel, hvis kørslen ikke genererede poster, eller hvis posterne mangler oplysninger.
> - Når du vælger **Allokeringsplan**, har siden ikke knappen **Ny**, **Rediger** eller **Slet** i handlingsruden, fordi datakilden ikke kan redigeres.
> - Når du vælger **Kør genopfyldning**, validerer systemet de valgte allokeringsskabeloner og processer.

#### <a name="create-replenishment"></a>Oprette genopfyldning

Når allokeringsplanen er blevet oprettet, skal du oprette et *genopfyldningsarbejde* baseret på planen.

- Vælg **Kør genopfyldning** i handlingsruden. Der vises en orienterende meddelelse, når processen er fuldført. Denne meddelelse angiver det antal overskrifter, der er oprettet for arbejdsopbygnings-id'et.

Lokationsvejledninger, der bruges, identificeres ud fra den vejledningskode, der er angivet på hver skabelonlinje.

## <a name="tips"></a>Tip!

### <a name="set-up-automatic-slotting"></a>Konfigurere automatisk allokering

Når alle de påkrævede elementer er på plads, kan du konfigurere, at allokerings skal køre automatisk, ved at følge disse trin.

1. Gå til **Lokationsstyring \> Genopfyldning \> Kør allokering**.
1. Angiv de allokeringstrin, der skal køres. Markér ét eller flere af følgende allokeringstrin:

    - Generér behov
    - Find behov
    - Opret genopfyldningsarbejde

    > [!NOTE]
    > Allokeringstrinnene er progressive. Hvis du vil vælge *Find efterspørgsel*, skal du først vælge *Opret efterspørgsel*.

1. Angiv den allokeringsskabelon, der skal bruges.
1. Angiv, at gentagelsen skal køres automatisk, hvis du vil.

Med hensyn til øvelserne i scenariet skal du **ikke** konfigurere automatisk allokering.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]