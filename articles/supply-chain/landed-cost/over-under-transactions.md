---
title: Over-/undertransaktioner
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at konfigurere detaljerne om politikker for over-/undertransaktioner, så systemet kan bestemme, hvordan det skal administrere overbehandlingen og underbehandlingen af varer på modtagelsestidspunktet.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9027d5dc73ebd78a65429f7bc63a1ebf8ef60dac
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500976"
---
# <a name="overunder-transactions"></a>Over-/undertransaktioner

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Når ordrerne i en fragt behandles, forventer systemet, at det modtagne vareantal på det endelige destinationslagersted til forbrug svarer til det antal, der er angivet på de indkøbsordrelinjer, der er tilknyttet fragten. Da det nøjagtige antal på indkøbsordrelinjerne dog ikke altid modtages på lagerstedet, definerer modulet **Landingsomkostninger** et sæt regler, der bruges til håndtering af over- og undermodtagelse af varer. Disse regler er især vigtige, fordi den oprindelige indkøbsordre er faktureret og ikke længere kan ændres. Hvis du konfigurerer detaljerne om politikker for over-/undertransaktioner, kan systemet bestemme, hvordan det skal administrere overbehandlingen og underbehandlingen af varer på modtagelsestidspunktet. Du kan også administrere over- og underlager manuelt ved hjælp af siden **Over-/undertransaktioner**.

## <a name="overunder-tolerances"></a>Over/under-tolerancer

Du angiver tolerancer for over- og underlevering for at angive de over- og underantal eller mængder, der kan behandles på en fragt uden fejl. Hvis modtagelsen af fragtlinjen ligger uden for disse tolerancer, skal den redigeres og løses, før fragtlinjen kan lukkes for yderligere behandling.

Hvis du vil konfigurere tolerancerne, skal du gå til **Landingsomkostninger \> Over-/underopsætning \> Over-/undertolerancer**. Her kan du se, redigere, tilføje og fjerne toleranceposter. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Kontokode | <p>Definer omfanget af leverandører, som tolerancen gælder for, ved at vælge en af følgende værdier:</p><ul><li>**Tabel** – Over-/under-tolerancen gælder kun for den leverandør, der er valgt for rækken.</li><li>**Gruppe** – Over-/under-tolerancen gælder for alle leverandører i den leverandørtolerancegruppe, der er valgt for rækken.</li><li>**Alle** – Over-/undertolerancen gælder for alle leverandører.</li></ul> |
| Kontorelation | Vælg den leverandør- eller leverandørgruppe, som over-/undertolerancen gælder for, afhængigt af den værdi, du har valgt i feltet **Kontokode**. |
| Varekode | <p>Definer omfanget af varer, som tolerancen gælder for, ved at vælge en af følgende værdier:</p><ul><li>**Tabel** – Over-/under-tolerancen gælder kun for den vare, der er valgt for rækken.</li><li>**Gruppe** – Over-/under-tolerancen gælder for alle varer i den varetolerancegruppe, der er valgt for rækken.</li><li>**Alle** – Over-/undertolerancen gælder for alle varer.</li></ul> |
| Varerelation | Vælg den vare- eller varegruppe, som over-/undertolerancen gælder for, afhængigt af den værdi, du har valgt i feltet **Varekode**. |
| Beløbstolerance | Angiv den beløbstolerance, der skal anvendes på en hel indkøbsordre. |
| Procent tolerance | Angiv den toleranceprocent, der skal anvendes på en individuel indkøbsordrelinje. |

## <a name="overunder-reasons"></a>Over/under-årsager

Når der er knyttet et over- eller underantal til en fragtlinje, der modtages, skal du muligvis identificere årsagen til over- eller underantallet. I dette tilfælde kan du vælge årsagen til overlevering eller underlevering på modtagelseslinjen, når varerne modtages.

Hvis du vil konfigurere årsager til overlevering og underlevering, skal du gå til **Landingsomkostninger \> Over-/underopsætning \> Over-/underårsager**. Her kan du se, redigere, tilføje og fjerne de tilgængelige årsager til overlevering og underlevering. I følgende tabel forklares de felter, der er tilgængelige for hver årsag.

| Felt | Beskrivelse |
|---|---|
| Over/under-årsag | Angiv et entydigt navn på årsagen til transaktionen for over- eller undermodtagelse. |
| Beskrivelse | Angiv en beskrivelse af over-/underårsagen. |
| Bevægelse | Vælg den bevægelseskladde, der er knyttet til over-/underårsagen. Dette felt viser alle tilgængelige kladder, som kladdetypen *Bevægelse* er tilknyttet på siden **Lagerkladdenavne** (**Opsætning af lagerstyring \> Kladdenavne \> Lager**). |

## <a name="item-overunder-tolerance-groups"></a>Over/under-tolerancegrupper for vare

Varer, der har ens tolerancer, kan grupperes sammen. På denne måde kan du angive over-/undertolerancen for alle varer i den pågældende gruppe på én gang.

Hvis du vil konfigurere over/under-tolerancegrupper for varer, skal du gå til **Landingsomkostninger \> Over-/underopsætning \> Over/under-tolerancegrupper for varer**. Her kan du se, redigere, tilføje og fjerne poster for over/under-tolerancegrupper. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Over/under-tolerancegruppe | Angiv et entydigt navn til gruppen. Vælg et navn, der beskriver tolerancen, f.eks. *1 % Var*. |
| Beskrivelse | Angiv en beskrivelse af gruppen. |

## <a name="vendor-overunder-tolerance-groups"></a>Over/under-tolerancegrupper for leverandør

Du kan gruppere leverandører, der regelmæssigt har overlevering eller underlevering. Du kan derefter angive over-/undertolerancen for hver gruppe.

Hvis du vil konfigurere over/under-tolerancegrupper for leverandører, skal du gå til **Landingsomkostninger \> Over-/underopsætning \> Over/under-tolerancegrupper for leverandør**. Her kan du se, redigere, tilføje og fjerne poster for over/under-tolerancegrupper. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Over-/undergrupper | Angiv et entydigt navn til gruppen. Vælg et navn, der beskriver den type leverandør, der tilhører gruppen. |
| Beskrivelse | Angiv en beskrivelse af gruppen. |

## <a name="view-and-process-overunder-transactions"></a>Se og behandle over-/undertransaktioner

Der genereres over- og undertransaktioner, når det antal varer, der lægges væk, ikke svarer til det initialiserede antal. Antallet i modtagelseskladden bør kun opdateres med det antal, der er lagt væk.

Når modtagelsen af fragtlinjer behandles, kan der angives over-/undertolerancer for en leverandør. Varerne gennemses og valideres derefter. Tolerancen kan angives som en procent, et lokalt beløb eller begge dele.

Hvis en vare, der er modtaget, er inden for tolerancen, genererer systemet en bevægelseskladde. Denne kladde kan angives på siden for fragtparametre. Der oprettes desuden en over-/undertransaktion. Ordreværdien kan f.eks. være 100, og modtagelsesværdien 99, så disse værdier opfylder tolerancereglerne. I dette tilfælde oprettes der en negativ bevægelseskladde for det undermodtagne antal.

Hvis en vare, der modtages, ligger uden for tolerancen, genererer systemet en over-/undertransaktion for forskellen i antal.

Hvis du vil se og behandle over-/undertransaktioner, skal du gå **Landingsomkostninger \> Forespørgsler \> Over-/undertransaktioner**. Der knyttes en over-/undertransaktion til alle varer i en fragt, der er over- eller undermodtaget. Det anbefales, at du bruger siden **Over/under-transaktioner** til at løse alle over-/undertransaktioner, der er tilknyttet fragt. Det anbefales også, at du **ikke** bruger bevægelses- eller optællingskladder til manuelt at løse lagertransaktioner for underlevering. Du skal i stedet bruge siden **Over-/undertransaktioner** til at administrere lagerstedsantal for underlevering.

### <a name="upper-overview-tab"></a>Øverste fane Oversigt

Hvis du vil have vist over-/undertransaktioner, skal du vælge fanen **Oversigt** i den øverste del af siden **Over-/undertransaktioner**. I følgende tabel forklares de felter, der er tilgængelige i gitteret.

| Felt | Beskrivelse |
|---|---|
| Over/under-transaktionsnummer | Det entydige navn på over-/undertransaktionsposten, der automatisk blev oprettet, da modtagelseskladden blev behandlet. |
| Fragt | Den fragt, som indkøbslinjen er tilknyttet. |
| Forsendelsescontainer | Den container, som indkøbslinjen er tilknyttet. |
| Modtagelseskladde | Den modtagelseskladde, som over-/underlinjen blev oprettet fra. |
| Reference | En reference til enten indkøbsordren eller den flytteordre, der er knyttet til over/undertransaktionen. |
| Nummer | Den indkøbsordre, der refereres til i over/undertransaktionen. |
| Kreditorkonto | Den kreditor, som over- eller undertransaktionen er relateret til. |
| Nummer for varer i transit | Varernes transitnummer, hvis dette er relevant. |
| varenummer | Det varenummer, som over- eller undertransaktionen er relateret til. |
| Oprindeligt antal | Det oprindelige antal på indkøbsordrelinjen, der er tilknyttet forsendelsen. |
| Modtaget antal | Det antal, der faktisk er modtaget. |
| Difference | Forskellen mellem det forventede modtagelseskladdebeløb og det beløb, der blev bogført i modtagelseskladden. En negativ værdi angiver en overlevering af varer. |
| Rest | Det antal, der resterer på modtagelseskladdelinjen. |
| Over-/underlevering | En værdi, der angiver, om det modtagne antal er over- eller underlevering. |
| Status | Status for over-/undertransaktionen. Afhængigt af indstillingerne på siden **[Parametre for landingsomkostninger](landed-cost-parameters.md)** kan overlevering automatisk oprette en bevægelseskladde for overleveringsbeløbet og bogføre kladden. I dette tilfælde vil over-/undertransaktionen have status af *Fuldført*. Hvis der skal udføres en handling for at flytte varerne ud af lagerstedet for underlevering, får posten status af *Under behandling*. |
| Over/under-årsag | Årsagen, der er knyttet til over-/undertransaktionen. |
| Andre lagerdimensioner | Du kan få vist kolonnerne for flere dimensioner i gitteret efter behov. Disse dimensioner omfatter batchnummer, lagerstatus og lagersted. Vælg **Lager \> Vis dimensioner** i handlingsruden for at åbne en dialogboks, hvor du kan vælge de dimensioner, der skal medtages. |

### <a name="upper-general-tab"></a>Øverste fane Generelt

Hvis du vil have vist flere oplysninger om den linje, der aktuelt er valgt under den øverste fane **Oversigt**, skal du vælge fanen **Generelt** i den øverste del af siden **Over-/undertransaktioner**. Oplysningerne under denne fane indeholder værdierne for alle tilgængelige dimensioner. Disse oplysninger hentes fra den oprindelige indkøbsordre.

### <a name="lower-overview-tab"></a>Nederste fane Oversigt

Hvis du vil se dokumenttypen for den række, der er valgt under den øverste fane **Oversigt**, skal du vælge fanen **Oversigt** i den nederste del af siden **Over-/undertransaktioner**. I følgende tabel forklares de felter, der er tilgængelige.

| Felt | Beskrivelse |
|---|---|
| Ny dokumenttype | Dette felt er angivet til enten *Bevægelseskladde* eller *Indkøbsordre* afhængigt af, hvilken handling der vises på den valgte over-/undertransaktionslinje. |
| Tal | En reference og et link til enten indkøbsordren eller den bevægelseskladde, der er knyttet til den valgte over-/undertransaktionslinje. |
| Over/under-årsag | Årsagen, der er knyttet til den valgte over-/undertransaktionslinje. |
| Kvantitet | Det antal, som du har valgt til indkøbsordren eller den bevægelseskladde, der er knyttet til den valgte over-/undertransaktionslinje. |

### <a name="lower-general-tab"></a>Nederste fane Generelt

Hvis du vil have vist over-/undertransaktionsnummer, parti-id og dimensionsnummer, der er knyttet til den valgte over-/undertransaktionslinje, skal du vælge fanen **Generelt** i den nederste del af siden **Over-/undertransaktioner**. 

### <a name="process-overunder-transactions"></a>Behandle over-/undertransaktioner

Handlingsruden på siden **Over-/undertransaktioner** indeholder følgende kommandoer til behandling af de transaktioner, der er valgt på siden. Du kan bruge de enkelte kommandoer til at vælge, hvordan hver enkelt transaktion skal behandles.

- **Opret \> Bevægelse** – Opret og bogfør en bevægelseskladde for den valgte transaktion. I forbindelse med undertransaktioner oprettes der automatisk en bevægelseskladde, som bogføres for forskellen mellem det forventede og det faktiske modtagne antal. Vælg denne kommando til overtransaktioner, hvis du ønsker, at leverandøren skal realisere omkostningsdifferencen.
- **Opret \> Indkøbsordre** – Opret en indkøbsordre for forskellen mellem det forventede og det faktiske modtagne antal for den valgte transaktion. Vælg denne kommando til overtransaktioner, hvis din organisation skal realisere omkostningsdifferencen.
- **Opret \> Overfør til destination** – Denne kommando gælder kun for flytteordrer. Vælg den, hvis du vil overføre over- eller underantallet til destinationslagerstedet.
- **Opret \> Overfør til oprindelsessted** – Denne kommando gælder kun for flytteordrer. Vælg den, hvis du vil overføre over- eller underantallet til oprindelseslagerstedet.
