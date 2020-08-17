---
title: Genopfyldning over lokationskapacitet
description: Dette emne indeholder oplysninger om funktionen Genopfyldning over lokationskapacitet. Denne funktion aktiverer alt genopfyldningsarbejde, der kræves for dagen, der skal oprettes, og styrer tilgængeligheden af genbestillingsarbejdet for at sikre, at plukpladsen ikke løber tør for lager eller overstiger kapaciteten.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5591af5fce4eb3fc901919b98f654faa5e160c54
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652219"
---
# <a name="replenishment-over-location-capacity"></a>Genopfyldning over lokationskapacitet

[!include [banner](../includes/banner.md)]

Nogle store eller pladsbegrænsende lagersteder skal levere et større antal varer på en dag, end der er plads til på plukpladsen. Funktionen *Genopfyldning over lokationskapacitet* aktiverer alt genopfyldningsarbejde, der kræves for dagen, der skal oprettes, og styrer tilgængeligheden af genbestillingsarbejdet for at sikre, at plukpladsen ikke løber tør for lager eller overstiger kapaciteten.

Funktionen gør det muligt at oprette mere genopfyldningsarbejde, end der er plads til på en lokation, og den blokerer genopfyldningsarbejde i at blive fuldført, når lokationen er fuld. Efterhånden som lager på plukpladsen falder under en konfigurerbar grænse, bliver det mere genopfyldningsarbejde tilgængeligt.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Aktivere funktionen Genopfyldning over lokationskapacitet

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge):

1. Blokering af arbejde i hele organisationen
1. Genopfyldning over lokationskapacitet

## <a name="set-up-the-feature-for-the-example-scenario"></a>Konfigurere funktionen til eksempelscenariet

Dette afsnit indeholder retningslinjer og et eksempel, der viser, hvordan du kan konfigurere denne funktion og forberede eksempeldata til det eksempelscenario, der er angivet senere i dette emne.

### <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil arbejde dig gennem [eksempelscenariet](#example-scenario) ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

### <a name="location-profile"></a>Lokationsprofil

Aktivér funktionen til genopfyldning over kapacitet på lokationsprofilen.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **PICK-06** i venstre rude.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Genopfyldning** kan du angive følgende værdier:

    - **Overstiger lokationskapacitet:** *Ja*

        Når indstillingen er aktiveret, kan den maksimale kapacitet for lokationen overskrides med genopfyldningsarbejde. Dette aktiverer også andre felter i oversigtspanelet **Genopfyldning**.

    - **Grænsetype for arbejdstilgængelighed:** *Antal*

        Dette felt definerer den metode, der bruges til at bestemme, hvornår der skal frigives mere arbejde. Du kan frigive enten procentsats eller antal:

        - *Procent* – Vælg denne indstilling for at bruge den procentvise kapacitet, der er baseret på lagergrænser eller volumenmålinger. Hvis du vælger denne indstilling , aktiveres feltet **Overløbsprocent**, og det deaktiverer de to relaterede felter af typen antal, **Overløbsantal** og **Overløbsenhed**.

            Du kan bruge denne indstilling, hvis plukpladserne bruger volumenmålinger.

            Hvis denne indstilling er valgt, skal du angive feltet **Overløbsprocent** til den procentdel, hvor der skal være mere tilgængeligt genopfyldningsarbejde.

        - *Antal* – Vælg denne indstilling for at bruge en bestemt antalsværdi. Hvis du vælger denne indstilling , deaktiveres feltet **Overløbsprocent**, og det aktiverer felterne **Overløbsantal** og **Overløbsenhed**.

            Brug denne indstilling, når du ikke bruger volumenmålinger til de pladser, der genopfyldes, eller når du har ensartede mængder, der skal tilføres mere lager på pladsen.

           Hvis denne indstilling er valgt, skal du angive felterne **Overløbsantal** og **Overløbsenhed** til det antal og den enhed, hvor mere genopfyldningsarbejde skal være tilgængeligt.

    - **Overløb i antal:** *0,65*

        Dette felt definerer det antal, hvormed pladsen overløber.

        Arbejde vil være tilgængeligt, når summen af lagerbeholdningen på pladsen og arbejdsantallet er under denne værdi. En eventuel genopfyldning over denne værdi blokeres og skal ophæves manuelt.

        Grænser for lokalitetslagring tages i betragtning ved beregning af arbejdsantallet.

    - **Overløbsenhed:** *PL*

        I dette felt defineres den enhed, der er knyttet til overløbsantallet.

        I dette tilfælde gøres der mere genopfyldningsarbejde tilgængeligt, når lokationen kommer ned på 0,65 palle (PL).

    - **Overløb i procent**

        Dette felt definerer den procent, hvormed pladsen overløber.

        Arbejde vil være tilgængeligt, når summen af lagerbeholdningen på pladsen og arbejdsantallet er under denne procent. En eventuel arbejdsmængde i procent for arbejdet ved genopfyldning over denne værdi blokeres og skal ophæves manuelt.

        Grænser for lokalitetslagring tages i betragtning ved beregning af arbejdsantallet i procent. Hvis der ikke er defineret grænser for lokationslagring, beregnes procenten af arbejdsmængden efter volumen, hvis der er defineret volumenbegrænsninger på lokationsprofilen.

> [!IMPORTANT]
> Hvis du bruger demodataene til den juridiske enhed **USMF** og tidligere har aktiveret funktionen *Placering af lokations-id*, skal du deaktivere indstillingen **Aktivér placering af id** for lokationsprofilen **MASSE-06** for at fuldføre de mobile trin i eksempelscenariet.

### <a name="wave-step-code"></a>Kode for bølgetrin

> [!NOTE]
> Hvis du vil oprette en bølgetrinkode som beskrevet her, skal du muligvis først bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionen med navnet *Bølgetrinkode for hele organisationen*.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinkoder**.
1. Vælg **Ny**, og angiv derefter følgende værdier:

    - **Kode for bølgetrin:** *Genopfyld*
    - **Bølgetrinsbeskrivelse:** *Genopfyldning*
    - **Bølgetrinstype:** *Genopfyldning*

1. Vælg **Gem**.

### <a name="replenishment-template"></a>Genopfyldningsskabelon

Genopfyldningsskabeloner er et sæt regler, der styrer, hvornår og hvordan en lokation skal genopfyldes.

1. Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**.
1. Vælg **Rediger** i handlingsruden.
1. Vælg den linje, hvor feltet **Genopfyldningsskabelon** er angivet til **Genopfyldning af behov** i sektionen *Oversigt*.
1. Angiv følgende værdier:

    - **Kode for bølgetrin:** *Genopfyld*
    - **Tillad bølgeefterspørgsel at bruge ikke-reserverede antal:** *Ja*

1. Vælg **Gem**.

### <a name="wave-template"></a>Bølgeskabelon

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. I venstre rude skal du angive feltet **Bølgeskabelontype** til *Forsendelse*.
1. Vælg skabelonen **61 Forsendelse** på listen.
1. Vælg **Rediger** i handlingsruden.
1. Brug oversigtspanelet **Generelt** til at angive indstillingen **Automatiser frigivelse af genopfyldningsarbejde** til *Ja*.

    Angiv denne indstilling til *Ja* for at oprette behovsbaseret genopfyldningsarbejde og frigive det automatisk. Du skal føje genbestillingsbølgemetoden til bølgeskabelonen og oprette en genbestillingsskabelon af typen **Bølgebehov**. Konfigurer en genopfyldningsskabelon på siden **Genopfyldningsskabeloner**. Hvis du vil konfigurere en genopfyldningsskabelon, skal du føje genopfyldningsmetoden til bølgeskabelonen.

1. Find følgende linje i kolonnen **Valgte metoder** i oversigtspanelet **Metoder**:

    - **Metodenavn:** *Genopfyld*
    - **Navn:** *Genopfyldning*

1. Indstil feltet **Kode for bølgetrin** for denne linje til *Genopfyld*.
1. Vælg **Gem**.

## <a name="example-scenario"></a>Eksempelscenario

Når du har gjort alle de tidligere nævnte eksempeldata tilgængelige og konfigureret dem, kan du arbejde gennem dette scenario for at afprøve funktionen *Genopfyldning over lokationskapacitet*. De værdier, der vises i dette scenarie, forudsætter, at du arbejder med standarddemodataene, at du har valgt **USMF** som juridisk enhed, og at du har forberedt de eksempelposter, der er beskrevet tidligere i dette emne. Dette scenario fungerer også som et eksempel, der viser, hvordan funktionen kan bruges i en produktionsopsætning.

### <a name="create-replenishment-work"></a>Opret genopfyldningsarbejde

#### <a name="create-sales-order-1"></a>Opret salgsordre 1

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. I handlingsruden skal du vælge **Ny** for at åbne dialogboksen Opret ny salgsordre.
1. I dialogboksen skal du angive følgende værdier:

    - **Debitorkonto:** *US-007*
    - **Lagersted:** *61*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Den indeholder en ny tom linje i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *T0100*
    - **Antal:** *40*

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
1. På siden **Reservation** skal du vælge **Reservér parti**.
1. Luk siden.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Du modtager orienterende meddelelser, der viser bølgen og forsendelses-id'et, der blev oprettet. Der oprettes også en genopfyldningsbølge.

    Du får også vist en advarselsmeddelelse om, at "Arbejde-id XXXX ikke kan ophæves, fordi det ikke har fuldført genopfyldningsarbejde".

#### <a name="create-sales-order-2"></a>Opret salgsordre 2

1. I handlingsruden på siden **Alle salgsordrer** skal du vælge **Ny** for at åbne dialogboksen Opret ny salgsordre.
1. I dialogboksen skal du angive følgende værdi:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *61*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Den indeholder en ny tom linje i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *T0100*
    - **Antal:** *60*

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
1. På siden **Reservation** skal du vælge **Reservér parti**.
1. Luk siden.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Du modtager orienterende meddelelser, der viser bølgen og forsendelses-id'et, der blev oprettet. Der oprettes også en genopfyldningsbølge.

    Du får også vist en advarselsmeddelelse om, at "Arbejde-id XXXX ikke kan ophæves, fordi det ikke har fuldført genopfyldningsarbejde".

#### <a name="create-sales-order-3"></a>Opret salgsordre 3

1. I handlingsruden på siden **Alle salgsordrer** skal du vælge **Ny** for at åbne dialogboksen Opret ny salgsordre.
1. I dialogboksen skal du angive følgende værdier:

    - **Debitorkonto:** *US-004*
    - **Lagersted:** *61*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Den indeholder en ny tom linje i oversigtspanelet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *T0100*
    - **Antal:** *30*

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
1. På siden **Reservation** skal du vælge **Reservér parti**.
1. Luk siden.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Du modtager orienterende meddelelser, der viser bølgen og forsendelses-id'et, der blev oprettet. Der oprettes også en genopfyldningsbølge.

    Du får også vist en advarselsmeddelelse om, at "Arbejde-id XXXX ikke kan ophæves, fordi det ikke har fuldført genopfyldningsarbejde".

#### <a name="view-work-details"></a>Se arbejdsdetaljer

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Filtrer **Lagersted**-kolonnen for lagerstedet **61** i sektionen *Oversigt*.
1. Du bør se, at der er oprettet syv arbejds-id'er for de tre behovssalgsordrer.

    - Tre af de syv arbejds-id'er har en **Arbejdsordretype**-værdi for *Genopfyldning*, og fire har en **Arbejdsordretype**-værdi for *Salgsordrer*.
    - Alle tre arbejds-id'er, der har **Arbejdsordretype**-værdien *Genopfyldning*, har samme *Pluk* og *Læg på lager*-placeringer i afsnittet **Linjer**:

        - **Pluk:** *02A01R5S1B*
        - **Læg på lager:** *06A01R2S1B*

    - Der er oprettet to arbejds-id'er for salgsordre 1.

1. Notér arbejds-id'erne for salgsordrene.

Afhængigt af de disponible antal kan de arbejdsantal, der oprettes, variere en smule. De overordnede arbejdsoverskrifter, der oprettes, skal dog svare til dette scenarieeksempel.

#### <a name="on-hand-inventory-license-plate-id"></a>Id for disponibel lagerbeholdning

Senere i dette scenario skal du bruge appen Lagersted (eller en emulator), hvor du skal identificere id'et for at fuldføre pluk- og genopfyldningsscenarierne.

Du kan finde de id'er, du skal bruge, senere ved at følge disse trin.

1. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.
1. Vælg knappen **Vis filtre** for at åbne filterruden.
1. Angiv følgende filtreringskriterier for at få id'erne til scenariet. Brug filteret *begynder med*.

    - **Varenummer:** *T0100*
    - **Lagersted:** *61*

1. Vælg **Anvend**.
1. Vælg **Dimensioner** i handlingsruden.
1. Vælg alle værdierne i sektionen **Lagringsdimensioner** i dialogboksen **Dimensionsvisning**.
1. I afsnittet **Transaktioner** skal du vælge **Varenummer** og **Antal \<\> 0**.
1. Når du er færdig, skal du vælge **OK** for at lukke dialogboksen.
1. **Beholdning**-gitteret viser id-numrene for varen *T0100* på hver lokation. Notér dig det id, der findes på hver lokation, da du skal bruge disse oplysninger senere.
1. Luk siden.

### <a name="process-steps"></a>Procestrin

Du skal udføre genopfyldning af lagerstedet for de første to arbejds-id'er. Arbejdet på det tredje genopfyldningsarbejde blokeres, indtil lagerniveauet på plukpladsen falder under grænsen.

#### <a name="replenishment"></a>Opfyldning

1. Log på lagerstedsappen som en bruger på lagersted *61*. (Angiv *61* som bruger-id og *1* som adgangskode).
1. Gå til **Lager \> Genopfyldning**.

    Du bliver bedt om at fuldføre det første genopfyldningsarbejde. Varenummeret, antallet og pluklokationen vises.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.
1. Vælg knappen **OK** (markeringssymbol).

    Systemet opretter et id-nummer til målet for det nye id til den plukkede vare.

1. Vælg **OK** for at bekræfte værdien.

    Der vises et læg på lager-arbejde, som beder brugeren om at anbringe en mål-id'et på genopfyldningspladsen. Pladsen *Læg på lager* skal være **06A01R2S1B**.

1. Bekræft læg på lager-oplysningerne, og vælg **OK**.

    Du får vist meddelelsen "Arbejde fuldført", og detaljerne i den næste plukopgave til genopfyldning vises: varenummeret, antallet og lokationen, der skal plukkes fra. Plukpladsen vil være den samme som den første genopfyldningsplads. Derfor vil id'et være det samme nummer, der blev brugt til den første arbejdsopgave for genopfyldning.

1. Gentag de foregående trin for at fuldføre genopfyldningsarbejdet for den anden arbejdsopgave. Antallet og mål-id'et licens vil være forskellig fra antallet og mål-id'et for den første arbejdsopgave.

Når det andet genopfyldningsarbejde er fuldført, vises meddelelsen "Arbejde fuldført". Din mobilenhed informerer dig også om, at der ikke er noget arbejde tilgængeligt, også selvom noget genopfyldningsarbejde resterer. Dette problem opstår, fordi genopfyldningsarbejdet har tilgængelighedsstatussen *På hold* og derfor er markeret som **Blokeret**.

*På hold*-status blev udløst, fordi lokationsprofilen for den plukplads, som arbejdet tildeles, har en **Overløbsantals**-værdi på *0,65 PL*. De to tidligere opgaver for genopfyldningsarbejde har udfyldt lokationen næsten til dens overløbsgrænse for vare *T0100*. (Enhedsomregningen for varen er *1 PL = 100 hver*). Derfor vil det resterende genopfyldningsarbejde medføre, at lokationen overskrider dens overløbsgrænse.

Indtil der er plukket tilstrækkeligt med lagervarer fra lokationen, så de kommer under grænsen for arbejdsfrigivelsen i menupunktet for mobilenheden, forbliver dette genopfyldningsarbejde blokeret.

#### <a name="sales-order-pick"></a>Salgsordrepluk

Før den resterende genopfyldningsarbejdsopgave kan fuldføres, skal plukpladsen tømmes for lager til et niveau, hvor blokering af det resterende genopfyldningsarbejde kan ophæves. Det vil sige, at summen af antallet af disponible lagerbeholdninger på lokationen og genopfyldningsantallet ikke overstiger værdien af **Overløbsantal**. Når denne sum er mindre end overløbsantallet, fjernes spærringen af det resterende genopfyldningsarbejde.

1. Log på lagerstedsappen som en bruger på lagersted *61*. (Angiv *61* som bruger-id og *1* som adgangskode).
1. Gå til **Udgående \> Salgsplukning**.
1. Angiv første arbejds-id for salgsordre 1.

    Se arbejds-id'erne for de salgsordrer, du har noteret tidligere, på siden **Arbejdsdetaljer**. Det arbejds-id, du angiver her, genererer plukarbejde for et antal på 10 hver fra to forskellige lokationer.

1. Vælg **OK**.

    Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra for den første lokation.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.
1. Vælg knappen **OK** (markeringssymbol).

    Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra for den næste lokation.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.
1. Vælg knappen **OK** (markeringssymbol).

    **Salgsordrer: Læg på lager**-siden giver dig besked på at lægge begge fuldførte plukarbejder til den udgående lokation for midlertidig lagring.

1. Vælg **OK**.

    Du modtager en meddelelse om arbejde fuldført.

1. Angiv andet arbejds-id for salgsordre 1.

    Der er kun én plukopgave for dette arbejds-id.

1. Vælg **OK**.

    Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.

    Det id, du angiver, vil være et af de systemgenererede id'er fra arbejdsopgaverne for genopfyldning. Hvis du vil være sikker på, at du indlæser det korrekte id, skal du kontrollere lageret på siden **Beholdningsliste** for varen, lokationen og antallet.

1. Vælg knappen **OK** (markeringssymbol).
1. Bekræft instruktionerne til læg på lager-opgaven på den udgående midlertidige lagring.
1. Vælg **OK**.

    Du modtager en meddelelse om arbejde fuldført.

Salgsordre 2 er spærret for pluk, fordi genopfyldningsopgaven, som den er knyttet til, ikke er fuldført. Der er i øjeblikket stadig et antal på 30 hver på plukpladsen, og genopfyldningsantallet for salgsordre 2 er 60 hver. Summen af disponibel lagerbeholdning og genopfyldningslageret (90 hver) overskrider overløbsantallet på 0,65 PL (eller 65 hver). Salgsordre 3 skal plukkes, før genopfyldningsarbejdet kan fuldføres.

1. Angiv arbejds-id for salgsordre 3.

    Der er kun én plukopgave for dette arbejds-id.

1. Vælg **OK**.

    Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.

    Det id, du angiver, vil være et af de systemgenererede id'er fra arbejdsopgaverne for genopfyldning. Hvis du vil være sikker på, at du indlæser det korrekte id, skal du kontrollere lageret på siden **Beholdningsliste** for varen, lokationen og antallet.

1. Vælg knappen **OK** (markeringssymbol).
1. Bekræft instruktionerne til læg på lager-opgaven på den udgående midlertidige lagring.
1. Vælg **OK**.

    Du modtager en meddelelse om arbejde fuldført.

Så snart summen af det disponible antal på plukpladsen og opfyldningsantallet er under grænsen, vil du kunne behandle det resterende genopfyldningsarbejde.

Vend tilbage til siden **Arbejdsdetaljer**, og bemærk, at tilgængeligheden af genopfyldningsarbejde for det sidste stykke genopfyldning (for salgsordre 2) er *Åben*, fordi der nu er tilstrækkelig plads på lokationen til at acceptere genopfyldningen.

Du kan nu behandle dette genopfyldningsarbejde via mobilenheden.

1. Gå til **Lager \> Genopfyldning**.

    Du bliver bedt om at fuldføre det resterende genopfyldningsarbejde. Varenummeret, antallet og pluklokationen vises.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.
1. Vælg knappen **OK** (markeringssymbol).

    Systemet opretter et id-nummer til målet for det nye id til den plukkede vare.

1. Vælg **OK** for at bekræfte værdien.

    Der vises et læg på lager-arbejde, som beder brugeren om at anbringe en mål-id'et på genopfyldningspladsen. Pladsen *Læg på lager* skal være **06A01R2S1B**.

1. Bekræft læg på lager-oplysningerne, og vælg **OK**.

    Du modtager meddelelsen "Arbejde fuldført" og "Der er intet tilgængeligt arbejde".

Du kan nu plukke salgsordre 2. Spærringen blev ophævet, da genopfyldningsarbejdet, der er knyttet til salgsordren, blev fuldført.

1. Angiv arbejds-id for salgsordre 2.

    Der er kun én plukopgave for dette arbejds-id.

1. Vælg **OK**.

    Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra.

1. I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.

    Det id, du angiver, vil være et af de systemgenererede id'er fra arbejdsopgaven for genopfyldning. Hvis du vil være sikker på, at du indlæser det korrekte id, skal du kontrollere lageret på siden **Beholdningsliste** for varen, lokationen og antallet.

1. Vælg knappen **OK** (markeringssymbol).
1. Bekræft instruktionerne til læg på lager-opgaven på den udgående midlertidige lagring.
1. Vælg **OK**.

    Du modtager en meddelelse om arbejde fuldført.

## <a name="notes-and-tips"></a>Noter og tip

- Denne funktionalitet fungerer sammen med alle former for genopfyldning: bølgebehov, minimum/maksimum, lastbaseret behov og allokering.
- Du kan manuelt tilsidesætte genopfyldningsarbejdets tilgængelighed for hver arbejdsoverskrift fra siden **Arbejdsdetaljer**, hvis du ønsker det.
- Når systemet angiver genopfyldningsarbejdets tilgængelighed, tages der højde for ethvert lager, der allerede findes på lokationen, før et arbejde fuldføres.
- Hvert stykke af salgsordrearbejdet er knyttet til et bestemt genopfyldningsarbejde. Der findes ingen tilsvarende funktionalitet for tilgængeligt salgsarbejde.
