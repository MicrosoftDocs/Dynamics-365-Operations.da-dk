---
title: Opsætning af Indtægtsføring
description: Dette emne beskriver opsætningsindstillingerne for Indtægtsføring og deres konsekvenser.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c395aabfc8705b4713cf1041b5644ac478d8c1a4c4c211334aea3572f1618b84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759011"
---
# <a name="revenue-recognition-setup"></a>Opsætning af Indtægtsføring
[!include [banner](../includes/banner.md)]

Der er blevet tilføjet et nyt **Indtægtsføring**-modul, som indeholder menupunkter for alle de opsætninger, der kræves. Dette emne beskriver opsætningsindstillingerne og deres konsekvenser.

> [!NOTE]
> Funktionen Indtægtsføring kan ikke aktiveres via Funktionsstyring. I øjeblikket skal du bruge konfigurationsnøgler til at aktivere funktionen.

> Indtægtsføring, herunder bundtfunktionalitet, understøttes ikke til brug i Commerce-kanaler (e-handel, POS, callcenter). Varer, der er konfigureret med indtægtsføring, bør ikke føjes til ordrer eller transaktioner, der er oprettet i Commerce-kanaler.

Modulet **Indtægtsføring** har følgende opsætningsindstillinger:

- Indtægtsføringskladder
- Parametre for indtægtsføring
- Indtægtstidsplaner 
- Opsætning af lager

    - Varegrupper og frigivne produkter
    - Definere indtægtstidsplan
    - Definere indtægtspris

        - Posteringsprofiler
        - Bundter

    - Bundtkomponenter
    - Bundtvare

- Opsætning af Projekt

## <a name="revenue-recognition-journals"></a>Indtægtsføringskladder

Der er blevet introduceret en ny kladdetype for indtægtsføring. Kladden er påkrævet og bruges i to scenarier.

Det første scenario forekommer, efter at alle de kontraktmæssige forpligtelser er opfyldt, når den udskudte indtægt registreres ved at oprette en indtægtsføringskladde, der er baseret på oplysningerne i indtægtstidsplanen. Kladden indeholder en regnskabspost, der flytter saldoen fra finanskontoen for udskudt indtægt til finanskontoen for indtægt.

Det andet scenarie forekommer, når der oprettes en kladde, efter at omfordelingen finder sted. Der foretages en omfordeling, når en salgsordrelinje føjes til en tidligere faktureret salgsordre, eller når der oprettes en ny salgsordre, som indeholder en linje, der er en del af den oprindelige kontrakt. Hvis en faktura blev bogført, før den nye salgsordrelinje tilføjes, skal der oprettes en korrigerende regnskabspost for den bogførte debitorfaktura.

Kladden konfigureres på siden **Kladdenavne** (**Indtægtsføring \> Opsætning \> Kladdenavne**). Kladdetypen skal være angivet til **Indtægtsføring**. Indtægtsføringskladden giver dig mulighed for at vælge det posteringslag, der skal bogføres på.

## <a name="parameters-for-revenue-recognition"></a>Parametre for indtægtsføring

Indstillingerne for indtægtsføring konfigureres på fanen **Indtægtsføring** på siden **Finansparametre** (**Indtægtsføring \> Opsætning \> Finansparametre**). Følgende indstillinger er tilgængelige:

- **Navn på indtægtsføringskladde** – Vælg den kladde, der er oprettet til indtægtsføring. Kladden er påkrævet, når der registreres indtægter fra indtægtstidsplanen, eller når du foretager ny omfordeling for en salgsordre, der allerede er faktureret.
- **Aktivér rabatfordelingsmetode** – Angiv denne indstilling til **Ja** for at fastlægge indtægtsprisen via tildelingen af den fair markedsværdi, der er defineret i indtægtsprisen for de enkelte udleverede produkter. Denne fordeling omfatter fordelingen af eventuelle linjerabatter på tværs af varerne. Hvis denne indstilling er angivet til **Nej**, bruger systemet den medianpris, der er angivet i indtægtsprisen for hvert af de frigivne produkter. Hvis denne indstilling er angivet til **Nej**, men der ikke er konfigureret nogen medianpris for de frigivne produkter, foretages fordelingen af indtægtsprisen ikke.
- **Medtag hovedrabatter** – Angiv denne indstilling til **Ja** for at fastsætte indtægtsprisen ved at fordele hovedrabatterne på tværs af produkter. Hvis denne indstilling er angivet til **Nej**, medtages hovedrabatten ikke i fordelingen af indtægtsprisen.
- **Deaktiver kontraktvilkår** – Angiv denne indstilling til **Ja**, hvis produkter, der har indtægtstypen **Support efter kontrakt**, kan frigives, selvom kontraktens start- og slutdato ikke er defineret for dem. Kontraktens start-og slutdato skal typisk angives for varer af indtægtstypen **Support efter kontrakt**. Hvis kontraktens start-og slutdato ikke er defineret, beregnes oplysningerne om indtægtstidsplanen på bogføringen ved hjælp af antallet af forekomster og fakturadatoen.
- **Bogfør fakturarettelser til debitor ved omfordeling** – Hvis du foretager en omfordeling for fakturaer, der allerede er bogført, skal regnskabsposten for den bogførte faktura rettes. Brug denne indstilling til at angive, hvordan rettelsen skal udføres.

    - Angiv indstillingen til **Nej** for at begrænse bogføringen af den korrigerende transaktion til Finans. Når denne indstilling er angivet til **Nej**, oprettes der ikke yderligere dokumenter under Debitor for den interne regnskabsrettelse. Når fakturaen betales, bruger udligningsprocessen den gamle regnskabspost til at bogføre eventuelle kasserabatter, realiserede gevinster eller tab.
    - Angiv denne indstilling til **Ja** for automatisk at oprette et tilbageført dokument og en ny faktura for den korrigerende transaktion i Debitor. Da denne rettelse er en intern regnskabsrettelse, sendes eller kommunikeres de nye dokumenter ikke til kunden. Det tilbageførte dokument udlignes med den oprindelige faktura, og den nye rettede faktura betales af kunden. Bemærk, at alle tre dokumenter vises i rapporter, f.eks. kundeopgørelsen.

[![Oplysninger om opsætning.](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Indtægtstidsplaner

Der skal oprettes en indtægtstidsplan for hver forekomst, som indtægten kan udskydes for. Hvis din organisation f.eks. yder support over en periode på seks måneder, 12 måneder, 18 måneder og 24 måneder, skal du oprette en indtægtstidsplan for de enkelte perioder. Opsætningen af indtægtstidsplanen bestemmer, hvordan indtægtsprisen fordeles i det antal perioder, du vælger. Den bestemmer også de standarddatoer, der angives for den indtægtstidsplan, der oprettes, når fakturaen bogføres.

Hvis du registrerer indtægt efter milepæl, anbefales det, at du opretter en indtægtsføringstidsplan for antallet af milepæle, uanset registreringsdatoerne. Når du har oprettet tidsplanerne, kan du redigere dem, så de afspejler de forventede milepælsdatoer. Disse poster kan sættes på hold, indtil du får besked om, at milepælen er opfyldt, og indtægterne kan registreres.

Indtægtstidsplaner oprettes på siden **Indtægtstidsplaner** (**Indtægtsføring \> Opsætning \> Indtægtstidsplaner**).

[![Indtægtstidsplaner.](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Angiv beskrivende værdier i felterne **Indtægtstidsplan** og **Beskrivelse**. Følgende yderligere indstillinger bruges til at oprette indtægtstidsplanen, når fakturaen bogføres.

- **Forekomster** – Angiv antallet af måneder eller Forekomster for udskydelse af indtægt.
- **Automatisk hold** – Markér dette afkrydsningsfelt, hvis alle linjer i indtægtstidsplanen automatisk skal sættes på hold, når fakturaen bogføres. Holdet skal fjernes manuelt fra hver linje i tidsplanen, før linjens udskudte indtægt kan registreres.
- **Automatiske kontraktvilkår** – Markér dette afkrydsningsfelt, hvis kontraktens start-og slutdato skal angives automatisk. Disse datoer angives automatisk for frigivne produkter af indtægtstypen **Support efter kontrakt**. Kontraktens startdato angives automatisk til salgsordrelinjens ønskede afsendelsesdato, og kontraktens slutdato angives automatisk til startdatoen plus det antal måneder eller forekomster, der er defineret i opsætningen af indtægtstidsplanen. Produktet på salgsordrelinjen er f.eks. for en garanti på ét år. Standardtidsplanen for indtægt er **12M** (12 måneder), og afkrydsningsfeltet **Automatiske kontraktvilkår** er markeret for denne indtægtstidsplan. Hvis salgsordrelinjen har den ønskede afsendelsesdato d. 16. december, 2019, er standardkontraktens startdato 16. december 2019, og standardkontraktens slutdato er 15. december 2020.
- **Indregningsgrundlag** – Indregningsgrundlaget bestemmer, hvordan indtægtsprisen fordeles hen over forekomsterne.

    - **Månedligt efter dato** – beløbet fordeles på grundlag af de faktiske dage i hver måned.
    - **Månedligt** – Beløbet fordeles ligeligt mellem det antal måneder, der er defineret i forekomsterne.
    - **Forekomster** – Beløbet fordeles ligeligt på tværs af forekomsterne, men det kan inkludere en ekstra periode, hvis du vælger **Faktisk startdato** som registreringsprincip.

- **Registreringsprincip** – Registreringsprincippet bestemmer de standarddatoer, der er angivet i indtægtstidsplanen for fakturaen.

    - **Faktisk startdato** – Tidsplanen oprettes ved hjælp af kontraktens startdato (for \[PCS\]-varer (Support efter kontrakt)), eller fakturadatoen (for vigtige og mindre vigtige varer).
    - **Den 1. i måneden** – Datoen på den første linje i tidsplanen er kontraktens startdato (eller fakturadatoen). Alle efterfølgende linjer i tidsplanen oprettes dog for den første i måneden.
    - **Midt i måneden** – Datoen på den første linje i tidsplanen afhænger af fakturadatoen. Hvis fakturaen bogføres den første til den 15. i måneden, oprettes indtægtstidsplanen ved hjælp af den første dag i måneden. Hvis fakturaen bogføres den 16. i måneden eller senere, oprettes indtægtstidsplanen ved hjælp af den første dag i den næste måned.
    - **D. 1. i næste måned** – Datoen i tidsplanen er den første dato i næste måned.

Vælg knappen **Oplysninger om indtægtstidsplan** for at få vist de generelle perioder og de procentdele, der registreres i hver periode. Værdien for **Registrer procent** opdeles som standard ligeligt over antallet af perioder. Hvis registreringsgrundlaget er angivet til enten **Månedligt** eller **Forekomster**, kan registreringsprocenten blive ændret. Når du ændrer registreringsprocenten, får du besked om, at totalen ikke er lig med 100 procent. Hvis du modtager meddelelsen, kan du fortsætte med at redigere linjer. Den samlede procentdel skal dog være lig med 100, før du lukker siden.

[![Oplysninger om indtægtstidsplan.](./media/revenue-recognition-revenue-schedule-details.png)](./media/revenue-recognition-revenue-schedule-details.png)

## <a name="inventory-setup"></a>Opsætning af lager

Du kan genkende indtægten for frigivne produkter på salgsordrer, men ikke for salgskategorier på salgsordrer eller i fritekstfakturaer, hvis der ikke er medtaget nogen varer i dokumentet. De valg, du foretager, når du konfigurerer frigivne produkter, bestemmer, hvordan varens indtægt registreres. Valget bestemmer f.eks., om indtægtsprisen er fordelt, og om indtægten er udskudt ved hjælp af en indtægtstidsplan.

Opsætningen kan begynde i oversigtspanelet **Indtægtsføring** på siden **Varegruppe** (**Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Varegruppe**). Denne side indeholder flere opsætningsfelter. Disse felter bruges kun til at angive standardværdier for nye frigivne produkter, der er oprettet i systemet. Når der oprettes nye produkter, angives de værdier, du angiver her, som standard for varegruppen. Du kan tilsidesætte standardværdierne for frigivne produkter på siden **Frigivne produkter** (**Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Frigivne produkter**). De standardværdier, der er angivet for de frigivne produkter, overføres derefter til salgsordren.

## <a name="item-groups-and-released-products"></a>Varegrupper og frigivne produkter

### <a name="define-the-revenue-schedule"></a>Angiv indtægtstidsplanen

Indtægten på salgsordrelinjen udskydes, hvis der er defineret en indtægtstidsplan for det frigivne produkt, og anvendes som standard på salgsordrelinjen. Hvis indstillingen skal bruges som standard for produktet, kan du definere indtægtstidsplanen på oversigtspanelet **Indtægtsføring** på siden **Varegruppe** (**Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Varegruppe**). Du kan også angive indstillingen for det frigivne produkt i oversigtspanelet **Indtægtsføring** på siden **Frigivne produkter** (**Indtægtsføring \> Opsætning \> Lageropsætning \> Frigivne produkter**).

I feltet **Indtægtstidsplan** skal du vælge den indtægtstidsplan, der repræsenterer den periode, hvor indtægten skal udskydes. Indtægtstidsplanen angives automatisk på salgsordrelinjen, og oplysningerne for tidsplanen oprettes, når fakturaen bogføres.

### <a name="define-the-revenue-price"></a>Definer indtægtsprisen

Der kan oprettes varegrupper og frigivne produkter ved hjælp af enten medianpris-metoden eller rabatfordelings-metoden. Begge metoder kræver forskellige indstillinger på siden **Frigivne produkter**:

- **Er indtægtsfordeling aktiv** – Angiv denne indstilling til **Ja** for at medtage det frigivne produkt i beregning af indtægtsfordeling. Hvis denne indstilling er angivet til **Nej**, anvender det frigivne produkt medianpris-metoden, hvil medianprisen er angivet. Hvis medianprisen ikke er angivet, anvendes enhedsprisen på salgsordrelinjen til bogføring af indtægt eller udskudt indtægt.
- **Indtægtstype** – Vælg den indtægtstype, der definerer det frigivne produkt:

    - **Vigtig** – Varen er en primær kilde til en organisations indtægt. Denne værdi er standardindstillingen.
    - **Mindre vigtig** – Varen er ikke en primær kilde til en organisations indtægt. Når indstillingerne for medianpris anvendes, udføres der en "carve-out" af prisen i forhold til medianprisen, og den fordeles derefter. En vigtig vare har f.eks. en fast pris, der skal godkendes til indtægt. Hvis der er en rabat, kan rabatten blive taget fra indtægten fra vigtige varer, men **kun** op til det faste prisbeløb. Resten af rabatten tages ud af indtægten for mindre vigtige varer. Alternativt tages rabatten muligvis ikke fra indtægten fra vigtige varer.
    - **Support efter kontrakt** – Varen understøtter andre elementer, der er inkluderet i salget til kunden. Indtægtsprisen fordeles over de vigtige og mindre vigtige produkter, der er medtaget i salget. Afhængigt af opsætningen kræver PCS-varer muligvis ikke, at der angives start- og slutdatoer for kontrakter på salgsordrelinjen.

- **Udeluk fra carve out** – Angiv denne indstilling til **Ja** for at angive, at varens medianpris ikke kan reguleres under den minimale procentdel, der er defineret, eller over den maksimale procentdel. En eventuel indtægtspris vil blive afledt af indtægtsprisen for et andet frigivet produkt, der er medtaget på salgsordren. Hvis denne indstilling er angivet til **Nej**, kan varens medianpris blive justeret eller "carved out". Bemærk, at hvis du sælger mere end én vare, der er konfigureret som medianpris, skal der oprettes mindst ét frigivet produkt, hvor indstillingen **Udeluk fra carve-out** er angivet til **Nej**. På den måde er der mindst én vare, som eventuelle forskelle i indtægtsprisen kan tildeles.
- **Medianpris** – Angiv denne indstilling til **Ja** for at angive, at varens indtægtspris skal justeres, så den er lig med medianprisen, hvis den er under den minimumtolerance, som du angiver, eller overstiger maksimumtolerancen, og at carve-out-beløbet skal fordeles til linjer, som har produkter, hvor indstillingen **Udeluk fra carve-out** er angivet til **Nej**.

    - **Maksimumtolerance** – Angiv den tilladte procentdel over medianprisen.
    - **Minimumtolerance** – Angiv den tilladte procentdel under medianprisen.

Når du er færdig med at konfigurere indstillingerne for det frigivne produkt, skal du definere indtægtsprisen manuelt ved at angive prisen for handelsværdien eller medianprisen (hvis du anvender median-metoden) på siden **Indtægtspriser** (gå til **Indtægtsføring \> Opsætning \> Lageropsætning \> Frigivne produkter**, og derefter skal du i handlingsruden på fanen **Sælg** i gruppen **Indtægtsføring** vælge **Indtægtspriser**).

[![Indtægtspriser.](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Den indtægtspris, der er defineret manuelt på denne side, bruges til at bestemme fordelingen af indtægtsprisen for de enkelte salgsordrer baseret på de definerede kriterier. Hvert kriterie sammenholdes med salgsordrelinjen for at bestemme den indtægtspris, der skal bruges i fordelingsprocessen.

- **Varekode** og **Varerelation** – Der kan angives en indtægtspris for et individuelt produkt eller en gruppe af produkter. Hvis du vælger **Tabel** i feltet **Varekode**, skal du vælge det frigivne produkt i feltet **Varerelation**. Hvis du vælger **Gruppe** i feltet **Varekode**, skal du vælge varegruppen i feltet **Varerelation**.
- **Kontokode** og **Konto/gruppenummer** – Der kan angives en indtægtspris for alle kunder, individuelle kunder eller en gruppe af kunder. Hvis du vælger **Alle** i feltet **Kontokode**, anvendes prisen for alle kunder. Hvis du vælger **Tabel** i feltet **Kontokode**, skal du vælge kunden i feltet **Konto/gruppenummer**. Hvis du vælger **Gruppe** i feltet **Kontokode**, skal du vælge gruppen i feltet **Konto/gruppenummer**.
- **Valuta** – Du skal angive en separat indtægtspris for hver valuta, du angiver en salgsordre i. Hvis du f.eks. sælger i amerikanske dollar, canadiske dollar og euro, skal du angive en indtægtspris i alle tre valutaer. Indtægtsprisen er ikke oversat fra én valuta, f.eks. regnskabsvalutaen, til alle andre transaktionsvalutaer, som du bruger.
- **Beløb eller procentdel af liste** – Angiv, om indtægtsprisen er konfigureret som et beløb eller som en procentdel af listeprisen. Hvis du vælger **Procentdel af liste**, kan brugere angive medianprisen som en procentdel af listeprisen i stedet for et beløb. Værdien **Procentdel af liste** anvendes kun for frigivne produkter, der er konfigureret som PCS-varer.
- **Pris for indtægtsfordeling** – Afhængigt af den værdi, du har valgt i feltet **Beløb eller procentdel af liste**, skal du angive enten et beløb eller en procentdel, der repræsenterer den indtægtspris, der bruges til at fordele indtægten på tværs af elementerne på salgsordren.
- **Fra-dato** og **Til-dato** – Angiv det datointerval, som indtægtsprisen er aktiv for. Disse felter er valgfrie.

Hvis indstillingen **Aktivér rabatfordelingsmetode** på siden **Finansparametre** er angivet til **Ja**, og hvis feltet **Indtægtstype** for det frigivne produkt er angivet til **Support efter kontrakt**, skal du også angive de varer, der understøttes af det frigivne produkt. Denne opsætning udføres på siden **Opsætningsgrundlag** (gå til **Indtægtsføring \> Opsætning \> Opsætning af lager \> Frigivne produkter**, og i handlingsruden skal du derefter på fanen **Sælg** i gruppen **Indtægtsføring** vælge **Opsætningsgrundlag**).

På siden **Opsætningsgrundlag** skal du tilføje en post for hver varegruppe, som varen understøtter. Når indtægtsfordelingen udføres, fordeles indtægtsprisen for de vigtige og mindre vigtige dele for PCS-varen.

### <a name="posting-profiles"></a>Posteringsprofiler

Tre yderligere bogføringstyper understøtter muligheden for udskydelse af indtægt. Disse bogføringstyper oprettes under fanen **Salgsordre** på siden **Bogføring** (**Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Bogføring**).

- **Udskudt indtægt** – Angiv hovedkontoen for den indtægtspris, der skal bogføres til udskudt indtægt (i stedet for indtægt). Indtægtsprisen udskydes, hvis salgsordrelinjen har en indtægtstidsplan.
- **Udskudt vareforbrug** – Angiv hovedkontoen for vareforbrugsbeløbet, der bogføres til udskudte omkostninger for varforbrug, hvis indtægten også er udskudt.
- **Delvis clearing af fakturaindtægt** – Angiv hovedkontoen for den clearingkonto, der anvendes, når salgsordren faktureres delvist, eller når der foretages ny fordeling. Saldoen på denne konto returnerer til 0 (nul), når salgsordrerne er fuldt faktureret.

### <a name="bundles"></a>Bundter

Bundtede varer er entydige frigivne produkter, der er konfigureret, så de omfatter komponenter. Denne opsætning sker ved hjælp af stykliste-funktionen. Når der angives en bundtet vare på en salgsordre, bruges de enkelte komponenter til at bestemme indtægtspriserne og indtægtstidsplanerne. Men udskrevne dokumenter for kunden, f.eks. salgsordren og fakturaen, afspejler bundtvaren.

#### <a name="bundle-components"></a>Bundtkomponenter

De komponenter, der er medtaget i bundtet, skal være oprettet på siden **Frigivne produkter** (**Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Frigivne produkter**). Disse komponenter er frigivne produkter, og de skal oprettes på samme måde som produkter, der indgår i en stykliste. Et frigivet produkt kan f. eks. være en vare af typen **Vare** eller **Service**, men den skal være tildelt en varemodelgruppe, hvor indstillingen **Lagervare** er angivet til **Ja**. Du kan finde flere oplysninger i dokumentationen for opsætning af styklistevarer.

Komponenterne skal også opsættes til indtægtsføring, lige som hvis de var produkter, der kan sælges individuelt på en salgsordre. Kontroller f.eks., at den korrekte indtægtspris er angivet for de enkelte komponenter, og at prisgrundlaget er angivet for PCS-varer.

#### <a name="bundle-items"></a>Bundtvarer

Når du opretter en bundtvare, skal du opsætte to felter på siden **Frigivne produkter** (**Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Frigivne produkter**):

- På oversigtspanelet **Opret** i feltet **Produktionstype** skal varen oprettes som en styklistevare.
- På oversigtspanelet **Generelt** i feltet **Bundt** skal varen markeres som en bundtvare.

Komponenterne skal derefter tildeles til den overordnede bundt/styklistevare på siden **Styklisteversioner** (gå til **Indtægtsføring \> Opsætning \> Lager- og produktopsætning \> Frigivne produkter**, og i handlingsruden på fanen **Opret** i gruppen **Stykliste** skal du vælge **Styklisteversioner**). Du kan finde flere oplysninger i dokumentationen for opsætning af styklister.

[![Frigivne produkter, styklistetidsplaner.](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Hvis den overordnede bundtvare og bundtkomponenterne er indstillet til fordeling, fordeles bundt-indtægtsprisen til komponenterne ud fra deres procentdele af indtægtsbidrag.

## <a name="project-setup"></a>Opsætning af Projekt

Indtægtsføring kan også anvendes for salgsordrer, der er oprettet via et Tid og materialer-projekt. I forbindelse med salgsordrer, der stammer fra projekter, skal du blot angive hovedkontiene i de projektbogføringsprofiler, der bruges til at bogføre projektfakturaer. Hovedkontiene defineres på siden **Opsætning af finanskontering** (**Indtægtsføring \> Opsætning \> Opsætning af Projekt \> Opsætning af finanskontering**).

- **Udskudt fakturaindtægt** (under **Indtægtskonti**) – Angiv hovedkontoen for den indtægtspris, der skal bogføres til udskudt indtægt (i stedet for indtægt). Indtægtsprisen udskydes, hvis salgsordrelinjen har en indtægtstidsplan.
- **Udskudt omkostning** (under **Omkostningskonti**) – Angiv hovedkontoen for vareforbrugsbeløbet, der bogføres til udskudte omkostninger for varforbrug, hvis indtægten også er udskudt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]