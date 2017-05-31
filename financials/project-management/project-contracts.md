---
title: Projektkontrakter
description: "I denne artikel beskrives og gives eksempler på de projektkontrakter, du kan oprette for forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektets debitorer i Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9f3bdbd147f3132d64e3b9ac2bdd37f7278ae18d
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="project-contracts"></a>Projektkontrakter

[!include[banner](../includes/banner.md)]


I denne artikel beskrives og gives eksempler på de projektkontrakter, du kan oprette for forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektets debitorer i Microsoft Dynamics 365 for Operations.

Den type projekt, du opretter til en projektkontrakt, afgør, hvilken metode der bruges til fakturering af projektdebitorere. Du kan ændre en projektkontrakt og det relaterede projekt, men du kan ikke ændre projekttypen. 

Når du bruger en projektkontrakt, kan du fakturere ét eller flere projekter på én gang. Med projektkontrakten kan du også sikre en konsistent faktureringsprocedure til hvert underprojekt i en projektstruktur. 

Hvert projekt, der skal faktureres, skal være tilknyttet en projektkontrakt. Indstillingerne for en projektkontrakt gælder for alle projekter og underprojekter, der er tilknyttet den pågældende projektkontrakt. 

I en projektkontrakt kan der angives én eller flere finansieringskilder. Du kan derfor opdele fakturering blandt flere finansieringskilder, konfigurere finansieringsgrænser, så finansieringskilder ikke faktureres mere end et bestemt beløb, og konfigurere finansieringsregler for opkrævning af udgifter.

## <a name="funding-for-project-contracts"></a>Finansiering af projektkontrakter
Visse projektkontrakter kan angive, at flere parter deler ansvaret for finansiering af projektomkostningerne. Her er nogle eksempler:

-   En stor kunde, der har flere afdelinger, anmoder om, at finansieringen af et projekt skal opdeles efter afdeling.
-   Firmaet deler udgifterne til et stort projekt med en ekstern organisation.
-   Et vejprojekt finansieres i fællesskab af to kommuner.
-   Et broprojekt finansieres af statslige tilskud og en privat virksomhed.

I Microsoft Dynamics 365 for Operations kan du opdele fakturering for en enkelt transaktion eller et helt projekt mellem flere debitorer, tilskud eller organisationer. 

I projekter med flere bidragydere kaldes alle de parter, der bidrager til finansieringen af et avanceret finansieringsprojekt, for finansieringskilder. Når en debitor, en organisation eller et tilskud er defineret som en finansieringskilde, kan den/det tildeles en eller flere finansieringsregler. Finansieringsregler indeholder de kriterier, der afgør, hvordan gebyrer fordeles på et projekts forskellige finansieringskilder. 

Da lagerførte varer som dem, der vises i indkøbsrekvisitioner og indkøbsordrer, ikke kan opdeles, kan omkostningsbeløbet ikke fordeles mellem flere finansieringskilder på tidspunktet for fordeling. Finansieringskildens værdi er derfor 0 (nul), indtil lagerafgangen bogføres. Når lagerafgangen bogføres, fordeles omkostningsbeløbet i overensstemmelse med reglerne for kontofordeling på projektet.

Her er nogle trin, du kan udføre for at gøre det lettere at opdele fakturering blandt flere finansieringskilder:

-   Angiv, at alle de posteringer, der angives for et projekt, skal bruge samme salgsvaluta som i projektkontrakten.
-   Konfigurer finansieringsgrænser, så en finansieringskilde ikke faktureres med mere end et angivet beløb på et projekt.
-   Konfigurer finansieringsregler og finansieringsgrænser for hver arbejder, vare, kategori, kategorigruppe og posteringstype (eller for alle posteringstyper).
-   Vælg en valgfri start- og slutdato for at definere den periode, hvor hver finansieringsregel gælder for.
-   Angiv den procentdel, som hver finansieringskilde er ansvarlig for.
-   Angiv, hvilken finansieringskilde der er ansvarlig for afrundingsdifferencer, som skyldes beregninger af finansieringsfordelinger.
-   Konfigurer regler, der afgør, hvordan projektomkostninger skal faktureres til eksterne debitorer og debiteres på interne organisationer.
-   Registrer posteringer på en finansieringskonto på hold, indtil der kan opnås yderligere finansiering, eller indtil du beslutter at bære omkostningerne internt.

Hvis du vil finde ud af, hvilken momsgruppe der skal knyttes til en postering, kan du søge i projektet efter en tildeling af momsgruppe. Hvis der ikke er foretaget en tildeling af momsgruppe på projektniveau, kan du søge efter projektkontrakten.

### <a name="example-multiple-funding-sources-simple"></a>Eksempel: flere finansieringskilder (simpel)

Følgende tabel indeholder scenarier til administration af finansieringsfordeling mellem flere finansieringskilder. Disse scenarier er baseret på følgende forudsætninger:

-   Prioritetsindstillinger indregnes i tildelingen af midler, før andre finansieringsregelkriterier anvendes.
-   Der er ikke angivet et datointerval til at definere periode d, når finansieringsreglen er gyldig.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenarie</strong></td>
<td><strong>Finansieringskilde </strong></td>
<td><strong>Fordelingsprocent </strong></td>
<td><strong>Fordelingsprioritet </strong></td>
</tr>
<tr class="even">
<td>Du skal allokere omkostninger til én finansieringskilde, indtil dens midler er opbrugt, allokere omkostninger til en anden finansieringskilde, indtil dens midler er opbrugt, og endelig allokere de resterende omkostninger til en tredje finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du skal allokere 75 % af omkostningerne til én finansieringskilde og 25 % til en anden finansieringskilde. Når begge disse finansieringskilder er opbrugt, vil du betale de resterende omkostninger fra et tredje finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Du skal allokere 75 % af omkostningerne til én finansieringskilde og 25 % til en anden finansieringskilde. Hvis begge disse finansieringskilder er opbrugt, skal du dele de resterende omkostninger mellem en tredje og en fjerde finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
<li>Finansieringskilde 3</li>
<li>Finansieringskilde 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Du skal fordele de første 25 % af omkostningerne til én finansieringskilde og resten til en anden finansieringskilde.</td>
<td><ul>
<li>Finansieringskilde 1</li>
<li>Finansieringskilde 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Eksempel: flere finansieringskilder (kompleks)

Du har tre finansieringskilder, som du vil bruge i følgende rækkefølge:

1.  Brug lige meget af finansieringskilde 2 og finansieringskilde 3, indtil finansieringskilde 2 er opbrugt.
2.  Fortsæt med at bruge finansieringskilde 3, indtil den er opbrugt.
3.  Brug finansieringskilde 1, efter at finansieringskilde 3 er opbrugt.

For at nå dette mål skal du gøre følgende:

-   Opret finansieringsgrænser for finansieringskilde 2 og finansieringskilde 3 for deres respektive beløb.
-   Opret følgende finansieringsregler:
    -   Regel 1 (prioritet 1): Fordel 50 procent af posteringer til finansieringskilde 2 og 50 procent til finansieringskilde 3.
    -   Regel 2 (prioritet 2): Fordel 100 procent af posteringer til finansieringskilde 3.
    -   Regel 3 (prioritet 3): Fordel 100 procent af posteringer til finansieringskilde 1.

Denne opsætning fungerer, fordi posteringer kontrolleres mod regler og begrænsninger for at bestemme, om nogen af dem gælder for posteringen. Hvis ingen specifikke regler eller grænser gælder for posteringen, gælder reglen Alle posteringer. Reglen Alle posteringer afstemmer alle posteringer. 

Hvis der findes en regel, der passer til en postering, anvendes den procentsats, der er allokeret i denne regel, først, men først efter at forekomsterne er blevet kontrolleret mod eventuelle grænser. Hvis en grænse er nået, og en finansieringskildes midler er opbrugt, ignoreres finansieringsreglen for finansieringsgrænsen, og programmet søger efter den næste gældende regel. 

I nogle tilfælde kan kun en del af en postering tildeles under en regel. Det kan ske, fordi en grænse nås, når posteringen allokeres. I dette tilfælde tildeles kun et bestemt beløb i henhold til denne regel, f.eks 50 procent til hver finansieringskilde. Dette er tilfældet i regel 1, der er beskrevet tidligere i dette afsnit. Resten fordeles i henhold til den næste regel i rækkefølgen. 

I følgende tabel undersøges dette scenario yderligere.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokusering </strong></td>
<td><strong>Detaljer</strong></td>
</tr>
<tr class="even">
<td>Finansieringsregler</td>
<td><ul>
<li>Regel 1 (prioritet 1): Alle posteringer. Alloker finansieringskilde 2 på 50 % og finansieringskilde 3 på 50 %.</li>
<li>Regel 2 (prioritet 2): Alle posteringer. Alloker finansieringskilde 3 på 100 %.</li>
<li>Regel 3 (prioritet 2): Alle posteringer. Alloker finansieringskilde 1 på 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansieringsloft</td>
<td><ul>
<li>Grænse for finansieringskilde 1 = 10.000,00</li>
<li>Grænse for finansieringskilde 2 = 500,00</li>
<li>Grænse for finansieringskilde 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Postering 1</td>
<td><strong>Posteringens beløb:</strong> 100,00<strong>Finansiering:</strong> Posteringen betales i henhold til regel 1, da posteringen er fuldt betalt efter regel 1 anvendes. Posteringen finansieres ligeligt mellem finansieringskilde 2 og finansieringskilde 3.
<ul>
<li>Finansieringskilde 2: 50.00</li>
<li>Finansieringskilde 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Postering 2</td>
<td><strong>Transaktionsbeløb:</strong> 5.000,00<strong>Finansiering:</strong> Transaktionen betales i henhold til alle tre regler.<strong>Regel 1</strong>
<ul>
<li>Finansieringskilde 2: 450.00</li>
<li>Finansieringskilde 3: 450.00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finansieringskilde 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finansieringskilde 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Samlede midler, der distribueres for hver finansieringskilde</td>
<td><ul>
<li>Finansieringskilde 1: 3,850.00</li>
<li>Finansieringskilde 2: 500.00</li>
<li>Finansieringskilde 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regler for fakturering
Når du forhandler en projektkontrakt på plads med en kunde, skal du definere, hvordan og hvornår du kan fakturere kunden for arbejde på et projekt. Når du har oprettet projektkontrakten og projektet, kan du angive regler for fakturering af projektet. Faktureringsregler er baseret på de projektvilkår, der er angivet i projektkontrakten. De faktureringsregler, du kan oprette, afhænger af vilkårene i projektkontrakten og projekttypen, f.eks. tid og materialer eller fast pris, som du tilknytter til faktureringsreglen. Du kan oprette mere end én faktureringsregel for en projektkontrakt. Du kan også tildele en faktureringsregel til flere projekter, der er tilknyttet den samme projektkontrakt og har lignende vilkår. 

Du kan angive følgende typer faktureringsregler:

-   **Enhed for levering** – Fakturer en kunde, når du har fuldført en enhed for levering. Du definerer de enheder, der skal leveres, i kontrakten.
-   **Status** – Fakturer en kunde, når du har fuldført en nærmere angivet procentdel af projektet. Du kan oprette en faktureringsregel til automatisk beregning af procentdelen af udført arbejde, eller du kan manuelt beregne procentdelen af fuldført arbejde og det beløb, der skal faktureres kunden.
-   **Milepæl** – Fakturer en kunde for det fulde beløb for et projekts milepæl, når milepælen er nået.
-   **Gebyr** – Fakturer en kunde for dine servicer plus et administrationsgebyr, som typisk vil være en procentdel af kostprisen for servicen.
-   **Tid og materialer** – Fakturer en kunde for værdien af den tid og de materialer, der er brugt på et projekt.

For alle typer faktureringsregler gælder det, at du kan angive en tilbageholdelsesprocentdel, der trækkes fra debitorfakturaer, indtil et projekt når en aftalt fase. Tilbageholdelsesprocenten for betalingen angives i projektkontrakten. Beløbet beregnes baseret på og trækkes fra den samlede værdi af linjerne i en debitorfaktura. 

For faktureringsreglerne **Tid og materialer** og **Status** kan du tildele fakturerbare kategorier. Fakturerbare kategorier angiver de posteringer, der skal medtages i debitorfakturaer. 

Når du er klar til at fakturere debitoren, beregnes det beløb, der skal faktureres for projektet, på basis af faktureringsreglerne, og der genereres et projektfakturaforslag. 

De følgende afsnit indeholder eksempler, der viser, hvordan du kan konfigurere og administrere faktureringsregler for et projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Eksempel: Opret en faktureringsregel, der er baseret på det leverede antal enheder

Din organisation indgår en aftale om at levere fem træningssessioner i alt til en kundes medarbejdere til en pris af 10.000 pr. træningssession. Du fakturerer kunden efter hver træningssession. 

Når du konfigurerer faktureringsreglerne til kontrakten, skal du bruge følgende værdier:

-   Leveringsenheden er én træningssession.
-   Enhedsprisen er 10.000 kr. pr. træningssession.
-   Det samlede antal enheder er fem træningssessioner.

Når du har fuldført én træningssession, kan du oprette en faktura på 10.000 for den første enhed, der blev leveret, og sende fakturaen til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Eksempel: Opret en faktureringsregel, der er baseret på fuldførelse af en nærmere angivet procentdel af projektet (manuel beregning)

Din organisation, som tilbyder softwarerådgivning, indgår aftale med en kunde om at udvikle én del af et produkt, som kunden er ved at udvikle. Din organisation indgår aftale med kunden om at levere softwarekoden over en periode på seks måneder. Kunden indvilliger i at betale din organisation i alt 100.000 kr. for arbejdet. Du opretter en faktureringsregel for at fakturere kunden på baggrund af den procentdel af arbejdet, der er udført for projektet, som angivet i kontrakten.

-   Ved udgangen af den første måned mødes du med kunden for at fastslå, hvor stor en procentdel af arbejdet der er fuldført. Når du og kunden har gennemgået projektet, beslutter I, at 15 procent af projektet er fuldført.
-   Du opretter en faktura på 15.000 (15 procent af 100.000) og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Eksempel: Opret en faktureringsregel, der er baseret på fuldførelse af en nærmere angivet procentdel af projektet (automatisk beregning)

Organisationen, en softwareudviklingsvirksomhed, indvilliger i at udvikle en pakkeløsning med et system til lønningsregnskab for en kunde for 30.000. Kunden indvilliger i at betale din organisation på basis af den procentdel af arbejdet, der er fuldført. Du anslår, at projektomkostningerne beløber sig til 20.000 kr. Projektkontrakten specificerer de arbejdskategorier, som du skal bruge i forbindelse med faktureringen. Du opretter regler for fakturering, så fakturabeløbene beregnes automatisk, og så kunden faktureres for den procentdel af arbejdet, der er fuldført inden for hver kategori. Du opretter et budget for hver enkelt kategori:

-   **Udvikling** – omkostninger på 15.000 og indtægter på 20.000
-   **Installation** – omkostninger på 5.000 og indtægter på 10.000

Første gang du opretter en debitorfaktura, beregnes fakturabeløbet automatisk ud fra følgende oplysninger:

-   Efter en måned sender arbejderen på projektet en timeseddel for projektet. Omkostningerne til arbejderens timer er 5.000 kr. for udvikling og 1.000 kr. for installation. Udviklingsarbejdet er 33 procent fuldført (5.000 faktiske omkostninger/15.000 budgetomkostninger), og installationsarbejdet er 20 procent fuldført (1.000 faktiske omkostninger/5.000 budgetomkostninger).
-   Fakturabeløbet på 8.667 beregnes automatisk (33 procent af 20.000 plus 20 procent af 10.000).
-   Du opretter en faktura på 8.667 og sender den til kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Eksempel: Opret en faktureringsregel, der er baseret på nærmere aftalte milepæle

Din organisation tilbyder ledelsesrådgivning, accepterer at gennemføre markedsundersøgelser for et forbrugerprodukt, som kunden har til hensigt at sælge. Kunden indvilliger i at bruge dig i en periode på tre måneder fra og med marts og at betale din organisation 50.000 kr. Der er tre milepæle i projektet:

-   Milepæl 1: Indsamling af forbrugerdata – 31. marts
-   Milepæl 2: Analyse af forbrugerdata – 30. april
-   Milepæl 3: Fremlæggelse af rapport om produktets levedygtighed - 31. maj

Kunden indvilliger i at betale din organisation 10.000 for den første milepæl og 20.000 for såvel den anden som den tredje milepæl. 

Under udarbejdelsen af projektkontrakten aftales det, at kunden faktureres på basis af den milepæl, der er nået. Opsætningen af faktureringsreglen omfatter følgende trin:

-   Angiv milepælene i projektet.
-   Definer det beløb, der skal faktureres kunden, når hver milepæl er nået.

Når den første milepæl er nået d. 31. marts, skal du markere milepælen som fuldført og derefter oprette en faktura på 10.000 og sende den til kunden. Du kan ikke oprette en faktura for en milepæl, indtil du har markeret milepælen som fuldført.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Eksempel: Opret en faktureringsregel, der er baseret på tjenester plus et administrativt gebyr

Din organisation, et ledelsesrådgivningsfirma, accepterer at gennemføre markedsundersøgelser for at vurdere, om et produkt, som kunden, en detailvirksomhed, udvikler, vil kunne overleve på markedet. Aftalens vilkår angiver, at du stiller dit firmas tre bedste ledelseskonsulenter til rådighed. Deres opgave er at udføre undersøgelserne baseret på tids- og materialeforbrug. Kunden indvilliger i at betale 1000 pr. time for konsulenterne plus et ekstra administrationsgebyr på 10 procent for de konsulenttimer, der debiteres på projektet. 

Når du opretter projektkontrakten, skal du oprette en faktureringsregel, der fastslår, at der skal lægges et administrationsgebyr på 10 procent til de konsulenttimer, der debiteres på projektet. 

Når du opretter en faktura til kunden, faktureres kunden et administrativt gebyr på 10 procent plus prisen for konsulenttimerne. Hvis de tre konsulenter f.eks. i alt arbejder 200 timer på projektet, oprettes der en faktura på 220.000 baseret på følgende beregning:

-   200 timer til 1000 kr. pr. time = 200.000 kr.
-   10 procent management gebyr = 20.000
-   Samlet fakturabeløb = 220.000

Hvis gebyrer er afgiftspligtige for en debitor, og du vælger en salgsmomsgruppe i projektkontrakten, angives salgsmomsgruppen automatisk i en faktureringsregel for gebyrer.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Eksempel: Opret en faktureringsregel for tids- og materialeomkostninger

Din organisation, et softwarekonsulentfirma, aftaler at stille fem tekniske konsulenter til rådighed, som i løbet af de næste seks måneder skal arbejde med et projekt for en kunde om udvikling af computerprogrammer. Kunden indvilliger i at betale 1.500 kr. for hver konsulenttime plus udgifterne til kontorartikler. Din organisation sender en faktura til kunden ved udgangen af hver måned. 

Når du konfigurerer projektkontrakten, accepterer du at fakturere kunden hver måned for tid og materialer på projektet. Du kan oprette en faktureringsregel, der indeholder følgende oplysninger:

-   Kontraktens periode er seks måneder.
-   Konsulenttiden beregnes efter en sats på 1.500 kr. pr. time.
-   Kontorartikler faktureres med kostprisen, og de samlede omkostninger må ikke overstige 100.000 kr. for projektet.
-   Du opretter en debitorfaktura ved udgangen af hver kalendermåned under projektperioden.

I løbet af den første måned registrerer konsulenterne 800 timer i alt på projektet. Udgifterne for kontorartikler i forbindelse med projektet er 20.000 kr. I slutningen af måneden skal du derfor oprette en faktura på 1.220.000, som beregnes som 800 timer ved 1500 i timen plus 20.000 til kontorartikler.




