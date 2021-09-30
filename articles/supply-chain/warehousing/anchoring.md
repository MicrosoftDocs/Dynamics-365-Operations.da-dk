---
title: Forankring
description: Dette emne indeholder en forklaring på, hvordan forankring aktiveres og bruges.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505556"
---
# <a name="anchoring"></a>Forankring

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om forankringsprocessen. Det beskriver den nødvendige konfiguration og den logik, der køres, når en arbejder på lagerstedet ændrer enten den midlertidige lokation eller lastlokaliteten.

Forankringsfunktionen giver dig mulighed for at tilsidesætte den midlertidige lokation eller lastlokationen. Alle åbne anbringelser dirigeres derefter til den nye midlertidige lokation eller lastlokation, som du angiver.

Denne funktion kan hjælpe arbejdere med at blive mere effektive, når de afsender varer. Her er nogle eksempler:

- En arbejder, der skal lægge varer på lager for ordre nr. 1 på en midlertidig lokation ved dock 1, kan ikke gøre det, fordi en tidligere last ikke er fjernet fra lokationen. I stedet for at vente på, at den midlertidige lokation dock 1 bliver ledig, kan arbejderen beslutte at bruge den midlertidige lokation for dock 2. Derfor tilsidesætter arbejderen den foreslåede midlertidige lokation. Lokationen for anbringelser af alle resterende varer til arbejdet opdateres til den midlertidige lokation dock 2.
- En arbejder, der skal udføre flere pluk for samme levering, kan være sikker på, at alle varer til anbringelse er samlet på ét sted. Derfor kræves der mindre tid til at læsse varerne på lastbilen.

Du kan konfigurere forankring til menupunkterne i mobilenheden ved hjælp af indstillingen **Anker**. Hvis du angiver denne indstilling til *Ja*, kan du bruge feltet **Foretag forankring efter** til at angive, om du vil forankre efter forsendelse eller last. Hvis feltet **Foretag forankring efter** angives til *Forsendelse*, ændres de efterfølgende åbne anbringelser til den nye lokation for den pågældende forsendelse. Hvis du angiver det til *Last*, ændres de efterfølgende åbne anbringelser til den nye lokation for den pågældende last.

> [!IMPORTANT]
> Lokationen for efterfølgende åbne anbringelser ændres kun på de arbejdslinjer, der genereres fra samme arbejdsskabelonlinje. Det vil sige, at systemet forankrer de anbringelseslinjer, som kommer fra samme arbejdsskabelonlinje.

Dette emne indeholder et scenario, der viser, hvordan forankring fungerer. I løbet af scenariet opretter du et sæt af salgsordrer og frigiver dem til lagerstedet. Du skal derefter tilsidesætte den foreslåede midlertidige lokation og kontrollere, at alt resterende læg på-arbejde dirigeres til den nye lokation.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Forudsætninger for scenario: Gøre demodata tilgængelige

Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til *USMF*, før du går i gang.

## <a name="scenario-setup"></a>Konfigurere scenarie

Før du gennemgår eksempelscenariet, skal du aktivere forankring for det relevante menupunkt til mobilenhed.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Konfigurere et menupunkt for mobilenheden til aktivering af forankring

Benyt følgende fremgangsmåde for at aktivere forankring for et menupunkt til en mobilenhed.

1. Gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg den post, der hedder *Salgspluk*, i listeruden. Hvis der ikke findes en eksisterende post med dette navn, skal du oprette den. Bekræft eller angiv følgende værdier for posten:

    - **Menupunktnavn:** *Salgspluk*
    - **Titel:** *Salgspluk*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*
    - **Styret af:** *Brugerstyret*
    - **Forankring:** *Ja*

        Denne indstilling bevirker, at systemet forankrer flere arbejdsordrelinjer sammen under salgspluk.

    - **Foretag forankring efter:** *Last*

        Denne indstilling bevirker, at systemet forankrer efter last.

    - **Tilsidesæt mål-id:** *Ja*
    - **Tilsidesæt nummerplade under læg på lager:** *Ja*
    - **Hold arbejde låst af bruger:** *Ja*
    - **Tillad overpluk:** *Ja*

### <a name="set-up-a-work-template-to-enable-staging"></a>Konfigurere en arbejdsskabelon for at aktivere midlertidig lagring

Benyt følgende fremgangsmåde for at konfigurere en arbejdsskabelon for at aktivere midlertidig lagring. Denne konfiguration understøtter scenariet, hvor en arbejder placerer varer for en ordre på en midlertidig lokation.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.
1. I gitteret skal du vælge arbejdsskabelonen **61 Salgsordrestadie**.
1. I afsnittet **Arbejdsskabelondetaljer** skal du kontrollere, at følgende linjer findes og er konfigureret som vist her:

    - Linje 1:

        - **Arbejdstype:** *Pluk*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Arbejdsklasse-id:** *Salgsordrepluk*

    - Linje 2:

        - **Arbejdstype:** *Læg på lager*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Vejledningskode:** *Stadie*
        - **Arbejdsklasse-id:** *Salgsordrepluk*

    - Linje 3:

        - **Arbejdstype:** *Pluk*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Stop arbejde:** *Ja*
        - **Arbejdsklasse-id:** *Salgsordrelast*

    - Linje 4:

        - **Arbejdstype:** *Læg på lager*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Vejledningskode:** *Baydoor*
        - **Arbejdsklasse-id:** *Salgsordrelast*

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at åbne forespørgselseditoren.
1. Kontrollér, at følgende linje er konfigureret under fanen **Område**:

    - **Tabel:** *Midlertidige arbejdstransaktioner*
    - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
    - **Felt:** *Lagersted*
    - **Afgrænsning:** *61*

1. Kontrollér, at følgende linje er konfigureret under fanen **Sortering**:

    - **Tabel:** *Midlertidige arbejdstransaktioner*
    - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
    - **Felt:** *Forsendelses-id*
    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at anvende dine indstillinger og lukke forespørgselseditoren. Acceptér ændringerne, hvis du bliver bedt om det.
1. Vælg **Opgaveoverskriften skifter** i handlingsruden.
1. På den linje, hvor feltet **Feltnavn** er angivet til *Forsendelses-id*, skal afkrydsningsfeltet **Gruppér efter dette felt** være markeret.

### <a name="set-up-license-plates-locations-and-inventory"></a>Oprette id-numre, lokationer og lager

Før du kan oprette salgsordrer og forsendelser, skal du sikre dig, at de nødvendige lokationer, id-numre og lager findes.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Id-numre**, og opret to id-numre:

    - MyLP1
    - MyLP2

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**, og opret følgende placeringer, hvis de ikke allerede findes.

    | Lagersted | Lokation   | Id for lokationsprofil | Zone-id   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | FLOOR     |
    | 61        | 06A01R3S1B | PICK-06             | FLOOR     |
    | 61        | STAGE01    | STAGE               | *(Tom)* |
    | 61        | STAGE02    | STAGE               | *(Tom)* |
    | 61        | STAGE03    | STAGE               | *(Tom)* |
    | 61        | STAGE04    | STAGE               | *(Tom)* |

1. Kontrollér, at følgende lager er tilgængeligt. Hvis du skal justere lagerbeholdning, kan du oprette manuelle bevægelser, bruge genopfyldning eller anvende en anden proces.

    | varenummer | Mængde | Lagersted | Lokation   | Nummerplade |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Oprette efterspørgsel

Før du kan prøve forankringsfunktionaliteten, skal du oprette et behov. I dette scenario opretter du tre salgsordrer til samme kunde.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette den første salgsordre.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *61*

1. Vælg **OK**.
1. Den nye indkøbsordre åbnes. Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier for denne linje:

    - **Varenummer:** *A0001*
    - **Antal:** *1*

1. Vælg **Tilføj linje** på værktøjslinjen for at tilføje en anden salgsordrelinje, og angiv følgende værdier for den:

    - **Varenummer:** *A0002*
    - **Antal:** *1*

1. Brug følgende fremgangsmåde for hver salgslinje på ordren for at reservere lager for den:

    1. I oversigtspanelet **Salgsordrelinjer** skal du vælge en salgsordrelinje.
    1. Vælg **Lager \> Reservation** på værktøjslinjen.
    1. På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.
    1. Vælg **Gem** i handlingsruden.

1. Gentag trin 2 til 6 for at oprette endnu en salgsordre. Angiv følgende værdier for den:

    - I dialogboksen **Opret salgsordre**:

        - **Debitorkonto:** *US-001*
        - **Lagersted:** *61*

    - På salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *2*

    - På salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *2*

1. Gentag trin 7 for at reservere hver linje på salgsordre 2.
1. Gentag trin 2 til 6 for at oprette en tredje salgsordre. Angiv følgende værdier for den:

    - I dialogboksen **Opret salgsordre**:

        - **Debitorkonto:** *US-001*
        - **Lagersted:** *61*

    - På salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *3*

    - På salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *3*

1. Gentag trin 7 for at reservere hver linje på salgsordre 3.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Brug panelet for lastplanlægning til at oprette en last og frigive den til lagerstedet

Udfør følgende trin for at oprette en last for de ordrer, du har oprettet i dette scenarie, og frigiv dem derefter til lagerstedet.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. Find og vælg alle salgsordrelinjer for salgsordre 1 og salgsordre 2 under fanen **Salgslinjer**.
1. I handlingsruden skal du under fanen **Udbud og efterspørgsel** i gruppen **Tilføj** vælge **Til ny last**.
1. I dialogboksen **Tildeling af lastskabelon** skal du i feltet **Lastskabelon-id** vælge en lastskabelon, f.eks. *Standardlastskabelon*.
1. Vælg **OK** for at lukke dialogboksen.
1. I sektionen **Laster** skal du vælge og finde den last, du har oprettet.
1. Vælg **Frigiv \> Frigiv til lagersted** på værktøjslinjen.
1. I dialogboksen **Frigiv last til lagersted** skal du vælge **OK** for at frigive den valgte last til lagerstedet.
1. Gå til **Lokationsstyring \> Arbejde \> Alt arbejde** for at få vist det oprettede arbejde. Du skal finde to nye arbejds-id'er, én for hver forsendelse. Der er pluk- og læg på lager-linjer i hvert enkelt arbejds-id, som overfører lagerbeholdningen fra plukpladserne til den midlertidige lokation og fra den midlertidige lokation til lagerporten. Notér værdien i **Arbejds-id** for den første forsendelse, da du får brug for det i næste procedure.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Salgsordrepluk til lokationen for midlertidig lagring af den første forsendelse

1. Log på mobilappen Warehouse Management som arbejder på lagersted *61*. (I standarddemodataene kan du logge på med bruger-id'et _61_ og adgangskoden _1_.)
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Salgspluk**.
1. Vælg feltet **Id**, og angiv derefter arbejds-id'et for den første forsendelse.
1. Bekræft indtastningen.
1. Angiv et id-nummer for den første vare (*MyLP1*) i feltet **LP**.
1. Bekræft indtastningen.
1. Angiv et vilkårligt tal i feltet **Mål-NP** (mål-id'et behøver ikke at findes på forhånd).

    Du skal plukke alle linjer, der er oprettet ud fra den behandlede bølge, til samme nummerplade.

1. Bekræft indtastningen.
1. Angiv et id-nummer for den anden vare (*MyLP2*) i feltet **LP**.
1. Bekræft indtastningen.

    Forestil dig, at arbejderen nu har indsamlet ordren, men når de kommer til den midlertidige lokation, der er angivet i arbejdet, finder de ud af, at pladsen allerede er optaget. Arbejderen kan dog se, at en anden lokation tæt på (*STAGE03*) er tilgængelig. De vil derfor anmode om at få ændret den midlertidige lokation. Da forankringsfunktionen er aktiveret, opdaterer systemet automatisk den midlertidige lokation for dette og alt relateret arbejde.

1. Vælg **Tilsidesæt lokation** for at tilsidesætte den foreslåede midlertidige lokation.
1. Angiv **Midlertidig lagring er ændret** i feltet *Arbejdsundtagelser*.
1. Angiv i feltet **Lokation** en ny midlertidig lagringslokation (*STAGE03*).
1. Bekræft indtastningen. Du modtager en meddelelse om, at "arbejde er fuldført".
1. Gå til **Lagerstedsstyring \> Arbejde \> Alt arbejde**.
1. Åbn arbejds-id'et for den første forsendelse. Kontrollér, at den midlertidige lokation blev opdateret til den nye lokation (*STAGE03*), der blev defineret ved hjælp af mobilenheden.
1. Åbn arbejds-id'et for den anden forsendelse. Kontrollér, at den midlertidige lokation er blevet opdateret til en ny midlertidig lokation (*STAGE03*) på grund af opsætningen af forankring.

> [!NOTE]
> Lokationen for alle de resterende åbne læg på lager-arbejdslinjer, der har samme midlertidige lokation, og som blev genereret fra samme arbejdsskabelonlinje, opdateres til den nye lokation.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Bruge lastplanlægningspanelet til at føje den nye salgsordre til den eksisterende last

Benyt følgende fremgangsmåde for at føje en ordre til lasten og derefter frigive den til lagerstedet.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. Find og vælg alle salgsordrelinjer for salgsordre 3 under fanen **Salgslinjer**.
1. I handlingsruden skal du under fanen **Udbud og efterspørgsel** vælge **Til eksisterende last** i gruppen **Tilføj** for at føje de valgte ordrelinjer til en eksisterende last.
1. Vælg **OK** for at lukke dialogboksen.
1. I sektionen **Laster** skal du finde og vælge lasten fra de forrige trin.
1. Vælg **Frigiv \> Frigiv til lagersted**.
1. I dialogboksen **Frigiv last til lagersted** skal du vælge **OK** for at frigive den valgte last til lagerstedet.
1. Gå til **Lokationsstyring \> Arbejde \> Alt arbejde** for at få vist det oprettede arbejde. Notér værdien i **Arbejds-id**, da du får brug for det i næste procedure.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Salgsordrepluk til lokationen for midlertidig lagring af den tredje forsendelse

1. Log på mobilappen som en arbejder på lagerstedet *61*.
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Salgspluk**.
1. Vælg feltet **Id**, og angiv derefter arbejds-id'et for den tredje forsendelse.
1. Bekræft indtastningen.
1. Angiv et id-nummer for den første vare (*MyLP1*) i feltet **LP**.
1. Bekræft indtastningen.
1. Angiv et vilkårligt tal i feltet **Mål-NP** (mål-id'et behøver ikke at findes på forhånd).
1. Bekræft indtastningen.
1. Angiv et id-nummer for den anden vare (*MyLP2*) i feltet **LP**.
1. Bekræft indtastningen.

    Hvad angår den første last, skal du forestille dig, at arbejderen opdager, at den angivne midlertidige lokation ikke er tilgængelig. Derfor skal der bruges en anden midlertidig lokation (*STAGE04*).

1. Vælg **Tilsidesæt lokation** for at tilsidesætte den foreslåede midlertidige lokation.
1. Angiv **Midlertidig lagring er ændret** i feltet *Arbejdsundtagelser*.
1. Angiv i feltet **Lokation** en ny midlertidig lagringslokation (*STAGE04*).
1. Bekræft indtastningen. Du modtager en meddelelse om, at "arbejde er fuldført".
1. Gå til **Lagerstedsstyring \> Arbejde \> Alt arbejde**.
1. Åbn arbejds-id'et for den første forsendelse. Kontrollér, at den midlertidige lokation ikke er opdateret til den nye midlertidige lokation (*STAGE04*), fordi den resterende åbne læg på lager-linje ikke svarer til arbejdsskabelonlinjen for den fuldførte læg på lager-linje.
1. Åbn arbejds-id'et for den anden forsendelse. Kontrollér, at den midlertidige lokation ikke er opdateret til den nye midlertidige lokation (*STAGE04*), fordi den midlertidige lokation ikke svarer til den midlertidige lokation for den fuldførte læg på lager-linje. Det vil sige, at den fuldførte arbejdslinje og den resterende åbne arbejdslinje har forskellige midlertidige lokationer, og i dette tilfælde er det kun linjer med samme midlertidige lokation, der opdateres.
1. Åbn arbejds-id'et for den tredje forsendelse. Kontrollér, at den midlertidige lokation er blevet opdateret til den nye midlertidig lokation (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
