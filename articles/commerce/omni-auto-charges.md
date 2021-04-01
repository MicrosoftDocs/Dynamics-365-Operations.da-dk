---
title: Avancerede automatiske gebyrer for omni-kanal
description: I dette emne beskrives funktioner til styring af ekstra ordregebyrer for Commerce-kanalordrer ved hjælp af funktioner til avancerede automatiske gebyrer.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: b7a309cc9e8901aa50e1d4ea3be6ee37d9fc5450
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244929"
---
# <a name="omni-channel-advanced-auto-charges"></a>Avancerede automatiske gebyrer for omni-kanal

[!include [banner](includes/banner.md)]

Dette emne indeholder oplysninger om konfiguration og implementering af funktionen til avancerede automatiske gebyrfunktion, der er tilgængelig i Dynamics 365 for Retail version 10.0.

Når de avancerede automatiske gebyrfunktioner er aktiveret, kan ordrer, der oprettes i en understøttet Commerce-kanal (POS, callcenter og online), udnytte de konfigurationer for [automatiske gebyrer](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services), der er defineret i ERP-programmet for gebyrer på både for ordrehoved- og -linjeniveau.

I versioner før Retail version 10.0 er konfigurationer af [automatiske gebyrer](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) kun tilgængelige for ordrer, der er oprettet i e-handels- og callcenter-kanaler. I 10.0 og senere versioner kan POS-oprettede ordrer udnytte de automatiske gebyrkonfigurationer. På denne måde kan flere gebyrer systematisk føjes til salgstransaktioner.

I versioner før version 10.0 bliver POS-brugere bedt om at angive et forsendelsesgebyr manuelt under oprettelse af en "send alle" eller "send valgte" POS transaktion. Når gebyrfunktionerne i programmet bruges i forhold til, hvordan gebyrerne skrives til ordren, foretages der ingen systematisk beregning – beregningen til bestemmelse af værdien af gebyrerne er baseret på input fra brugeren. Gebyrerne kan kun tilføjes som en enkelt "forsendelse"-relaterede gebyrkode og kan kun dårligt redigeres eller ændres i POS, når de først er oprettet.

Der bruges stadig manuelle prompts ved tilføjelse af forsendelsesgebyrer i version 10.0 og nyere. Hvis en organisation ikke aktiverer parameteren **Avancerede automatiske gebyrer**, forbliver POS-prompts om manuel angivelse af gebyrer uændret.

Med den avancerede automatiske gebyrfunktion kan POS-brugere få systematiske beregninger for ethvert defineret gebyr baseret på tabeller til opsætning af automatiske gebyrer. Desuden får brugere mulighed for at tilføje eller redigere et ubegrænset antal ekstra gebyrer og gebyrer for enhver POS-salgstransaktion på hoved- eller linjeniveau (for en cash and carry- eller kundeordre).

## <a name="enabling-advanced-auto-charges"></a>Aktivering af avancerede automatiske gebyrer

På siden **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** skal du gå til fanen **Kundeordrer**. I oversigtspanelet **Gebyrer** skal du indstille **Brug avancerede automatiske gebyrer** til **Ja**.

![Parametre for avancerede automatiske gebyrer](media/advancedchargesparameter.png)

Når avancerede autogebyrer er aktiveret, bliver brugerne ikke længere bedt om manuelt at indtaste et forsendelsesgebyr i POS-klienten, når de opretter en kundeordre af typen send alle eller send valgte. POS-gebyrer beregnes systematisk og føjes til POS-transaktionen (hvis der findes en tilsvarende tabel for automatiske gebyrer, der svarer til kriteriet for den ordre, der oprettes). Brugere kan også tilføje eller vedligeholde gebyrer på hoved- eller linjeniveau manuelt via nye, tilføjede POS-handlinger, der kan føjes til POS-skærmlayoutet.

Når avancerede automatiske gebyrer er aktiveret, bruges de eksisterende **Commerce-parametre** for **Kode for forsendelsesgebyrer** og **Refunder forsendelsesgebyrer** ikke længere. Disse parametre gælder kun hvis parameteren **Brug avancerede automatiske gebyrer** er indstillet til **Nej**.

Inden du aktiverer denne funktion, skal du teste og uddanne dine medarbejdere, fordi den aktiverede funktion ændrer forretningsprocessen for, hvordan forsendelsesgebyrer eller andre gebyrer beregnes og føjes til salgsordrer i POS. Du skal kunne forstå, hvilken virkning procesforløbet har på oprettelsen af transaktioner fra POS. Virkningen af at aktivere avancerede automatiske gebyrer er minimal for callcenter- og e-handelsordrer. Callcenter- og e-handels-programmer vil fortsat fungere på samme måde, som de har gjort historisk i forbindelse med tabeller for automatiske gebyrer til beregning af yderligere gebyrer. Callcenterkanalbrugere har fortsat mulighed for manuelt at redigere eventuelle systemberegnede automatiske gebyrer på hoved- eller linjeniveau eller manuelt tilføje ekstra gebyrer på hoved- eller linjeniveau.

## <a name="additional-pos-operations"></a>Yderligere POS-handlinger

Der er tilføjet nye operationer i POS, der sikrer, at avancerede automatiske gebyrer kan fungere korrekt i dit POS-programmiljø. Disse handlinger skal føjes til dine [POS-skærmlayout](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) og installeres på POS-enhederne, når du implementerer avancerede automatiske gebyrer. Hvis disse handlinger ikke tilføjes, kan brugerne ikke administrere eller vedligeholde gebyrer på POS-transaktioner og har ingen mulighed for at justere eller ændre værdierne for gebyrer, der systematisk er beregnet ud fra konfigurationer af automatiske gebyrer. Det anbefales, at du som minimum anvender handlingen **Administrer gebyrer** på dit POS-layout.

Der findes følgende nye handlinger.

- **142 - Administrer gebyrer** – Brug denne handling til at give POS-brugere tilladelse til at se og redigere gebyrer for den POS-transaktion, der enten blev tilføjet manuelt eller systematisk via beregninger af automatiske gebyrer.
- **141 – Tilføj gebyrer i hoved** – Brug denne handling for at give brugeren mulighed for manuelt at føje et gebyr på hovedniveau til eventuelle POS-salgstransaktioner (og vælge den gebyrkode, der skal bruges).
- **140 – Tilføj linjegebyrer** – Brug denne handling for at give brugeren mulighed for manuelt at føje et gebyr på linjeniveau til en eventuel POS-salgstransaktionslinje (og vælge den gebyrkode, der skal bruges).
- **143 - Genberegn gebyrer** – Brug denne handling til at udføre en komplet genberegning af gebyrerne for salgstransaktionen. Eventuelle tidligere automatiske gebyrer, der er tilsidesat af en bruger, genberegnes baseret på den aktuelle konfiguration af indkøbsvognen.

Som med alle POS-handlinger kan sikkerhedskonfigurationer udføres, så det kræver godkendelse fra lederen at udføre handlingen.

Det er vigtigt at bemærke, at de ovenfor angivne POS operationer også kan føjes til POS layout, selvom **Brug avancerede automatiske gebyrer**-parameteren er deaktiveret. I dette scenario får organisationer stadig fordelene ved at kunne få vist gebyrer, der er tilføjet manuelt, og redigere dem ved hjælp af handlingen **Administrer gebyrer**. Brugere kan også bruge handlingerne **Tilføj hovedgebyrer** og **Tilføj linjegebyrer** for POS-transaktioner, selv når **Brug avancerede automatiske gebyrer**-parameteren er deaktiveret. Handlingen **Genberegn gebyrer** har mindre funktionalitet, hvis den bruges, når **Brug avancerede automatiske gebyrer** er deaktiveret. I dette scenarie skal intet genberegnes, og eventuelle gebyrer, der er føjet til transaktionen manuelt, nulstilles blot til $0,00.

## <a name="use-case-examples"></a>Eksempler på brugsmønstre

I dette afsnit beskrives brugsmønstre, som kan hjælpe dig med at forstå konfiguration og brug af automatiske gebyrer og andre gebyrer inden for rammerne af kanalordrer. Disse eksempler illustrerer funktionsmåden af programmet, når parameteren **Brug avancerede automatiske gebyrer** er aktiveret.

### <a name="auto-charges-header-charges-example"></a>Eksempel på automatiske gebyrer af typen hovedgebyrer

#### <a name="use-case-scenario"></a>Brugsmønsterscenario

En forhandler ønsker automatisk at tilføje gebyrer for fragt, når der oprettes transaktioner i en Commerce-kanal, der kræver en forsendelse af produkter til kunden. Detailhandleren tilbyder to leveringsmåder: Fragt og Luft. Hvis en kunde vælger Fragt-levering, og ordreværdien er mindre end 100 USD, vil detailhandleren kræve et fragtgebyr af kunden på 10,00 USD. Hvis ordreværdien er over 100 USD, og kunden vælger Fragt-levering, opkræves kunden ikke yderligere fragtgebyrer. Hvis kunden vælger leveringsmetoden Luft for alle ordrer, uanset deres samlede værdi, opkræves et fragtgebyr på 20,00 USD.

#### <a name="setup-and-configuration"></a>Installation og konfiguration

Dette scenario kræver konfiguration af to tabeller for automatiske gebyrer.

Gå til **Debitor \> Konfiguration af gebyrer \> Automatiske gebyrer**.

Konfigurer to forskellige automatiske gebyrer på overskriftsniveau. Konfigurer ét for "Fragt-leveringsmåde" og ét for "Luft-leveringsmåde". I dette scenarie skal du konfigurere dem, så de kan bruges til "Alle kunder".

For Fragt-leveringsgebyrerne skal du i området Linjer på siden **Automatiske gebyrer** definere et gebyr, der gælder for ordrer mellem 0,01 USD og 100 USD som 10,00 USD. Opret en anden gebyrlinje for at angive, at ordrer over 100,01 USD er gebyrfri.

![Eksempel på to tabeller med automatiske gebyr](media/headerchargesexample.png)

For Luft-leveringsgebyrerne skal du i området Linjer i formularen Automatiske gebyrer definere et gebyr på 20,00 USD, der skal anvendes på alle ordrer (mellem en værdi på 0,01 og 9.999.999 USD).

Send gebyrerne til Commerce Scale Unit/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet **Distributionsplan 1040**.

#### <a name="sales-processing-for-this-scenario"></a>Salgsbehandling i dette scenarie

Når konfigurationen ovenfor er fuldført, og ændringerne er anvendt på kanaldatabasen, udnytter enhver kundeordre eller salgstransaktion, der er oprettet i POS, callcenter eller e-handels-kanaler, og har leveringsmetoden Fragt eller Luft angivet på hovedniveau, disse gebyrer og anvender dem automatisk på salget.

På nuværende tidspunkt anvendes gebyrerne på alle salgstransaktioner, der er oprettet inden for den juridiske enhed, og bruger disse leveringsmåder, fordi der ikke findes nogen funktionalitet, som angiver, at en konfiguration af automatiske gebyrer kun gælder for en bestemt salgskanal.

Hvad angår POS- og e-handelsscenarier – fordi der ikke er noget klart defineret "hoved" på disse ordrer, anvendes gebyrer på hovedniveau kun, hvis alle salgslinjer i transaktionen er indstillet til levering med nøjagtig samme leveringsmåde. Hvis der er "blandede måder" for ordreopfyldning på de transaktioner, der er oprettet af POS- eller e-handel, er det kun automatiske gebyrer på linjeniveau, der tages i betragtning og anvendes.

Brugeren har kontrol over indstillingen af leveringsmåden på ordrehovedet i callcenterscenarier, og derfor anvendes gebyrer på hovedniveau for disse ordrer, selvom nogle af salgslinjerne er konfigureret til at bruge en anden leveringsmåde. Gebyrer på hovedniveau for callcenterordrer baseres altid på den leveringsmåde, der er defineret på ordrehovedniveau i salgsordren.

### <a name="auto-charges-line-charges-example"></a>Eksempel på automatiske gebyrer af typen linjegebyrer

#### <a name="use-case-scenario"></a>Brugsmønsterscenario 

En forhandler ønsker at tilføje et ekstra gebyr til kunden som et opsætningsgebyr, når kunden køber en bestemt computermodel. Denne computer kræver yderligere ikke-obligatoriske opsætningshandlinger, som forhandleren skal udføre for kunden. Forhandleren har underrettet kunderne om, at der vil være et ekstra gebyr for denne opsætning. Forhandleren foretrækker at administrere de gebyrer, der er relateret til dette gebyr separat fra salgsprisen for produktet af økonomiske rapporteringshensyn. Et gebyr for opsætning på 19,99 USD vil blive faktureret kunden, når denne computer købes via en kanal.

#### <a name="setup-and-configuration"></a>Installation og konfiguration

Dette scenario kræver konfiguration af én tabel for automatiske gebyrer på linjeniveau.

Gå til **Debitor \> Konfiguration af gebyrer \> Automatiske gebyrer**.

Indstil **Niveau** rullemenuen til **Linje**, og opret en ny post til automatiske gebyrer for alle kunder og for det specifikke produkt eller produktgruppe, hvor opsætningsgebyrerne bliver opkrævet.

![Eksempel på et tabel med automatiske tillæg på linjeniveau](media/linechargesexample.png)

Send gebyrerne til Commerce Scale Unit/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet **Distributionsplan 1040**.

#### <a name="sales-processing-for-this-scenario"></a>Salgsbehandling i dette scenarie

Når konfigurationen ovenfor er fuldført, og ændringerne er anvendt på kanaldatabasen, udløser enhver kundeordre eller salgstransaktion, der er oprettet i POS, callcenter eller e-handels-kanaler, der har denne vare på ordren, et gebyr på linjeniveau, der systematisk føjes til ordretotalen.

På nuværende tidspunkt anvendes gebyrerne på enhver salgslinje, der matcher konfigurationen af automatiske gebyrer på linjeniveau inden for den juridiske enhed, fordi der ikke findes nogen funktioner til konfiguration af automatiske gebyrer på linjeniveau, så de kun gælder for en bestemt salgskanal.

### <a name="manual-header-charges-example"></a>Eksempel på manuelle hovedgebyrer

#### <a name="use-case-scenario-description"></a>Beskrivelse af brugsmønsterscenario

En forhandler gør en undtagelse fra typiske processer ved at tilbyde at levere en særlig privat levering af produkter til kunder, der bestiller produkter i butikken. Forhandleren og kunden har aftalt, at kunden skal betale et gebyr på 25 USD ekstra for håndtering af denne service. Medarbejderen hos forhandleren skal føje dette ekstra gebyr til transaktionen. Da gebyret er et rammeordregebyr og ikke er relateret til et enkelt produkt i ordren, bruges et hovedgebyr.

#### <a name="setup-and-configuration"></a>Installation og konfiguration

Sørg for, at den gebyrkode, der skal bruges i dette scenario, er konfigureret korrekt, ved at gå til **Debitor \> Konfiguration af gebyrer \> Tillæg** for at definere en tillægskode, der er relevant for scenariet.

![Eksempel på gebyrer](media/chargesexample.png)

Hvis gebyret skal betragtes som et gebyr, der er relateret til "forsendelse" med henblik på forsendelsesrelaterede rabatter eller kampagnetilbud, skal du indstille **Forsendelsesgebyr** i gebyrkoden til **Ja**. Hvis dette gebyr også må refunderes systematisk under behandlingen af en returtransaktion i POS-programmet, kan du indstille **Kan refunderes** til **Ja**. Flaget **Kan refunderes** kan kun anvendes, når **Brug avancerede automatiske gebyrer** parameter er indstillet til **Ja**.

Send gebyrerne til Commerce Scale Unit/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet **Distributionsplan 1040**.

Handlingen **Tilføj gebyrer i hoved** skal være konfigureret i dit [POS-skærmlayout](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), så en knap, der er tilgængelig for brugeren fra POS, kan kalde denne handling (handling 141). Skærmlayout-ændringer skal distribueres til kanalen samt via distributionsplansfunktionen.

#### <a name="sales-processing-of-manual-header-charges"></a>Salgsprocessen for manuelle hovedgebyrer

Du kan udføre scenariet i POS-programmet. POS-brugeren opretter salgstransaktionen som sædvanlig og tilføjer produkterne og eventuelle andre konfigurationer til salget. Før opkrævning af betaling skal brugeren udføre **Tilføj gebyrer i hoved** handlingen, hvor brugeren bliver bedt om at vælge en gebyrkode og angive værdien for gebyret. Når brugeren har fuldført processen, føjes gebyret til salgsordren som et gebyr på overskriftsniveau.

Denne proces kan anvendes i callcenter ved hjælp af den eksisterende **Tillæg** funktion, der findes under fanen **Sælg** på værktøjslinjen. På siden **Vedligehold gebyrer** kan brugeren tilføje en ny gebyrlinje i ordrehovedet.

### <a name="manual-line-charges-example"></a>Eksempel på manuelt linjegebyr

#### <a name="use-case-scenario"></a>Brugsmønsterscenario

En kunde har anmodet om, at to af fem varer på salgsordren bliver pakket som gave. Detailhandleren tilbyder denne valgfrie tjeneste for et gebyr på 2,00 USD pr. vare. Medarbejderen hos detailhandleren skal tilføje disse gebyrer til de forskellige varer, som skal pakkes som gave.

#### <a name="setup-and-configuration"></a>Installation og konfiguration

Sørg for, at den gebyrkode, der skal bruges i dette scenario, er konfigureret korrekt, ved at gå til **Debitor \> Konfiguration af gebyrer \> Tillæg** for at definere en tillægskode, der er relevant for scenariet.

Hvis gebyret skal betragtes som et gebyr, der er relateret til "forsendelse" med henblik på forsendelsesrelaterede rabatter eller kampagnetilbud, skal du indstille **Forsendelsesgebyr** i gebyrkoden til **Ja**. Hvis gebyret også må refunderes systematisk under behandlingen af en returtransaktion i POS-programmet, kan du indstille **Kan refunderes** til **Ja**. Flaget **Kan refunderes** kan kun anvendes, når **Brug avancerede automatiske gebyrer** parameter er indstillet til **Ja**.

Send gebyrerne til Commerce Scale Unit/Kanaldatabase, så POS kan udnytte dem, ved at køre jobbet **Distributionsplan 1040**.

Handlingen **Tilføj linjegebyrer** skal være konfigureret i dit [POS-skærmlayout](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), så en knap, der er tilgængelig for brugeren fra POS, kan kalde denne handling (handling 140). Skærmlayout-ændringer skal distribueres til kanalen samt via distributionsplansfunktionen.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Salgsprocessen for det manuelle linjegebyr

Du kan udføre scenariet i POS-programmet. POS-brugeren opretter salgstransaktionen som sædvanlig og tilføjer produkterne og eventuelle andre konfigurationer til salget. Før opkrævning af betaling, skal brugeren vælge den specifikke linje, hvor gebyret anvendes, fra visningen med POS-varelisten og udføre **Tilføj linjegebyr**-handlingen. Brugeren bliver bedt om at vælge en gebyrkode og angiv værdien af gebyret. Når brugeren har fuldført processen, knyttes gebyret til linjen og føjes til ordretotalen som et gebyr på linjeniveau. Brugeren kan gentage processen for at føje yderligere linjegebyrer til andre varelinjer i posteringen, hvis det er nødvendigt.

Den samme proces kan anvendes i callcenteret ved hjælp af funktionen "Vedligehold gebyrer", som du finder under **Regnskaber**-rullemenuen i **Salgsordrelinjer** sektionen på siden **Salgsordre**. Hvis du vælger denne indstilling, åbnes siden **Vedligehold gebyrer**, hvor brugeren kan tilføje et nyt linjespecifikt gebyr til transaktionen.

## <a name="additional-features"></a>Yderligere funktioner

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Redigering af gebyrer på en POS-salgstransaktion

Handlingen **Administrer gebyrer** (142) skal føjes til [POS-skærmlayoutet](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), så en bruger kan få vist og redigere eller tilsidesætte eventuelle gebyrer på linje- eller overskriftsniveau, der er beregnet af systemet eller oprettet manuelt. Hvis handlingen ikke tilføjes, kan brugerne ikke justere værdien gebyret på POS-transaktionen, og de kan heller ikke se detaljerne for gebyrerne, f.eks. typen gebyrkode, der er knyttet til gebyret.

På siden **Administrer gebyrer** i POS kan brugeren kan få vist detaljer om gebyrer på både hoved- og linjeniveau. Brugeren kan anvende **Rediger** funktionen, der er tilgængelig på denne side, til at foretage ændringer af det beløb, der lægges til en linje for specifikke gebyrer. Når en linje for gebyrer overskrives manuelt, genberegnes den ikke systematisk, medmindre brugeren starter handlingen **Genberegn gebyrer**.

Hvis **Årsagskode for tilsidesættelse af gebyr** er konfigureret på opsætningssiden **Commerce-parametre**, bliver brugeren bedt om at angive en årsagskode, når gebyrer er blevet ændret i POS-programmet.

Hvis der er hentet årsagskoder for tilsidesatte gebyrer, findes der også en ny rapport til gennemsyn og overvågning af disse tilsidesættelser. Rapporten findes i **Retail og Commerce \> Forespørgsler og rapporter \> Tilsidesættelseshistorik for gebyr**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Tilbagebetaling af gebyrer på en POS-returtransaktion

Hvis parameteren **Brug avancerede automatiske gebyrer** er indstillet til **Ja**, gælder den eksisterende Commerce-parameter for **Refunder forsendelsesgebyrer** ikke længere. Du kan angive, hvilke gebyrer der systematisk skal refunderes til en kunde, når der bruges avancerede automatiske gebyrer, skal du sikre, at koden for relaterede gebyrer er konfigureret som **Kan refunderes** på opsætningssiden **Gebyrkode**. Sørg for, at indstillingerne er synkroniseret med Commerce-kanalens databaser via behandling af distributionsplanen.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Tilbagebetaling af gebyrer på en returordretransaktion

Gebyrer refunderes ikke systematisk til **Returordrer**, der er oprettet i Commerce. Brugerne skal vælge indstillingen **Kopiér gebyrer**, når de opretter deres **Returordre**. Hvis **Kopiér gebyrer** er ikke markeret, refunderes gebyrer fra den oprindelige salgstransaktion ikke automatisk. Hvis **Kopiér gebyrer** er markeret, kopieres alle gebyrer til returordren, og brugeren kan manuelt redigere eller fjerne eventuelle gebyrer, som de ikke vil have refunderet. Callcenterets returordreproces kan i øjeblikket ikke bekræfte flaget **Kan refunderes** i **Gebyrkode**-opsætningen.

### <a name="configuring-pos-receipts-to-show-charges"></a>Konfiguration af POS-kvitteringer til visning af gebyrer

Der er tilføjet følgende kvitteringselementer til kvitteringslinjen og -sidefoden til understøttelse af den avancerede automatiske gebyrfunktion.

- **Forsendelsesgebyrer for linje** – Dette element på linjeniveau kan bruges til at opsummere bestemt gebyrkoder, der er anvendt til salgslinjen. Kun gebyrkoder, der er blevet afmærket som **Forsendelse**-gebyrer på siden **Gebyrkode**, vises her.
- **Andre gebyrer for linje** – Dette element på linjeniveau kan bruges til at opsummere ikke-forsendelsesgebyrkoder, der er anvendt på salgslinjen. Disse er gebyrkoder, hvor flaget **Forsendelse** på siden **Gebyrkode** er ikke aktiveret.
- **Oplysninger om forsendelsesgebyrer for ordre** – Dette element sidefodsniveau vises beskrivelserne af de gebyrkoder, der er anvendt på ordren, der er afmærket som **Forsendelse**-gebyr på opsætningssiden **Gebyrkode**.
- **Forsendelsesgebyrer for ordre** – Dette element på sidefodsniveau vises værdien i dollar af de forsendelsesrelaterede gebyrer.
- **Oplysninger om andre gebyrer for ordre** – Dette element sidefodsniveau vises beskrivelsen af de gebyrkoder, der er anvendt på ordren, der ikke er mærket som forsendelsesrelaterede gebyrer.
- **Andre gebyrer for ordre** – Dette element på sidefodsniveau vises værdien i dollar af de andre gebyrer, der ikke er forsendelsesrelaterede.

Det anbefales, at organisationen også føjer fritekstfelter i kvitteringens sidefod for at definere de områder, hvor gebyrerne opsummeres.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Forhindre, at gebyrer beregnes, før POS-ordren er fuldført

Visse organisationer kan foretrække at vente på, at brugeren er færdig med at tilføje alle salgslinjerne til POS transaktionen før beregning af gebyrer. For at forhindre beregning af gebyrer i takt med at varer føjes til POS-transaktionen, skal du slå parameteren **Beregning af manuelt gebyr** i den **Funktionalitetsprofil**, der bruges i butikken. Aktivering af denne parameter forudsætter, at POS-brugeren bruger handlingen **Beregn totaler** efter at have føjet produkterne til POS-transaktionen. Handlingen **Beregn totaler** udløser derefter beregningen af de automatiske gebyrer for det/de relevante ordrehoved eller -linjer.

### <a name="charges-override-reports"></a>Rapporter over gebyrtilsidesættelser

Hvis brugere tilsidesætter de beregnede gebyrer manuelt eller føjer et manuelle gebyr til transaktionen, vil disse data være tilgængelige til revidering i rapporten **Tilsidesættelseshistorik for gebyr**. Rapporten findes i **Retail og Commerce \> Forespørgsler og rapporter \> Tilsidesættelseshistorik for gebyr**. Det er vigtigt at bemærke, at de data, der skal bruges til denne rapport, importeres fra kanaldatabasen til Headquarters via "P"-distributionsplanlægningsopgaver. Derfor er oplysninger om tilsidesættelser, der netop er udført i POS, muligvis ikke umiddelbart tilgængelige i denne rapport, før dette job har overført butikkens transaktionsdata til Headquarters.

## <a name="additional-resources"></a>Yderligere ressourcer

[Aktivere og konfigurere automatiske gebyrer efter kanal](auto-charges-by-channel.md)

[Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer](pro-rate-charges-matching-lines.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]