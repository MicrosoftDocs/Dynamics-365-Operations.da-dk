---
title: Konfigurere ordreopfyldning for butikker
description: Dette emne giver en oversigt over, hvordan du konfigurerer butiksordreopfyldning.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 118517fe0d7208113bd361a0295ff00cacd14f3d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410986"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Konfigurere ordreopfyldning for butikker

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Overblik

Mange detailhandlere ønsker at optimere deres ordreopfyldning ved at gøre det muligt for butikker at opfylde ordrer. Ordreopfyldning på butiksniveau kan afhjælpe situationer med overfyldte lagre i en bestemt butik eller kan være nødvendigt fra et logistisk synspunkt i tilfælde, hvor en butik har ekstra kapacitet eller ligger inden for nærmere leveringsafstand i forhold til kunden. Du kan løse dette behov ved hjælp af en samlet ordreopfyldningsoperation, der er tilgængelig på salgsstedet (POS).

På opfyldningsordrer i en bestemt butik er butikkens lagersted angivet på hovedet eller linjerne i ordren.

Ordreopfyldningsoperationen på POS'et indeholder et enkelt arbejdsområde på POS'et, der kan bruges til behandling af ordrer. Dette omfatter alt fra accept af ordren til at markere den som leveret eller start af afhentning i butikken.

## <a name="set-up-the-order-fulfillment-operation"></a>Konfigurere ordreopfyldningsoperationen

Ordreopfyldning, [Handlings-id 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations) kan bruges til at få adgang til arbejdsområdet Butiksordreopfyldning på POS'et.

Følg trinnene i [Føje operationen til en knapmatrix](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) for at angive, hvilken parameter der skal bruges til aktivering af ordreopfyldning på POS. Når du har angivet ordreopfyldningsoperationerne, er **Alle ordrer** som standard markeret. Når operationen er konfigureret med denne parameter, viser den alle ordrelinjer til opfyldning i den aktuelle butik. **Ordrer, der skal afsendes**, som kan tildeles til en knap og udnyttes, når brugeren kun vil se ordrer, der skal afsendes fra butikken, er også tilgængelig. Endelig er der **Ordrer, der skal afhentes**. Når dette aktiveres på salgsstedet (POS), vises kun ordrer, der skal afhentes i butikken. De forskellige parametre kan tildeles til forskellige knapper for at give brugeren flere forskellige måder at få vist ordreopfyldningen på.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Gøre det muligt for brugere at få adgang til ordreopfyldning på POS

Ordreopfyldningsoperationen ikke har sin egen standardrettighed, men i fremtiden kan brugerne kræve rettigheden **Tillad hentning af ordre** for at aktivere operationen fra POS.

Der findes en konfigurationsindstilling på butiksniveau, som kan bruges til at bestemme, om en ordrelinje skal accepteres manuelt fra POS. Hvis denne konfigurationsindstilling ikke er indstillet, accepteres ordrelinjer som standard. Hvis denne konfigurationsindstilling er aktiveret, skal brugere på POS'et have rettigheden **Tillad accept af ordre** for at acceptere ordrer fra POS'et.

### <a name="enable-manual-order-acceptance"></a>Aktivere manuel ordreaccept

Som standard er ordrelinjer, der er tildelt til en butik, markeret som **Accepteret**. Det betyder, at det forudsættes, at de opfyldes fra den tildelte butik og ikke får yderligere tildelinger. I visse tilfælde vil detailhandlere acceptere ordrer manuelt, før de kan opfyldes. Hvis en butik er underbemandet f.eks. og ikke kan levere ordrer, accepterer en butikschef kun så mange ordrer til behandling, som han eller hun mener kan behandles på en given dag. Indtil en ordre er accepteret, kan den overdrages af administrationen til en anden butik. På denne måde udgør accept af ordren også en måde til at angive, at en ordre er blevet accepteret af butikken, og at den bliver opfyldt.

Ordrelinjer for afhentning i butikken er markeret som **Afventer** og kræver ikke accept.

Hvis du vil aktivere manuel accept af ordrelinjer, skal du gå til **Retail og Commerce** \> **Kanaler** \> **Butikker** \> **Alle butikker**. Vælg butikken, og klik på butiks-ID'et for at få vist oplysninger om butikken. Klik på **Rediger**. I oversigtspanelet **Generelt** skal du finde underoverskriften **Ordreopfyldelse** og ændre **Manuel godkendelse** fra **Nej** til **Ja**.

### <a name="enable-reject-order-line-capability"></a>Aktivere funktionen til ordrelinjeafvisning

Ordrelinjer kan også blive afvist fra POS'et. Afvisning af en ordrelinje betyder, at den ikke bliver opfyldt i den pågældende butik, og linjen sendes tilbage til omfordeling til en anden butik eller lagersted. Rettigheden til ordrelinjeafvisning gives via rettigheden **Tillad afvisning af ordre** i den POS-rettighedsgruppe, der er knyttet til medarbejderen. Når detailhandlerne afviser en linje, kan de give deres medarbejdere bemyndigelse for at angive en årsag til afvisningen. Dette kan opnås ved at bruge årsagskoder af **Årsagskodeaktivitet**-typen **Ordreopfyldning** og tildele årsagskoden til **Afvis ordrelinje** i funktionalitetsprofilen, der er tilknyttet kanalen.

> [!NOTE]
> Kun årsagskoderne af **Årsagskodeaktivitet**-typen **Ordreopfyldning** kan tildeles til handlingen **Afvis ordrelinje**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkroniser ændringerne til kanaldatabasen

Når operationen er tildelt til en knapmatrix, de korrekte tilladelser er tildelt, og kanalen er konfigureret, skal ændringerne synkroniseres til kanaldatabasen. Gør det ved at gå til **Retail og Commerce** \> **Retail og Commerce IT** \> **Distributionsplan**. Vælg tidsplanen "1090-kasseapparater" for at synkronisere knapmatrixændringerne, og klik derefter på **Kør nu**. Synkroniser derefter ændringer af rettigheder ved at vælge "1060-personale", og klik derefter på **Kør nu**. Synkroniser derefter kanalændringer ved at vælge "1070-Kanalkonfiguration", og klik på **Kør nu**. Endelig skal du synkronisere den nyoprettede årsagskode for afvisningsårsag ved at vælge "1110-Global konfiguration", og klik på **Kør nu**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Bruge ordreopfyldning på POS'et

Åbn POS'et, og vælg ordreopfyldningsoperationen. Afhængigt af konfigurationen angives enten alle linjer, ordrelinjer til afhentning eller ordrelinjer, der skal leveres.

### <a name="order-fulfillment-view"></a>Ordreopfyldelsesvisning

Ordreopfyldningsvisningen omfatter ordrelinjer til opfyldning i butikken og indeholder følgende kolonner:

- Ordrenummer
- Produktnummer
- Betegnelse
- Antal, der er bestilt.
- Ønsket leveringsdato
- Kundenavn
- Opfyldelsesstatus

Yderligere oplysninger om en bestemt ordrelinje kan ses ved at markere ordrelinjen og derefter åbne pop op-menuen, der er placeret lige under oplysningerne om den bruger/det skift, der er logget på, som vises i POS-overskriften. Denne menu indeholder to faner: én til linjedetaljer og en anden til ordreoplysninger. Fanen med linjedetaljer indeholder følgende oplysninger:

- Antal, der er bestilt.
- Antal, der endnu ikke er blevet afsendt/afhentet
- Antal, der er plukket
- Pakket antal
- Faktureret antal (allerede afhentet eller afsendt)
- Leveringsmåde
- Leveringsadresse

Pop op-menuen med oplysninger indeholder også en fane med flere oplysninger på ordreniveau, herunder:

- Kundenavn
- Debitor-id
- Ordrenummer
- Ordretotal
- Ordresaldo

Nederst i ordreopfyldningsvisningen findes en handlingsrude. Denne rude indeholder alle de handlinger, der kan udføres på en ordrelinje. Hvis en handling ikke er tilgængelig, baseret på status for en linje, er den pågældende handling ikke tilgængelig.

Som standard har ordrer status **Accepteret**. Ordrestatus kan ses som en kolonne på listen over ordrelinjer. Hvis **Manuel godkendelse** er konfigureret på kanalniveau, vises alle linjer, der skal leveres, som **Afventer** og skal godkendes, før de kan opfyldes. Ordrer til afhentning i butikken har som standard status **Afventer** og behøver ikke at blive accepteret.

### <a name="order-fulfillment-line-actions"></a>Handlinger på ordreopfyldningslinjer

- **Rediger** – Hvis en ordrestatus er ventende, den kan redigeres på POS'et. Ordrer, der er allerede er delvist plukket, pakket eller faktureret, kan ikke redigeres fra ordreopfyldningsvisningen.
- **Acceptér** – Hvis **Manuel godkendelse** er konfigureret på kanalniveau, skal linjer først godkendes, før de kan flyttes gennem ordreopfyldningsprocessen.
- **Pluk** – Indstillingen Pluk understøtter flere handlinger. Første opdaterer **Pluk** for ordrelinjen, så andre i butikken ikke forsøger at plukke den samme linje. Derefter udskriver **Udskrivning af plukliste** en plukliste for den eller de valgte linjer og opdaterer også deres status til **Pluk**. Pluklisteformater styres som en del af kvitteringsformater. Du kan finde flere oplysninger om, hvordan du konfigurerer kvitteringsformater i [Kvitteringsskabeloner og udskrivning](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Endelig **Markér som plukket** angiver, at linjen er blevet plukket. **Markér som plukket** starter tilsvarende lagertransaktioner i administrationen. Plukhandlinger kan udføres på samme tid for flere ordrelinjer på tværs af ordrer og for alle leveringsmåder.
- **Afvis** – Linjer eller delvise linjer kan afvises. Dette gør muligt at omfordele dem fra administrationen til en anden butik eller lagersted. Linjer kan kun afvises, hvis de endnu ikke er plukket eller pakket. Hvis du vil afvise en linje, der allerede er plukket eller pakket, skal plukningen eller pakningen af linjen fjernes af administrationen.
- **Pakke** – Pakkeindstillingen understøtter to handlinger: **Udskrivning af følgeseddel** udskriver en følgeseddel for de valgte linjer og **Markér som pakket** markerer linjerne som pakkede og markerer linjerne som leveret i administrationen. Kun ordrelinjer, der tilhører samme ordre og har samme leveringsmåde kan pakkes på samme tid. Følgeseddelformater styres som en del af kvitteringsformater. Du kan finde flere oplysninger om, hvordan du konfigurerer kvitteringsformater i [Kvitteringsskabeloner og udskrivning](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Send** – Afsendelseshandlingen markerer valgte linjer som **Leveret** i administrationen. Når en linje er fuldt ud leveret, vises den ikke længere i ordreopfyldningsvisningen.
- **Afhentning** – Handlingen Afhentning føjer linjerne til transaktionsvisningen for afhentning. Hvis der er andre linjer i ordren, der ikke i øjeblikket er afhentet, føjes de til transaktionsvisningen med et antal på nul. Når en linje er helt afhentet, vises den ikke længere i ordreopfyldningsvisningen.

### <a name="order-fulfillment-filtering"></a>Ordreopfyldningsfiltrering

Ordreopfyldning på POS'et omfatter filtrering, så brugerne nemt kan finde det, de har brug for. Filtre kan ændres i handlingsruden nederst på skærmbilledet **POS**. Som standard anvendes et **Leveringstype**-filter, baseret på hvordan operationen er konfigureret. Hvis operationen er konfigureret med parameteren **Alle ordrer**, anvendes dette filter ved adgang til ordreopfyldning. Det samme gælder for parametrene **Afhentning i butik** og **Afsend fra butik**. Andre filtre, der kan anvendes til ordreopfyldningsvisningen, omfatter:

- Kundenummer
- Kundenavn
- Kundens mail
- Ordrenummer
- Leveringsmåde
- Kvitteringsnummer
- Id for kanalreference
- Nummer på oprindelig butik
- Linjestatus
- Oprettet dato
- Leveringsdato
- Modtagelsesdato
