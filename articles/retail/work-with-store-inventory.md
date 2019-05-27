---
title: Butikslagerstyring
description: I dette emne beskrives de typer af dokumenter, du kan bruge til at lagerstyring.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: efc729c83b81bd8afb806c403d52fd85b36efc9d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1523755"
---
# <a name="store-inventory-management"></a>Butikslagerstyring

[!include [banner](includes/banner.md)]

Når du arbejder med lager i Dynamics 365 for Retail og bruger POS-programmet, det er vigtigt at bemærke, at POS yder begrænset understøttelse til lagerdimensioner og visse lagervaretyper.  

POS-løsningen understøtter ikke følgende varekonfigurationer:
- Styklistevarer (undtagen pakkeprodukter, som anvender nogle komponenter af styklistestrukturen)
- Fastvægtvarer
- Batchstyrede varer

POS-programmet understøtter i øjeblikket ikke følgende sporingsdimensioner i POS:
- Batchsporingsdimension
- Ejerdimension

POS-løsningen har begrænset understøttelse af følgende dimensioner. Begrænset understøttelse angiver, at en POS evt. vil bruge standardværdien for nogle af disse dimensioner i lagerposteringer, der automatisk baseres på konfigurationen af lagersted/butiksopsætning. POS understøtter ikke dimensionerne fuldstændigt på den måde, de understøttes, hvis en salgstransaktion angives manuelt i ERP. 

- **Lagerstedslokation** – Brugerne har ikke mulighed for at administrere det modtagende lagersteds lokation for varer, der modtages på et butikslager, når butikken ikke er konfigureret til at bruge lokationsstyringsprocessen.  En standard modtagelseslokation, der er defineret på butikslagerstedet, bruges til disse varer.  Hvis lokationsstyringsprocessen er aktiveret for butikken, udløses der en begrænset support, som beder brugeren om at vælge en modtagelseslokation for hele tilgangen.  Varer, der er solgt fra butikken, bliver altid solgt fra standarddetaillokationen, som defineret i opsætningen af butikkens lagersted.   Lokationen for håndtering af returvarer kan styres via standarddefinitionen af returneringsstedet på butikslagerstedet eller baseret på returårsagskoder, som er defineret i politikken for returlokationen.
- **Id** - Id'er er kun relevante, når **Brug lokationsstyringsprocesser** er aktiveret på varen og butikkens lagersted.  Hvis lagervarer modtages på et butikslagersted, hvor lokationsstyringsprocessen er aktiveret, og den lokation, der er valgt for modtagelse af varen, er bundet til en lokationsprofil, der kræver kontrol af id'er, anvender POS-programmet systematisk et id på modtagelseslinjen.  Brugere i POS vil ikke kunne ændre eller administrere disse id-data.   Hvis det er nødvendigt med fuld styring af id'er, foreslås butikken at bruge WMS mobil-programmet eller ERP-administrationsklienten til at styre modtagelsen af disse varer.
- **Serienummer** - POS-programmet har begrænset understøttelse af et enkelt serienummer, der skal registreres på en transaktions salgslinje for ordrer, der er oprettet i POS, med serialiserede varer.  Dette serienummer bliver ikke valideret mod registrerede serienumre, der allerede findes på lageret.  Hvis der oprettes en salgsordre i callcenterkanalen, eller den opfyldes via ERP, og der er registreret flere serienumre på en enkelt salgslinje under opfyldningsprocessen i ERP, kan disse serienumre ikke anvendes eller valideres, hvis en returværdi behandles i POS for disse ordrer.
- **Lagerstatus** - For varer, der bruger lokationsstyringsprocessen og kræver en lagerstatus, kan dette statusfelt ikke angives eller ændres via POS-programmet.  Standardlagerstatussen som defineret i konfigurationen af butikkens lagersted bruges, når varer modtages på lageret.  

> [!NOTE]
> Alle organisationer skal teste varekonfigurationer via POS i udviklings- eller testmiljøer, inden de installeres til produktion. Test dine varer ved at udføre almindelige cash and carry-salgstransaktioner og oprette kundeordrer (hvis relevant) via POS med dine varer. Test skal omfatte kørsel af en fuldstændig redegørelse for bogføringsprocesser i testmiljøet og skal kontrollere, at der ikke er nogen problemer.
> Hvis varer konfigureres på en måde, der ikke understøttes af POS-programmet, uden grundige test, kan det medføre, at der opstår fejl i dine bogføringsprocesser i produktionen, og at der ikke er nogen nem måde at løse problemet på. Partner- eller kundetilpasninger til programmet kan eventuelt komme i betragtning, så disse bogføringsprocesser kan fuldføres. Hvis tilpasninger ikke er nødvendige, skal organisationen sikre, at produktkonfigurationen af dine produkter er udført på en måde, der understøttes af det POS-program/den ordreoprettelse/bogføring af opgørelsesprocessen, der bruges som standard.

## <a name="purchase-orders"></a>Indkøbsordrer

Indkøbsordrer oprettes på hovedkontoret. Hvis et detaillagersted er medtaget i indkøbsordrehovedet, kan ordren modtages i butikken ved hjælp af Modern POS (MPOS) eller Cloud POS i Microsoft Dynamics 365 for Retail via handlingen **Pluk-/tilgangs-id**. Når de antal, der er modtaget i butikken, angives i feltet **Modtag nu** i POS for indkøbsordredokumentet, kan de gemmes lokalt eller allokeres. Hvis du gemmer disse data lokalt, har det ingen indflydelse på lagerbeholdningen. Lagring skal kun udføres, hvis brugeren ikke er klar til at bogføre tilgangen til hovedkontoret og blot har brug for en metode til midlertidigt at gemme de tidligere angivne **Modtag nu**-data.  Derved gemmes Modtag nu-dataene lokalt i brugerens kanaldatabase. Når dokumentet er behandlet ved hjælp af **Bekræft**-indstillingen, sendes dataene i **Modtag nu** til hovedkontoret, og indkøbsordretilgangen bogføres. 

## <a name="transfer-orders"></a>Flytteordrer

En flytteordre kan angive, at en bestemt butik er den lokation, som varerne kan afsendes fra, eller den lokation, som lagerbeholdningen skal modtages på. Hvis POS-brugeren er afsenderlagerstedet for en flytteordre, kan vedkommende angive antal for **Afsend nu** fra POS.  De data, der angives af afsendelseslageret, kan gemmes lokalt eller allokeres.  Når de gemmes lokalt, foretages der ingen opdateringer af dokumentet for flytteordren i hovedkontoret. Lagring skal kun udføres, hvis brugeren ikke er klar til at bogføre forsendelsen til hovedkontoret og blot har brug for en metode til midlertidigt at gemme de tidligere angivne **Afsend nu**-data. Når butikken er klar til at bekræfte forsendelsen, skal du vælge indstillingen **Bekræft**. Derved bogføres forsendelsen af flytteordren i hovedkontoret, så tilgangslagerstedet nu kan modtage imod den. 

Hvis POS-brugeren er tilgangslagerstedet for en flytteordre, kan vedkommende angive antal for **Modtag nu** fra POS.  De data, der angives af tilgangslageret, kan gemmes lokalt eller allokeres. Lagring skal kun udføres, hvis brugeren ikke er klar til at bogføre tilgangen til hovedkontoret og har brug for en metode til midlertidigt at gemme de tidligere angivne **Modtag nu**-data. Derved gemmes Modtag nu-dataene lokalt i brugerens kanaldatabase. Når dokumentet er behandlet ved hjælp af **Bekræft**-indstillingen, sendes dataene i **Modtag nu** til hovedkontoret, og flytteordretilgangen bogføres. Det er vigtigt at bemærke, at den modtagende butik bliver begrænset, så det kun er muligt at modtage antal, der er lig med eller mindre end de afsendte antal. Et forsøg på at modtage antal på en flytteordre, der ikke tidligere er afsendt, vil resultere i fejl, og tilgangen bekræftes ikke i hovedkontoret.

## <a name="stock-counts"></a>Lagerstatus

Status kan enten være planlagt eller ikke-planlagt. Planlagte statusopgørelser startes i hovedkontoret, der angiver, hvilke varer der skal optælles. Hovedkontoret opretter et optællingsdokument, som kan modtages i butikken, hvor antallet af den disponible beholdning angives i MPOS eller Cloud POS. Ikke-planlagte statusoptællinger startes i en butik, og antal i den disponible lagerbeholdning opdateres i enten i MPOS eller Cloud POS. I modsætning til planlagt status har ikke-planlagt status ikke en foruddefineret liste over varer. Når en status af en af typerne er fuldført, gøres den bindende og sendes til hovedkontoret. På hovedkontoret valideres antallet og bogføres som et særskilt trin.

## <a name="inventory-lookup"></a>Lagersøgning

Det aktuelle antal disponible produkter for flere butikker og lagersteder kan ses på siden **Lagersøgning**. Udover den aktuelle disponible beholdning kan det fremtidige disponible tilsagn (DTT) vises for hver enkelt butik. Det gør du ved at vælge den butik, du vil have vist DTT for, og derefter klikke på **Vis butikkens tilgængelighed**.
