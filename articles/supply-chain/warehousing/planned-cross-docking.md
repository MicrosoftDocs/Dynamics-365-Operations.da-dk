---
title: Planlagt direkte levering
description: Denne artikel beskriver et avanceret planlagt cross-docking, hvor det lagerantal, der kræves til en ordre, anvises direkte ved modtagelse eller oprettelse til den korrekte dock i forsendelsesområde eller det midlertidige område. Alt restlager fra den indgående kilde sendes til den korrekte lagerplacering via den almindelige læg på lager-proces.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 28ebf1b4fb966fd6801e75e7b3a6c8741114938d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863673"
---
# <a name="planned-cross-docking"></a>Planlagt cross-docking

[!include [banner](../includes/banner.md)]

Denne artikel beskriver avanceret planlagt cross-docking. Cross-docking er en lagerproces, hvor det lagerantal, der kræves til en ordre, anvises direkte ved modtagelse eller oprettelse til den korrekte dock i forsendelsesområde eller det midlertidige område. Alt restlager fra den indgående kilde sendes til den korrekte lagerplacering via den almindelige læg på lager-proces.

Cross-docking giver arbejdere mulighed for at overspringe indgående læg på lager og udgående plukning af lager, der allerede er markeret for en udgående ordre. Derfor minimeres det antal gange, som lageret berøres med, hvor det er muligt. Da der desuden sker mindre interaktion med systemet, forhøjes tids- og lagerpladsbesparelserne i forhold til lagerets produktion.

Før cross-docking kan køres, skal du konfigurere en ny cross-docking/skabelon, hvor forsyningskilden og andre sæt af krav til cross-docking er angivet. Efterhånden som den udgående ordre oprettes, skal linjen markeres i forhold til en indgående ordre, der indeholder den samme vare. Du kan vælge feltet med vejledningskode i skabelonen for cross-docking, på samme måde som du konfigurerer genopfyldnings- og indkøbsordrer.

På tidspunktet for modtagelse af indgående ordrer identificerer opsætningen af cross-docking automatisk behovet for cross-docking og opretter bevægelsesarbejdet for den ønskede mængde på basis af opsætningen af lokationsvejledningen.

> [!NOTE]
> Registreringen af lagertransaktioner annulleres *ikke*, når cross-docking annulleres, også selvom indstillingen for denne funktion er aktiveret i parametrene for lokationsstyring.

## <a name="turn-on-the-planned-cross-docking-features"></a>Slå funktionerne til planlagt cross-docking til

Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i Denne artikel, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funktioner i denne rækkefølge:

1. *Planlagt direkte levering*
1. *Skabeloner til cross-docking med lokationsvejledninger*
    > [!NOTE]
    > Denne funktion gør det muligt at angive feltet **Vejledningskode** i skabelonen til cross-docking, ligesom du konfigurerer genopfyldningsskabeloner. Hvis du aktiverer denne funktion, kan du ikke føje en vejledningskode til linjerne i arbejdsskabelonen til cross-docking for den endelige *Læg*-linje. Derved sikres, at den endelige læg-placering kan bestemmes under oprettelsen af arbejdet, før du overvejer arbejdsskabeloner.

## <a name="setup"></a>Konfiguration

### <a name="regenerate-load-posting-methods"></a>Genoprette lastbogføringsmetoder

Planlagt cross-docking implementeres som en lastbogføringsmetode. Når du har aktiveret funktionen, skal du generere metoderne igen.

1. Gå til **Lagerstedsstyring \> Opsætning \> Lastbogføringsmetoder**.
1. Vælg **Genopret metoder** i handlingsruden.

    Når genoprettelsen er fuldført, bør du kunne se en metode, der har værdien **planCrossDocking** for *Metodenavn*.

1. Luk siden.

### <a name="create-a-cross-docking-template"></a>Oprette en skabelon for cross-docking

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Skabeloner for cross-docking**.
1. Vælg **Ny** i handlingsruden for at oprette en skabelon.
1. Angiv følgende værdier i overskriften:

    - **Sekvens:** *1*

        Dette felt definerer den rækkefølge, som skabelonerne evalueres i.

    - **Id for skabelon for cross-docking:** *51*
    - **Beskrivelse:** *Lagersted 51*
    - **politik for behovsfrigivelse:** *Før leveringskvittering*
    - **Lagersted:** *51*

1. Opsætningen i oversigtspanelet **Planlægning** bestemmer, hvordan skabelonen fungerer. Angiv følgende værdier:

    - **Efterspørgselskrav:** *Ingen*

        Dette felt definerer kravene til lagerbeholdningen. Hvis behovet skal være knyttet til leveringen før frigivelsen, skal du vælge *Markering*. Hvis behovet skal ordrereserveres i forhold til leveringen, skal du vælge *Ordrereservation*.

    - **Finde type:** *Forsendelseslokationer*

        I dette felt defineres, om cross-docking-arbejde skal bruge de midlertidige lokationer/læsselokationer fra forsendelsen, eller om de skal bruge lokationsvejledninger til at finde dens egne midlertidige lokationer/læsselokationer.

    - **Arbejdsskabelon:** Lad feltet stå tomt.

        Dette felt definerer den arbejdsskabelon, der skal bruges, når der oprettes cross-docking-arbejde.

    - **Valider ved modtagelse af forsyning:** *Nej*

        Denne indstilling angiver, om forsyningen skal valideres igen under modtagelsen. Hvis denne indstilling er angivet til *Ja*, kontrolleres både det maksimale tidsinterval og udløbsintervallet i dage.

    - **Vejledningskode:** Lad feltet være tomt

        Denne indstilling aktiveres med funktionen *Skabeloner til cross-docking med lokationsvejledninger*. Systemet bruger lokationsvejledninger som en hjælp til at bestemme, hvilken lokation cross-docking-lager skal flyttes til. Du kan definere den ved at tildele en vejledningskode til hver relevante cross-docking-skabelon. Hvis der er angivet en vejledningskode, når arbejde genereres, søger systemet i lokationsvejledninger ved hjælp af vejledningskoden. På denne måde kan du begrænse lokationsvejledninger, der bruges til en bestemt cross-docking-skabelon.

    - **Valider tidsvindue:** *Ja*

        Denne indstilling angiver, om det maksimale tidsvindue skal evalueres, når der er valgt en forsyningskilde. Hvis denne indstilling er angivet til *Ja*, bliver de felter, der er relateret til de maksimale og minimale tidsvinduer, tilgængelige.

    - **Maksimalt tidsvindue:** *5*

        Dette felt definerer den maksimale periode, der tillades mellem forsyningstilgang og efterspørgselsafgang.

    - **Enhed for maksimalt tidsvindue:** *Dage*
    - **Mindste tidsvindue:** *0*

        Dette felt definerer den mindste periode, der tillades mellem forsyningstilgang og efterspørgselsafgang.

    - **Enhed for minimalt tidsvindue:** *Dage*
    - **Udløbsinterval i dage:** *0*

        *FEFO-kriterier (First expiry first out):* Dette felt definerer det maksimale antal dage mellem udløbsdatoen for batchen med den første udløbsdato, der aktuelt findes på lagerstedet, og den batch, der modtages.

1. I oversigtspanelet **Forsyningskilder** angiver du de typer forsyning, der er gældende for denne skabelon. Vælg **Ny**, og vælg derefter følgende værdier:

    - **Løbenummer:** *1*
    - **Forsyningskilde:** *Indkøbsordre*

> [!NOTE]
> Du kan konfigurere en forespørgsel til at styre, hvornår en bestemt cross-docking-skabelon bruges. Forespørgslen på cross-docking-skabeloner har kun tabellen *InventTable* (varer) og den indre join-tabel *WHSInventTable* (WHS-varer). Hvis du vil føje andre tabeller til forespørgslen, kan du sammenkæde dem ved kun at bruge *eksisterende joinforbindelser* eller *ikke-eksisterende joinforbindelser*. Når du filtrerer på de joinforbundne tabeller, hentes der en post fra hovedtabellen for hver tilsvarende post i den joinforbundne tabel. Hvis join-typen er *eksisterende joinforbindelse*, afsluttes søgningen, når det første match er fundet. Hvis du f.eks. joinforbinder tabellen med salgsordrelinjer til varetabellen, valideres og returneres varer, hvor mindst én salgsordrelinje har den definerede betingelse. Dataene hentes reelt fra den overordnede tabel (varer) og ikke fra den underordnede tabel (salgsordrelinjen). Derfor kan der ikke som standard foretages filtrering efter kildedokumenter som f.eks. salgsordrelinjer eller kunder.

### <a name="create-a-work-class"></a>Oprette en arbejdsklasse

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.
1. Vælg **Ny** i handlingsruden for at oprette en arbejdsklasse.
1. Angiv følgende værdier:

    - **Arbejdsklasse-id:** *CrossDock*
    - **Beskrivelse:** *Cross Dock*
    - **Arbejdsordretype:** *Cross-docking*

### <a name="create-a-work-template"></a>Oprette en arbejdsskabelon

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Angiv feltet **Arbejdsordretype** til *Cross-docking*.
1. Gå til handlingsruden, og vælg **Ny** for at føje en linje til fanen **Oversigt**.
1. Angiv følgende værdier på den nye linje:

    - **Løbenummer:** *1*
    - **Arbejdsskabelon:** *51 Cross Dock*
    - **Arbejdsskabelonbeskrivelse:** *51 Cross Dock*

1. Vælg **Gem** for at gøre oversigtspanelet **Arbejdsskabelondetaljer** tilgængeligt.
1. Gå til oversigtspanelet **Arbejdsskabelondetaljer**, og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Arbejdstype:** *Pluk*
    - **Arbejdsklasse-id:** *CrossDock*

1. Vælg **Ny** for at tilføje en anden linje, og angiv følgende værdier på den:

    - **Arbejdstype:** *Læg på lager*
    - **Arbejdsklasse-id:** *CrossDock*

1. Vælg **Gem**, og kontroller, at afkrydsningsfeltet **Gyldig** er markeret for skabelonen *51 Cross Dock*.
1. Valgfrit: Vælg **Rediger forespørgsel**, hvis du vil angive kriterier, der styrer, hvornår og hvor arbejdsskabelonen anvendes.

    Du kan konfigurere en forespørgsel til at styre, hvornår en bestemt arbejdsskabelon bruges. Du kan f.eks. angive, at en skabelon kun kan bruges til arbejde et bestemt sted. Hvis arbejdsskabelonen til cross-docking skal anvendes på en bestemt lokation, skal du filtrere i feltet **Startlokation** og ikke i feltet **Lokation**, da arbejdsoprettelsen for de indgående processer (indkøb, cross-docking og genopfyldning) starter fra læg på-linjen. Når arbejdet oprettes, angiver lokationsvejledningen feltet **Lokation** til læg på lager-lokationen. Pluklokationen gemmes dog i feltet **Startlokation**.

> [!NOTE]
> Arbejdsklasse-id'erne for arbejdstyperne *Pluk* og *Læg på lager* skal være ens.

### <a name="create-location-directives"></a>Oprette lokalitetsvejledninger

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I venstre rude skal du angive feltet **Arbejdsordretype** til *Cross-docking*.
1. I handlingsruden skal du vælge **Ny** og derefter vælge følgende værdier:

    - **Løbenummer:** *1*
    - **Navn:** *51 Cross Dock – læg på lager*
    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *5*
    - **Lagersted:** *51*

1. Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.
1. Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Fra antal:** *1*
    - **Til antal:** *1000000*

1. Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.
1. Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Navn:** *Båsedør*
    - **Anvendelse af fast lokation:** *Faste og ikke-faste lokationer*

1. Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig på værktøjslinjen **Handlinger i lokationsvejledning**.
1. Vælg **Rediger forespørgsel** for at åbne forespørgselseditoren.
1. Kontroller, at følgende to linjer er konfigureret under fanen **Område**:

    - Linje 1:

        - **Tabel:** *Lokationer*
        - **Afledt tabel:** *Lokationer*
        - **Felt:** *Lagersted*
        - **Afgrænsning:** *51*

    - Linje 2:

        - **Tabel:** *Lokationer*
        - **Afledt tabel:** *Lokationer*
        - **Felt:** *Lokation*
        - **Afgrænsning:** *Båsedør*

1. Vælg **OK** for at lukke forespørgselseditoren.

### <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. På listen over menupunkter i ruden til venstre skal du vælge **Læg indkøb på lager**.
1. Vælg **Rediger**.
1. Gå til oversigtspanelet **Arbejdsklasser**, og vælg **Ny** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Arbejdsklasse-id:** *CrossDock*
    - **Arbejdsordretype:** *Cross-docking*

1. Vælg **Gem**.

## <a name="scenario"></a>Scenario

### <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

Udfør følgende trin for at oprette en indkøbsordre som en kilde til levering.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:

    - **Kreditorkonto:** *104*
    - **Lagersted:** *51*

1. Vælg **OK**, og noter ordrenummeret.
1. Der føjes en ny linje til gitteret i oversigtspanelet **Indkøbsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *A0001*
    - **Antal:** *5*

### <a name="create-a-sales-order"></a>Oprette en salgsordre

Udfør følgende trin for at oprette en salgsordre som en kilde til efterspørgsel.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-002*
    - **Lagersted:** *51*

1. Vælg **OK**.
1. Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *A0001*
    - **Antal:** *3*

### <a name="create-planned-cross-docking"></a>Oprette planlagt cross-docking

Udfør følgende trin for at oprette planlagt cross-docking fra salgsordren.

1. På siden **Salgsordredetaljer** for den salgsordre, du netop har oprettet, skal du i handlingsruden vælge **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Frigiv til lagersted**.

    Handlingen Frigiv til lagersted opretter en forsendelses- og lastlinje for salgsordrelinjen og forsøger at fordele lagerbeholdningen.
    
    Du får en orienterende meddelelse. Du får også vist følgende advarselsmeddelelse: "Der blev ikke oprettet noget arbejde for bølge XXXX. Du kan finde flere oplysninger i logfilen over historik for oprettelse af arbejde." Denne funktionsmåde forventes, fordi der ikke er nogen lagerbeholdning på lagerstedet.

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Forsendelsesoplysninger** i menuen **Lagersted**.

    Siden **Forsendelsesoplysninger** vises og viser den forsendelse, der er oprettet for salgsorden.

1. I oversigtspanelet **Lastlinjer** skal du bemærke, at feltet **Planlagt antal til cross-docking** er angivet til *3*. Da der ikke var en tilgængelig lagerbeholdning på lagerstedet, men der vil blive oprettet en gyldig forsyningskilde inden for det tidsvindue, der er defineret i skabelonen til cross-docking, blev antallet for cross-docking angivet.
1. I oversigtspanelet **Lastlinjer** skal du vælge **Planlagt cross-docking** for at få vist detaljerne om den cross-docking, der er oprettet.

## <a name="process-the-cross-docking"></a>Behandle cross-docking

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Købsordre, der modtages på Warehouse Mobile App

Systemet vil modtage antallet på 5 fra indkøbsordren til modtagelseslokationen og oprette to x arbejde.

Det første arbejds-id, der oprettes, har værdien **Cross-docking** for *Arbejdsordretype* og er knyttet til salgsordren. Det har antallet 3 og sendes til den endelige afsendelseslokation, så det kan leveres med det samme.

Det andet arbejds-id, der oprettes, har værdien **Indkøbsordrer** for *Arbejdsordretype* og er knyttet til indkøbsordren. Den har det resterende antal på 2, der ikke blev cross-docked, og som sendes til opbevaring med læg på lager.

1. Log på mobilenheden som en bruger på lagerstedet *51*.
1. Gå til **indgående \> Købsmodtagelse**.
1. Angiv dit indkøbsordrenummer i feltet **IO-num**.
1. Angiv **5** i feltet *Antal*.
1. Vælg **OK**.
1. På næste side skal du angive feltet **Vare** til *A0001*.
1. Vælg **OK**.
1. På næste side skal du bekræfte værdierne for **IO-num**, **Vare** og **Antal** ved at vælge **OK**.

    Du modtager en meddelelse om arbejde fuldført.

1. Vælg **Annuller** for at afslutte.

### <a name="put-away-to-cross-docking-and-bulk"></a>Læg på lager til cross-docking og masse

I øjeblikket har begge arbejds-id'er samme målnummerplade. Hvis du vil udføre de næste trin, skal du hente arbejds-id'et og målnummerplade-id'et. Du kan få disse oplysninger fra arbejdsdetaljerne om indkøbsordrelinjen og salgsordrelinjen. Du kan også gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer** og filtrere efter arbejde, hvor værdien **Lagersted** er *51*.

1. På mobilenheden skal du gå til **Indgående \> Læg køb på lager** og angive målnummerpladen fra arbejdet.
1. I feltet **Id** skal du angive målnummerplade-id'et fra arbejdsdetaljerne.

    Siden til plukning til cross-docking viser pluklokationen (*RECV*), målnummerpladen (*nummerplade*), varen (*A0001*) og antallet (*3*).

1. Vælg **OK**.
1. I feltet **Mål-NP** skal du angive en målnummerplade for nummerplade-id'et, der skal lægges på lager (cross-docked) på forsendelseslokationen. Du kan vælge et hvilket som helst nummerplade-id efter eget valg.
1. Vælg **OK**.
1. På den næste side skal du i feltet **Id** angive målnummerplade-id'et.
1. Vælg **OK**.
1. Bekræft arbejdet til plukning af det resterende antal på 2, og vælg derefter **OK**.
1. På næste side skal du vælge **Udfør** for at afslutte plukprocessen og begynde læg på lager-processen.

    Mobilappen indeholder lokationen og nummerpladen, hvor varen skal lægges på lager.

1. Bekræft **Læg på lager** ved masseopbevaring ved at vælge **OK**.
1. På den næste side skal du bekræfte **Læg på lager** for cross-docking ved at vælge **OK**.

    Du modtager en meddelelse om arbejde fuldført.

1. Vælg **Annuller** for at afslutte.

I følgende illustration vises, hvordan det færdige arbejde til cross-docking kan blive vist i Microsoft Dynamics 365 Supply Chain Management.

![Arbejde med cross-docking udført.](media/PlannedCrossDockingWork.png "Arbejde med cross-docking udført")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
