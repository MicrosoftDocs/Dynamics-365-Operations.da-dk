---
title: Konfigurere parameterværdier for efterkalkulation
description: Når du konfigurerer modulet Landingsomkostninger, kan du definere flere sæt af fælles værdier, som er tilgængelige, når du vælger bestemte typer parameterværdier for efterkalkulation i andre dele af appen. I dette emne forklares, hvordan du konfigurerer disse værdisæt.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 51c3360afc48f4f9143118ee6139803b95e5df28
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500472"
---
# <a name="costing-parameter-values-setup"></a>Konfigurere parameterværdier for efterkalkulation

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Når du konfigurerer modulet **Landingsomkostninger**, kan du definere flere sæt fælles værdier og relaterede indstillinger pr. værdi. Disse værdier vil derefter være tilgængelige, når du vælger bestemte typer parameterværdier for efterkalkulation i andre dele af appen. I dette emne forklares, hvordan du konfigurerer disse værdisæt.

## <a name="set-up-cost-type-codes"></a>Konfigurere omkostningstypekoder

Omkostningstypekoder bestemmer, hvilken omkostningstype der påløber, når varerne ankommer på lagerstedet, eller de fragtens landingsomkostninger. Selvom de normalt øger varernes værdi, kan de også bruges til at periodisere beløb i finansmodulet. Finansreguleringer bruges, når en omkostning periodiseres over tid, eller under en række fragter, og modposteres i en enkelt transaktion.

> [!NOTE]
> Hvis tabellen med omkostningstyper deles på tværs af juridiske enheder, skal kontoplanen også deles på tværs af juridiske enheder. Ellers fungerer bogføringstransaktionerne ikke korrekt.

Du kan konfigurere dine omkostningstypekoder ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Omkostningstypekoder**. Du kan bruge knapperne i handlingsruden til at oprette nye omkostningstypekoder, redigere eksisterende koder eller slette en valgt omkostningstype.

I følgende tabel forklares de felter, der er tilgængelige for hver omkostningstypekode.

| Felt | Beskrivelse |
|---|---|
| Omkostningstypekode | Angiv et navn til omkostningstypekoden. |
| Beskrivelse | Angiv en beskrivelse af omkostningstypekoden. |
| Brug forsendelsessats | Angiv denne indstilling til *Ja*, hvis fragtens valutakurs (også kaldet en styringskurs) skal bruges til at beregne værdien af disse omkostninger. I dette tilfælde vil forsendelsessatsen blive brugt i stedet for standardværdien eller spotvalutakursen til fakturaer i udenlandsk valuta. |
| Rapporteringskategori | Dette felt opretter en rapporteringskategori for omkostningstypen. Rapporter kan udskrives enten af rapporteringskategorier eller efter omkostningstype. |
| Debettype | Vælg, om omkostningstypen skal debitere varen, finanskontoen eller kreditoren. |
| Debetkontering | Hvis feltet **Debettype** er angivet til *Finanskonto*, skal du vælge bogføringsbeskrivelsen. |
| Debetkonto | Hvis feltet **Debettype** er angivet til *Finanskonto*, skal du vælge den finanskonto, der skal bruges. |
| Kredittype | Vælg, om omkostningstypen skal kreditere varen, finanskontoen eller kreditoren. |
| Kreditkontering | Hvis feltet **Kredittype** er angivet til *Finanskonto*, skal du vælge bogføringsbeskrivelsen. |
| Kreditkonto | Hvis feltet **Kredittype** er angivet til *Finanskonto*, skal du vælge den finanskonto, der skal bruges. |
| Clearingkonto | Vælg clearingkontoen for omkostningstypen: Det anbefales, at du angiver en separat clearingkonto pr. omkostningstype som hjælp til afstemningen. |
| Standardbogføringstype for omkostning | Hvis du bruger standardefterkalkulation, skal du vælge bogføringsbeskrivelsen. |
| Konto for standardomkostningsafvigelse | <p>Hvis du bruger standardefterkalkulation, bruges den konto, der er angivet her, til at bogføre en afvigelse. Denne konto bruger fordelingen af landingsomkostninger på siden **Varepriser**. Denne fordeling oprettes ved hjælp af den periodiske rutine til opdatering af priser.</p><p>Standardkostprisen for en vare er f.eks. $15,00, FOB er $13,00, og fragten er $2,00. Når fakturaen modtages for lageret, modtages varen til $15,00, men der er en standardprisafvigelse på $2,00 for varen, fordi den faktiske FOB er $13,00. Denne afvigelse bogføres på den standardkonto til prisafvigelse, der er konfigureret i varebogføringsprofilen. Da den forkalkulerede fragt er $2,00, er der ingen afvigelse, når lagerfakturaen bogføres. Når fakturaen for fragten modtages, vil fragten dog blive $2,50 pr. enhed. Derfor bogføres $0,50 som afvigelse i den angivne omkostning. |
| Konto for afvigelse i glidende gennemsnit | <p>Hvis du bruger efterkalkulation med glidende gennemsnit, bruges den konto, der er angivet her, til at bogføre en afvigelse.</p><p>Den forkalkulerede fragt er f.eks. $2,00. Når fakturaen for fragten modtages, vil fragten dog blive $2,50 pr. enhed. Derfor skal $0,50 bogføres som afvigelse.</p><p>Når indstillingen **Bogfør reguleringer som afvigelse** er angivet til *Ja* på siden **Parametre for landingsomkostninger**, bogføres alle afvigelser mellem de forventede og faktiske forsendelsesomkostninger på den konto for afvigelse i glidende gennemsnit, som angives her. Når indstillingen **Bogfør reguleringer som afvigelse** er angivet til *Nej*, bruges standardfunktionaliteten, og afvigelsen anvendes enten på lageret eller på den konto for afvigelse i glidende gennemsnit, som er angivet her, afhængigt af lagerbeholdningen.</p> |
| Periodiseringskonto for gebyr | Vælg den konto, der skal bruges til periodisering af omkostningsestimater, når indkøbsfakturaen bogføres. Dette felt bruges kun, når indstillingen **Brug gebyrkonto for periodisering af omkostningstype** er angivet til *Ja* i oversigtspanelet **Efterkalkulation** under fanen **Generelt** på siden **Parametre for landingsomkostninger**. |
| Gebyrkonto | Vælg den konto, der bruges til at registrere de indgående transportomkostninger, som er faktureret af en leverandør. Beløbet bogføres som debet. Modkontoen er kontoen til lagervariation. Denne bogføring bruges kun, når indstillingen **Bogfør på omkostningskontoen i finans** er angivet til *Ja* på siden **Kreditorparametre**. |
| Afvigelseskonto | Den konto, der skal bruges som modkonto for gebyrperiodiseringer, når indkøbsfakturaen bogføres. Dette felt bruges kun, når indstillingen **Brug gebyrkonto for periodisering af omkostningstype** er angivet til *Ja* i oversigtspanelet **Efterkalkulation** under fanen **Generelt** på siden **Parametre for landingsomkostninger**. |

## <a name="vendor-cost-type-groups"></a>Omkostningstypegrupper for leverandør

Du kan bruge kosttypegrupper for kreditorer til at bestemme, hvordan *automatiske omkostningsgebyrer* kan findes og anvendes på en fragt. Kreditorer, der har ens importomkostninger, er kædet sammen. Alle leverandører fra nye markeder betaler f.eks. samme afgiftsprocent for den samme type produkt, der købes fra et eksisterende marked.

Du kan vedligeholde kreditoromkostningstypegrupper ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Kreditoromkostningstypegrupper**. Siden **Kreditoromkostningstypegrupper** indeholder et gitter, der viser alle eksisterende omkostningstypegrupper for kreditorer. Du kan tilføje, fjerne og redigere rækker i gitteret ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de felter, der er tilgængelige for hver række i gitteret.

| Felt | Beskrivelse |
|---|---|
| Omkostningstypegrupper for leverandør | Angiv et entydigt navn til omkostningstypegruppen for kreditorer (f.eks. *Nye markeder*). |
| Beskrivelse | Angiv en beskrivelse af omkostningstypegruppen for kreditorer. Denne beskrivelse kan indeholde oplysninger om niveau eller type af gebyr, der er knyttet til kreditorgruppen. |

## <a name="item-cost-type-groups"></a>Omkostningstypegrupper for vare

Du kan bruge kosttypegrupper for varer til at bestemme, hvordan *automatiske omkostningsgebyrer* kan findes og anvendes på en fragt. Lignende varer er kædet sammen. Alle varer med en afgiftssats på 5 procent kan f.eks. tilhøre en bestemt omkostningstypegruppe.

Du kan vedligeholde omkostningstypegrupper for varer ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Omkostningstypegrupper for varer**. Siden **Omkostningstypegrupper for varer** indeholder et gitter, der viser alle eksisterende omkostningstypegrupper for varer. Du kan tilføje, fjerne og redigere rækker i gitteret ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de felter, der er tilgængelige for hver række i gitteret.

| Felt | Beskrivelse |
|---|---|
| Omkostningstypegrupper for vare | Angiv et entydigt navn til omkostningstypegruppen for varer (f.eks. *Afgift 5 %*). |
| Beskrivelse | Angiv en beskrivelse af omkostningstypegruppen for varer. Denne beskrivelse kan indeholde oplysninger om niveau eller type af gebyr, der er knyttet til varegruppen. |

> [!NOTE]
> Vareomkostningstypen er knyttet til varen via feltet **Omkostningstypegruppe** i oversigtspanelet **Indkøb** på siden **Frigivne produkter** for varen.

## <a name="transfer-order-cost-type-groups"></a>Omkostningstypegrupper for flytteordre

Du kan bruge omkostningstypegrupper for flytteordrer til at bestemme, hvordan *automatiske omkostningsgebyrer* kan findes. Lignende varer er kædet sammen. Alle varer med en afgiftssats på 7 procent kan f.eks. tilhøre en bestemt omkostningstypegruppe.

Du kan vedligeholde omkostningstypegrupper for flytteordrer ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Omkostningstypegrupper for flytteordrer**. Siden **Omkostningstypegrupper for flytteordrer** indeholder et gitter, der viser alle eksisterende omkostningstypegrupper for flytteordrer. Du kan tilføje, fjerne og redigere rækker i gitteret ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de indstillinger, der er tilgængelige for hver række i gitteret.

| Felt | Beskrivelse |
|---|---|
| Omkostningstypegrupper for flytteordre | Angiv et entydigt navn til omkostningstypegruppen for flytteordrer (f.eks. *Afgift 7 %*). |
| Beskrivelse | Angiv en beskrivelse af omkostningstypegruppen for flytteordrer. Denne beskrivelse kan indeholde oplysninger om niveau eller type af gebyr, der er knyttet til omkostningstypegruppen for flytteordrer. |

> [!NOTE]
> Omkostningstypen for flytteordrer er knyttet til varen via feltet **Omkostningsgruppe for flytteordrer** i oversigtspanelet **Indkøb** på siden **Frigivne produkter** for varen.

## <a name="cost-templates"></a>Omkostningsskabeloner

Du kan bruge omkostningsskabeloner til at angive standardværdier for indstillinger, som de brugere, der får estimatet over kostprisen, muligvis ikke kender. Omkostningsskabeloner kan være med til at reducere kompleksiteten i estimeringsprocessen ved at minimere de valg, brugerne skal foretage for at opnå et præcist estimat.

Du kan arbejde med omkostningsskabeloner ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Omkostningsskabeloner**. På siden **Omkostningsskabeloner** viser listeruden til venstre alle aktuelle omkostningsskabeloner. Du kan tilføje, fjerne og redigere skabeloner ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de indstillinger, der er tilgængelige for hver skabelon.

| Felt | Beskrivelse |
|---|---|
| Omkostningsskabelon | Angiv et entydigt navn til omkostningsskabelonen. Navnet beskriver typisk faktoren eller omkostningsmultiplikatoren for skabelonen. |
| Beskrivelse | Angiv en beskrivelse af omkostningsskabelonen. |
| Fragtfirma | Vælg leverandørkontoen for det fragtfirma, der skal knyttes til omkostningsskabelonen. |
| Leveringsmåde | Vælg den leveringsmåde, som omkostningsskabelonen skal bruge, når den forkalkulerede omkostning for en vare beregnes. Dette felt hjælper med at bestemme de automatiske omkostninger, der er knyttet til varerne i omkostningsestimatet. |
| Forsendelsescontainertype | Vælg den type af forsendelsescontainer, der skal knyttes til omkostningsskabelonen. Dette felt hjælper med at bestemme de automatiske omkostninger, der er knyttet til varerne i omkostningsestimatet. |
| Toldmægler | Vælg den toldmægler (kreditor), der skal tilknyttes omkostningsskabelonen. Dette felt hjælper med at bestemme de automatiske omkostninger, der er knyttet til omkostningsestimatet. |
| Faktor | Angiv en faktor, der skal anvendes på den endelige forkalkulerede vareomkostning. Hvis du f.eks. vil lægge 10 procent til det beregnede omkostningsestimat, skal du angive *1,10*. |

## <a name="volumetric-divisors"></a>Volumendivisorer

Volumendivisorer bruges til at beregne den volumenvægten. Hvert fragtfirma formulerer egne volumendivisorer. Derudover varierer et firmas divisorer typisk, afhængigt af leveringsmåden. Der er f.eks. ofte meget forskellige divisorer for luft- og skibsfragt. Et firma kan også gøre reglerne mere komplekse, afhængigt af hvor det afsender fra.

En pakke, der sendes med fly, har f.eks. en volumen på 3 kubikmeter (m³). Firmaet opkræver gebyrer efter volumenvægt og anvender en volumendivisor på 6. Denne divisor ganges med volumen for at bestemme volumenvægten. Volumenvægten i dette eksempel er derfor 3 × 6 = 18 kilogram (kg).

Du kan konfigurere volumendivisorer ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Volumendivisorer**. Siden **Volumendivisorer** indeholder et gitter, der viser alle eksisterende volumendivisorer. Du kan tilføje, fjerne og redigere rækker i gitteret ved at bruge knapperne i handlingsruden.

I følgende tabel forklares de felter, der er tilgængelige for hver række i gitteret.

| Felt | Beskrivelse |
|---|---|
| Fragtfirma | Vælg leverandørkontoen for det fragtfirma, der er knyttet til volumendivisoren. |
| Omkostningstypekode | Vælg den omkostningstypekode, der er tilknyttet volumendivisoren. Brug dette felt til at placere omkostningstyper i rapporteringspuljer. Rapporter kan udskrives enten af rapporteringskategorier eller efter omkostningstype. |
| Fra havn | Vælg den "fra"-havn som volumendivisoren gælder for. |
| Volumendivisor | Angiv den værdi af volumendivisoren, som gælder for rækken. Den værdi, du angiver, vil blive *ganget* med volumen af hver pakke for at bestemme pakkens volumenvægt. |
