---
title: Styklisteberegningsgrupper
description: Denne artikel indeholder oplysninger om beregningsgrupper for styklister, og hvordan du opretter dem. For at køre en styklisteberegning skal du enten konfigurere beregningsgrupper og tildele dem til enkelte varer eller oprette en standardberegningsgruppe. Beregningsindstillingerne fra beregningsgruppen bruges derefter som standardværdier på siden Styklistekalkulation på tidspunktet for styklistekalkulationen.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 098a2fc065f6ace992dba1b1ae78756d456eb73a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579850"
---
# <a name="bom-calculations-groups"></a>Styklisteberegningsgrupper

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om beregningsgrupper for styklister, og hvordan du opretter dem. For at køre en styklisteberegning skal du enten konfigurere beregningsgrupper og tildele dem til enkelte varer eller oprette en standardberegningsgruppe. Beregningsindstillingerne fra beregningsgruppen bruges derefter som standardværdier på siden Styklistekalkulation på tidspunktet for styklistekalkulationen. 

Der kræves en standardberegningsgruppe på siden **Parametre til lager- og lokationsstyring**, eller der kræves en produktspecifik beregningsgruppe på siden **Frigivne produktdetaljer**. Systemet søger først efter opsætningen af beregningsgruppen på siden **Frigivne produktdetaljer**. Hvis der ikke findes en beregningsgruppe, søger det på siden **Parametre til lager- og lokationsstyring**. Hvis systemet ikke kan finde en beregningsgruppe, får brugeren en fejlmeddelelse under beregningen. En beregningsgruppe indeholder politikker for kostprismodellen, salgsprismodellen og advarselskontrollisten. Beregningsindstillingerne fra beregningsgruppen bruges som standardværdier på siden **Styklistekalkulation** på tidspunktet for styklistekalkulationen.

## <a name="purposes-of-bom-calculation-groups"></a>Formålet med styklisteberegningsgrupper
Du kan tildele en styklisteberegningsgruppe til varer af flere årsager:

-   Ved at indstille feltet **Kostprismodel** angiver du kilden til kostbidragsdataene for en købt komponent under beregningen af de planlagte omkostninger for en produceret vare. Visse producenter ønsker at beregne planlagte omkostninger ved hjælp af samhandelsaftalerne om indkøbspriser for købte komponenter eller et andet grundlag, f.eks. indkøbsprisposterne i en efterkalkulationsversion.
-   Ved at indstille feltet **Salgsprismodel** angiver du, hvordan varens data bruges til at beregne en foreslået salgspris. Du kan enten angive varesalgsprisen eller omkostningsgruppen. Visse producenter ønsker at beregne en foreslået salgspris for producerede varer. Den foreslåede salgspris kan afspejle en fremgangsmåde med registrerede priser, der er baseret på komponentens salgsprispost. Den foreslåede salgspris kan også afspejle en fremgangsmåde med beregning af omkostninger plus avance, der er baseret på komponentens kostpris og gældende avanceprocent, som er knyttet til varens omkostningsgruppe.
-   Ved at bruge feltet **Stop udfoldning** angiver du, at en produceret vare skal behandles som en købt vare med henblik på omkostningstotaler under styklisteberegning. Af typiske situationer kan nævnes en købt vare, der indimellem produceres, eller en produceret vare, der nu købes. Varen angives først som en produceret vare for at definere stykliste- og ruteoplysninger og for at understøtte produktionsordrer for varen. Flaget **Stop udfoldning** forhindrer imidlertid, at omkostningsberegninger bruger varens stykliste og rute. I stedet bruger styklisteberegningen den angivne kostpris for varen.

## <a name="calculation-groups"></a>Beregningsgrupper
Du kan definere beregningsgrupper under **Konfiguration af foruddefinerede omkostningspolitikker** i Omkostningsstyring. Ved hjælp af beregningsgrupper, der er tildelt til varer, kan du angive, hvordan den kostpris eller salgspris for komponenter, der er anført i beregningsgruppen, leveres til beregningen. På siden **Beregningsgrupper** kan du definere en kostprismodel, alternativ kostprismodel, en salgsprismodel og advarsler.

### <a name="cost-price-model"></a>Kostprismodel

Der er fire indstillinger for feltet **Kostprismodel**:

-   **Varens kostpris** – Kostprisen fra tabellen **Frigivet produkt** bruges, eller en kombination af varedimensioner bruges som kostpris.
-   **Købspris for vare** – Købsprisen fra feltet **Kostpris** under fanen **Køb** på siden **Listen Frigivne produkter** bruges.
-   **Samhandelsaftaler** – Du kan konfigurere samhandelsaftaler for bestemte kombinationer af varer og leverandører eller for bestemte websteder. Når du derefter vælger indstillingen **Samhandelsaftaler** her, bruges den samhandelsaftale, du har oprettet til købsprisen sammen med varen og webstedet.
-   **Lagerpris** – Den aktuelle lagerværdi for varen bruges til at beregne enhedskostprisen i styklistekalkulationen. En kostpris pr. enhed beregnes kun, hvis det bogførte antal og det fysiske antal er større end 0 (nul).

### <a name="alternative-cost-price"></a>Alternativ kostpris

Feltet **Alternativ kostpris** har de samme muligheder som feltet **Kostprismodel**. Dette felt bruges dog kun, når der ikke kan findes en pris i den primære kostprismodel.

### <a name="sales-price-model"></a>Salgsprismodel

Der er to indstillinger til beregning af feltet **Salgspriser**:

-   **Omkostningsgruppe** – Når denne indstilling er valgt, beregnes salgsprisen på grundlag af kostprisen og procentdelen af avancesættet fra omkostningsgruppe.
-   **Salgspris for vare** – Når denne indstilling er valgt, bruges salgsprisen i oversigtspanelet **Sælg** fra tabellen Frigivet produkt.

### <a name="stop-explosion"></a>Stop udfoldning

Afkrydsningsfeltet **Stop udfoldning** bruges til at angive, hvornår en produceret vare skal behandles som en indkøbsvare. Feltet **Stop udfoldning** er typisk ikke markeret. Når du markerer dette afkrydsningsfelt, angiver du, at en produceret vare skal behandles som en købskomponent i stedet for en produceret komponent med henblik på Styklistekalkulation. Afhængigt af webstedet kan varens omkostninger stadig beregnes ved hjælp af styklisteberegningerne. Udfoldning af indkøbsordreforslag og produktionsordrer stopper ved styklisten, hvis komponenter er forbundet med den beregningsgruppe, som afkrydsningsfeltet **Stop udfoldning** er markeret for. Behovsplanlægningen opretter ordreforslagene på selve styklisten og ikke på de varer, som indgår i styklisten. Ved at markere dette afkrydsningsfelt, angiver du grundlæggende, at der ikke bliver tilføjet en omkostning i styklistekalkulationen for varer, der har denne beregningsgruppe.

### <a name="warnings"></a>Advarsler

I oversigtspanelet **Advarsler** skal du vælge indstillingerne for advarselsmeddelelser, som brugere skal have vist, når de udfører styklisteberegninger. 

For eksempel, hvis du markerer afkrydsningsfeltet **Ingen stykliste**, modtager brugeren en advarsel, hvis der findes nogen aktiv styklisteversion for en af komponenterne eller den overordnede vare, som styklistekalkulationen køres for. Hvis du markerer afkrydsningsfeltet **Ingen rute**, får brugeren vist en advarsel, hvis der ikke findes nogen aktiv ruteversion. Hvis du bruger ressourcer på ruter og operationer, kan du bede systemet kontrollere disse ressourcer. Hvis en ressource ikke findes på hver linje i den aktive rute, modtager brugeren en advarsel. 

Du kan også kontrollere og undersøge forbruget. Forbruget er antallet i en bestemt rute. Det repræsenterer typisk den tid, der kræves for at udføre en bestemt handling for en produktionsproces. Du kan kontrollere, om en vare har en kostpris. Hvis der ikke er en aktiv kostpris for en vare, tilføjes der ingen omkostning i styklistekalkulationen. 

Du kan også kontrollere og bekræfte alderen for kostprisen. Skriv f.eks. **60** for at angive, at enhedskostprisen skal reevalueres efter 60 dage. Hvis denne grænse nås, genererer systemet en advarsel. For eksempel blev der angivet en kostpris for en vare i januar i år. Hvis det nu er august, hvilket er mere end 60 dage, efter at kostprisen blev angivet, modtager brugeren en advarsel, når styklistekalkulationen køres. Du kan angiv en procent i feltet **Min. dækningsbidrag**. Denne værdi angiver det punkt, hvor det mindste dækningsbidrag ikke er opfyldt. Hvis dækningsbidraget for en bestemt komponent ikke er opfyldt, modtager brugeren en advarsel. Dette felt kan derfor være med til at sikre, at du ikke underbyder omkostningerne og de ekstra lagerbindingsomkostninger, der kan kræves for dine varer.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Standardkonfiguration af parametre til lager- og lokationsstyring

Da der kræves beregningsgrupper for at kunne køre beregninger, skal du oprette en standardberegningsgruppe i lagerstyringsparametrene. Denne opsætning gør det muligt for virksomheder at have en standardomkostningsgruppe og -avancesæt for alle varer. Hvis en bestemt vare har særlige beregningskrav, kan brugeren tildele en anden beregningsgruppe til varen. Typisk kan du angive beregningsgrupper for styklistekomponentvarer i stedet for styklistevarer. Når der vises advarsler, kan der dog anvendes beregningsgrupper. En beregningsgruppe, der er tildelt til varer, tilsidesætter den standardværdi, der er angivet i lagerstyringsparametrene. 

Du kan definere standardparameteren i **Omkostningsstyring** &gt; **Konfiguration af regnskabspolitik for lager** &gt; **Parametre** &gt; **Lagerregnskab** &gt; **Beregningsgruppe**. Ved at oprette en standardkonfigurationsgruppe kan du også konfigurere advarsler i situationer, hvor brugerne bliver advaret under styklistekalkulationsprocessen, hvis de valgte komponenter kan det medføre beregningsfejl.

### <a name="view-warning-messages-on-the-complete-page"></a>Vise advarsler på siden Fuldført

En styklistekalkulation genererer advarsler. Du kan få vist advarslerne om den valgte vare. For eksempel kan du i Salg og marketing oprette en ny salgsordre for varen D0001. Derefter skal du på salgsordrelinjen klikke på **Beregn baseret på stykliste/formel** i menuen **Opdater linje** for at få vist oplysninger om beregningen og advarsler. Du kan også få vist resultater af styklistekalkulationer på siden **Fuldført**. For advarselsmeddelelser gælder der kun to advarselssituationer for producerede varer, mens der gælder fire advarselssituationer for alle varer:
-   Identificer, hvornår en produceret vare ikke har en aktiv stykliste.
-   Identificer, hvornår en produceret vare ikke har en aktiv rute.
-   Identificer, hvornår varen på en styklistelinje har et antal på 0 (nul).
-   Identificer, hvornår varen på en styklistelinje har en kostpris på 0 (nul), eller hvornår den ikke har en kostprispost.
-   Identificer, hvornår varen på en styklistelinje har en forældet kostpris. Advarslen afspejler en sammenligning af beregningsdatoen og de angivne dage for den maksimale alder for en kostpris.
-   Identificer, hvornår varen på en styklistelinje har en rentabilitetsprocentdel, der er mindre end ønsket.

Du kan definere flere styklisteberegningsgrupper, afhængigt af dine behov for variationer i advarselsmeddelelser. En styklisteberegningsgruppe, der f.eks. har advarselssituationer om en aktiv stykliste, et komponentantal på 0 (nul) og en komponentkostpris på 0 (nul), kan være tilstrækkeligt. Når du starter en styklisteberegning, kan du tilsidesætte de gældende advarselssituationer, der er knyttet til styklisteberegningsgruppen. Du kan også tilføje eller fjerne advarselsbetingelser. Hvis den aktuelle situation ikke omfatter rutedata, kan du f.eks. fjerne den gældende advarselsbetingelse for en aktiv rute. **Bemærk:** Tid og fremmøde omfatter en **Beregningsgrupper**-side, men siden har ingen relation til styklisteberegningsgrupper. Under Tid og fremmøde kan arbejdere tilknyttes beregningsgrupper, der afspejler grupperingen af arbejdere, der er tilknyttet den samme tilsynsførende eller leder. En tilsynsførende eller leder kan automatisk eller manuelt rette beregningen af registreringer til arbejdere.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]