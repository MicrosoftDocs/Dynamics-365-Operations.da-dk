---
title: Automatiske opdateringer af forsendelser
description: Dette emne indeholder en oversigt over funktioner, der leverer automatiske opdateringer til forsendelser.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e42e7f19311adee7cc48f0ad0b59a4d0d54df9aa
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773537"
---
# <a name="shipment-auto-updates"></a>Automatiske opdateringer af forsendelser

[!include [banner](../includes/banner.md)]

Funktionen til automatisk opdatering af forsendelser opdaterer automatisk mængder (både stigninger og reduktioner) på en lastlinje, der er knyttet til en forsendelse, efter at lasten er frigivet til et lagersted. Denne funktionalitet forbliver slået til, indtil lastlinjen på forsendelsen eller lasten er behandlet på en bølge. Når den bruges, kan ordreopdateringer automatisk bevæge sig frem til lagerstedet uden at kræve manuel indgriben, før der oprettes lagerstedsarbejde.

Når funktionen til automatisk opdatering af forsendelser ikke bruges, er det kun antallet, der reduceres, indtil der oprettes lagerstedsarbejde. Brugere skal opdatere eller slette linjer manuelt, og de skal derefter genfrigive linjer, hvis ordreantallet øges, eller der tilføjes nye ordrelinjer. Ved at bruge funktionen til automatisk opdatering af forsendelser kan virksomheder uden problemer foretage opdateringer af lagerstedet uden at skulle bekymre sig om, at relaterede forsendelser og laster ikke afspejler opdateringer af ordrelinjer.

Funktionaliteten til automatisk opdatering af forsendelser gælder for både salgsordrelinjer og flytteordrelinjer, og den er aktiveret for et bestemt lagersted. Virksomheder kan derfor anvende forskellige politikker til automatisk opdatering af forsendelser på lagersteder efter behov. Som standard anvendes politikken for automatisk opdatering af forsendelser for reduktioner af antal for alle lagersteder, der bruger lokationsstyringsprocesser. Når denne standardpolitikindstilling bruges, er det kun antallet, der reduceres for en forsendelse og en last, indtil der oprettes lagerstedsarbejde. Denne funktionsmåde ligner den funktionsmåde, der blev brugt, før funktionen til automatisk opdatering af forsendelse blev introduceret.

## <a name="main-elements-of-the-functionality"></a>Hovedelementer i funktionaliteten

Funktionen til automatisk opdatering af forsendelse afhænger primært af forsendelsesstatussen for at bestemme, om antallet på en lastlinje skal ændres, når der foretages en ændring på en salgsordrelinje eller flytteordrelinje. Den baseres også primært på forsendelsens status for at bestemme, hvornår der automatisk skal føjes en ny lastlinje til en eksisterende last. Når forsendelsesstatussen er **I bølge** eller højere, sker der ingen automatisk opdatering.

Bølgestatus tages også i betragtning ved automatiske opdateringer. Når bølgen, der er relateret til lastlinjen har statussen **På hold**, **Udfører**, **Frigivet**, **Plukket** eller **Afsendt**, vises der følgende fejlmeddelelse, hvis en bruger forsøger at reducere antallet på en lastlinje (via en reduktion af antal på sagsordrelinjen eller flytteordrelinje): "Reservationer kan ikke fjernes, fordi der er oprettet arbejde, som er afhængigt af reservationerne". Hvis bølgen har en af de tidligere nævnte bølgestatusser, og en bruger forsøger indirekte at øge lastlinjens antal ved at reducere antallet på salgsordrelinjen eller flytteordrelinjen, vil antallet lastlinjen ikke automatisk blive øget. I dette tilfælde skal lastlinjen opdateres manuelt.

## <a name="scenarios"></a>Scenarier

Funktionen til automatisk opdatering af forsendelse understøtter fire scenarier: tilføjelse af en ny ordrelinje, forøgelse af antallet på en ordrelinje, reduktion af antallet på en ordrelinje og fjernelse af en ordrelinje.

- **Tilføj en ny ordrelinje** – Når feltet **Opdater forsendelse automatisk** på oversigtspanelet **Lagersted** på siden **Lagersteder** (**Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**) er indstillet til **Altid**, opdateres den eksisterende last ikke, hvis der findes en forsendelse for ordren, og der føjes en ny ordrelinje til en salgsordre eller flytteordre, når der allerede er oprettet en last for salgsordren. Der oprettes en ny lastlinje, der ikke har nogen reference til den eksisterende last, og som knyttes til den eksisterende forsendelse. Den nye linje føjes til lasten og frigives.
- **Forøg antallet på en ordrelinje** – Når feltet **Opdater forsendelse automatisk** er indstillet til **Altid**, øges lastlinjen med det samme antal som ordrelinjen, hvis der findes en forsendelse for ordren, og antallet på en eksisterende salgsordrelinje eller flytteordrelinje øges, efter der er oprettet en last for salgsordren. Hvis lasten frigives, men der ikke er oprettet noget arbejde, øges lastlinjen med det samme antal som ordrelinjen.
- **Reducer antallet på en ordrelinje** – Når feltet **Opdater forsendelse automatisk** er indstillet til **Altid** eller **Ved reduceret antal**, opdateres antallet på den tilknyttede lastlinje til at stemme overens, hvis der findes en forsendelse for ordren, og antallet på en eksisterende salgsordrelinje eller flytteordrelinje reduceres, efter der er oprettet en last for salgsordren, medmindre antallet på denne lastlinje allerede er lig med eller mindre end det nye antal på ordrelinjen. Hvis det er tilfældet, påvirkes lastlinjen ikke. Hvis lasten er frigivet, men der ikke er oprettet noget arbejde, opdateres antallet på den tilknyttede linje til at stemme overens, medmindre antallet på lastlinjen allerede er lig med eller er mindre end det nye antal på ordrelinjen. Hvis det er tilfældet, påvirkes lastlinjen.
- **Fjern en ordrelinje** – Når feltet **Opdater forsendelse automatisk** er indstillet til **Altid** eller **Ved reduceret antal**, vises der en fejlmeddelelse, hvis brugeren forsøger at fjerne en ordrelinje, som der findes lastlinje for.

## <a name="example-scenario"></a>Eksempelscenario

I dette scenario skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Aktiver funktionen til automatisk opdatering af forsendelse

Følg disse trin for at aktivere funktionen til automatisk opdatering af forsendelse.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
2. Vælg lagersted **24**.
3. I oversigtspanelet **Lagersted** i feltet **Opdater forsendelse automatisk** skal du ændre værdien fra **Ved reduceret antal** til **Altid**.

Når du har ændret værdien til **Altid**, vil eventuelle stigninger eller reduktioner i antallene på salgsordrelinjer og flytteordrelinjer samt eventuelle tilføjelser af nye linjer blive afspejlet i forsendelser og laster for det valgte lagersted, under forudsætning af tidligere nævnte opdateringsbegrænsninger.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Rediger bølgeskabelonen, så lastlinjer ikke behandles automatisk

Udfør følgende trin for at konfigurere bølgeskabelonen, så den ikke automatisk behandler lastlinjer.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
2. Vælg bølgeskabelonen **24 Standard for forsendelse**.
3. Vælg **Rediger**.
4. I oversigtspanelet **Generelt** skal du angive indstillingen **Automatiser bølgeoprettelse** til **Ja**, og du skal sørge for, at alle andre indstillinger er indstillet til **Nej**.

Det er vigtigt, at der ikke automatisk oprettes og frigives arbejde som en del af bølgeoprettelsesprocessen. Når du har oprettet arbejdet, der er relateret til den lastlinje, der er oprettet for salgsordrelinjen, opdateres lastlinjen ikke længere automatisk, hvis antallet på salgsordrelinjen ændres.

### <a name="create-a-sales-order"></a>Oprette en salgsordre

Følg disse trin for at oprette en salgsordre.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
2. Vælg kunde **US-003**.
3. Opret en linje for varenummer **A0001**.
4. Angiv et antal på **10**. (Kontroller, at du bruger lagersted **24**).
5. Vælg **Gem**.
6. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden. Der oprettes en forsendelse og en bølge.

Da du har ændret bølgeskabelonen i den foregående procedure, oprettes der ingen last eller arbejde. Forsendelsens status er **Åben**, og bølgestatussen er **Oprettet**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Reducer antallet på en salgsordrelinje

Benyt følgende fremgangsmåde for at reducere antallet på en salgsordrelinje.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
2. Vælg den salgsordre, du netop har frigivet til lagerstedet.
3. Vælg salgsordrelinjen. I feltet **Antal** skal du ændre værdien fra **10** til **8**.
4. Vælg **Lagersted \> Forsendelsesoplysninger** på salgsordrelinjen. På siden **Forsendelses oplysninger** på oversigtspanelet **Lastlinjer** afspejler antallet ændringen på salgsordrelinjen.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Forøg antallet på en salgsordrelinje

Benyt følgende fremgangsmåde for at øge antallet på en salgsordrelinje.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
2. Vælg den salgsordre, du tidligere har frigivet til lagerstedet.
3. Ret linjeantallet fra fra **8** til **12**.
4. Vælg **Gem**.
5. Gå tilbage til siden **Alle salgsordrer**, og vælg salgsordren igen.
5. Vælg **Forsendelsesoplysninger** i gruppen **Relaterede oplysninger** under fanen **Lagersted** i handlingsruden. På siden **Forsendelses oplysninger** på oversigtspanelet **Lastlinjer** afspejler antallet ændringen på salgsordrelinjen.

Selvom antallet på lastlinjen er steget fra 8 til 12, forbliver der kun otte varer reserverede, medmindre automatisk reservation er slået til. Da det antal, der er føjet til den eksisterende forsendelse, ikke er reserveret, hvis den pågældende bølge afvikles på dette tidspunkt uden reservation, oprettes der kun arbejde for det antal, der allerede er reserveret.

> [!NOTE]
> Når antallet på en ordrelinje reduceres, vil antallet på lastlinjen ikke blive påvirket, hvis den allerede er lig med eller er mindre end det nye antal på ordrelinjen. Når antallet på en ordrelinje øges, øges lastlinjen med det samme antal som ordrelinjen. Hvis antallet på ordrelinjen er forskelligt fra antallet på lastlinjen, forbliver differencen den samme.

### <a name="add-a-sales-order-line"></a>Tilføj en salgsordrelinje

Hvis du vil tilføje en salgsordrelinje, skal du følge disse trin.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
2. Vælg den salgsordre, du tidligere har frigivet til lagerstedet.
3. Opret en linje for varenummer **A0002**.
4. Angiv **10** i feltet **Antal**. (Kontroller, at du bruger lagersted **24**). Den nye linje føjes automatisk til den eksisterende forsendelse.
5. Vælg **Gem**.
6. Gå tilbage til siden **Alle salgsordrer**, og vælg salgsordren igen.
7. Vælg **Forsendelsesoplysninger** i gruppen **Relaterede oplysninger** under fanen **Lagersted** i handlingsruden. Bemærk den anden lastlinje i oversigtspanelet **Lastlinjer** på siden **Forsendelsesoplysninger**.

Da den salgsordrelinje, du netop har føjet til den eksisterende forsendelse, ikke er reserveret, oprettes der kun arbejde for antallet på den første salgsordrelinje og den første lastlinje, hvis bølgen afvikles på dette tidspunkt.

### <a name="process-a-wave"></a>Udfør behandling af en bølge

Følg disse trin for at behandle bølgen.

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
2. Vælg den bølge, som du oprettede tidligere.
3. I handlingsruden under fanen **Bølge** i gruppen **Bølge** skal du vælge **Udfør behandling**.

Bølgen behandles, og der oprettes arbejde for de reserverede antal på lastlinjerne. Forsendelsens status opdateres fra **Åben** til **I bølge**. Efterhånden som forsendelsesstatussen opdateres til **I bølge**, påvirker eventuelle ændringer, der opstår, f.eks. reduktioner eller forøgelser i linjeantal eller tilføjelsen af nye linjer i salgsordren, ikke de eksisterende lastlinjer, der er knyttet til forsendelsen i bølge.

Hvis en forsendelse har statussen **I bølge** eller højere, vil opdateringer af antallet på en salgsordrelinje ikke blive afspejlet eller valideret mod en lastlinje, der er knyttet til forsendelsen. Ændringer i antallet på en lastlinje skal foretages direkte på lastlinjen.

Validering udføres, efter at der er oprettet arbejde for lastlinjen, og der er foretaget en reservation. En reduktion af antallet på salgsordrelinjen valideres derefter i forhold til arbejdslinjereservationen.
