---
title: Beregning af lagertilgængelighed for detailkanaler
description: I dette emne beskrives de indstillinger, der er tilgængelige for visning af butikkens og onlinekanalernes disponible lager.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 68fa26daac055cd0fd72035683f05ed36052b3a3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995814"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Beregning af lagertilgængelighed for detailkanaler

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan et firma kan bruge Microsoft Dynamics 365 Commerce til at få vist den forkalkulerede disponible tilgængelighed for produkter i online- og butikskanalerne.

## <a name="accuracy-of-calculation"></a>Nøjagtigheden af beregningen

I Commerce anvendes flere servere og databaser for at sikre skalerbarhed og ydeevne. Derfor er det vigtigt, at du forstår, at de tilgængelige lagerværdier, som leveres gennem POS-programmet (Point Of Sale), e-Commerce-lagertilgængeligheds-API'erne (Application Programming Interface), og de disponible lagersider i Commerce Headquarters muligvis ikke er 100 procent nøjagtige i realtid. Hvis transaktioner, der er oprettet for produkter i online- eller butikskanalen, endnu ikke er synkroniseret med Commerce Headquarters-serveren og -databasen, vil de disponible lagerbeholdningssider i Commerce Headquarters muligvis ikke vise en præcis lagerværdi i realtid for disse produkter. Hvis du på den anden side konfigurerede din virksomhed, så brugere i Commerce Headquarters eller andre integrerede programmer kan sælge, modtage, returnere eller på anden måde justere lager ud af en butik eller et online lager, vil POS eller den online kanal muligvis ikke have alle de oplysninger, som er nødvendige for at vise en nøjagtig disponibel værdi for varer i realtid.

I dette emne forklares de datasynkroniseringsprocesser, der kan køres hyppigt med henblik på at begrænse ventetiden for data mellem programmer eller kanaler. Det er dog vigtigt, at du forstår, at alle disponible tilgængelighedsdata, der angives i løbet af arbejdsdagen, anses for at være en estimeret værdi. Hvis du derfor prøver at sammenligne oplysningerne om det disponible lager, som programmet leverer, med det faktiske fysiske lager på hylderne, eller hvis du prøver at sammenligne de disponible værdier, som vises i POS, med de disponible data, som du finder i det samme lager i Commerce Headquarters, kan værdierne være forskellige. Denne forskel i løbet af arbejdsdagen er forventelig og bør ikke betragtes som et problem. Hvis du vil revidere data og sikre, at de værdier, som leveres i lagertilgængeligheds-API'erne og Commerce Headquarters, matcher de faktiske fysiske enheder, som du finder i din butik eller på lagerets hylder, er den bedste tid at gøre det på, efter at kanalhandlinger er stoppet om dagen, og alle transaktioner er blevet korrekt synkroniseret mellem Commerce Headquarters og kanalen.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Brug API'er til lagersøgning til e-Commerce-anmodninger om lagertilgængelighed

Du kan bruge følgende API'er til at få vist lagertilgængeligheden for et produkt, når kunderne handler på et e-Commerce-websted.

- **GetEstimatedAvailability** – Brug denne API til at få oplyst lagertilgængeligheden for varen på e-Commerce-kanalens lagersted eller alle de lagersteder, der er knyttet til konfigurationen af ordreopfyldningsgruppen for e-Commerce-kanalen. Denne API kan også bruges til lagersteder i et specifikt søgeområde eller en bestemt radius baseret på data for længdegrad og breddegrad.
- **GetEstimatedProductWarehouseAvailability** – Brug denne API til at anmode om lageroplysninger for en vare fra et bestemt lagersted. Du kan f.eks. bruge den til at få vist lagertilgængelighed i scenarier, der omfatter ordreafhentning.

> [!NOTE]
> Disse API'er erstatter API'erne **GetProductAvailabilities** og **GetAvailableInventoryNearby** i Dynamics 365 Retail, version 10.0.7 og tidligere.

Begge API'er henter data fra Commerce-serveren og giver en forkalkulation af det disponible lager for en bestemt kombination af et produkt eller en produktvariant og et lagersted. Selvom andre API'er, der er tilgængelige på Commerce-serveren, kan gå direkte til Commerce Headquarters for at hente disponible mængder for produkter, anbefales det ikke, at de bruges i et e-Commerce-miljø på grund af potentielle problemer med ydeevnen og relaterede virkninger, som disse hyppige anmodninger kan have på dine Commerce Headquarters-servere. Hvis det disponible lager beregnes via Commerce-serveren, er det mere sandsynligt, at beregningen omfatter den lagerbeholdning, der blev solgt i seneste e-Commerce-transaktioner, som endnu ikke er blevet synkroniseret med Commerce Headquarters. Selvom der måske ikke er oplysninger om disse transaktioner i Commerce Headquarters, har Commerce-serveren og kanaldatabasen dataene. Dataene vil derfor blive indregnet i og kan hjælpe med at give et mere nøjagtigt estimat over det tilgængelige lager for et produkt.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Introduktion til beregnet lagertilgængelighed i e-Commerce

Før du bruger de to API'er, der er nævnt tidligere, skal du aktivere funktionen **Beregning af optimeret produkttilgængelighed** via arbejdsområdet **Funktionsstyring** i Commerce Headquarters.

Før API'erne kan beregne det bedst mulige estimat over lagertilgængelighed for en vare, skal et periodisk øjebliksbillede af lagertilgængeligheden fra Commerce Headquarters behandles og sendes til den kanaldatabase, som e-Commerce Scale Unit bruger. Øjebliksbilledet repræsenterer de oplysninger, som Commerce Headquarters har om lagertilgængeligheden for en bestemt kombination af et produkt eller en produktvariant og et lagersted. Det kan indeholde lagerreguleringer eller -bevægelser, der er forårsaget af lagerkvitteringer eller forsendelser eller andre processer, der udføres i Commerce Headquarters, og som e-Commerce-kanalen kun har oplysninger om på grund af synkroniseringsprocessen.

Det øjebliksbillede af databasen, som jobbet **Produkttilgængelighed** opretter, beregner kun de lagertransaktioner, der er behandlet og bogført i Commerce Headquarters på det tidspunkt, hvor øjebliksbilledet blev taget. Hvis lageret for et produkt blev solgt i en butiks lagersted via cash-and-carry eller et asynkront kundeordresalg i POS-programmet, vil Commerce Headquarters ikke omgående få oplysninger om den relaterede lagerafgangstransaktion for salget. Det vil først have oplysninger om det lager, der sælges for disse typer butikssalg, efter P-jobbet overfører den relaterede transaktion fra butikkens kanaldatabase til Commerce Headquarters, og den relaterede salgsordre oprettes via bogføring eller sivende feedbaseret bogføring. Processen med at oprette ordren i Commerce Headquarters opretter de relaterede lagertransaktioner. For så vidt angår e-Commerce-kanalordrer indeholder Commerce Headquarters kun oplysninger om lagertransaktionerne, når transaktionerne er sendt til Commerce Headquarters via P-jobbet, og processen til synkronisering af ordren er fuldført. Det er derfor vigtigt, at du forstår, at den værdi for lagerøjebliksbilledet, der vises i jobbet **Produkttilgængelighed**, muligvis ikke er 100 % nøjagtig i realtid på grund af den konstante salgsbehandling, der opstår på tværs af distribuerede servere.

Hvis du vil tage et øjebliksbillede af lageret i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Produkter og lager \> Produkttilgængelighed**.
1. Vælg **OK** for at køre jobbet **Produkttilgængelighed**. Du kan også planlægge dette job, så det køres i en batch.

Når jobbet **Produkttilgængelighed** er kørt færdigt, skal de data, der blev registreret, sendes til e-Commerce-kanalens databaser, så det seneste lager øjebliksbillede for lageret i Commerce Headquarters kan tages i betragtning i forbindelse med beregningen af den forkalkulerede disponible lagerbeholdning.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Kør jobbet **1130** (**Produkttilgængelighed**) for at synkronisere de øjebliksdata, som jobbet **Produkttilgængelighed** oprettede fra Commerce Headquarters til dine kanaldatabaser.

Når der anmodes om lagertilgængelighed fra API'erne **GetEstimatedAvailability** eller **GetEstimatedProductWarehouseAvailability**, køres der en beregning for at forsøge at få det bedst mulige estimat over produktets lageret. Beregningen refererer til alle kundeordrer, der findes i kanaldatabasen, men som ikke var medtaget i de øjebliksdata, som 1130-jobbet angav. Denne logik udføres ved at spore den seneste behandlede lagertransaktion fra Commerce Headquarters og sammenligne den med transaktionerne i kanaldatabasen. Det giver en basislinje for beregningslogikken for kanalsiden, så de ekstra lagerbevægelser, der forekom for kundeordresalgstransaktioner i e-Commerce-kanaldatabasen, kan medtages i den estimerede lagerværdi, som API 'et tilvejebringer.

I beregningslogikken for kanalsiden returneres en estimeret værdi for den fysiske tilgængelighed og en samlet tilgængelighedsværdi for det anmodede produkt og lagersted. Værdierne kan vises på dit e-Commerce-websted, hvis du ønsker det, eller de kan bruges til at udløse en anden forretningslogik på dit e-Commerce-websted. Du kan f.eks. vise en "uden for lager"-meddelelse i stedet for det faktiske disponible antal, som API'et har videregivet.

Den beregningslogik, som API'erne for e-Commerce-kanalsiden anvender i den forkalkulerede lagerværdi, kan kun evaluere lageret ud fra de kundeordrer, der er oprettet i kanaldatabasen, men som endnu ikke er blevet synkroniseret og bogført i Commerce Headquarters. Hvis kanaldatabasen også indeholder transaktionsdata til cash-and-carry-salg for butiksspecifikke lagersteder, indregnes cash-and-carry-salgene ikke i kanalsiden for e-Commerce-beregningen for de pågældende lagersteder.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Konfigurer handlingen lagersøgning i POS-kanalen

I Retail version 10.0.9 og tidligere har handlingen **Lagersøgning** fra POS brugt et realtids servicekald til Commerce Headquarters til at hente lageroplysninger om det valgte produkt for både brugerens aktuelle butik og eventuelle andre butikker, der er konfigureret i opfyldelsesgruppen, som en del af kanalkonfigurationen for butikken. I Commerce version 10.0.10 og nyere kan du deaktivere realtids servicekald til Commerce Headquarters. Du kan i stedet bruge beregningen på kanalsiden på Commerce-serveren til at bestemme det disponible lager, der skal være fysisk tilgængeligt for butikken og de andre placeringer, der er defineret i opfyldelsesgruppen. Denne kanalberegnede lagerkonfiguration er også nyttig for placeringer, hvor der er upålidelig forbindelse til internettet, da du ikke behøver at være online for at hente lagersøgninger fra Commerce Headquarters.

Når kanalsideberegningen er korrekt konfigureret og administreret, kan det give et mere pålideligt estimat over det aktuelle butikslager, fordi det bruger de transaktionsdata, der findes i Commerce-kanaldatabasen, men som Commerce Headquarters måske endnu ikke indeholder oplysninger om. Hvis du f.eks. bruger det eksisterende real-time servicekald til at foretage lagersøgninger i POS, har Commerce Headquarters sandsynligvis ikke nogen oplysninger om et cash-and-carry-salg af et produkt, som netop er foretaget. Derfor vil den disponible lagerværdi, som Commerce Headquarters returnerer for det pågældende produkt, formentlig overstige butikkens faktiske disponible lager med én enhed. Men hvis du bruger kanalsideberegningen, kan cash-and-carry-salg medtages i beregningen og trækkes fra den disponible værdi, der vises. Selvom de værdier, som både kanalsideberegninger og realtids servicekald tilvejebringer, blot er estimater af det disponible lager, er det meget mere sandsynligt, at den værdi, som kanalsideberegningen giver, er et nøjagtigt billede af den aktuelle butik.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Introduktion til beregnet lagertilgængelighed på en POS-kanalside

Hvis du vil bruge beregningslogikken for kanalsiden og deaktivere realtidstjenesteopkald for lageropslag fra POS-programmet, skal du først aktivere funktionen **Beregning af optimeret produkttilgængelighed** via arbejdsområdet **Funktionsstyring** i Commerce Headquarters. Ud over at aktivere funktionen skal du foretage ændringer af **funktionalitetsprofilen**.

Benyt følgende fremgangsmåde for at ændre **funktionalitetsprofilen**:

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**.
1. Vælg en funktionalitetsprofil.
1. I oversigtspanelet **Funktioner** i sektionen **Beregning af disponibelt lager** skal du ændre værdien i feltet **Metode til beregning af disponibelt lager** fra **Realtidstjeneste** til **Kanal**. Alle funktionalitetsprofiler anvender som standard realtidstjenestekald. Du skal derfor ændre værdien i dette felt, hvis du vil bruge kanalsidens beregningslogik. Alle de detailbutikker, der er kædet sammen med den valgte funktionalitetsprofil, påvirkes af ændringen.

Du skal derefter synkronisere ændringerne af kanalen ved hjælp af processen for distributionsplanlægning ved at udføre følgende trin:

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Kør jobbet **1070** (**Kanalkonfiguration**).

Når konfigurationen er fuldført, bruger de oplysninger, der er til rådighed for tilgængeligheden på det fysiske lager, ikke længere et realtids servicekald, når en bruger i POS-programmer anvender handlingen **Lagersøgning** (standard- og matrixvisninger). I stedet beregnes data om det fysisk disponible lager for den aktuelle butik og alle butikker i opfyldelsesgruppen på grundlag af det sidst kendte øjebliksbillede, der blev leveret til kanaldatabasen fra Commerce Headquarters. Værdien i øjebliksbilledet bestemmes endvidere af kanalsideberegningen for at justere den fysisk tilgængelighedsværdi og er baseret på de yderligere salgs- eller returneringstransaktioner, der er foretaget for det valgte produkt i kanaldatabasen, og som ikke var medtaget i det sidste synkroniserede øjebliksbillede fra 1130-jobbet. Hvis kanaldatabasen ikke indeholder transaktionsdata for nogle af lagerstederne eller butikkerne i opfyldelsesgruppen, indeholder den ikke yderligere transaktioner, som kan tages i betragtning i forbindelse med en genberegning af værdien. Det bedste estimat over det disponible lager, der kan vises for de pågældende lagersteder eller butikker, er derfor data fra det sidst kendte øjebliksbillede af Commerce Headquarters.

POS' skærmbillederne **Opfyldelse af ordre** bruger også kanalsideberegningen til at vise det disponible lager for varer, når en ordreopfyldelseslinje vælges, og en bruger får vist panelet **Detaljer** for den valgte vare.

## <a name="optimize-your-inventory-data"></a>Optimer lagerdataene

For at sikre det bedst mulige estimat over lageret, er det vigtigt, at du bruger følgende Commerce-batchjob og kører dem ofte:

- **P-job** – P-jobbet findes på siden **Distributionsplaner** og bør køres ofte. Dette job overfører e-Commerce-ordrer, asynkrone kundeordrer, som er oprettet af POS, samt cash-and-carry-ordrer, som POS har oprettet på baggrund af kanaldatabaserne, til Commerce Headquarters, så de kan behandles yderligere. Indtil disse data er synkroniseret fra kanalen til Commerce Headquarters, har Commerce Headquarters ingen oplysninger om lagerreguleringer af produkter på de lagersteder, der er resultatet af disse transaktioner.
- **Synkroniser ordrer** – Dette job behandler de rå transaktionsdata i Commerce Headquarters, som P-jobbet tilvejebringer, og konverterer e-Commerce-transaktioner og asynkrone kundeordretransaktioner til salgsordrer i Commerce Headquarters. Der oprettes ingen lagertransaktioner, før dette job er blevet behandlet, og der er blevet oprettet salgsordrer. Det disponible lager i Commerce Headquarters vil derfor ikke tage højde for transaktionerne.
- **Beregn transaktionsopgørelser i batch** – For så vidt angår cash-and-carry-transaktioner, der oprettes i butikken, sikrer den sivende feedbaseret bogføringsproces, at det lager, der er relateret til salget, opdateres effektivt. Hvis du vil opnå den mest effektive behandling af lagertransaktioner for cash-and-carry-ordrer, skal du sikre dig, at du konfigurerer dit system til at anvende [sivende feedbaseret bogføring](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Bogfør transaktionsopgørelser i batch** – Dette job er også påkrævet ved sivende feedbaseret bogføring. Den følger jobbet **Beregning af transaktionsopgørelser i batch**. Dette job bogfører systematisk de beregnede opgørelser, så der oprettes salgsordrer for cash-and-carry-salg i Commerce Headquarters, og Commerce Headquarters mere nøjagtigt kan afspejle butikkens lagerbeholdning.
- **Produkttilgængelighed** – Dette job opretter øjebliksbilledet af lageret fra Commerce Headquarters.
- **1130 (Produkttilgængelighed)** – Dette job kan findes på siden **Distributionsplaner** og bør køres umiddelbart efter jobbet **Produkttilgængelighed**. Dette job viderefører øjebliksdataene for lageret fra Commerce Headquarters til kanaldatabaserne.

Det anbefales, at du ikke kører disse batchjob for ofte (med få minutters mellemrum). Hyppige kørsler vil overbelaste Commerce Headquarters (hovedkontor) og kan påvirke ydeevnen. Generelt er det en god ide at køre produkttilgængeligheden og 1130 job hver time, planlægge P-job, synkronisere ordrer og udføre sivende feedbaseret bogføring med samme eller højere frekvens.

> [!NOTE]
> Af hensyn til ydeevnen bruger beregningen en cache til at angive, om der er forløbet nok tid til at kunne begrunde at køre beregningslogikken igen, når der anvendes kanalsideberegninger til at beregne lagertilgængelighed til at foretage en anmodning om varetilgængelighed ved hjælp af beregninger af e-Commerce-API'erne eller den nye POS-kanalsidelagerlogik. Standardcachen er angivet til 60 sekunder. Du har f.eks. slået kanalsideberegningen til for din butik og har fået vist det disponible lager for et produkt på siden **Lagersøgning**. Hvis der derefter sælges en enhed af produktet, vil siden **Lagersøgning** ikke vise det reducerede lager, før cachen er blevet ryddet. Når brugere har bogført transaktioner i POS, bør de vente 60 sekunder, før de bekræfter, at det disponible lager er blevet reduceret.

Hvis dit forretningsscenarie kræver en mindre cacheperiode, skal du kontakte produktsupportmedarbejderen for at få hjælp.
