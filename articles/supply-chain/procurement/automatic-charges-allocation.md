---
title: Automatisk fordeling af gebyrer
description: Funktionen Gebyr i Microsoft Dynamics 365 Supply Chain Management hjælper dig med automatisk at fordele gebyrer til indkøbsordrer eller salgsordrer.
author: GalynaFedorova
ms.date: 09/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c6729e9a485205a6beb53441798952fac2b93ef7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673040"
---
# <a name="automatic-allocation-of-charges"></a>Automatisk fordeling af gebyrer

[!include [banner](../includes/banner.md)]

På baggrund af den kunde, du arbejder med, eller den vare, du sælger, kan du anvende specifikke ekstragebyrer. Funktionen *Gebyr* i Microsoft Dynamics 365 Supply Chain Management hjælper dig med automatisk at fordele gebyrer til indkøbsordrer eller salgsordrer.

Automatiske gebyrer, eller automatiske tillæg, anvendes automatisk, når du opretter en salgsordre eller indkøbsordre. Du kan definere automatiske tillæg for bestemte leverandører, kunder grupper af leverandører eller varer. Du kan også definere automatiske tillæg, der gælder for alle leverandører, kunder eller varer.

## <a name="set-up-parameters"></a>Konfigurer parametre

Siden **Indkøbs- og forsyningsparametre** indeholder nogle få indstillinger, der især er relevante, når du vil tildele gebyrer automatisk. Gør følgende for at fuldføre konfigurationen.

1. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.
1. Åbn fanen **Priser**.
1. Foretag følgende indstillinger i oversigtspanelet **Priser**:
    - **Find automatiske gebyrer til overskrift** – Angiver, om der automatisk skal tildeles tillæg for indkøbsordreoverskrifter. Angiv dette til *Ja*, hvis du vil bruge automatisk fordeling af gebyrer.
    - **Find automatiske gebyrer til linje** – Angiver, om der automatisk skal tildeles tillæg for indkøbsordrelinjer. Angiv dette til *Ja*, hvis du vil bruge automatisk fordeling af gebyrer.

## <a name="set-up-charges-codes"></a>Oprette gebyrkoder

Hvis du vil tildele gebyrer, skal du først definere gebyrkoder.

1. Udfør ét af følgende trin:

    - For indkøbsordrer: Gå til **Kreditor \> Konfiguration af gebyrer \> Gebyrkode**.
    - For salgsordrer: Gå til **Debitor \> Konfiguration af gebyrer \> Gebyrkode**.

1. Vælg **Ny** i handlingsruden for at oprette en ny gebyrkode.
1. Angiv følgende felter i den nye posts overskrift:

    - **Gebyrkode** – Angiv en kode for gebyrerne.
    - **Beskrivelse** – Indtast en beskrivelse af gebyrerne.
    - **Varemomsgruppe** – Vælg en varemomsgruppe, hvis det er relevant.
    - **Beregn forholdsmæssigt** – Angiv denne indstilling til *Ja*, hvis du vil beregne gebyrer forholdsmæssigt. Denne indstilling kan kun vælges for salgsordrer.
    - **Maks. beløb** – Angiv det maksimale beløb, der er tilladt for gebyrkoden. Dette felt bruges til at validere gebyrer for kreditorfakturaer. Det er kun tilgængeligt for indkøbsordrer.

        > [!NOTE]
        > Hvis du vil aktivere funktionen til validering af gebyrer for indkøbsordrer, skal du gå til **Kreditor \> Konfiguration \> Kreditorparametre**. I oversigtspanelet **Fakturavalidering** skal du i sektionen **Fakturavalidering** angive indstillingen **Aktivér validering af fakturasammenholdelse** til *Ja*.

1. Oversigtspanelet **Bogføring** indeholder **Debet**- og **Kredit**-sektioner. Angiv følgende felter afhængigt af, hvilken finanskonto gebyrerne skal bogføres på:

    - **Type** – Vælg den kontotype, som du vil bogføre på (*Finans*, *Debitor* eller *Vare*).
    - **Bogføring** – Vælg den type posteringer, der skal oprettes (f.eks. *Mæglergebyr* eller *Debitorudligning*).
    - **Konto** – Vælg den konto, gebyret skal bogføres for.

1. Vælg **Gem** i handlingsruden.

## <a name="create-charge-groups"></a>Oprette gebyrgrupper

Gebyrgrupper tildeler automatisk specifikke gebyrer til en gruppe af debitorer eller kreditorer. I følgende underafsnit beskrives, hvordan du kan oprette og tildele disse gebyrgrupper.

### <a name="charge-groups-for-purchase-orders"></a>Gebyrgrupper for indkøbsordrer

Benyt følgende fremgangsmåde for at oprette gebyrgrupper for indkøbsordrer.

1. Gå til **Kreditor \> Konfiguration af gebyrer \> Leverandørgebyrgruppe**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret, og angiv derefter følgende felter:

    - **Gebyrgruppe** – Angiv navnet på gebyrgruppen.
    - **Beskrivelse** – Indtast en beskrivelse af gebyrgruppen.

1. Vælg **Gem** i handlingsruden.
1. Gå til **Kreditor \> Kreditorer \> Alle kreditorer**, og åbn en eksisterende kreditor, eller opret en ny kreditor.
1. I oversigtspanelet **Indkøbsordrestandarder** i sektionen **Indkøbsordre** skal du angive feltet **Gebyrgruppe** til den gebyrgruppe, du netop har oprettet.

### <a name="charge-groups-for-sales-orders"></a>Gebyrgrupper for salgsordrer

Benyt følgende fremgangsmåde for at oprette gebyrgrupper for salgsordrer.

1. Gå til **Debitor \> Konfiguration af gebyrer \> Debitorgebyrgrupper**.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret, og angiv derefter følgende felter:

    - **Gebyrgruppe** – Angiv navnet på gebyrgruppen.
    - **Beskrivelse** – Indtast en beskrivelse af gebyrgruppen.

1. Vælg **Gem** i handlingsruden.
1. Gå til **Debitor \> Debitorer \> Alle debitorer**, og åbn en eksisterende debitor, eller opret en ny debitor.
1. I oversigtspanelet **Indkøbsordrestandarder** i sektionen **Salgsordre** skal du angive feltet **Gebyrgruppe** til den gebyrgruppe, du netop har oprettet.

## <a name="define-auto-charges"></a>Definere automatiske gebyrer

Når gebyrkoderne er konfigureret, skal du udføre disse trin for at definere de automatiske gebyrer.

1. Udfør ét af følgende trin:

    - For indkøbsordrer: Gå til **Indkøb og forsyning \> Konfiguration \> Gebyrer \> Automatiske gebyrer**.
    - For salgsordrer: Gå til **Debitor \> Konfiguration \> Konfiguration af gebyrer \> Automatiske gebyrer**.

1. Vælg det niveau, som dit automatiske gebyr skal gælde for, i feltet **Niveau** i listeruden:

    - *Primær* – Anvend gebyrer i ordrehovedet.
    - *Linje* – Anvend gebyrer på ordrelinjerne.

1. Vælg et eksisterende automatisk gebyr for at redigere det, eller Vælg **Nyt** for at definere et nyt automatisk gebyr.
1. På listen **Kontokode** skal du vælge en af følgende værdier for at angive omfanget af de konti, der påvirkes:

    - *Tabel* – Tildel gebyrer til en bestemt debitor eller kreditor.
    - *Gruppe* – Tildel gebyrer til en blandet gebyrgruppe.
    - *Alle* – Tildel gebyrer til alle debitorer eller kreditorer.

1. I feltet **Debitorrelation** eller **Kreditorrelation** skal du vælge en specifik debitor eller kreditor, hvis du angiver feltet **Kontokode** til *Tabel*. Hvis du har valgt **Gruppe** i feltet *Kontokode*, skal du vælge en gebyrgruppe for kreditorer eller debitorer.
1. I feltet **Varekode** skal du vælge en af følgende værdier for at angive omfanget af de varer, der påvirkes: Du kan kun vælge en varekode, når du definerer automatiske gebyrer på linjeniveau.

    - *Tabel* – Tildel gebyrer til en bestemt vare.
    - *Gruppe* – Tildel gebyrer til en bestemt varegebyrgruppe.
    - *Alle* – Tildel gebyrer til alle varer.

1. Hvis du vælger **Tabel** i feltet **Varekode**, skal du vælge en bestemt vare i feltet *Varerelation*. Hvis du har valgt **Gruppe** i feltet *Varekode*, skal du vælge en varegebyrgruppe.
1. **Kun for salgsordrer:** I feltet **Kode for leveringsmåde** skal du vælge en af følgende værdier for at angive det omfang af leveringsmåder, der vil blive påvirket:

    - *Tabel* – Tildel gebyrer til en bestemt leveringsmåde.
    - *Gruppe* – Tildel gebyrer til en bestemt gruppe af leveringsmåder.
    - *Alle* – Tildel gebyrer til alle leveringsmåder.

1. **Kun for salgsordrer:** Hvis du vælger **Tabel** i feltet **Kode for leveringsmåde**, skal du vælge en bestemt leveringsmåde i feltet *Leveringsmåderelation*. Hvis du vælger **Gruppe** i feltet *Kode for leveringsmåde*, skal du vælge en leveringsmådegruppe.
1. I oversigtspanelet **Linjer** skal du definere de gebyrer og gebyrsatser, der skal anvendes, når det aktuelle automatiske gebyr anvendes. Du kan bruge værktøjslinjen i dette oversigtspanel til at tilføje så mange linjer, du har brug for. For hver linje skal du angive følgende felter:

    - **Valuta** – Vælg den valuta, der skal bruges til beregning af gebyret.
    - **Gebyrkode** – Vælg koden for gebyret.
    - **Kategori** – Vælg en af følgende værdier:

        - *Fast* – Gebyret angives som et fast beløb på linjen. Faste gebyrer kan bruges både i ordrehovedet og på ordrelinjerne.
        - *Styk* – Gebyret er baseret på enheden. Disse tillæg kan kun bruges på ordrelinjerne. De vises, når du beregner den samlede ordretotal.
        - *Procent* – Gebyret angives som en procentdel på linjen. Procentgebyrer kan bruges både i ordrehovedet og på ordrelinjerne.
        - *Intern procent* – Gebyret angives som en procentdel på linjen for interne ordrer. Interne procentvise gebyrer kan kun bruges på ordrelinjerne.
        - *Ekstern* – Gebyret beregnes af en tredjepartstjeneste, der er knyttet til en eller flere fragtmænd.

    - **Gebyrværdi** – Angiv gebyrværdien baseret på den valgte kategori.
    - **Gebyrvalutakode** – Angiv en valuta til gebyret, hvis du vil bruge en anden valuta end den valuta, som du har angivet i feltet **Valuta**. Du kan kun bruge en anden valuta, hvis **Debet** eller **Kredittype** for den valgte gebyrkode er indstillet til *Finanskonto* eller *Vare*.
    - **Fra beløb** – Angiv et startbeløb, det automatiske gebyr skal anvendes på. Beløb i denne sammenhæng refererer til det samlede ordrebeløb.
    - **Til beløb** – Angiv et slutbeløb, det automatiske gebyr skal anvendes på. Beløb i denne sammenhæng refererer til det samlede ordrebeløb.
    - **Momsgruppe** – Angiv en momsgruppe.
    - **Lokation** og **Lagersted** – Angiv en lokation og et lagersted, hvis der kun skal anvendes gebyrer for en bestemt lokation og lagersted.
    - **Behold** – Markér afkrydsningsfeltet for at bevare gebyrposteringerne efter fakturering er fuldført, så gebyret anvendes, hver gang du opretter en ny faktura for den valgte debitorkonto.

1. **Kun for salgsordrer:** Hvis du vil beregne lagdelte gebyrer, skal du se [Lagdelte gebyrer på salgsordrer](/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) for at få oplysninger.

## <a name="allocate-charges-from-the-header-to-a-line"></a>Tildele gebyrer fra overskriften til en linje

Følgende fremgangsmåde viser, hvordan du kan tildele gebyrer på overskriftsniveau til en linje. Før du starter denne procedure, skal du allerede have et overskriftsgebyr for typen *faste beløb* og en ordre, hvor gebyret anvendes. Ordren skal desuden allerede indeholde mindst ét linjeelement.

1. Åbn indkøbsordren eller gebyrordren.
1. Benyt en af følgende fremgangsmåder i handlingsruden:

    - For indkøbsordrer: Vælg **Fordel gebyrer** i gruppen **Gebyrer** under fanen **Indkøb**.
    - For salgsordrer: Vælg **Fordel gebyrer** i gruppen **Gebyrer** under fanen **Salg**.

1. I dialogboksen **Fordel gebyrer på ordrelinjer** skal du angive følgende felter:

    - **Gebyrtildeling** – Vælg en af følgende værdier for at angive, hvordan gebyrerne skal fordeles:

        - *Nettobeløb* – Tildel gebyrer relativt for de enkelte linjebeløb i forhold til det samlede nettobeløb.
        - *Antal* – Fordel gebyrer i forhold til antallet af enheder for hver linje i forhold til det samlede antal enheder.
        - *Pr. linje* – Fordel gebyrer ligeligt mellem det samlede antal linjer.

    - **Fordel gebyrer på linjer** – Vælg en værdi for at angive, om gebyrer skal fordeles på alle linjer, kun på positive linjer eller kun på negative linjer.
    - **Fordel alt** – Markér dette afkrydsningsfelt for at fordele gebyrer til ordrelinjer, også selvom gebyrkoden har en anden debettype end *Vare*.
    - **Modtaget** – Markér dette afkrydsningsfelt for udelukkende at fordele gebyrer til modtagne ordrelinjer.
    - **Lagerført** – Markér dette afkrydsningsfelt for udelukkende at fordele gebyrer til lagerførte ordrelinjer.
    - **Vis valg, og ryd bestemte linjer** – Markér dette afkrydsningsfelt for at udelukke bestemte linjer fra denne fordeling. Når du markerer dette afkrydsningsfelt, åbnes **Vælg linjer, der skal udelades fra fordeling**-gitteret. Gitteret indeholder kun de linjer, der opfylder kriterierne i felterne **Fordel gebyrer til linjer** og **Lagerført**. Hvis du f.eks. vælger **Positive linjer** i feltet *Fordel gebyrer til linjer* og vælger indstillingen **Lagerført**, vises kun linjer, som både er positive og lagerførte i gitteret. Desuden filtrerer gitteret automatisk de linjer fra, hvor hele antallet allerede er modtaget. Når gitteret er åbent, skal du fjerne markeringen i afkrydsningsfeltet **Medtag** for hver linje, der skal udelades fra tildelingen. 

        > [!IMPORTANT]
        > Når du arbejder med **Vælg linjer, der skal udelades fra fordeling**-gitteret, skal du sørge for at lade gitteret være åbent, indtil du vælger **Alloker**. Hvis du lukker gitteret, før du vælger **Alloker**, går dine indstillinger i gitteret tabt. Derfor tildeles gebyrer ud fra de kriterier, du tidligere har defineret.

1. Vælg **Alloker** for at anvende dine indstillinger og lukke dialogboksen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
