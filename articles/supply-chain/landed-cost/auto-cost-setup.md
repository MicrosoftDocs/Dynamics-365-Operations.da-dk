---
title: Konfigurere automatiske omkostninger
description: Dette emne beskriver, hvordan du konfigurerer omkostningsregler for forskellige indgående niveauer. Ud fra disse regler beregner systemet omkostningerne og tilføjer dem automatisk. Brugerne behøver derfor ikke tilføje omkostningerne manuelt.
author: sherry-zheng
manager: tfehr
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 86dcbfbe6e00e7324e29541da6d682794e7487b3
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501144"
---
# <a name="auto-costs-setup"></a>Konfigurere automatiske omkostninger

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Du kan bruge siden **Automatiske omkostninger** til at definere omkostningsregler for forskellige omkostningsområder (f.eks. fragter, forsendelsescontainere, porteføljer, indkøbsordrer, varer eller flytteordrelinjer). Ud fra reglerne og de felter, brugerne vælger, når de opretter poster for et af omkostningsområderne, beregner systemet omkostningerne og tilføjer dem automatisk. Brugerne behøver derfor ikke tilføje omkostningerne manuelt.

Du kan arbejde med automatiske omkostninger ved at gå til **Landingsomkostninger \> Opsætning af efterkalkulation \> Automatiske omkostninger**. Konfigurer derefter dine regler for automatiske omkostninger som beskrevet i resten af dette emne.

## <a name="work-with-cost-areas"></a>Arbejde med omkostningsområder

Automatiske omkostninger fungerer ligesom samhandelsaftaler eller automatiske tillæg. Hver automatiske omkostningspost tilhører et bestemt omkostningsniveau. Brug feltet **Omkostningsområde** i listeruden på siden **Automatiske omkostninger** til at vælge det omkostningsområde, du vil arbejde med. Listeruden viser kun automatiske omkostninger, der tilhører det aktuelt valgte omkostningsområde. Eventuelle automatiske omkostninger, du opretter, vil tilhøre det aktuelt valgte omkostningsområde.

Omkostningsområder gør det muligt for systemet at fordele omkostninger på tværs af indkøbsordrelinjerne i et omkostningsområde. En omkostning for en forsendelsescontainer vil f.eks. fordele værdien på alle produkterne i den pågældende forsendelsescontainer. Hvis der er to eller flere forsendelsescontainere, kan der angives samme omkostningstype for hver container. Containertypen kan derfor bruges til at finde den korrekte automatiske omkostning.

## <a name="buttons-on-the-action-pane"></a>Knapper i handlingsruden

I følgende tabel beskrives de knapper, der er tilgængelige i handlingsruden på siden **Automatiske omkostninger**.

| Knap | Beskrivelse |
|---|---|
| Redigér | Rediger en eksisterende automatisk omkostning. |
| Nye | Opret en automatisk omkostning. |
| Delete | Slet en automatisk omkostning. |
| Kopier fra | Opret en ny post for automatisk omkostning, der er baseret på en eksisterende post. Derefter kan du frit redigere den nye post. Denne knap hjælper dig med hurtigt at oprette nye automatiske omkostninger. |
| Vis dimensioner | Åbn en dialogboks, hvor du kan vælge de lagerdimensioner, der skal vises for de omkostningstransaktioner, du får vist. Hvis du fjerner markeringen i afkrydsningsfelterne, vises der færre lagerdimensioner for omkostningstransaktionerne. Der vises derfor færre detaljer for transaktionen. Hvis der er angivet en lagerdimension for en automatisk omkostning, anvendes den automatiske omkostning kun, når den angivne lagerdimension bruges for varen i en fragt. |

## <a name="settings-on-the-header"></a>Indstillinger i overskriften

Kombinationen af indstillinger i overskriften afgør, hvornår og hvordan en bestemt automatisk omkostning skal føjes til en fragt. En automatisk omkostning anvendes kun for en fragt, forsendelsescontainer eller folio, når oplysningerne om den automatiske omkostning svarer til oplysningerne i overskriften til det pågældende omkostningsområde. Summen af alle matchende automatiske omkostninger bestemmer den forkalkulerede landingsomkostning for en fragt. Denne omkostning fordeles på tværs af alle varerne i fartøjet eller fragten.

I følgende tabel forklares alle de felter, der kan være tilgængelige i overskriften. De tilgængelige felter afhænger dog af, hvilket omkostningsområde og hvilke dimensioner der er valgt i øjeblikket.

| Felt | Beskrivelse |
|---|---|
| **Kontokode** | <p>Vælg en af følgende værdier:</p><ul><li>**Tabel** – Omkostningsreglen gælder kun for en bestemt leverandør.</li><li>**Gruppe** – Omkostningsreglen gælder for en bestemt leverandørgruppe. Systemet søger efter den [leverandøromkostningstypegruppe](costing-parameters-setup.md), der er knyttet til leverandørposten.</li><li>**Alle** – Omkostningsreglen anvendes til alle leverandører. |
| **Fragtfirma** | Vælg den leverandør eller leverandørgruppe, som omkostningsreglen gælder for. Dette felt er kun tilgængeligt, hvis du vælger enten *Tabel* eller *Gruppe* i feltet **Kontokode**. |
| **Toldmægler** | Vælg den leverandør eller leverandørgruppe, som omkostningsreglen gælder for. Dette felt er kun tilgængeligt, hvis du vælger enten *Tabel* eller *Gruppe* i feltet **Kontokode**. |
| **Varekode** | <p>Vælg en af følgende værdier:</p><ul><li>**Tabel** – Omkostningsreglen gælder kun for en bestemt vare.</li><li>**Gruppe** – Omkostningsreglen gælder for en bestemt varegruppe. Systemet søger efter den [vareomkostningstypegruppe](costing-parameters-setup.md), der er knyttet til vareposten.</li><li>**Alle** – Omkostningsreglen anvendes til alle varer.|
| **Varerelation** | Vælg den vare eller varegruppe, som omkostningsreglen gælder for. Dette felt er kun tilgængeligt, hvis du vælger enten *Tabel* eller *Gruppe* i feltet **Varekode**. |
| **Leveringsmåde** | Vælg den leveringsmåde (f.eks. fly eller skibsfragt), som omkostningsreglen gælder for. |
| **Containertype** | Den type forsendelsescontainer, varerne afsendes i. En automatisk omkostning kan kun anvendes for en fragt, hvis containertypen i den automatiske omkostningsopsætning svarer til containertypen for fragten. |
| **Fra havn** og **Til havn** | Kildens ("fra") havn og destinationens ("til") havn i fragten. (Nogle forsendelsescontainere kan have forskellige "til"-havne, fordi fragten kan stoppe ved flere havne). En automatisk omkostning kan kun anvendes for en fragt, hvis havnene "fra" og "til" i opsætningen af automatiske omkostninger stemmer overens med havnene "fra" og "til" for fragten. |
| **Automatisk omkostningsnummer** | Angiv det entydige id til reglen for automatiske omkostninger. Værdien i dette felt genereres automatisk på basis af den nummerserie, der er konfigureret på siden **Parametre for landingsomkostninger**. |
| **Lagerdimensioner** | Nogle omkostningsområder giver dig mulighed for at medtage en eller flere varedimensioner i overskriften (f.eks. størrelse, farve, lagersted og batchnummer). Vælg **Vis dimensioner** i handlingsruden for at vælge de dimensioner, der skal medtages. |

## <a name="settings-on-the-lines-fasttab"></a>Indstillinger i oversigtspanelet Linjer

Tilføj en række for hver valuta, der kan bruges, når en omkostning anvendes på en indkøbsordrelinje til en fragt, i oversigtspanelet **Linjer**. 

For varer og indkøbsordrer vil systemet matche valutaen for hver indkøbsordrelinje i forhold til de valutaer, der er angivet i oversigtspanelet **Linjer**. Det vil kun anvende den kostværdi, der er angivet for den tilsvarende linje eller vare. Hvis der ikke er konfigureret en linje for valutaen for linjen eller varen, anvendes den automatiske omkostning ikke på den pågældende linje eller vare.

I forbindelse med andre typer omkostningsområder gælder alle linjer i oversigtspanelet **Linjer** for hver fragt, forsendelsescontainer, folio eller flytteordrelinje, der svarer til de værdier, der er oprettet i overskriften.

I følgende tabel forklares alle de felter, der kan være vist på hver linje. De tilgængelige felter afhænger dog af, hvilket omkostningsområde der er valgt i øjeblikket.

| Felt | Beskrivelse |
|---|---|
| **Valuta** | Vælg den valuta, som linjen gælder for. Denne valuta er relateret til indkøbsordren. Når systemet forsøger at finde de automatiske omkostninger, der skal anvendes på en fragt og dens linjer, vælges den linje, der har samme valuta som indkøbsordren. Dette felt er kun tilgængeligt, når feltet **Omkostningsområde** er angivet til *Indkøbsordre* eller *Vare*. |
| **Omkostningstypekode** | Omkostningstypen. |
| **Fordelingsmetode** | <p>Den metode, der bruges til at fordele omkostninger på linjer. Der findes følgende indstillinger:</p><ul><li><p>**Procent** – Værdien i feltet **Kostværdi** er en procent, der gælder for den samlede vareværdi.</p><p>Hvis feltet **Kostværdi** f.eks. er angivet til *10*, og den samlede værdi af varer er $800, vil kostværdien være $80 (= $800 × 10 procent).</p></li><li>**Antal** – Omkostningen vil blive fordelt baseret på antallet af varer.</li><li>**Beløb** – Omkostningen vil blive fordelt baseret på værdien af varerne.</li><li>**Volumen** – Omkostningen vil blive fordelt baseret på varernes volumen. Volumen angives på varens master.</li><li>**Vægt** – Omkostningen vil blive fordelt baseret på varernes vægt. Vægt angives på varens master.</li><li>**Volumetrisk** – Omkostningen vil blive fordelt baseret på varernes volumetriske mål.</li><li><p>**Mål** – Denne indstilling giver mulighed for at angive et mål i modulet **Landingsomkostninger**. Det bruges ofte af organisationer, der ikke kender varernes individuelle volumen eller vægt, men som kræver en mere præcis fordeling, end indstillingerne af **Beløb** og **Antal** tillader. Speditøren eller agenten sørger for, at organisationen får vægten eller kubikmålet, enten på vareniveau eller indkøbsordreniveau.</p><p>Skibsfragt er f.eks. lig med $900. Vare A har en vægt på 800 kilogram (kg) og en volumen på 2 kubikmeter (m³). Vare B har en vægt på 100 kg og en volumen på 1 m³. Her er resultaterne, når omkostningerne fordeles efter vægt:</p><ul><li>Vare A = $800</li><li>Vare B = $100</li></ul><p>Her er resultaterne, når omkostningerne fordeles efter volumen:</p><ul><li>Vare A = $600</li><li>Vare B = $300</li></ul><p>**Bemærk:** Når feltet **Fordelingsmetode** er angivet til *Mål*, bruger systemet de mål, der er angivet for både omkostningsområdet (forsendelsescontaineren) og linjerne. Disse mål behøver ikke nødvendigvis at være lig med den forventede total. Hvis du kræver, at de udgør den forventede total, kan du dog udføre en kontrol ved at bruge statistikken til at gennemgå det samlede mål. Indstillingen for målprompten og den automatiske opdatering af målet på forsendelses- eller containerniveau angives i fragthovedet.</p></li></ul> |
| **Fra-dato** | Angiv starten af datointervallet for efterkalkulation, hvis der er et datointerval. Denne dato er den første dato, hvor den automatiske omkostning anvendes. |
| **Til-dato** | Angiv slutningen af datointervallet for efterkalkulation, hvis der er et datointerval. Denne dato er den sidste dato, hvor den automatiske omkostning anvendes. |
| **Kategori** | <p>Vælg den metode, der skal bruges til beregning af omkostning. Der findes følgende indstillinger:</p><ul><li>**Fast** – Omkostningen vil blive fordelt baseret på fordelingsmetoden.</li><li>**Styk** – Omkostningen fordeles pr. styk. Derfor bruges fordelingsmetoden ikke.</li><li>**Procent** – En procent af varernes værdi lægges til. Derfor bruges fordelingsmetoden ikke.</li><li>**Sats** – Vælg denne indstilling, hvis der er mængdereduktioner. Feltet **Fordelingsmetode** for linjen skal være angivet til *Mål*.</li><ul> |
| **Opdelt efter antal** | <p>Markér dette afkrydsningsfelt for at gøre knappen **Mængdereduktioner** tilgængelig i oversigtspanelet **Linjer**. Med mængdereduktioner fordeles omkostningen, så de forskellige omkostninger varierer afhængigt af antallet på fragtens indkøbsordrelinje. Denne funktion bruges ofte, når leveringsmåden er luftfragt. Feltet **Kategori** for linjen skal være angivet til *Sats*.</p><p>Antallet er baseret på den indstilling, der er valgt i feltet **Fordelingsmetode**. Kostværdien er op til det antal, der er angivet i feltet **Kostværdi**.<p>Mængder på 45-100 kg giver f.eks. et gebyr på $6,00 pr. mål (f.eks. kg/m³). Mængder over 100 kg giver f.eks. et gebyr på $5,50 pr. mål (f.eks. kg/m³).</p> |
| **Omkostningsværdi** | Angiv værdien af omkostningen. |
| **Omkostningsvalutakode** | Vælg valutaen for omkostningen. |
| **Varemomsgruppe** | Vælg momskoden til omkostningen. |
| **Minimumsomkostning** | <p>Dette felt gælder kun, hvis afkrydsningsfeltet **Fordelt efter antal** er markeret. Hvis målet ikke når op på denne værdi, vælges minimumværdien, uanset hvilke omkostninger der er angivet på siden **Mængdereduktioner**.<p>Mængder på 0-45 kg giver f.eks. et gebyr på $6 pr. mål (kg/m³). Mængder på 46-100 kg giver et gebyr på $5,50 pr. mål (kg/m³). Hvis der afsendes 2 kg, opretter mængdereduktionen en kostværdi på $12. Hvis feltet **Minimumomkostning** angives til *$100*, vil den endelige omkostning dog blive $100.</p> |
| **Aggregering** | Markér dette afkrydsningsfelt for at tillade, at brugere flytter denne omkostning fra forsendelsescontainerniveau til fragtniveau. I dette tilfælde kan omkostninger beregnes automatisk på forsendelsescontainerniveau. De kan dog også kombineres og fordeles på tværs af alle varer i alle containere for en fragt i stedet for alle varer i de enkelte forsendelsescontainere. |
| **Tilknyttet omkostningstype** | <p>Knyt den aktuelle linje til en anden linje i samme automatiske omkostningspost ved at angive **Kode for omkostningstype** for den linje, du vil knytte til. Denne funktionalitet er kun tilgængelig, når feltet **Kategori** for den aktuelle linje er angivet til *Procent*. Når den aktuelle linje er knyttet til en anden linje, vil omkostningen for den aktuelle linje blive baseret på omkostningerne for den anden linje.</p><p>Fragten er f.eks. $1.000, og brændstoftillægget skal være 10 procent af fragtomkostningen. I dette tilfælde skal linjen have **Kategori**-værdien *Procent*, en **Kostværdi** på *10 %* og en **Tilknyttet omkostningstype**-værdi for *Fragt*.</p> |
| **Værdiregulering** og **Reguleringsbeløb** | <p>Brug disse felter til at justere værdien og beløbet for forskellige procentværdier. De er kun tilgængelige, når feltet **Omkostningsområde** er angivet til *Vare*.</p><p>Der kan oprettes forskellige efterkalkulationer for forskellige komponenter af en vare. En komponent i en vare kan have en anden omkostningsprocent end de andre komponenter i den pågældende vare. Det kan i visse tilfælde være nødvendigt at bruge denne metode for at værdisætte en bestemt del af varerne med andre satser.</p><p>Afgift for et ur beregnes f.eks. med to satser: En komponent af uret har en afgiftssats på 10 procent, og en anden komponent har en afgiftssats på 2 procent. I dette tilfælde opdeles efterkalkulationen mellem de to komponenter.</p><p>Omkostningen beregnes for varen, men kostværdien reguleres med værdien af de komponenter, der har den anden omkostningskategori. Omkostningen for de resterende komponenter kan derefter beregnes ved hjælp af det beløb, som den tidligere beregning blev reguleret med.</p><p>Komponent A har f.eks. en pris på $9,50 og en afgift på 10 procent, og komponent B har en pris på $0,50 og en afgift på 2 procent. Derfor er totalomkostningen $10,00. Den første post er for linjen på 10 procent. Den har følgende værdier:</p><ul><li>**Kategori:** *Procent*</li><li>**Kostværdi:** *10*</li><li>**Værdireguleret:** *Reguler med*</li><li>**Reguleret værdi:** *-0,50*</li></ul><p>Denne opsætning angiver, at kostprisen for varen ($10) skal reduceres med $0,50 (prisen på komponent B), før der beregnes afgiftsgebyr på 10 procent. Derfor anvendes der 10 procent på $9,50.</p><p>Den anden post er for linjen med 2 procent ($0,50, som den foregående post blev reguleret med). Den har følgende værdier:</p><ul><li>**Kategori:** *Procent*</li><li>**Kostværdi:** *2*</li><li>**Værdireguleret:** *Brug*</li><li>**Regulering:** *0,50*</li></ul><p>I denne opsætning beregnes den resterende afgift, der skal betales for komponent B.</p> |
