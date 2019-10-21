---
title: Styring af detailsalgspriser
description: I dette emne beskrives begreberne for oprettelse og styring af salgspriser i Dynamics 365 Retail.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 081fadf0c120eba50af9e6c396fb3e492051bb3c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025212"
---
# <a name="retail-sales-price-management"></a>Retail-salgsprisestyring

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om processen for oprettelse og styring af salgspriserne i Dynamics 365 Retail. Der fokuseres på de begreber, der er involveret i processen, og om virkningerne af de forskellige konfigurationsindstillinger for salgspriser.

## <a name="terminology"></a>Terminologi

Følgende begreber anvendes i dette emne.

| Periode | Definition, brug og noter |
|---|---|
| Pris | Beløbet for én enhed, som et produkt sælges til, til en kunde gennem et salgssted (POS) eller en salgsordre. I dette emne henviser begrebet *pris* altid til salgsprisen, ikke lagerprisen eller kostprisen. |
| Basispris | Den pris, der er angivet i feltet **Pris** for et frigivet produkt. |
| Pris i samhandelsaftale | Den pris, der er angivet for et produkt eller en variant gennem en samhandelsaftale af typen **Pris (salg)**. |
| Bedste pris | Når mere end én pris eller rabat kan gælde for et produkt, er prisen det mindste prisbeløb og/eller det største rabatbeløb, som giver det laveste mulige nettobeløb, som kunden skal betale. I dette emne betegnes den bedste pris altid "den bedste pris". Den bedste pris adskiller sig fra og bør ikke forveksles med tællerværdien for **Bedste pris** for en samtidig rabattilstand. |

## <a name="price-groups"></a>Prisgrupper

Prisgrupper er omdrejningspunktet for styring af priser og rabatter i Retail. Prisgrupper anvendes til at tildele priser og rabatter til detailenheder (dvs. kanaler, kataloger, tilknytninger og fordelskundeprogrammer). Eftersom prisgrupper bruges til alle priser og rabatter, er det vigtigt, at du planlægger, hvordan du vil bruge dem, før du starter.

I sig selv er en prisgruppe blot et navn, en beskrivelse og eventuelt en prioritet for prissætning. Det vigtigste at huske om prisgrupper er, at de bruges til at administrere de utallige relationer, rabatter og priser har med detailenheder.

I følgende illustration vises, hvordan prisgrupperne bruges. I denne illustration skal du bemærke, at "Prisgruppe" bogstaveligt talt er placeret midt i administrationen af prissætning og rabat. De detailenheder, du kan bruge til at administrere differentierede priser og rabatter, er placeret til venstre, og de faktiske pris- og rabatposter er placeret til højre.

![Prisgrupper](./media/PriceGroups.png "Prisgrupper")

Når du opretter prisgrupper, bør du ikke bruge samme prisgruppe til flere typer detailenheder. I modsat fald kan det være vanskeligt at afgøre, hvorfor en bestemt pris eller rabat anvendes til en transaktion.

Når den røde stiplede linje i illustrationen vises, understøtter Retail kernefunktionaliteten i Microsoft Dynamics 365 for en prisgruppe, som er indstillet direkte for en debitor. I så fald får du imidlertid kun samhandelsaftaler om salgspris. Hvis du vil anvende kundespecifikke priser, anbefales det, at du ikke angiver prisgrupper direkte for debitoren. Du skal i stedet bruge tilknytninger.

De følgende afsnit indeholder flere oplysninger om de detailenheder, du kan bruge til at angive specifikke priser, når der anvendes prisgrupper. Konfigurationen af priser og rabatter for disse enheder er en proces i to trin. Disse trin kan udføres i vilkårlig rækkefølge. Den logiske rækkefølge er dog først at angive prisgrupperne for enhederne, fordi dette trin ofte kun skal udføres en enkelt gang under implementeringen. Derefter, når der oprettes priser og rabatter, kan du oprette prisgrupper for de enkelte priser og rabatter.

### <a name="channels"></a>Kanaler

Det er meget almindeligt at have forskellige priser i forskellige kanaler i detailbranchen. De to primære faktorer, der påvirker kanalspecifikke priser, er omkostninger og lokale markedsforhold.

- **Omkostninger** – Jo længere væk en kanal er fra produktkilden, jo mere koster det at lagerføre et produkt. Friske produkter har f.eks. en begrænset hyldelevetid og specifikke produktionsbetingelser (f.eks. en enkelt vækstsæson). Om vinteren koster frisk salat sandsynligvis mere i det nordlige klima end i det sydlige klima. Hvis du angiver priser for kanaler over et stort geografisk område, vil du sandsynligvis angive forskellige priser for forskellige kanaler.
- **Lokale markedsbetingelser** – Et lager, som har en direkte konkurrent på den anden side af gaden, vil være meget mere prisfølsomt end en butik, som ikke har en direkte konkurrent i nærheden.

### <a name="affiliations"></a>Tilhørsforhold

Den generelle definition af en tilknytning er et hyperlink til eller en tilknytning til en gruppe. I Retail er tilknytninger grupper af debitorer. Tilknytninger er et meget fleksibelt værktøj for priser og rabatter for debitorer end den centrale opfattelse af debitorgrupper og rabatgrupper i Microsoft Dynamics 365. Først og fremmest kan en tilknytning bruges til både priser og rabatter, mens ikke-detailpriser har en ny gruppe for hver rabat- og pristype. Derefter kan en debitor tilhøre flere tilknytninger, men de kan kun tilhøre én ikke-detailprisgruppe for hver type. Endelig kan der konfigureres tilknytninger til en kunde, selvom det ikke er nødvendigt. En ad hoc-tilknytning kan bruges til anonyme debitorer på salgsstedet. Et typisk eksempel på rabat på en anonym tilknytning er rabat for ældre eller studerende, hvor en debitor kan modtage en rabat ved blot at fremvise et medlemskort for gruppen.

Selvom tilknytninger oftest omhandler rabatter, kan du også bruge dem til at angive differentieret prissætning Når en forhandler f.eks. sælger til en medarbejder, vil forhandleren muligvis ændre salgsprisen i stedet for at anvende en rabat på den almindelige pris. Et andet eksempel er, når en forhandler, der sælger til både forbrugere og virksomheder, tilbyde virksomheder bedre priser, der er baseret på volumen af deres indkøb. Tilknytninger muliggør begge disse scenarier.

### <a name="loyalty-programs"></a>Fordelskundeprogrammer

I forbindelse med priser og rabatter er fordelskundeprogrammer grundlæggende blot en tilknytning med en særlig betegnelse. Både priser og rabatter kan angives for et fordelskundeprogram, ligesom de kan angives for en tilknytning. Den måde, hvorpå debitorer får fordelskundepriser under en transaktion eller ordre, adskiller sig dog fra den måde, hvorpå de får tilknytningspriser. Kunder kan kun få fordelskundepriser, hvis et fordelskundekort føjes til en transaktion. Når et fordelskundekort føjes til en transaktion, tilføjes fordelskundeprogrammet også. Fordelskundeprogrammet muliggør derefter særlige priser og rabatter.

Fordelskundeprogrammer kan have flere niveauer, og rabatterne kan være forskellige for forskellige niveauer. På denne måde kan detailhandlere give hyppige debitorer større fordele uden at skulle placere dem manuelt i en specialgruppe.

Kundefordelsprogrammer omfatter yderligere funktioner ud over priser og rabatter. I forhold til priser og rabatter er de dog det samme som tilknytninger.

### <a name="catalogs"></a>Kataloger

Nogle detailhandlere bruger fysiske eller virtuelle kataloger til at markedsføre og prissætte produkter til målrettede grupper af debitorer. Som en del af deres forretningsmodel for at målrette markedsføringen gennem et katalog, kan disse detailhandlere angive differentierede priser i deres forskellige kataloger. Microsoft Dynamics 365 understøtter denne funktion ved at lade dig definere katalogspecifikke rabatter og priser, ligesom du kan definere kanalspecifikke eller tilknytningsspecifikke rabatter. Når du redigerer et katalog, kan du kan knytte prisgrupper til kataloget, ligesom du kan knytte dem til en kanal, en tilknytning eller et fordelskundeprogram.

### <a name="best-practices-for-price-groups"></a>Bedste praksis for prisgrupper

Brug ikke en prisgruppe til flere detailenhedstyper. I stedet anvendes et sæt prisgrupper for kanaler, et sæt prisgrupper for tilknytninger eller fordelskundeprogrammer osv. Du kan bruge et præfiks eller suffiks i navnet på prisgruppen for at gruppere de forskellige prisgruppetyper visuelt.

Undlad at angive prisgrupper direkte for en debitor. Anvend i stedet en tilknytning. På denne måde kan du tildele alle typer priser og rabatter til debitorer, ikke blot samhandelsaftaler for salgspriser.

## <a name="pricing-priority"></a>Prioritet for prissætning

I sig selv er en prioritet for prissætning blot et tal og en beskrivelse. Prioriteter for prissætning kan anvendes til prisgrupper, eller de kan anvendes direkte til rabatter. Når der anvendes prioriteter for prissætning, kan en detailhandler tilsidesætte princippet for bedste pris ved at styre rækkefølgen for tildeling af priser og rabatter til produkter. Et højere prioritetsnummer for prissætning evalueres før et lavere prioritetsnummer. Derudover ignores alle priser og rabatter, der har lavere prioritetsnumre, hvis der er placeret en pris eller rabat ved et prioritetsnummer.

Prisen og en rabat kan stamme fra to forskellige priser prioriteter for prissætning, fordi prioriteterne gælder uafhængigt af priser og rabatter.

Hvis du vil bruge prioriteter for prissætning til priser, skal du tildele en prioritet til en prisgruppe og derefter oprette en samhandelsaftale for salgspris for den pågældende prisgruppe.

Funktionen til prioriteter for prissætning blev indført for at understøtte det scenarie, hvor en detailhandler ønsker at anvende højere priser i et bestemt række af butikker. Et eksempel er, når en detailhandler har defineret regionale priser for den amerikanske østkyst i USA, men ønsker højere priser for visse produkter i butikkerne i New York City, fordi det koster mere at sælge visse produkter i byen, og/eller fordi en højere pris er gælder på det lokale marked.

Som beskrevet i afsnittet "Bedste pris" i dette emne, vælger programmet for detailprissætning typisk den mindste af to priser. Derfor forhindres detailhandleren normalt i at bruge den højeste af to priser i en butik, der har både har prisgrupper for østkysten og i New York. For at løse problemet, inden funktionen for prioriteter for prissætning blev indført, måtte detailhandleren definere priser for hvert produkt to gange og ikke tildele prisen til begge prisgrupper. Detailhandleren kunne også oprette ekstra prisgrupper for at isolere de produkter, der har højere priser, fra produkter med de normale, lavere priser.

Funktionen til prioriteter for prissætning lader imidlertid detailhandleren oprette en prioritet for butikkens priser, som er højere end prioriteten for de regionale priser. Forhandleren kan også oprette en prioritet for prissætning, der kun gælder for butikspriser, mens de regionale priser får standardprioriteten for prissætning, dvs. 0 (nul). Begge opsætninger er med til at sikre, at butikspriser altid bruges før de regionale priser.

### <a name="pricing-priority-example"></a>Eksempel på prioriteter for prissætning

Lad os se et eksempel, hvor butikspriser tilsidesætter andre priser.

En national detailhandler angiver de fleste priser pr. område, hvilket omfatter fire områder: Nordøst, Sydøst, Midtvest og Vest. Den har identificeret flere markeder med høje omkostninger, som kan bære højere priser. Disse markeder er i New York City, Chicago og området ved San Francisco Bay.

I dette eksempel vil vi dykke ned i den nordøstlige region. Butik 1 er i Boston, og butik 2 er i Manhattan. For butikken i Boston er der tilknyttet to prisgrupper til kanalen: Nordøst og Butik 1. For butikken i Manhatten er der tilknyttet tre prisgrupper til kanalen: Nordøst, NYC og Butik 2.

Detailhandleren konfigurerer to prioriteter for prissætning: Høje omkostninger har prioritetsnummeret 5, og butikspriser for butikken har prioritetsnummeret 10. (Husk, at som standard er prioriteten for prissætning 0 \[nul\], og en pris eller rabat med et højere prioritetsnummer bruges før en pris eller rabat med et lavere prioritetsnummer.) For prisgruppen Nordøst beholder prioriteten for prissætning standardværdien på **0** (nul). For prisgruppen NYC er prioriteten for prissætning indstillet til **5**, da New York City er et marked med høje omkostninger. For prisgrupperne Butik 1 og Butik 2 er prioriteten for prissætning indstillet til **10**.

To produkter, der sælges af detailhandleren, er produkt 1, en T-shirt i basisudgave, og produkt 2, et par modejeans med varemærke.

| Produkt | Pris for Nordøst | Pris for NYC | Butikspris |
|---|---|---|---|
| T-shirt | $15 | Ikke angivet | Ikke angivet |
| Modejeans | $50 | $70 | Ikke angivet |

T-shirten sælges for den samme pris (dvs. $15) i både Boston- og Manhattan-butikkerne, fordi kun én pris er angivet for prisgruppen Nordøst, der er tilknyttet begge kanaler. De måde cowboybukser sælger for $50 i butikken Boston, fordi denne pris er den eneste pris, der er tilgængelige i butikken. I Manhattan-butikken gælder imidlertid to priser: $50 og $70. Da prioriteten for prissætning på 5 for prisgruppen NYC er højere end prioriteten for prissætning på 0 (nul) for prisgruppen Nordøst, skal prisen angives som $70 i POS-systemet.

> [!NOTE]
> For hver prioritet for prissætning kræves en fuld gennemgang af logikken for programmet for detailprissætningen. For at forbedre performance for beregningen af pris og rabat, skal du derfor bruge prioriteter for prissætning med måde.

## <a name="types-of-prices"></a>Pristyper

I Microsoft Dynamics 365 kan du angive prisen på et produkt tre steder:

- Direkte for produktet (basisprisen)
- I en samhandelsaftale for salgspriser
- I en prisjustering

Basisprisen og samhandelsaftaleprisen er en central del af Microsoft Dynamics 365 og er tilgængelige, selvom du ikke bruger Retail. Funktionen til prisjustering er kun tilgængelig i Retail. Næste afsnit indeholder flere oplysninger om hver af disse indstillinger for indstilling af priser og beskriver, hvordan indstillingerne arbejder sammen.

## <a name="setting-prices"></a>Indstilling af priser

### <a name="base-price"></a>Basispris

Det sted, der er lettest at angive prisen for et produkt, er direkte for produktet. Den værdi, du angiver direkte for et produkt, kaldes ofte basisprisen for produktet. Du kan angive basisprisen i feltet **Pris** på fanen **Sælg** på siden **Frigivne produktdetaljer**. Værdier angives i virksomhedens valuta. Prisen gælder som standard for et antal på 1 for måleenheden (UoM), der er angivet i feltet **Enhed** på fanen **Sælg**. Den faktiske pris pr. enhed af et produkt er baseret på måleenhed, prisantal og valuta.

Hvis et produkt har én pris for alle, udgør basisprisen den mest effektive metode til at administrere prisen på produktet. Selvom du bruger samhandelsaftaler til at angive priser, kan du også angive basisprisen for et produkt. Hvis du ikke bruger en samhandelsaftale af typen **Alle**, du har en reservepris, der bruges, når ingen samhandelsaftale er gældende.

Hvis en detailkanals valuta afviger fra firmavalutaen, fastlægges basisprisen i den pågældende detailkanal ved hjælp af valutaomregning af den pris, der er angivet for produktet.

Selvom prisenheden ikke er et almindeligt scenarie for detailhandel, understøttes den af programmet for prissætning i detailhandlen. Hvis prisenheden er indstillet til en anden værdi end **0** (nul), er prisen pr. enhed lig med Pris ÷ Prisenhed. Hvis et produkts pris f.eks. er $10,00, og Prisenheden er 50, er prisen for et antal på 1 lig med $0,20 (= $10,00 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Samhandelsaftale for salgspriser

Ved hjælp af en samhandelsaftalekladde kan du oprette samhandelsaftaler om salgspriser for hvert produkt. I Microsoft Dynamics 365 findes der tre forskellige omfang af debitorer for samhandelsaftaler for salgspriser: **Tabel**, **Gruppe** og **Alle**. Omfanget af debitorer bestemmer, hvilke debitorer en bestemt samhandelsaftale for salgspriser gælder for.

En samhandelsaftale for salgspriser af typen **Tabel** gælder for en enkelt kunde, som er angivet direkte i samhandelsaftalen. Dette scenario er ikke et typisk detailscenarie for salg fra virksomheder til forbrugere (B2C). Hvis det forekommer, anvender programmet for detailprissætning samhandelsaftaler af typen **Tabel** til at fastlægge prisen..

En samhandelsaftale for salgspriser af typen **Gruppe** er den type, der bruges oftest til detailscenarier. Uden for Retail gælder samhandelsaftaler for salgspriser af typen **Gruppe** en simpel debitorgruppe. I Retail er begrebet for en debitorgruppe udvidet til en mere generel detailprisgruppe. En prisgruppe kan knyttes til en detailkanal, en tilknytning, et fordelskundeprogram eller et katalog. Detaljerede oplysninger om prisgrupper finder du i afsnittet "Prisgrupper" tidligere i dette emne.

> [!NOTE]
> En samhandelsaftale for priser bruges altid før basisprisen.

### <a name="price-adjustment"></a>Prisjustering

Som navnet antyder, anvendes en prisjustering til at ændre prisen, som enten er angivet direkte for produktet eller ved hjælp af en samhandelsaftale. En prisjustering kan kun bruges til at sænke prisen, ikke til at hæve den. En prisjustering er den anbefalede metode for detailhandlere til at oprette, spore og administrere prisreduktioner for produkterne over tid.

Der findes tre typer prisjusteringer: rabatprocent, rabatbeløb og pris. En prisjustering af typen rabatprocent eller rabatbeløb anvendes altid til en salgstransaktion. En prisjustering af pristypen anvendes dog kun, hvis den justerede pris er mindre end den pris, der blev angivet ved hjælp af basisprisen eller samhandelsaftalen for pris. Hvis den pris, der er angivet i en prisjustering er større end prisen inden justeringen, anvendes prisjusteringen således ikke.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Fastlæggelse af prisen for et produkt i en transaktion

Beregningen af prisen og rabatten for en transaktion følger princippet for at finde den bedste pris for debitoren. I overensstemmelse med dette princip bruges den laveste pris, hvis der findes mere end en pris. Derudover anvendes den kombination af rabatter, der giver det største rabatbeløb for hele transaktionen. I nogle tilfælde skal der anvendes en mindre rabat på et enkelt produkt, så yderligere rabatter kan anvendes til andre produkter i transaktionen.

Den eneste undtagelse fra princippet om at finde den bedste pris for debitoren er muligheden for at blande og sammensætte rabatter til den laveste slutrabat. Denne mulighed sikrer de billigste rabatter til fordel detailhandleren, når produkterne vælges og grupperes. Når en transaktion inkluderer flere produkter, end der kræves for at opnå den billigste rabat, vælger programmet for detailprissætning de produkter, der resulterer i det mindste mulige rabatbeløb for debitoren.

Programmet for detailprissætning returnerer tre priser for hvert produkt: basisprisen, samhandelsaftalens pris og den aktive pris.

Basisprisen er blot en fast egenskab for produktet og er den samme for alle overalt.

Hvis indstillingen **Find næste** er angivet til **Ja**, bruges den laveste pris, der findes for de gældende samhandelsaftaler for salgspriser som samhandelsaftalens pris. Samhandelsaftaler findes ved at bruge prisgrupper eller kontokoden **Alle**. Samhandelsaftalerne kan også tildeles direkte til en debitor. Hvis indstillingen **Find næste** er angivet til **Nej**, bruges den pris i samhandelsaftalen, som findes først. Hvis der ingen samhandelsaftaler for salgspriser findes, angives samhandelsaftalens pris til basisprisen.

Den aktive pris beregnes ved at bruge samhandelsaftalens pris og anvende den største prisjustering, der gælder for produktet. Hvis der ingen prisjusteringer findes, eller hvis den beregnede aktive pris er højere end samhandelsaftalens pris, indstilles den aktive pris til samhandelsaftalens pris. Husk, at du ikke kan hæve prisen på et produkt ved hjælp af en prisjustering. Gældende prisreguleringer finder du ved hjælp at bruge prisgrupper, der er knyttet til en kanal, et katalog, en tilknytning eller et fordelskundeprogram.

## <a name="category-price-rules"></a>Regler for kategoripriser

Funktionen for kategoriprisregler i Retail giver dig en nem metode til at oprette nye samhandelsaftaler for alle produkter i en kategori. Denne funktion gør det også muligt automatisk at finde eksisterende samhandelsaftaler for produkterne i kategorien og ophæve dem.

Når du vælger indstillingen for at ophæve eksisterende samhandelsaftaler, opretter systemet en ny samhandelsaftalekladde for produkterne i kategorien, der har en aktiv samhandelsaftale. Kladden skal dog bogføres manuelt. Kategoriprisregler kan desuden finde eksisterende samhandelsaftaler, hvis du bruger den samme prisregel (dvs, hvis du opretter en ny prisregel, som anvender den samme kategori som før). Hvis du ikke bruger den samme prisregel, ophæves de eksisterende samhandelsaftaler ikke.

Priserne kan hæves eller sænkes ved hjælp af felterne **Prisregel** og **Prisbasis** kategoriprisreglerne.

- I feltet **Prisregel** skal du vælge den type prisændring, der skal bruges:

    - **Avance** – En procentdel af prisbasis anvendes til at beregne salgsprisen. Et produkt, der f.eks. koster 10,00 og sælges til 15,00, har en avance på 50 procent.
    - **Dækningsbidrag** – En procentdel af salgsprisen bruges til at beregne overskuddet. Et produkt, der f.eks. koster 10,00 og sælges til 15,00, har en avance på 33,3 procent.
    - **Fast beløb** – Et beløb, der lægges til prisbasis, bruges til at beregne salgsprisen. Et produkt, der f.eks. koster 10,00 og sælges til 15,00, har et fast beløb på 5,00.

- Vælg den pristype, der skal ændres, i feltet **Prisbasis**.

    - **Basisomkostninger** – Det beløb, som detailhandleren betalte til leverandøren.
    - **Basispris** – Salgsprisen, før der er blevet anvendt samhandelsaftaler og prisjusteringer.
    - **Aktuel pris** – Salgsprisen, efter der er blevet anvendt samhandelsaftaler og prisjusteringer.

For nemt at opdatere priserne på forskellige produkter fra forskellige produktkategorier kan du bruge de supplerende produktkategorier sammen med kategoriprisregler.

## <a name="best-practices"></a>Bedste fremgangsmåder

Microsoft SQL Server Express bruges ofte til kanaldatabaser på grund af prisen (gratis). Husk, at SQL Server Express har hardwarebegrænsninger og begrænsninger på datastørrelsen. Hvis du ikke planlægger det nøje, kan du hurtigt nå datastørrelsesgrænserne for SQL Server Express. Dette hensyn gælder ikke kun for prissætning, men også andre områder for produktet. Her er nogle få retningslinjer for bedste praksis, som kan hjælpe dig med at reducere størrelsen på dine data:

- Hvis du bruger samhandelsaftaler og priserne ændrer sig, skal du ophæve de gamle samhandelsaftaler ved at angive en slutdato. Denne fremgangsmåde kan med tid reducere antallet af samhandelsaftaler, der opbevares i kanaldatabaserne. Dette er også med til at reducere den datamængde, som algoritmen for prisberegning skal bruge.
- Hvis priserne varierer afhængigt af produktvariant, kan du overveje at bruge produktets basispris som prisen på den mest almindelige variant. Du kan derefter kun bruge samhandelsaftaler for de variantpriser, som er undtagelser. Denne fremgangsmåde er med til at reducere antallet af poster i samhandelsaftalen. Da det er så nemt at importere data til Microsoft Dynamics 365, kan du være fristet til at importere en samhandelsaftale for hver variant af hvert enkelt produkt. Denne fremgangsmåde kan imidlertid resultere i mange samhandelsaftaler med samme værdi. Dette kan øge størrelsen på dataene unødvendigt.
- Retail behandler variantspecifikke priser i rækkefølge, fra den mest specifikke til den mindst specifikke. Hvis en produktdimension ikke påvirker prisen, behøver du ikke at definere samhandelsaftaler for den. Et produkt er f.eks. tilgængeligt i tre farver og fire størrelser, men prisen varierer kun efter størrelsen. Hvis du definerer en samhandelsaftale for alle varianter, vil du oprette 12 poster. I stedet kan du definere en samhandelsaftale kun for hver størrelse og lade farvedimensionen stå tom. I så fald oprettes der kun fire poster.

    Hvis ikke alle værdier i en dimension resulterer i en anden pris, kan du også definere en samhandelsaftale for produktmasteren og lade alle produktdimensioner stå tomme. Definer derefter en særskilt samhandelsaftale kun for hver dimensionsværdi, der giver en anden pris. Hvis størrelsen XXL f.eks. har en højere pris, mens alle andre størrelser har den samme pris, kræves der kun to samhandelsaftaler: én for produktmasteren og én for XXL-størrelsen.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Priser inklusive moms, vs. priser eksklusive moms

Når du angiver salgspriser i Microsoft Dynamics 365, skal du ikke angive, om den angivne prisværdi er med eller uden moms. Værdien er kun prisen. Med indstillingen **Pris er inklusive moms** for detailkanaler kan du konfigurere detailkanaler, så de enten er inklusive eller eksklusive moms i priser. Denne indstilling er angivet for kanalen og kan ændres selv i en enkelt virksomhed.

Hvis du arbejder både med inklusive og eksklusive moms, er det vigtigt, at du angiver priserne korrekt, da det samlede beløb, som kunden betaler, ændres, hvis indstillingen **Pris er inklusive moms** for kanalen ændres.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Forskelle mellem detailprissætning og ikke-detailprissætning

Et enkelt program til prissætning bruges til at beregne detailpriserne på tværs af alle kanaler: Callcenter, Detailbutik og Onlinebutikker. Dette hjælper med at muliggøre ensartede handelsscenarier.

Detailprissætning er designet til at fungere sammen med detailenheder i stedet for enheder uden for detailhandel. Den er specifikt designet til at angive butikspriser, ikke lagerpriser.

Programmet til prissætning i detailhandel understøtter ikke følgende prisfunktioner:

- Angivelse af pris ved hjælp af lagerdimensionerne Lokation og Lagersted.
- Attributbaseret prissætning
- Gennemgang af kreditorrabatter

Programmet til prissætning i detailhandel understøtter desuden **kun** følgende prisfunktioner:

- Prisen baseres på produktdimensioner i rækkefølge fra den mest specifikke variantpris til den mindst specifikke variantpris til produktmasterprisen. En pris, der er angivet ved hjælp af to produktdimensioner (f.eks. Farve og Størrelse), bruges før en pris, der er angivet kun ved hjælp af en produktdimension (f.eks. Størrelse).
- Den samme prisgruppe kan bruges til at styre priser og rabatter.

## <a name="pricing-api-enhancements"></a>Forbedringer af pris-API

Prisen er en af de vigtigste faktorer, der styrer mange kunders indkøbsbeslutninger, og mange kunder sammenligner priserne på forskellige websteder, før de foretager et køb. For at hjælpe med at sikre, at de har konkurrencedygtige priser, holder detailhandlerne nøje øje med konkurrenterne og kører ofte kampagner. For at hjælpe disse forhandlere med at tiltrække kunder er det vigtigt at produktsøgning, gennemsynsfunktion, lister og siden med produktdetaljer viser de mest nøjagtige priser.

I en kommende udgivelse af Retail returnerer **GetActivePrices**-API'en (Application Programming Interface) priser, der omfatter simple rabatter (f.eks. en enkeltlinjerabatter, der ikke er baseret på andre varer i indkøbsvognen). På denne måde er de priser, der vises, tæt på det faktiske beløb, som kunderne skal betale for varerne. Denne API indeholder alle typer simple rabatter: tilknytningsbaserede, loyalitetsbaserede, katalogbaserede og kanalbaserede rabatter. Derudover returnerer API'en navnene og gyldighedsoplysningerne for de anvendte rabatter, så detailhandlerne kan give en mere detaljeret beskrivelse af prisen og skabe en oplevelse af, at det haster, hvis rabatten udløber snart.
