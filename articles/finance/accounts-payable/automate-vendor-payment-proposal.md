---
title: Automatisere kreditorbetalingsforslag
description: I dette emne forklares det, hvordan organisationer, der betaler kreditorer i en tilbagevendende tidsplan, kan automatisere processen med at generere kreditorbetalingsforslag.
author: kweekley
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 63f2d3dc55799efefaedb10134edb219fa8588e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003572"
---
# <a name="automate-vendor-payment-proposals"></a>Automatisere kreditorbetalingsforslag

[!include [banner](../includes/banner.md)]

Organisationer, der betaler kreditorer i en tilbagevendende tidsplan, kan nu automatisere processen med at generere kreditorbetalingsforslag. Automatisering af kreditorbetalingsforslag definerer følgende oplysninger:

- Når der køres betalingsforslag
- Hvilke kriterier bruges til at vælge, hvilke fakturaer der skal betales
- Hvilken kreditorbetalingskladde de resulterende betalinger gemmes i

Automatiseringer af betalingsforslag bogfører ikke automatisk betalingerne. Du kan derfor fortsætte med at bruge validerings- og arbejdsgangsprocesser, som du i øjeblikket bruger til at godkende de betalinger, der oprettes.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Definere forekomsten af forslag til kreditorbetalinger

Automatiseringer af kreditorbetalingsforslag bruger automatiseringsstrukturen Proces. Forskellige forretningsprocesser bruger denne struktur til at definere gentagelsen af en valgt proces. I forbindelse med kreditorbetalingsforslag kan der opnås adgang til automatiseringen i forbindelse med **Kreditor \> Betalingsopsætning \> Procesautomatisering**.

Du skal først bruge automatiseringsindstillinge **Opret ny proces** og vælge **Kreditorbetalingsforslag**. En guide fører dig derefter igennem processen for opsætning af kreditorbetalingsforslaget.

## <a name="general-page"></a>Siden Generelt

På siden **Generelt** i guiden skal du angive navnet på det kreditorlbetalingsforslag, som du opretter. Hvis du f.eks. betaler alle indenlandske kreditorer med check mandag, skal du angive et beskrivende navn, f.eks. **Indenlandsk\_Check**. Det navn, du angiver, vises i den ugentlige visning af procesautomatiseringen i arbejdsområdet **Kreditorbetalinger**.

Derefter skal du definere ejeren af den betalingskladde, der er oprettet. Ejeren er normalt betalingsmedarbejderen for kreditorer (AP), der er ansvarlig for betalingskladden, når den er oprettet.

De resterende indstillinger på siden er generiske og bruges til at definere forekomstmønsteret for denne version af kreditorbetalingsforslaget. Hvis en forekomst f.eks. er til kontrol af betalinger mandag, kan du definere den, så den kører en gang om ugen, og du kan vælge mandag som dag i ugen, hvor den skal køres. Du kan også angive et tidspunkt for tidlig planlægning, f.eks. kl. 2, så procesautomatiseringen er fuldført før starten på næste arbejdsdag.

Det er vigtigt, at du forstår, at du bruger guiden til at definere, hvornår kreditorbetalingsforslaget skal behandles. Du definerer ikke, hvornår kreditorbetalingerne genereres, udskrives og bogføres. I den ugentlige visning vises procesautomatiseringen af kreditorbetalingsforslag de dage, der er valgt i forekomstmønsteret.

Yderligere oplysninger om de andre felter på siden **Generelt** finder du i dokumentationen til procesautomatisering.

## <a name="vendor-payment-proposal-page"></a>Siden Kreditorbetalingsforslag

Den næste side i guiden er siden **Kreditorbetalingsforslag**. Den bruges til at definere kriterierne for valg af de kreditorfakturaer, der skal betales. Generelt findes de samme indstillinger i betalingsforslaget i kreditorbetalingskladden. Der er dog nogle få undtagelser. Alle datoerne på denne side skal f.eks. defineres som relative datoer, fordi datoen for betalingsforslaget ændres, hver gang forslaget køres.

### <a name="journal-name"></a>Kladdenavn

I feltet **Kladdenavn** defineres det kladdenavn, som kreditorbetalingerne er oprettet i. Resultaterne af automatiseringen af kreditorbetalingsforslagene vil oprette betalinger i den definerede kladde, men kladden bogføres ikke.

### <a name="from-date-and-to-date"></a>"Fra" dato og "til" dato

I stedet for at definere en "fra"-dato og en "til"-dato for at vælge fakturaer på basis af forfaldsdatoen eller kasserabatdatoen skal du bruge indstillingen **Definer kriterier for til-dato** og feltet **Antal dage for regulering af Til-dato** for at definere "Til"-datoen. Der er intet koncept for en "fra"-dato i automatiseringen af betalingsforslag.

Som standard er indstillingen **Definer kriterier for til-dato** angivet til **Nej**. Hvis du bruger denne standardværdi, vil processen vælge alle fakturaer til betaling, når processen køres, da der ikke er defineret en "til"-dato.

Hvis du angiver indstillingen **Definer kriterierne for til-dato** til **Ja** skal du bruge feltet **Antal dage for regulering af Til-dato** til at definere den dato, hvor fakturaer vælges, som det angivne antal dage før eller efter den dato, hvor processen køres. Tallet kan være positivt, negativt eller 0 (nul). Derefter betaler systemet fakturaer, hvor forfaldsdatoerne eller kasserabatdatoerne er det angivne antal dage før eller efter den dato, hvor processen køres. For alle fakturaer, der forfalder på eller før fredag, opretter betalingsserien f.eks. betalinger til alle kreditorer pr. check om onsdagen. I dette tilfælde skal du angive feltet **Antal dage for regulering af Til-dato** til **2**. Når forekomsten af betalingsforslaget afbrydes om onsdag, den 25. marts, vil alle fakturaer, der har en forfaldsdato eller kasserabatdato på eller før den 27, blive valgt til betaling.

### <a name="minimum-payment-date"></a>Dato for minimumsbetaling

Datoen for minimumsbetaling bliver den tidligste dato, der blev brugt, da betalingerne blev oprettet. Du skal først angive indstillingen **Definer kriterier for datoen for minimumstaling** til **Ja**. Denne indstilling giver dig mulighed for at bruge funktionen dato for minimumsbetaling. Hvis denne indstilling angives til **Ja**, skal du bruge feltet **Antal dage for regulering af datoen for minimumsbetaling** for at definere datoen for minimumsbetaling som et bestemt antal dage før eller efter datoen, hvor processen køres. Tallet kan være positivt, negativt eller 0 (nul). Betalingsserien genererer f.eks. betalinger onsdag for at medtage alle betalinger, der har den foregående mandag som minimumsbetalingsdato. I dette tilfælde skal du angive feltet **Antal dage for regulering af datoen for minimumsbetaling** til **-2**.

Her er et eksempel, der viser, hvordan felterne for "til"-dato og minimumsbetalingsdatoen fungerer sammen. Automatiseringen af betalingsforslag er konfigureret til at køre onsdag. Feltet **Antal dage for regulering af Til-dato** angives til **1** for at definere "til"-datoen på baggrund af forfaldsdatoen. Feltet **Antal dage for regulering af datoen for minimumsbetaling** er angivet til **-2**. Hvis den automatiske betalingsproces starter onsdag, d. 25. marts, vil alle fakturaer, der forfalder på eller før den 26. marts, blive medtaget i betalingsforslaget. Der genereres betalingsforslag på følgende måde:

- Alle fakturaer, der forfalder på eller før 23. marts, vil have betalingsdato den 23. marts.
- Fakturaer, der forfalder den 24. marts, vil have betalingsdato den 24. marts.
- Fakturaer, der forfalder den 25. marts, vil have betalingsdato den 25. marts.
- Fakturaer, der forfalder den 26. marts, vil have betalingsdato den 26. marts.

### <a name="summarized-payment-date"></a>Opsummeret betalingsdato

Den opsummerede betalingsdato bruges kun, når feltet **Periode** er indstillet til **Total** for betalingsmetoden for fakturaerne. Hvis feltet **Periode** er angivet til **Total** for dine betalingsmåder, skal du angive indstillingen **Definer kriterier for opsummeret betalingsdato** til **Ja**. Hvis denne indstilling angives til **Ja**, skal du bruge feltet **Antal dage for regulering af den opsummerede betalingsdato** for at definere den opsummerede betalingsdato som det specificerede antal dage før eller efter datoen, hvor processen køres. Tallet kan være positivt, negativt eller 0 (nul). F.eks. genererer serien betalinger onsdag, og firmaet vil oprette en opsummeret betaling til onsdag. I dette tilfælde skal du angive feltet **Antal dage for regulering af den opsummerede betalingdato** til **0**.

### <a name="records-to-include"></a>Poster, der skal indgå

Filterindstillingerne kan stadig defineres for betalingsforslaget. Hvis der er defineret et filter, vises filterkriterierne ikke på siden i guiden. De kan dog ses ved at genåbne filteret.

De resterende felter for forslaget fungerer på samme måde, som de virker for betalingsforslaget i kreditorbetalingskladden. Du kan finde flere oplysninger om de andre felter under [Oprette kreditorbetalinger ved hjælp af betalingsforslag](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Nogle lande-/områdespecifikke felter og visse felter for den offentlige sektor er endnu ikke tilgængelige i automatiseringerne af kreditorbetalingsforslag.

Det anbefales, at du vurderer, om automatiseringen vil være en fordel for din organisation, baseret på dine behov.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Få vist resultaterne af automatiseringen af et kreditorbetalingsforslag

Når automatiseringsserien for kreditorbetalingsforslag er oprettet, vises hændelserne for hver betaling i en ugentlig visning af automatiseringsprocesserne. I forbindelse med kreditorbetalinger er den ugentlige visning af procesautomatiseringer føjet til arbejdsområdet for **kreditorbetalinger** og siden **Procesautomatisering**.

[![Ugentlig visning af procesautomatiseringer i arbejdsområdet kreditorbetalinger](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

Den ugentlige visning af procesautomatiseringer i arbejdsområdet **Kreditorbetalinger** viser kun automatisering af kreditorbetalingsforslag. Den viser alle forekomster af betalinger for den aktuelle uge for alle juridiske enheder, som den bruger, der er logget på, har sikkerhedsrettigheder til. Hvis f.eks. medarbejderen for kreditorbetalinger er ansvarlig for betalinger i USMF- og USSI-virksomhederne, vil de se forekomsterne af automatisering af kreditorbetalingsforslag for disse to virksomheder, men ikke for andre virksomheder.

[![Ugentlig visning af procesautomatiseringer i USMF- og USSI-virksomheder](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Hver forekomst viser den virksomhed, som betalingskladden blev eller vil blive oprettet i. Hvis betalinger oprettes ved hjælp af centraliserede betalinger, vil den virksomhed, der vises, være den virksomhed, som der oprettes betalinger i. Denne forekomst viser ikke nødvendigvis, hvilke virksomheders fakturaer der vil blive betalt.

Navnet på hver forekomst vises også som en hjælp til at identificere betalingsforslaget.

Desuden vises status for hver forekomst. Følgende statusangivelser bruges:

- **Planlagt** – Betalingsforslaget er planlagt, men er endnu ikke kørt.
- **Fejl** – Betalingsforslaget er blevet kørt, men der opstod en fejl. Du kan få vist fejlene ved at vælge knappen **Vis resultater**.
- **Fuldført** – Betalingsforslaget er blevet kørt. Du kan få vist betalingerne ved at vælge linket **Vis betalinger**. Dette link åbner den betalingskladde, der blev oprettet af denne forekomst.

Når betalingerne er oprettet, kan du få vist betalingsbeløbene i kladden. Beløbene vises i transaktionsvalutaerne. Hvis betalingskladden f. eks. indeholder betalinger i både amerikanske dollar og canadiske dollar, vises de samlede betalinger for hver valuta. 

Betalingskladden kan slettes, når den er oprettet via automatisering af processen. Hvis en betaling er slettet fuldstændigt, finder følgende hændelser sted:

- Status for procesautomatiseringen for ugen forbliver **Fuldført**.
- Processen fjerner de samlede betalinger, og linket **Vis betalinger** erstattes med knappen **Vis resultater**.
- Når du får vist resultaterne, modtager du en meddelelse, der bekræftet, at den oprindelige kladde er slettet.

Når en betaling slettes, åbnes fakturaerne igen for betaling. Der kan derefter oprettes en ny forekomst for at betale fakturaerne igen.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Redigere en automatisering af kreditorbetalingsforslag

Via automatiseringsstrukturen Procews kan du redigere betalingen, serien og de forekomster, der er oprettet for betalingsforslaget. Serien kan redigeres enten fra siden **Procesautomatisering** eller i den ugentlige visning af procesautomatiseringer. Hvis kreditorchefen f.eks. beslutter at generere alle checds til indenlandske leverandører onsdag i stedet for mandag, kan de finde en forekomst i den ugentlige visning og vælge **Vis/rediger – serie**. Hvis du redigerer en serie, beder systemet dig om at angive, om ændringen skal foretages i alle eksisterende forekomster eller kun i nye forekomster. Historiske forekomster, der allerede har statussen **Udført**, eller som er afsluttet i en **fejl**-status, ændres ikke.

Du kan også tilføje en ny forekomst eller ændre en eksisterende forekomst. Den næste forekomst af betalingsforslag er f.eks. planlagt til at køre onsdag den 1. januar, men denne dato er en helligdag. Serien kan ændre forekomsterne fra enten den ugentlige visning af procesautomatiseringer eller siden **Procesautomatisering**. Der åbnes en side, som viser oplysninger om tidsplan og kriterier for betalingsforslag. Her kan du redigere den planlagte tid og dato. Du kan også redigere kriterierne for betalingsforslag, hvis der kræves ændringer. Hvis du f.eks. ændrer den planlagte dato for betaling fra 1. januar til 2. januar, kan du også ændre de tilhørende datoer for "til"-datoen.

Du kan også deaktivere en forekomst eller en serie. Hvis du vil deaktivere en forekomst og suspendere behandlingen af den, skal du vælge den i den ugentlige visning af procesautomatiseringer og derefter vælge **Deaktiver**. Du kan deaktivere en serie på siden **procesautomatisering**.

## <a name="security-for-payment-proposal-automations"></a>Sikkerhed for automatisering af betalingsforslag

Følgende opgaver og rettigheder er blevet tilføjet for automatiseringer af kreditorbetalingsforslag. Disse opgaver og rettigheder er standardsikkerhedsindstillingerne, men de kan ændres ud fra organisationens behov. Hvis det f.eks. ikke kun er kreditorchefen, men også medarbejderen for kreditorbetalinger der kan redigere og oprette tidsplanforekomslter, skal du knytte pligten til at **opretholde tidsplanforekomster** til personen i rollen som medarbejder med ansvar for kreditorbetalinger.

| Programadgangsrettighed                              | Rolle                                                                       | Rettigheder |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Opretholde tidsplansserie          | Kreditorchef                                                   | Denne pligt giver ret til at oprette og opretholde automatiseringsserien for betalingsforslag og forekomster via følgende rettigheder:<ul><li>Opretholde tidsplanforekomster</li><li>Opretholde tidsplansserie</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Få vist den ugentlige visning af forekomster</li></ul> |
| Forespørgsel om tidsplanforekomster | Medearbejder for kreditorbetalinger, medarbejder for centraliseret kreditorbetaling | Denne pligt giver ret til at se forekomsterne af automatisering af betalingsforslag i kraft af følgende rettigheder:<ul><li>Få vist tidsplanforekomster</li><li>Få vist den ugentlige visning af forekomster</li></ul> |
| Forespørge om tidsplansserier      | None                                                                       | Denne pligt giver ret til at se indstillingerne for serier og forekomster i kraft af følgende rettigheder:<ul><li>Få vist tidsplanforekomster</li><li>Få vist listesiden med forekomster</li><li>Få vist den ugentlige visning af forekomster</li></ul>|
| Opretholde tidsplanforekomster     | None                                                                       | Denne pligt giver ret til at oprette og opretholde en forekomst i kraft af følgende rettigheder:<ul><li>Opretholde tidsplanforekomster</li><li>Få vist den ugentlige visning af forekomster</li></ul> |
