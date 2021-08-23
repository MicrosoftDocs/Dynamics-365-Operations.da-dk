---
title: Beregne lagertilgængelighed for detailkanaler
description: I dette emne beskrives det, hvordan et firma kan bruge Microsoft Dynamics 365 Commerce til at få vist den forkalkulerede disponible tilgængelighed for produkter i online- og butikskanalerne.
author: hhainesms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: da79aadace09ad480fa34bc03220831023e469645bb7d53af1647bd2d35af0ea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741806"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Beregne lagertilgængelighed for detailkanaler

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan et firma kan bruge Microsoft Dynamics 365 Commerce til at få vist den forkalkulerede disponible tilgængelighed for produkter i online- og butikskanalerne.

## <a name="accuracy-of-inventory-availability"></a>Nøjagtighed for lagertilgængelighed

I Commerce anvendes flere servere og databaser for at sikre skalerbarhed og ydeevne. Derfor er det vigtigt, at du forstår, at værdierne for den tilgængelige lagerbeholdning, som leveres gennem POS-programmet (Point Of Sale), API'er (Application Programming Interface) for e-Commerce-lagertilgængelighed og de disponible lagersider i Commerce-hovedkvarteret muligvis ikke er 100 procent nøjagtige i realtid. Hvis transaktioner, der er oprettet for produkter i online- eller butikskanalen, endnu ikke er synkroniseret med hovedkontoret, vil siderne for disponibel lagerbeholdning i hovedkvarteret muligvis ikke vise en præcis realtidsværdi for lagerbeholdningen for disse produkter. Hvis du derimod har konfigureret din virksomhed, så brugere i hovedkvarteret eller andre integrerede programmer kan sælge, modtage, returnere eller på anden måde justere lagerbeholdningen ud fra en butik eller et onlinelagersted, vil POS eller onlinekanalen muligvis ikke have alle de oplysninger, der kræves for at vise nøjagtige værdier i realtid for varerne.

Det er vigtigt at forstå, at alle data om disponibel tilgængelighed, som er angivet i løbet af arbejdsdagen, anses for at være estimerede værdier. Hvis du derfor forsøger at sammenligne oplysningerne om den disponible lagerbeholdning, som programmet leverer, med den faktiske fysiske lagerbeholdning på hylderne, eller hvis du forsøger at sammenligne de disponible værdier, som vises i POS, med data om den disponible lagerbeholdning, som du finder for det samme lagersted i hovedkvarteret, kan værdierne være forskellige. Denne forskel i løbet af arbejdsdagen er forventelig og bør ikke betragtes som et problem. Hvis du vil revidere data og sikre, at de værdier, som leveres i POS, API'er og hovedkvarteret, svarer til de faktiske fysiske enheder, som du finder i din butik eller på lagerstedets hylder, er den bedste tidspunkt, når kanalhandlingerne er stoppet for dagen, og alle transaktioner er blevet korrekt synkroniseret mellem hovedkvarteret og kanalerne.

## <a name="channel-side-inventory-calculation"></a>Lagerberegning på kanalsiden

Lagerberegning på kanalsiden er en mekanisme, der bruger de senest kendte kanallagerdata i Commerce-hovedkvarteret som udgangspunkt, og derefter indregner yderligere lagerændringer på kanalsiden, som ikke er inkluderet i dette grundlag med henblik på at beregne en estimeret disponibel lagerbeholdning næsten i realtid. 

Følgende lagerændringer tages i øjeblikket i betragtning i lagerberegningslogikken på kanalsiden:

- Lagerbeholdning solgt via cash-and-carry-ordrer i butik
- Lagerbeholdning solgt via kundeordrer i butik eller via onlinekanal
- Lagerbeholdning returneret til butik
- Lagerbeholdning opfyldt (pluk, pakning, levering) fra butiks lagersted

Hvis du vil bruge lagerberegning på kanalsiden, er forudsætningen at der sendes et periodisk øjebliksbillede af lagerdata fra hovedkontoret, som oprettes af jobbet **Produkttilgængelighed**, til kanaldatabaserne. Øjebliksbilledet repræsenterer de oplysninger, som hovedkvarteret har om lagerbeholdningens tilgængelighed for en bestemt kombination af et produkt eller en produktvariant og et lagersted. Det omfatter kun de lagertransaktioner, der blev behandlet og bogført i hovedkontoret på det tidspunkt, hvor øjebliksbilledet blev taget, og det er muligvis ikke 100 % nøjagtigt i realtid på grund af den konstante behandling af salgsordrer, som foregår på tværs af distribuerede servere.

- Hvis lagerbeholdningen for et produkt er solgt fra en butik via cash-and-carry eller et asynkront kundeordresalg i POS-programmet, vil hovedkvarteret ikke omgående få oplysninger om den relaterede lagerafgangstransaktion for salget. Hovedkvarteret vil først have oplysninger om den lagerbeholdning, der er solgt for disse typer butikssalg, efter P-jobbet har overført den relaterede transaktion fra butikkens kanaldatabase til hovedkvarteret, og de relaterede salgsordrer er oprettet via bogføring af opgørelsen eller sivende feedbaseret bogføring. Processen for oprettelsen af ordrer i hovedkvarteret opretter de relaterede lagertransaktioner. 
- For e-handelskanalers ordrer indeholder hovedkvarteret kun oplysninger om lagertransaktionerne, når transaktionerne er sendt til hovedkvarteret via P-jobbet, og processen til synkronisering af ordren er fuldført.

Hvis du vil tage et øjebliksbillede af lagerbeholdningen i Commerce-hovedkvarteret, skal du benytte denne fremgangsmåde.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Produkter og lager \> Produkttilgængelighed**.
1. Vælg **OK** for at køre jobbet **Produkttilgængelighed**. Du kan også planlægge dette job, så det køres i et batch.

Når jobbet **Produkttilgængelighed** er kørt, skal de data, der blev registreret, sendes til kanalens databaser, så det seneste øjebliksbillede af lagerbeholdningen for hovedkvarteret kan tages i betragtning i kanalsidens beregning af forkalkulerede disponible lagerbeholdning.

Benyt følgende fremgangsmåde for at synkronisere øjebliksbilledets data fra hovedkontoret til kanaldatabaserne.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Kør jobbet **1130** (**Produkttilgængelighed**) for at synkronisere de øjebliksdata, som jobbet **Produkttilgængelighed** har oprettet fra hovedkvarteret til dine kanaldatabaser.

## <a name="inventory-availability-apis-for-e-commerce"></a>API'er for lagerbeholdnings tilgængelighed ved e-handel

Commerce indeholder følgende API'er for scenarier for e-handel med henblik på forespørgsel på lagerbeholdningens tilgængelighed for et produkt:

- **GetEstimatedAvailability** – Brug denne API til at forespørge på lagerbeholdninge for et produkt eller en produktvariant på onlinekanalens lagersted eller lagersteder, som er knyttet til onlinekanalens opfyldelsesgruppe.
- **GetEstimatedProductWarehouseAvailability** – Brug denne API til forespørge om et produkt eller en produktvariant fra et bestemt lagersted.

> [!NOTE]
> Disse API'er erstatter API'erne **GetProductAvailabilities** og **GetAvailableInventoryNearby** i Commerce version 10.0.7 og tidligere.

Begge API'er anvender beregningslogikken for kanalsiden og returnerer et forkalkuleret **fysisk tilgængeligt** antal, **samlet tilgængeligt** antal, **måleenhed** og **lagerniveau** for det ønskede produkt og lagersted. Værdierne kan vises på dit e-Commerce-websted, hvis du ønsker det, eller de kan bruges til at udløse en anden forretningslogik på dit e-Commerce-websted. Du kan f.eks. forhindre køb af produkter med lagerniveauet "ikke på lager".

Selvom andre API'er, der er tilgængelige i Commerce, kan gå direkte til hovedkvarteret for at hente disponible mængder for produkter, anbefales det ikke, at de bruges i et e-handelsmiljø på grund af potentielle problemer med ydeevnen og påvirkninger, som disse hyppige anmodninger kan have på serverne for hovedkvarteret. Desuden kan de to ovennævnte API'er ved beregning på kanalsiden give et mere præcist estimat over et produkts tilgængelighed under hensyntagen til de transaktioner, der er oprettet i de kanaler, som endnu ikke er kendte for hovedkontoret.

Hvis du vil bruge de to API'er, skal du aktivere funktionen **Beregning af optimeret produkttilgængelighed** via arbejdsområdet **Funktionsstyring** i hovedkvarteret. Hvis online- og butikskanalerne bruger samme opfyldningslagersted, skal du også aktivere funktionen **Udvidet lagerberegningslogik på kanalsiden for e-handel** for at beregningslogikken på kanalsiden i de to API'er indregner de ikke-bogførte transaktioner (cash-and-carry, kundeordrer og returneringer), som er oprettet i butikskanalen. Du skal køre jobbet **1070** (**Kanalkonfiguration**), når du har aktiveret disse funktioner.

Hvis du vil angive, hvordan produktantal skal returneres i API-output, skal du benytte denne fremgangsmåde.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre**.
1. Vælg fanen **Lagerbeholdning**, og konfigurer derefter værdien i indstillingen **Antal i API-output** i oversigtspanelet **API'er for lagerbeholdnings tilgængelighed for e-handel**.
1. Kør jobbet **1070** (**Kanalkonfiguration**) for at synkronisere den seneste indstilling med kanaler.

Indstillingen **Antal i API-output** giver tre valgmuligheder:

- **Returner lagerantal** – Fysisk tilgængeligt og samlet tilgængeligt antal af et ønsket produkt returneres i API-output.
- **Returner lagerantal, fratrukket lagerbuffer** – Det antal, der returneres i API-outputtet, reguleres ved at fratrække lagerbufferværdien. Yderligere oplysninger om lagerbufferen finder du i [Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md).
- **Returner ikke lagerantal** – Kun lagerniveauet returneres i API-outputtet. Yderligere oplysninger om lagerniveauer finder du i [Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md).

Du kan bruge API-parameteren `QuantityUnitTypeValue` til at angive den enhedstype, som API'er skal returnere antal i. Denne parameter understøtter indstillingerne for **lagerenhed** (standard), **købsenhed** og **salgsenhed**. Det returnerede antal afrundes til den definerede præcision for den tilsvarende måleenhed i hovedkontoret.

API'en **GetEstimatedAvailability** indeholder følgende inputparametre, der understøtter forskellige forespørgselsscenarier:

- `DefaultWarehouseOnly` – Brug denne parameter til at forespørge på lagerbeholdningen for et produkt på onlinekanalens standardlagersted. 
- `FilterByChannelFulfillmentGroup` og `SearchArea` – Brug disse to parametre til at forespørge på lagerbeholdningen for et produkt fra alle afhentningslokationer inden for et bestemt søgeområde på baggrund af `longitude`, `latitude` og `radius`. 
- `FilterByChannelFulfillmentGroup` og `DeliveryModeTypeFilterValue` – Brug disse to parametre til at forespørge på lagerbeholdningen for et produkt fra bestemte lagersteder, der er tilknyttet en onlinekanals opfyldelsesgruppe og er konfigureret til at understøtte bestemte leveringsmåder. Parameteren `DeliveryModeTypeFilterValue` understøtter indstillingerne for **alle** (standard), **forsendelse** og **afhentning**. I et scenario, hvor en onlineordre kan opfyldes fra flere forsendelseslagersteder, kan du f.eks. bruge disse to parametre til at forespørge på et produkts disponible lagerbeholdning på alle disse forsendelseslagersteder. API'en returnerer i dette tilfælde produktets disponible antal og lagerniveau på hvert af forsendelseslagerstederne plus et samlet antal og et samlet lagerniveau fra alle forsendelseslagersteder i forespørgselsområdet.
 
Modulerne for Commerce-købefelt, butiksvælger, ønskeliste, indkøbsvogn og indkøbsvognikon bruger de API'er og parametre, der er nævnt ovenfor, for at vise meddelelser om lagerniveau på tværs af e-handelswebstedet. Commerce-webstedsgeneratoren indeholder forskellige lagerindstillinger til styring af merchandising og købsadfærd. Du finder flere oplysninger under [Anvendelse af lagerindstillinger](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Opslag i POS-lager med beregning på kanalsiden

I Commerce version 10.0.9 og tidligere har handlingen **Lagersøgning** i POS brugt et servicekald i realtid til hovedkvarteret til at hente lageroplysninger om det valgte produkt for både brugerens aktuelle butik og eventuelle andre butikker, der er konfigureret i opfyldelsesgruppen som en del af kanalkonfigurationen for butikken. I Commerce version 10.0.10 og senere kan du deaktivere serviceopkald i realtid til hovedkontoret og i stedet bruge beregning på kanalsiden på Commerce-serveren til at bestemme den disponible lagerbeholdning, der er fysisk tilgængelig for butikken og eventualle andre lokationer, der er defineret i opfyldningsgruppen. Denne kanalberegnede lagerkonfiguration er også nyttig for lokationer, hvor internetforbindelsen er upålidelig, da du ikke behøver at være online for at foretage lagersøgninger fra hovedkvarteret.

Når beregningen på kanalsiden er korrekt konfigureret og administreret, kan det give et mere pålideligt estimat over det aktuelle butikslager, fordi det bruger de transaktionsdata, som findes i Commerce-kanaldatabasen, men hovedkvarteret måske endnu ikke har oplysninger om. Hvis du f.eks. bruger det eksisterende servicekald i realtid til at foretage lagersøgninger i POS, har hovedkvarteret sandsynligvis ingen oplysninger om et cash-and-carry-salg af et produkt, som netop er foretaget. Derfor vil værdien af den disponible lagerbeholdning, som hovedkvarteret returnerer for det pågældende produkt, formentlig overstige butikkens faktiske disponible lager med én enhed. Men hvis du bruger kanalsideberegningen, kan cash-and-carry-salg medtages i beregningen og trækkes fra den disponible værdi, der vises. Selvom de værdier, som både kanalsideberegninger og realtids servicekald tilvejebringer, blot er estimater af det disponible lager, er det meget mere sandsynligt, at den værdi, som kanalsideberegningen giver, er et nøjagtigt billede af den aktuelle butik.

Hvis du vil konfigurere POS-handlingen **Lagersøgning** i Commerce Headquarters for at bruge beregningslogikken for kanalsiden og deaktivere realtidstjenesteopkald, skal du først aktivere funktionen **Beregning af optimeret produkttilgængelighed** via arbejdsområdet **Funktionsstyring** i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**.
1. Vælg en funktionalitetsprofil.
1. I oversigtspanelet **Funktioner** i sektionen **Beregning af disponibelt lager** skal du ændre værdien i feltet **Metode til beregning af disponibelt lager** fra **Realtidstjeneste** til **Kanal**. Alle funktionalitetsprofiler anvender som standard realtidstjenestekald. Du skal ændre værdien i dette felt, hvis du vil bruge kanalsidens beregningslogik. Alle de detailbutikker, der er kædet sammen med den valgte funktionalitetsprofil, påvirkes af ændringen.

Du skal derefter synkronisere ændringerne med kanalerne ved hjælp af processen for distributionsplanlægning i hovedkvarteret ved at benytte denne fremgangsmåde.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Kør jobbet **1070** (**Kanalkonfiguration**).

Når konfigurationen er fuldført, bruger de oplysninger, der er til rådighed for tilgængeligheden på det fysiske lager, ikke længere et realtids servicekald, når en bruger i POS-programmer anvender handlingen **Lagersøgning** (standard- og matrixvisninger). I stedet beregnes data om det fysisk disponible lager for den aktuelle butik og alle butikker i opfyldelsesgruppen på grundlag af det sidst kendte øjebliksbillede, der blev leveret til kanaldatabasen fra Commerce Headquarters. Værdien i øjebliksbilledet bestemmes endvidere af kanalsideberegningen for at justere den fysisk tilgængelighedsværdi og er baseret på de yderligere salgs- eller returneringstransaktioner, der er foretaget for det valgte produkt i kanaldatabasen, og som ikke var medtaget i det sidste synkroniserede øjebliksbillede fra 1130-jobbet. Hvis kanaldatabasen ikke indeholder transaktionsdata for nogle af lagerstederne eller butikkerne i opfyldelsesgruppen, indeholder den ikke yderligere transaktioner, som kan tages i betragtning i forbindelse med en genberegning af værdien. Det bedste estimat over det disponible lager, der kan vises for de pågældende lagersteder eller butikker, er derfor data fra det sidst kendte øjebliksbillede af Commerce Headquarters.

POS' skærmbillederne **Opfyldelse af ordre** bruger også kanalsideberegningen til at vise det disponible lager for varer, når en ordreopfyldelseslinje vælges, og en bruger får vist panelet **Detaljer** for den valgte vare.

## <a name="optimize-your-inventory-data"></a>Optimer lagerdataene

For at sikre det bedst mulige estimat over lageret, er det vigtigt, at du bruger følgende Commerce-batchjob og kører dem ofte:

- **P-job** – P-jobbet findes på siden **Distributionsplaner** og bør køres ofte. Dette job overfører e-Commerce-ordrer, asynkrone kundeordrer, som er oprettet af POS, samt cash-and-carry-ordrer, som POS har oprettet på baggrund af kanaldatabaserne, til Commerce Headquarters, så de kan behandles yderligere. Indtil disse data er synkroniseret fra kanalen til Commerce Headquarters, har Commerce Headquarters ingen oplysninger om lagerreguleringer af produkter på de lagersteder, der er resultatet af disse transaktioner.
- **Synkroniser ordrer** – Dette job behandler de rå transaktionsdata i Commerce Headquarters, som P-jobbet tilvejebringer, og konverterer e-Commerce-transaktioner og asynkrone kundeordretransaktioner til salgsordrer i Commerce Headquarters. Der oprettes ingen lagertransaktioner, før dette job er blevet behandlet, og der er blevet oprettet salgsordrer. Det disponible lager i Commerce Headquarters vil derfor ikke tage højde for transaktionerne.
- **Beregn transaktionsopgørelser i batch** – For så vidt angår cash-and-carry-transaktioner, der oprettes i butikken, sikrer den sivende feedbaseret bogføringsproces, at det lager, der er relateret til salget, opdateres effektivt. Hvis du vil opnå den mest effektive behandling af lagertransaktioner for cash-and-carry-ordrer, skal du sikre dig, at du konfigurerer dit system til at anvende [sivende feedbaseret bogføring](./trickle-feed.md).
- **Bogfør transaktionsopgørelser i batch** – Dette job er også påkrævet ved sivende feedbaseret bogføring. Den følger jobbet **Beregning af transaktionsopgørelser i batch**. Dette job bogfører systematisk de beregnede opgørelser, så der oprettes salgsordrer for cash-and-carry-salg i Commerce Headquarters, og Commerce Headquarters mere nøjagtigt kan afspejle butikkens lagerbeholdning.
- **Produkttilgængelighed** – Dette job opretter øjebliksbilledet af lageret fra Commerce Headquarters.
- **1130 (Produkttilgængelighed)** – Dette job kan findes på siden **Distributionsplaner** og bør køres umiddelbart efter jobbet **Produkttilgængelighed**. Dette job viderefører øjebliksdataene for lageret fra Commerce Headquarters til kanaldatabaserne.

> [!NOTE]
> - Det er bedste praksis at køre jobbene **Produkttilgængelighed** og **1130** hver time og planlægge P-job, synkronisere ordrer og udføre sivende feedbaseret bogføring med samme eller højere hyppighed.
> - Når der anvendes beregninger af disponibel lagerbeholdning på kanalsiden til at anmode om disponibel lagerbeholdning ved hjælp af API'er for e-handel eller lagerlogikken på kanalsiden, anvender beregningerne af hensyn til ydeevnen en cache til at bestemme, om der er gået tilstrækkelig tid til at køre beregningslogikken igen. Standardcachen er angivet til 60 sekunder. Du har f.eks. slået kanalsideberegningen til for din butik og har fået vist det disponible lager for et produkt på siden **Lagersøgning**. Hvis der derefter sælges en enhed af produktet, vil siden **Lagersøgning** ikke vise det reducerede lager, før cachen er blevet ryddet. Når brugere har bogført transaktioner i POS, bør de vente 60 sekunder, før de bekræfter, at det disponible lager er blevet reduceret.

Hvis dit virksomhedsscenarie kræver en mindre cacheperiode, skal du kontakte produktsupportmedarbejderen for at få hjælp.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
