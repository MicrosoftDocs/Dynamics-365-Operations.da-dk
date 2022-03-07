---
title: Årsagskoder for lageroptælling
description: Dette emne beskriver, hvordan du konfigurerer og anvender årsagskoder til optællingsopgaver.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4c178ddf342b13a0ef8fee8b8b958554a9a31069
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500584"
---
# <a name="reason-codes-for-inventory-counting"></a>Årsagskoder for lageroptælling

[!include [banner](../includes/banner.md)]

Med årsagskoder kan du analysere resultaterne af en optællingsproces og eventuelle uoverensstemmelser, der opstår under denne proces. Du kan angive årsagen til optællingen, f.eks. en ødelagt palle eller en regulering af lageret, der er baseret på lagerprøver. Du kan samtidig bruge reguleringsfunktionen til at bogføre værdien af reguleringer af lagerbeholdningen på den relevante modkonto på baggrund af årsagen til hver enkelt lagerregulering.

## <a name="recommendation"></a>Anbefaling

Før du konfigurerer systemet, anbefales det, at du definerer en strategi for at arbejde med årsagskoder. Prøv f.eks. at besvare følgende spørgsmål:

- Skal årsagskoder være obligatoriske på lagersteder?
- Årsagskoder skal være obligatoriske eller valgfrie for bestemte varer?
- Hvor mange årsagskoder skal du bruge?
- Skal du vælge en begrænset liste over årsagskoder for reguleringer på forhånd?
- Hvordan skal brugere af stregkodescannere bruge årsagskoder? Skal årsagskoderne være forvalgte, obligatoriske eller ikke kunne redigeres?
- Kræver lagermedarbejdere andre funktionsmåder for årsagskoder på mobile scannere? Hvis svaret er Ja, kan du oprette flere menupunkter og tildele dem til forskellige personer.
- Skal årsagskoderne skabe økonomisk modkontobogføring?

## <a name="turn-on-reason-code-features-in-your-system"></a>Aktivere årsagskodefunktioner i systemet

Hvis du ikke kan se alle de funktioner, der er beskrevet i dette emne, i dit system, er du sandsynligvis nødt til at aktivere funktionen *Bogfør reguleringer af disponible mængder ved hjælp af konfigurerbare årsagskoder, der er tilknyttet modkonti*. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Bogfør reguleringer af disponible mængder ved hjælp af konfigurerbare årsagskoder, der er tilknyttet modkonti*

## <a name="set-up-reason-codes"></a>Definer årsagskoder

### <a name="set-up-reason-code-policies"></a>Konfigurere politikker for årsagskoder

Du kan oprette flere politikker for årsagskoder for at styre, hvornår og hvordan optælling af årsagskoder anvendes. Hver årsagskodepolitik kan have en af to typer optællingsårsagskoder (*Valgfri* eller *Obligatorisk*). Politikker for optællingsårsagskoder kan bruges på lagerstedsniveau eller vareniveau.

Hvis du vil oprette en årsagskodepolitik, skal du følge disse trin.

1. Gå til **Lagerstyring** \> **Konfiguration** \> **Lager** \> **Politikker for optællingsårsagskode**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en politik til gitteret.
1. Angiv feltet **Navn** for den nye politik.
1. I feltet **Type af optællingsårsagskode** skal du vælge enten *Obligatorisk* eller *Valgfrit* for at angive, om valget af en årsagskode skal være en valgfri eller obligatorisk handling i en af følgende lagerreguleringsprocesser:

    - Cyklusoptælling (mobilenhed)
    - Spotoptælling (mobilenhed)
    - Grænseoptælling (mobilenhed)
    - Regulering ind (mobilenhed)
    - Regulering ud (mobilenhed)
    - Optællingskladde (Rich Client)
    - Antalsjregulering/Onlineoptælling (Rich Client)

Du kan konfigurere politikker for årsagskoder til individuelle lagersteder og produkter. Årsagskodeopsætningen for et produkt kan tilsidesætte opsætningen af produktets lagersted.

> [!NOTE]
> For lagersteder og varer, hvor feltet **Politik for optællingsårsagskode** er angivet til *Obligatorisk* , kan optællingskladden ikke fuldføres og lukkes, før en årsagskode er angivet. Der er flere oplysninger i næste afsnit.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Tildele politikker for optællingsårsagskode til lagersteder

Hvis du vil tildele en politik for optællingsårsagskode til et lagersted, skal du følge disse trin.

1. Gå til **Lagerstyring** \> **Konfiguration** \> **Lageropdeling** \> **Lagersteder**.
1. Vælg et lagersted i listeruden.
1. I handlingsruden skal du under fanen **Lagersted** i gruppen **Konfiguration** vælge **Politik for optællingsårsagskode**. Følg derefter et af disse trin i dialogboksen **Tildel politik for optællingsårsagskode**:

    - Hvis du vil bruge politikopsætningen for den enkelte vare til at bestemme, om optællingskladder er obligatoriske for den, skal du ikke angive en værdi (eller slette den eksisterende værdi).
    - Hvis du vil kræve en årsagskode for optællingskladder for lagerstedet, skal du vælge en årsagspolitik, hvor feltet **Type af optællingsårsagskode** er angivet til *Obligatorisk*.
    - Hvis en årsagskode er valgfri for optællingskladder for lagerstedet, skal du vælge en årsagspolitik, hvor feltet **Type af optællingsårsagskode** er angivet til *Valgfri*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Tildele politikker for optællingsårsagskode til produkter

Hvis du vil tildele en politik for optællingsårsagskode til et produkt, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.
1. Vælg et produkt i gitteret.
1. I handlingsruden skal du under fanen **Produkt** i gruppen **Konfiguration** vælge **Politik for optællingsårsagskode**. Følg derefter et af disse trin i dialogboksen **Tildel politik for optællingsårsagskode**:

    - Hvis du vil bruge politikopsætningen for lagerstedet til at bestemme, om optællingskladder er obligatoriske for produktet, skal du ikke angive en værdi (eller slette den eksisterende værdi).
    - Hvis du vil kræve en årsagskode for optællingskladder for produktet, skal du vælge en årsagspolitik, hvor feltet **Type af optællingsårsagskode** er angivet til *Obligatorisk*. Denne indstilling tilsidesætter enhver indstilling for årsagskoder på lagerstedsniveau.
    - Hvis en årsagskode er valgfri for optællingskladder for produktet, skal du vælge en årsagspolitik, hvor feltet **Type af optællingsårsagskode** er angivet til *Valgfri*. Denne indstilling tilsidesætter enhver indstilling for årsagskoder på lagerstedsniveau.

### <a name="set-up-counting-reason-codes"></a>Konfigurere årsagskoder for optælling

Benyt følgende fremgangsmåde for at konfigurere dine optællingsårsagskoder.

1. Gå til **Lagerstyring** \> **Konfiguration** \> **Lager** \> **Optællingsårsagskoder**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.
1. Angiv og felterne **Optællingsårsagskode** og **Beskrivelse** for den nye række.
1. Hvis du vil tildele en modkonto, skal du angive eller vælge en værdi i feltet **Modkonto**.

    > [!NOTE]
    > Hvis en modkonto tildeles en årsagskode til optællingen, og du bogfører en optællingskladde med denne optællingsårsagskode, bogføres værdien mod den tildelte modkonto i stedet for standardkontoen til lagerposteringsprofilen.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Konfigurere årsagskodegrupper for optælling

*Optællingsårsagskodegrupper* kan bruges som en del af menupunkterne *Regulering ind* og *Regulering ud* i mobilappen Warehouse Management til at grænse listen over optællingsårsagskoder. (Du kan finde flere oplysninger om optællingsårsagskodegrupper i [Konfigurere menupunkter i mobilenhed for Regulering ind og Regulering ud](#setup-adjustment-in-out) senere i dette emne).

1. Gå til **Lagerstyring** \> **Konfiguration** \> **Lager** \> **Grupper for optællingsårsagskode**.
1. Vælg **Ny** i handlingsruden for at tilføje en gruppe.
1. Angiv felterne **Optællingsårsagsgruppe** og **Gruppebeskrivelse** for den nye gruppe.
1. Vælg **Gem** i handlingsruden.
1. Vælg **Ny** på værktøjslinjen i sektionen **Detaljer** for at føje en række til gitteret. Angiv feltet **Optællingsårsagskode** for den nye række. 
1. Gentag det forrige trin for at tildele flere koder efter behov. Hvis du skal fjerne en kode fra gruppen, skal du markere den og derefter vælge **Slet** på værktøjslinjen.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Konfigurere årsagskoder for mobilenheders menupunkter

Du kan konfigurere årsagskoder for følgende typer tilgængelige reguleringer:

- Cyklusoptælling
- Spotoptælling
- Grænseoptælling
- Regulering ind
- Regulering ud

I de fleste tilfælde kan du definere følgende oplysninger for hvert relevant menupunkt for en mobilenhed:

- Om årsagskoden vises for mobilenhedens arbejder under optælling.
- Den standardårsagskode, der vises i en mobilenheds menupunkt.
- Om brugeren kan redigere årsagskoden.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Konfigurere menupunkter for mobilenheders optællingsproces

Du kan konfigurere et menupunkt for en optællingsproces på en mobilenhed ved at følge nedenstående trin.

1. Gå til **Lagerstedsstyring** \> **Konfiguration** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.
1. Vælg det relevante menupunkt i listeruden, eller opret et nyt menupunkt.
1. Vælg **Cyklusoptælling** i handlingsruden.
1. I feltet **Standardkode for optællingsårsag** skal du angive den standardårsagskode, der skal registreres, når optællingen udføres ved hjælp af mobilenhedens menupunkt.
1. Vælg en af følgende værdier i feltet **Vis optællingsårsagskode**:

    - *Linje* – Vis årsagskoden, når hver afvigelse er registreret.
    - *Skjul* – Vis ikke årsagskoden.

1. Angiv **Rediger optællingsårsagskode** til *Ja*, så arbejderen kan redigere årsagskoden, når den vises på mobileenheden under optælling. Angiv det til *Nej* for at forhindre arbejderen i at redigere koden.

> [!NOTE]
> Knappen **Cyklusoptælling** kan aktiveres i menupunktet på enhver mobilenhed, hvor optælling kan udføres. Eksempler omfatter menupunkter for spotoptællinger, brugerstyret arbejde og systemstyret arbejde.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Konfigurere mobilenhedens menupunkter for Regulering ind og Regulering ud

Du kan konfigurere et menupunkt for Regulering ind eller Regulering ud på en mobilenhed ved at følge nedenstående trin.

1. Gå til **Lagerstedsstyring** \> **Konfiguration** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.
1. Vælg **Ny** i handlingsruden for at oprette et menupunkt.
1. Angiv felterne **Mobilpunktnavn** og **Titel** til det nye menupunkt.
1. Indstil feltet **Tilstand** til *Arbejde*.
1. Angiv indstillingen **Brug eksisterende arbejde** til *Nej*.
1. I feltet **Arbejdsoprettelsesproces** skal du vælge *Regulering ind* eller *Regulering ud*.
1. I oversigtspanelet **Generelt** skal du indstille følgende felter. (Alle disse felter tilføjes, når du vælger *Regulering ind* eller *Regulering ud* i feltet **Arbejdsoprettelsesproces**).

    - **Brug procesvejledning** – Hvis du skal oprette en *Regulering ud*-proces, skal du sørge for at angive denne indstilling til *Ja*. Hvis du opretter en *Regulering ud*-proces, er denne indstilling altid angivet til *Ja*.
    - **Standardkode for optællingsårsag** – Angiv den standardårsagskode, der skal registreres, når optællingen udføres ved hjælp af mobilenhedens menupunkt.
    - **Vis optællingsårsagskode** – Vælg en af følgende værdier:

        - *Linje* – Vis årsagskoden, når hver afvigelse er registreret.
        - *Skjul* – Vis ikke årsagskoden.

    - **Rediger optællingsårsagskode** – Angiv den til *Ja*, så arbejderen kan redigere årsagskoden, når den vises på mobileenheden under optælling. Angiv det til *Nej* for at forhindre arbejderen i at redigere koden.
    - **Optællingsårsagskodegruppe** – Vælg en årsagskodegruppe, hvis du vil begrænse listen over indstillinger, som arbejdere kan se. Du kan finde flere oplysninger om opsætning af årsagskodegrupper i afsnittet [Konfigurere årsagskodegrupper for optælling](#reason-groups) tidligere i dette emne. 

> [!NOTE]
> Når du tildeler en optællingsårsagskodegruppe til menupunkterne *Regulering ind* og *Regulering ud*, hvor indstillingen **Brug procesvejledning** er angivet til *Ja*, kan du få en begrænset liste over optællingsårsagskoder som en del af behandlingen i mobilappen Warehouse Management.
>
> Indstillingen **Brug procesvejledning** kan også hjælpe dig med at forhindre, at der sker store reguleringsantal ved en fejl. (En arbejder kan f.eks. ved en fejl scanne en stregkode på et varenummer i stedet for en antalsværdi). Du kan konfigurere denne funktion ved at indstille **Brug procesvejledning** til *Ja* for hvert af de relevante menupunkter. Gå derefter til **Lagerstedsstyring \> Konfiguration \> Arbejder**, og angiv feltet **Grænse for reguleringsantal** for hver relevant lagerarbejder for at angive det maksimale reguleringsantal, som arbejderen kan registrere.

## <a name="processing-that-uses-counting-reason-codes"></a>Behandling, der bruger optællingsårsagskoder

Når arbejdere bruger mobilappen Warehouse Management, registreres årsagskoder. Medmindre der er defineret en proces til godkendelse af optælling, bruges de registrerede årsagskoder med det samme som en del af den efterfølgende optællingskladdebogføring.

### <a name="cycle-count-approvals"></a>Godkendelse af cyklusoptælling

Før antallet godkendes, kan arbejderen ændre den årsagskode, der er tilknyttet optællingen. Når optællingen er godkendt, angives årsagskoden i optællingskladdens linjer.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Redigere årsagskoder for godkendelser af cyklusoptælling

Hvis du vil redigere en godkendelse af cyklusoptælling, skal du gøre følgende.

1. Gå til **Lagerstedsstyring** \> **Cyklusoptælling** \> **Ventende gennemsyn af cyklusoptællingsarbejde**.
1. Vælg en cyklusoptælling i gitteret.
1. I handlingsruden skal du gå til fanen **Arbejde** og vælge **Cyklusoptælling**. Vælg en ny årsagskode i feltet **Årsagskode**.

Årsagskoder føjes til kladdelinjerne i optællingskladder af typen *Optællingskladde*.

1. Gå til **Lagerstyring** \> **Kladdeposteringer** \> **Vareoptælling** \> **Optælling**.
2. Vælg den årsagskode, der passer til din aktuelle situation, i feltet **Optællingsårsagskode** i linjedetaljerne for optællingskladden.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Se de registrerede årsagskoder i optællingshistorikken

Hvis du vil se de årsagskoder, der er registreret i optællingshistorikken, skal du følge disse trin.

1. Gå til **Lagerstyring** \> **Forespørgsler og rapporter** \> **Optællingshistorik**.
1. Vælg en vareoptællingspost i listeruden.
1. I feltet **Optællingsårsagenskode** kan du se den optællingshistorik, der er registreret via en årsagskode.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Bruge årsagskoder til antalsregulering eller onlineoptælling

Hvis du vil bruge en årsagskode til en regulering af antal eller onlineoptælling, skal du følge disse trin.

1. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.
1. Vælg **Justering af antal** i handlingsruden.
1. Vælg **Justering af antal**, og vælg derefter en årsagskode i feltet **Optællingsårsagskode**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
