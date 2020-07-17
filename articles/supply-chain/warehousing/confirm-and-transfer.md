---
title: Bekræft og flyt
description: Dette emne forklarer, hvordan du bruger funktionen Bekræft og overfør, så brugerne kan sende laster ud af lagerstedet, før de fuldfører alt det arbejde, der er knyttet til disse laster.
author: mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 488eed23972022f9437e62a462ae5f70d6833a67
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530552"
---
# <a name="confirm-and-transfer"></a>Bekræft og flyt

[!include [banner](../includes/banner.md)]

Funktionen *Bekræft og overfør* lader brugerne sende laster ud af lagerstedet, før de fuldfører alt det arbejde, der er knyttet til disse laster. Når der modtages en forsendelse, som indeholder lastlinjer, der ikke er plukket fuldstændigt, bliver den bekræftende bruger enten spurgt, om vedkommende vil opdele restantallet på en ny last eller annullere antallet af ufuldstændige antal.

Systemer, der er konfigureret til at tillade understøttelse af opdeling af laster, hvor planlagte og delvist læssede laster skal tilpasses på grund af nye eller skiftende omstændigheder.

Klienten indeholder logik, der gør, at en delvist lastet last lukkes og bekræftes som leveret. Alle resterende forsendelser og lastlinjer (herunder hele eller delvise linjeantal) overføres derefter til en nyoprettet last og forsendelse, hvis denne overgang kræves, og opsætningen tillader det. Der oprettes automatisk nye forsendelser og laster ud fra de første kriterier for afsendelse og last, og deres hovedattributter forbliver uændrede. Der findes også en indstilling, hvor restantallet automatisk annulleres, hvis der endnu ikke er oprettet en arbejdsordre, og brugeren skønner, at denne annullering er nødvendig.

Denne funktionalitet understøtter scenarier, hvor den fulde last ikke passer på en enkelt lastbil, eller hvor noget af lasten skal forlade lagerstedet, før resten af lasten er klar til afsendelse. I disse scenarier kan de resterende produkter overføres til en ny last og derfor til en ny lastbil. Da denne funktion kan bruges sammen med laster, der ellers var tiltænkt forsendelse af fuld last, giver den ekstra fleksibilitet, så transportansvarlige kan løse ikke-standardiserede eller uforudsete scenarier.

Når en last er delt op, udfører funktionen *Bekræft og overfør* følgende handlinger:

- Der oprettes nye laster og forsendelser, efterhånden der er behov for dem. Hver last eller forsendelse vil have de fleste af de samme attributter som den oprindelige last eller forsendelse. Undtagelsen er laststatussen, som vil blive genberegnet på baggrund af arbejdsstatussen.
- Brugeren bliver informeret om, at der er oprettet en ny last. Brugeren får også besked om id'et for den nye last.
- Lastlinjerne, arbejdsoverskrifterne og arbejdslinjerne, der var opdelt, opdateres med de nye oplysninger om last og forsendelse.
- Hvis en hel forsendelse er ved at blive opsplittet, bevares forsendelsen, og kun lastreferencerne opdateres. Hvis forsendelsen skal opdeles, oprettes der en ny forsendelse.

Når et resterende antal annulleres, fjernes eventuelle lastlinjeantal, der ikke er plukket, og som ikke har et ikke-annulleret arbejde tilknyttet, fra lasten. Hvis et igangværende arbejde er i gang, kan brugeren kun opdele lasten. De resterende antal kan ikke annulleres.

Du kan kun opdele laster, der opfylder alle følgende kriterier:

- En eller flere lastlinjer har plukkede antal.
- Laststatussen er mindre end lastet.
- Der er ingen lastlinjedata. (Disse data oprettes ved konsolidering af nummerplader på den midlertidige placering, og funktionen *Bekræft og overfør* understøtter ikke nummerpladekonsolidering).
- Der er ingen lager, der i øjeblikket afventer pakning på en pakkelokation. (Funktionen *Bekræft og overfør* understøtter ikke den lagerbeholdning, der er plukket til pakkestationen, men endnu ikke er pakket.)

> [!NOTE]
> Denne funktionalitet adskiller sig fra funktionaliteten for transportlasten, som skal bruges på lagersteder, der aldrig kan planlægge og oprette laster før plukning, men som i stedet læsser den tilgængelige transportplads, når plukningen er fuldført.
>
> Brug funktionen *Bekræft og overfør* i situationer, hvor laster normalt planlægges og oprettes forud for tiden, men hvor der sommetider opstår undtagelser, hvor lasten ikke kan passer til den tilgængelige transport (f. eks. en lastbil).

## <a name="turn-on-confirm-and-transfer"></a>Slå Bekræft og overfør til

Før du kan bruge funktionen *Bekræft og overfør*, skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Bekræft og overfør*

## <a name="set-up-confirm-and-transfer"></a>Konfigurere Bekræft og overfør

Hvis du vil bruge funktionen *Bekræft og overfør*, skal du slå aktivere den på alle relevante lastskabeloner. Afhængigt af dine krav kan det også være en god ide at forberede dine arbejdsskabeloner til at understøtte denne funktion. Hvis du vil arbejde i det eksempelscenarie, der er angivet senere i dette emne, skal du konfigurere systemet som beskrevet i dette afsnit. (Dette scenarie er baseret på **USMF**-demodata).

### <a name="prepare-your-load-templates"></a>Forberede lastskabeloner

1. Gå til **Lagerstedsstyring \> Opsætning \> Last \> Lastskabeloner**.
1. Vælg **Rediger** i handlingsruden for at sætte siden i redigeringstilstand.
1. Marker afkrydsningsfeltet **Tillad opdeling af last under bekræftelse af forsendelse** for hver eksisterende skabelon, hvor du vil aktivere funktionen. Du kan også vælge **Ny** for at oprette en ny skabelon og konfigurere den, som du har brug for. Alle laster, du opretter ved hjælp af denne skabelon, nedarver denne funktionalitet. (Hvis du arbejder med **USMF**-demodata, skal du aktivere funktionen for lastskabelonen **20 Container**.

### <a name="prepare-your-work-templates"></a>Forberede arbejdsskabeloner

Denne opsætning er ikke påkrævet i alle situationer. Det eksempel, der vises her, sikrer, at arbejdet kan opdeles efter forsendelse for at understøtte det eksempelscenarie, der er angivet senere i dette emne. Der findes også andre måder at opnå dette resultat på.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Vælg en eksisterende arbejdsskabelon, hvor du vil konfigurere funktionen *Bekræft og overfør*, i gitteret på den øverste del af siden. (Hvis du arbejder med **USMF**-demodata, skal du vælge arbejdsskabelonen **51 Pluk til stadie**). Du kan også oprette en ny arbejdsskabelon.
1. I handlingsruden skal du vælge **Rediger forespørgsel** for at åbne dialogboksen **Salg**.
1. I dialogboksen **Salg** skal du under fanen **Sortering** vælge **Tilføj** for at føje en række til gitteret.
1. Angiv følgende værdier i den nye række:

    - **Tabel:** *Midlertidige arbejdstransaktioner*
    - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
    - **Felt:** *Forsendelses-id*
    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at gemme dine indstillinger, og luk dialogboksen **Salg**.
1. Hvis du får vist en meddelelse om, at gruppering bliver nulstillet, skal du vælge **Ja** for at fortsætte.
1. I gitteret på den øverste del af siden **Arbejdsskabeloner** skal du vælge den skabelon, du netop har redigeret, og derefter skal du vælge **Arbejdshovedpauser**.
1. Vælg **Rediger** i handlingsruden for at sætte siden i redigeringstilstand.
1. Angiv følgende værdier i gitteret:

    - **Tabelnavn:** *Midlertidige arbejdstransaktioner*
    - **Feltnavn:** *Forsendelses-id*
    - **Gruppér efter dette felt:** Marker dette afkrydsningsfelt.

1. Vælg **Gem** i handlingsruden.
1. Luk siden.

## <a name="scenario"></a>Scenario

Dette scenarie viser et eksempel på, hvor plukprocessen endnu ikke er fuldført, men de varer, der er blevet plukket indtil nu, skal læsses på en lastbil og afsendes alligevel. Brugeren kan derfor opdele de ikke-plukkede lastlinjer på en ny last. Alle datarelationerne opdateres derefter automatisk.

> [!NOTE]
> De specifikke værdier, der er beskrevet i dette scenarie, er baseret på **USMF**-demodataene. Det anbefales, at du bruger disse demonstrationsdata, mens du viser eller lærer, hvordan du bruger funktionen. Hvis du ikke bruger **USMF**-demodataene, skal du erstatte dine egne værdier efter behov.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Trin 1: Oprette en last, der har flere lastlinjer

Før du kan bruge denne funktion, skal du have en last, der indeholder flere lastlinjer. Du skal også sikre, at alle pluklokationerne har tilstrækkelig lagerbeholdning til alle varerne på de salgsordrer, du vil oprette. Gennemse opsætningen af lokationsvejledningen (**Lagerstyring \> Konfiguration \> Lokationsvejledninger**), og noter dig de pluklokationer, der bruges til plukning af salgsordrer. Hvis du skal justere lageret, skal du oprette manuelle bevægelser, bruge genopfyldning eller anvende et andet flow efter behov.

Hvis du vil oprette en kvalificerende last, skal du først oprette tre salgsordrer ved at følge disse trin.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. I handlingsruden skal du vælge **Nye** for at åbne dialogboksen **Opret salgsordre**.
1. Gå til dialogboksen **Opret salgsordrer**, og angiv følgende værdier (som minimum):

    - Gå til oversigtspanelet **Kunde**, og angiv feltet **Debitorkonto** til *US-004* (*Cave Wholesales*).
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *51*.

1. Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.
1. Din nye indkøbsordre åbnes. I gitteret **Salgsordrelinjer** skal du tilføje en linje, der har følgende værdier:

    - **Varenummer:** *M9200*
    - **Antal:** *40*
    - **Enhed:** *Styk*

1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. Gå til handlingsruden, og vælg **Reserver parti** for at åbne siden **Reservation**.
1. Reserver lageret på salgslinjen, og luk derefter siden **Reservation**.
1. Gentag trin 1 til og med 4 for at tilføje endnu en salgsordre for samme debitor og det samme lagersted.
1. Tilføj to salgslinjer, der har følgende værdier. Når du har tilføjet hver linje, skal du reservere lagerbeholdning for den som beskrevet i trin 6 til 8.

    - **Linje 1:** Indstil feltet **Varenummer** til *M9200*, feltet **Antal** til *30* og feltet **Enhed** til *EA*.
    - **Linje 2:** Indstil feltet **Varenummer** til *M9201*, feltet **Antal** til *20* og feltet **Enhed** til *EA*.

1. Gentag trin 1 til og med 4 for at tilføje en tredje salgsordre for samme debitor og det samme lagersted.
1. Tilføj to salgslinjer, der har følgende værdier. Når du har tilføjet hver linje, skal du reservere lagerbeholdning for den som beskrevet i trin 6 til 8.

    - **Linje 1:** Indstil feltet **Varenummer** til *M9201*, feltet **Antal** til *20* og feltet **Enhed** til *EA*.
    - **Linje 2:** Indstil feltet **Varenummer** til *M9202*, feltet **Antal** til *60* og feltet **Enhed** til *EA*.

#### <a name="load-planning-workbench"></a>Panelet Lastplanlægning

Lastplanlægningspanelet bruger lastskabelon-id'et til at bygge forsendelserne og frigive salgsordrelinjerne til lagerstedet.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. Vælg *51* i feltet **Lagersted**.

    Du skal nu opbygge lasten for de salgsordrer, som du lige har oprettet.

1. Under fanen **Salgslinjer** skal du vælge salgslinjerne for de nye salgsordrer i gitteret.
1. I handlingsruden skal du under fanen **Udbud og efterspørgsel** i gruppen **Tilføj** vælge **Til ny last**.
1. I dialogboksen **Tilknytning af lastskabelon** skal du i feltet **Lastskabelons-id** vælge *20' Container*.
1. Vælg **OK**.
1. Gå til sektionen **Laster** på siden **Lastplanlægningspanel** i gitteret, og find det netop oprettede last-id for lagersted *51*. Rul til højre, indtil du kan se kolonnen **Tillad opdeling af last under bekræftelse af forsendelse**. Afkrydsningsfeltet skal være markeret for lasten.
1. Vælg lasten.
1. I menuen **Frigiv** over gitteret skal du vælge **Frigiv til lagersted** for at oprette arbejde.
1. I dialogboksen **Frigiv last til lagersted** skal du kontrollere, at oversigtspanelet **Poster, der skal indgå** viser dit last-id.
1. Vælg **OK**.

    Du kan modtage en meddelelse om "behandlingsoperation", mens systemet opretter forsendelser og arbejde.

1. I sektionen **Laster** på siden **Lastplanlægningspanel** skal lasten nu have laststatussen *I bølge*. Vælg lasten, og vælg derefter **Bølgedetaljer** i menuen **Relaterede oplysninger** over gitteret for at få vist de forsendelses-id'er, der blev oprettet. Når du er færdig, skal du lukke siden **Bølger**.
1. I sektionen **Laster** på siden **Lastplanlægningspanel** skal du vælge lasten og derefter i menuen **Relaterede oplysninger** over gitteret vælge **Arbejdsdetaljer** for at få vist det arbejde, der er oprettet for salgsordrerne.
1. Noter de arbejds-id'er, der blev oprettet. Du skal muligvis rulle til højre for at få vist det salgsordrenummer og forsendelses-id, der er knyttet til arbejds-id'et.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Trin 2: Konfigurere kørselsforløbet for mobilenheder

Mobilenhedsopgaver kræver brugerinput af oplysninger, f.eks. arbejds-id eller nummerplade-id. I felterne er disse oplysninger typisk tilgængelige for lagerbrugere i form af stregkoder, der findes i dokumentation, emballage eller på reoler. Hvis du vil fuldføre trinnene i mobilenheden for scenarier, skal du kontrollere, at du har identificeret arbejds-id'erne for posteringerne og nummerplade-id'erne for varen og lokationen i transaktionerne.

1. Log på mobilenheden ved hjælp af et bruger-id og en adgangskode til lagerstedet *51*.
1. Vælg **Udgående**.
1. Vælg **Salgspluk**.
1. Du har mulighed for at angive arbejds-id'et eller nummerplade-id'et. Angiv arbejds-id'et for den første salgsordre, og vælg derefter **Angiv**.
1. I feltet **LOK** skal du angive den lokation, der vises, for at bekræfte pluklokationen. Vælg derefter **Angiv**.
1. Angiv nummerplade-id'et i feltet **NP**. Nummerplade-id'et skal være et match for varen, lagerstedet og lokationen for den vare, der plukkes fra den valgte lokation. Vælg **Angiv**, når du er færdig.
1. Angiv det varenummer, der skal bekræfte den vare, der skal plukkes, i feltet **Vare**, og vælg derefter **Angiv**.
1. I feltet **Antal** skal du angive det antal varen, der plukkes, og derefter vælge **Angiv**.
1. I feltet **Mål-NP** skal du angive et målnummerplade-id. Målnummerplader er brugerdefinerede. Sørg for at angive et nummerplade-id, som du vil huske. Det anbefales, at du bruger dags dato plus en tocifret sekvens (ÅÅMMDD\#\#) som formatet, f.eks. *19112301*. Vælg **Angiv**, når du er færdig.
1. Gennemse de oplysninger, der vises. Disse oplysninger er *plukkeoplysninger*, der nu vil blive *Læg på lager*-data for læg på lager-transaktionen. Vælg **Angiv**, når du er færdig.

    - Du modtager en meddelelse om **arbejde fuldført**.

1. Gentag trin 4 til 10 for arbejds-id'et for den anden salgsordre.

I det næste trin skal laste to plukkede nummerplader på lastbilen.

1. Log på mobilenheden ved hjælp af et bruger-id og en adgangskode til lagerstedet *51*.
1. Vælg **Udgående**.
1. Vælg **Salgslastning**.
1. Angiv det brugerdefinerede målnummerplade-id, som du oprettede for det første arbejds-id i den foregående procedure. Vælg derefter **Angiv** for at placere målnummerpladen på lokationen **STADIE**.
1. Angiv målnummerplade-id'et, og vælg derefter **Angiv** for at placere nummerpladen på lokationen **BÅSEDØR**.
1. Gentag trin 4 til 5 for det målnummerplade-id, du har oprettet til det andet arbejds-id.

De to arbejds-id'er vil nu blive lukket (lastet).

### <a name="step-3-confirm-the-outbound-shipment"></a>Trin 3: Bekræfte den udgående forsendelse

I dette trin skal du bekræfte de to salgsordrer og det arbejde, der er fuldført for lasten, for at afsende de plukkede varer i lasten og oprette en ny last for de ikke-plukkede varer. Der skal udføres en bekræftelse af udgående forsendelse på siden **Lastdetaljer**.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. I sektionen **Laster** skal du i gitteret vælge rækken for det last-id, du har oprettet.
1. Vælg last-id'et for at åbne siden **Lastdetaljer**.
1. På siden **Lastdetaljer** skal du i handlingsruden under fanen **Send og modtog** i gruppen **Bekræft** vælge **Udgående forsendelse** for at starte bekræftelsen.
1. I dialogboksen **Bekræftelse af afsendelse** skal du i feltet **Metode til opdeling af last under bekræftelse af afsendelse** vælge *Opdel antal til ny last*.
1. Vælg **OK**.

    Du kan få vist meddelelsen "behandlingsoperation".

    Du modtager orienterende meddelelser, der angiver, at forsendelsen af lasten er bekræftet, og at der er oprettet en ny last ud fra det opdelte antal.

Opdater siden **Lastplanlægningspanel** for at få vist den netop oprettede last.

Du kan også kontrollere, at posteringsrelationerne er blevet opdateret på følgende måder:

- Den resterende (ikke-behandlede) forsendelse og de resterende forsendelseslinjer opdateres med det nye last-id.
- Salgsordren er knyttet til det nye last-id.
- Den oprindelige last omfatter ikke de resterende lastlinjer.
- Det resterende arbejde er blevet opdateret med det nye last-id.
- Bølgen forbliver den samme.
- Statussen for den nye last er korrekt opdateret. (Hvis arbejdsstatussen er _Under behandling_, skal laststatussen også være _Under behandling_.)

## <a name="notes-and-tips"></a>Noter og tip

- Du kan også aktivere parameteren **Tillad opdeling af last under bekræftelse af forsendelse**, efter at lasten er oprettet med parameteren **Lastskabelon** slået fra, men før lastbehandlingen er startet. Gå til den ønskede last, og aktiver derefter parameteren i overskriftsvisningen.
- Indstillingen **Opdel antal til ny last** fungerer også, når nogle af de resterende arbejdsoverskrifter har statussen *Under behandling*. Du kan derfor stadig bruge funktionaliteten, selvom arbejdere allerede kører plukordrerne.
- Hvis du vælger **Annuller ikke-opfyldt antal**, mens der er resterende arbejde med statussen *Åben* eller *Under behandling*, får du vist følgende fejlmeddelelse: "det er ikke muligt at annullere det resterende antal til last. Der findes arbejde til last."
- Hvis du vælger **Annuller ikke-opfyldt antal**, når der ikke er noget resterende arbejde, men der er frigivne lastlinjer på lasten, får du vist følgende fejlmeddelelse: "Forsendelsen til last kunne ikke bekræftes, fordi antallet for varen overstiger den procentdel, der er defineret til underlevering". For at undgå denne fejl kan du angive procentdelen for **Underlevering** på den ikke-frigivne lastlinje til 100 %. Linjer, der ikke er frigivet, flyttes ikke til en ny last, men den aktuelle last bekræftes med underlevering. I dette tilfælde kan du ikke genudgive den oprindelige ordre. Derfor skal du håndtere den på en anden måde.
