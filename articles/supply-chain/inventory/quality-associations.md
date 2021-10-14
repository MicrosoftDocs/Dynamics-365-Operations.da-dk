---
title: Kvalitetstilknytninger
description: I dette emne beskriver, hvordan du kan bruge kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til automatisk at generere kvalitetsordrer, der er relateret til dine salgs-, indkøbs- og produktionsprocesser.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28984730e5660414eec1ba087eb5de1eba4cbbb8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571923"
---
# <a name="quality-associations"></a>Kvalitetstilknytninger

[!include [banner](../includes/banner.md)]

I dette emne beskriver, hvordan du kan bruge kvalitettilknytninger i Microsoft Dynamics 365 Supply Chain Management til automatisk at generere kvalitetsordrer, der er relateret til dine salgs-, indkøbs- og produktionsprocesser.

En kvalitetstilknytning angiver alle følgende oplysninger for en kvalitetsordre, der oprettes:

- Posteringshændelsen
- Det sæt test, der skal udføres på varerne
- Det acceptable kvalitetsniveau (AQL)
- Prøveplanen

Du skal definere en kvalitetstilknytning for hver afvigelse i en forretningsproces, der kræver automatisk generering af kvalitetsordrer. For eksempel kan der oprettes en kvalitetsordre i forretningsprocesserne for indkøbsordrer, karantæneordrer, salgsordrer og produktionsordrer.

## <a name="working-with-quality-associations"></a>Arbejde med kvalitetstilknytninger

Den forretningsproces, der bruger en kvalitetstilknytning, kan knyttes til forskellige kildedokumenter, f.eks. indkøbsordrer, salgsordrer eller produktionsordrer.

De enkelte kvalitetstilknytningsposter definerer de test, det acceptable kvalitetsniveau (AQL) og den vareprøveplan, der gælder for de kvalitetsordrer, der oprettes. Du skal definere en kvalitetstilknytningspost for hver ændring i en forretningsproces. Du kan f.eks. angive en kvalitetstilknytning, der genererer en kvalitetsordre, når en produktkvittering for en indkøbsordre opdateres. Afhængigt af opsætningen af udførelsesplanen kan selve udløserprocessen blokeres, mens der er en åben kvalitetsordre. Efterfølgende processer, f.eks. fakturering af indkøbsordrer, kan også blokeres.

> [!NOTE]
> Der kan være åbne kvalitetsordrer, men lagerantal blokeres automatisk fra at blive udstedt. Afhængigt af indstillingen for feltet **Fuld blokering** på siden **Varestikprøver** er antallet enten kvantiteten i kvalitetsordren eller kvantiteten i kildedokumentlinjen. Du kan finde flere oplysninger under [Varestikprøver for kvalitetsstyring](quality-item-sampling.md).

For en given virksomhedsproces identificerer kvalitetstilknytningsposten den hændelse og de betingelser, som en kvalitetsordre genereres for. Betingelserne kan være specifikke for et sted eller en juridisk enhed. En kvalitetsordre, der involverer destruktive prøvninger, kan kun oprettes, når der findes en disponible lagerbeholdning for hændelsen.

Du kan arbejde med kvalitetstilknytninger ved at gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetstilknytninger**. Følgende eksempler viser, hvordan en kvalitetstilknytningspost defineres for variationerne i de enkelte virksomhedsprocesser. Eksemplerne vises også i følgende tabel som en oversigt over de hændelser og betingelser, der er defineret af en kvalitetstilknytningspost.

<table>
<thead>
<tr>
<th>Referencetype</th>
<th>Hændelsestype</th>
<th>Udførelse</th>
<th>Hændelsesspærring</th>
<th>Dokumentreference</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lager</td>
<td>Ikke tilgængelig</td>
<td>Ikke tilgængelig</td>
<td>Ingen</td>
<td>Alle</td>
</tr>
<tr>
<td rowspan="7">Salg</td>
<td rowspan="4">Plukproces er planlagt</td>
<td rowspan="4">Før</td>
<td>Ingen</td>
<td rowspan="22">Bestemt id, gruppe eller kun alle</td>
</tr>
<tr>
<td>Plukproces</td>
</tr>
<tr>
<td>Følgeseddel</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Følgeseddel</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Følgeseddel</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="15">Indkøb</td>
<td rowspan="7">Tilgangsliste</td>
<td rowspan="4">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Tilgangsliste</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="3">Registrering</td>
<td rowspan="3">Ikke tilgængelig</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="5">Produktkvittering</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Produktkvittering</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="2">Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Faktura</td>
</tr>
<tr>
<td rowspan="8">Produktion</td>
<td rowspan="3">Registrering</td>
<td rowspan="3">Ikke tilgængelig</td>
<td>Ingen</td>
<td rowspan="12">Alle</td>
</tr>
<tr>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="5">Færdigmeld</td>
<td rowspan="3">Før</td>
<td>Ingen</td>
</tr>
<tr>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="2">Efter</td>
<td>Ingen</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="4">Karantæne</td>
<td rowspan="3">Færdigmeld</td>
<td rowspan="2">Før</td>
<td>Færdigmeld</td>
</tr>
<tr>
<td>Afslut</td>
</tr>
<tr>
<td>Efter</td>
<td>Afslut</td>
</tr>
<tr>
<td>Afslut</td>
<td>Før</td>
<td>Afslut</td>
</tr>
<tr>
<td rowspan="3">Ruteoperation</td>
<td rowspan="3">Færdigmelding</td>
<td rowspan="2">Før</td>
<td>None</td>
<td rowspan="3">Specifik Id, Gruppe eller Alle, og specifik Ressource, Gruppe eller Alle</td>
</tr>
<tr>
<td>Færdigmelding</td>
</tr>
<tr>
<td>Efter</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">Produktion af samprodukter</td>
<td>Registrering</td>
<td>Ikke anvendelig</td>
<td rowspan="3">None</td>
<td rowspan="3">Alt</td>
</tr>
<tr>
<td rowspan="2">Færdigmelding</td>
<td>Før</td>
</tr>
<tr>
<td>Efter</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Funktionen *Kvalitetsstyring for lagerstedsprocesser* føjer funktioner til behandlingen af kvalitetsordrer for produktion, hvor feltet **Hændelsestype** er angivet til *Færdigmelding* og feltet **Udførelse** er angivet til *Efter*, og til køb, hvor feltet **Hændelsestype** er angivet til *Registrering*. Du kan finde flere oplysninger i [Kvalitetsstyring for lagerstedsprocesser](quality-management-for-warehouses-processes.md).

Tabellen nedenfor indeholder flere oplysninger om, hvordan kvalitetsordrer kan oprettes for bestemte typer processer.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Procestype</th>
<th>Når kvalitetsordrer kan genereres automatisk</th>
<th>Når kvalitetsordrer kan genereres, hvis destruktiv prøvning er påkrævet</th>
<th>Betingelsesoplysninger</th>
<th>Manuel oprettelse af oplysninger</th>
</tr>
</thead>
<tbody>
<tr>
<td>Indkøbsordre</td>
<td>Før eller efter en tilgangsliste eller produktkvittering for det materiale, der er modtaget, bogføres</td>
<td>Efter produktkvitteringen for det materiale, der er modtaget, bogføres, da materialet skal være tilgængelig til destruktiv prøvning</td>
<td>Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller leverandør eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en indkøbsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Karantæneordre</td>
<td>Før eller efter karantæneordren rapporteres som færdigmeldt eller afsluttet</td>
<td>Kvalitetsordrer, der kræver destruktive test, kan ikke genereres. Det antages, at funktionen til karantæneordrer håndterer bortskaffelsen af det materiale, der skal destrueres.</td>
<td>Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller leverandør eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en karantæneordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Salgsordre</td>
<td>Før en planlagt plukproces eller opdatering af følgesedlen for de varer, der skal leveres</td>
<td>På alle trin</td>
<td>Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller kunde eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en salgsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Produktionsordre</td>
<td>Før eller efter det færdigmeldte antal for produktionsordren er rapporteret</td>
<td>Efter det færdigmeldte antal for produktionsordren er rapporteret</td>
<td>Behovet for en kvalitetsordre kan afhænge af en specifik lokation eller vare eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en produktionsordre, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Produktionsordre, der har en ruteoperation</td>
<td>Før eller efter rapporten er færdigmeldt for en operation</td>
<td>Efter færdigrapportering af produktionen for den sidste operation</td>
<td>Behovet for en kvalitetsordre kan afhænge af en specifik lokation, vare eller operationsressource eller en kombination af disse forhold.</td>
<td>En manuelt oprettet kvalitetsordre, der refererer til en ruteoperation, kan bruge oplysninger i en kvalitetstilknytningspost, som f.eks. prøveudtagningsplanen.</td>
</tr>
<tr>
<td>Lagerbeholdning</td>
<td>En kvalitetsordre kan ikke genereres automatisk for en transaktion i en lagerkladde eller for flytteordretransaktioner.</td>
<td></td>
<td></td>
<td>En kvalitetsordre skal oprettes manuelt for en vares lagerantal. Fysisk disponibel lagerbeholdning er påkrævet.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Eksempler på automatisk oprettelse af kvalitetsordrer

### <a name="purchasing"></a>Køb

Hvis du i forbindelse med indkøb angiver feltet **Hændelsestype** til *Produktkvittering* og feltet **Udførelse** til *Efter* på siden **Kvalitetstilknytninger**, får du følgende resultater:

- Hvis indstillingen **Pr. opdateret antal** er angivet til *Ja*, genereres der en kvalitetsordre for hver kvittering i forhold til indkøbsordren baseret på det modtagne antal og indstillinger i stikprøven af vare. Hver gang der modtages et antal på indkøbsordren, oprettes der nye kvalitetsordrer ud fra det nye antal, der er modtaget.
- Hvis indstillingen **Pr. opdateret antal** er angivet til *Nej*, genereres der en kvalitetsordre for den første kvittering i forhold til indkøbsordren baseret på det modtagne antal. Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne. Kvalitetsordrer genereres ikke for efterfølgende kvitteringer i forhold til indkøbsordren.

### <a name="production"></a>Produktion

Hvis du i forbindelse med produktion angiver feltet **Hændelsestype** til *Færdigmelding* og feltet **Udførelse** til *Efter* på siden **Kvalitetstilknytninger**, får du følgende resultater:

- Hvis indstillingen **Pr. opdateret antal** er angivet til *Ja*, genereres der en kvalitetsordre baseret på hvert færdige antal og indstillinger i stikprøven af vare. Hver gang et antal færdigmeldes på indkøbsordren, genereres der nye kvalitetsordrer ud fra det nye antal færdigmeldte varer. Denne genereringslogik stemmer overens med indkøb.
- Hvis indstillingen **Pr. opdateret antal** er angivet til *Nej*, genereres der en kvalitetsordre, første gang et antal færdigmeldes, baseret på det færdige antal. Derudover oprettes en eller flere kvalitetsordrer ud fra det resterende antal afhængigt af sporingsdimensionerne for stikprøven af varen. Kvalitetsordrer genereres ikke for efterfølgende færdige antal.

<table>
<thead>
<tr>
<th>Kvalitetsspecifikation</th>
<th>Pr. opdateret antal</th>
<th>Pr. sporingsdimension</th>
<th>Resultat</th>
</tr>
</thead>
<tbody>
<tr>
<td>Procent: 10 %</td>
<td>Ja</td>
<td>
<p>Batchnummer: Nej</p>
<p>Serienummer: Nej</p>
</td>
<td>
<p>Ordreantal: 100</p>
<ol>
<li>Færdigmelding for 30
<ul>
<li>Kvalitetsordre 1 for 3 (10 % af 30)</li>
</ul>
</li>
<li>Færdigmelding for 70
<ul>
<li>Kvalitetsordre. 2 for 7 (10 % af det resterende ordreantal, hvilket er lig med 70 i dette tilfælde)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fast antal: 1</td>
<td>Ingen</td>
<td>
<p>Batchnummer: Nej</p>
<p>Serienummer: Nej</p>
</td>
<td>Ordreantal: 100
<ol>
<li>Færdigmelding for 30
<ul>
<li>Kvalitetsordre 1 for 1 (for det første færdigmeldte antal, der har en fast værdi af 1)</li>
<li>Kvalitetsordre 2 for 1 (for det resterende antal, der stadig har en fast værdi af 1)</li>
</ul>
</li>
<li>Færdigmelding for 10
<ul>
<li>Der oprettes ingen kvalitetsordrer.</li>
</ul>
</li>
<li>Færdigmelding for 60
<ul>
<li>Der oprettes ingen kvalitetsordrer.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fast antal: 1</td>
<td>Ja</td>
<td>
<p>Batchnummer: Ja</p>
<p>Serienummer: Ja</p>
</td>
<td>
<p>Ordreantal: 10</p>
<ol>
<li>Færdigmelding for 3: 1 for batchnummer b1, serienummer s1, 1 for batchnummer b2, serienummer s2 og 1 for batchnummer b3, serienummer s3
<ul>
<li>Kvalitetsordre 1 for 1 af batchnummer b1, serienummer s1</li>
<li>Kvalitetsordre 2 for 1 af batchnummer b2, serienummer s2</li>
<li>Kvalitetsordre 3 for 1 af batchnummer b3, serienummer s3</li>
</ul>
</li>
<li>Færdigmelding for 2: 1 for batchnummer b4, serienummer s4 og 1 for batchnummer b5, serienummer s5
<ul>
<li>Kvalitetsordre 4 for 1 af batchnummer b4, serienummer s4</li>
<li>Kvalitetsordre 5 for 1 af batchnummer b5, serienummer s5</li>
</ul>
</li>
</ol>
<p><strong>Bemærk:</strong> Batchen kan genbruges.</p>
</td>
</tr>
<tr>
<td>Fast antal: 2</td>
<td>Ingen</td>
<td>
<p>Batchnummer: Ja</p>
<p>Serienummer: Ja</p>
</td>
<td>
<p>Ordreantal: 10</p>
<ol>
<li>Færdigmelding for 4: 1 for batchnummer b1, serienummer s1, 1 for batchnummer b2, serienummer s2, 1 for batchnummer b3, serienummer s3 og 1 for batchnummer b4, serienummer 4
<ul>
<li>Kvalitetsordre 1 for 1 af batchnummer b1, serienummer s1</li>
<li>Kvalitetsordre 2 for 1 af batchnummer b2, serienummer s2</li>
<li>Kvalitetsordre 3 for 1 af batchnummer b3, serienummer s3</li>
<li>Kvalitetsordre 4 for 1 af batchnummer b4, serienummer s4</li>
</ul>
<ul>
<li>Kvalitetsordre 5 for 2, uden en reference til et batchnummer eller et serienummer</li>
</ul>
</li>
<li>Færdigmelding for 6: 1 for batchnummer b5, serienummer s5, 1 for batchnummer b6, serienummer s6, 1 for batchnummer b7, serienummer s7, 1 for batchnummer b8, serienummer s8, 1 for batchnummer b9, serienummer s9 og 1 for batchnummer b10, serienummer s10
<ul>
<li>Der oprettes ingen kvalitetsordrer.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Yderligere ressourcer

- [Processer for kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
