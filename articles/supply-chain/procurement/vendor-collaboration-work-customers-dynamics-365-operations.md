---
title: Kreditorsamarbejde med kunder
description: Dette emne beskriver, hvordan du kan bruge kreditorsamarbejde til at arbejde med indkøbsordrer og overvåge konsignationslager.
author: TaylorVH
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: v-savanh
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9ad7f116f979d571a5e34eee67beb7218a271522
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777588"
---
# <a name="vendor-collaboration-with-customers"></a>Kreditorsamarbejde med kunder

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du kan bruge kreditorsamarbejde til arbejde med kunder i Microsoft Dynamics 365 Supply Chain Management. Kreditorer kan udføre en række forretningsprocesser fra følgende arbejdsområder:

- **Indkøbsordrebekræftelse** – Overvåge og reagere på indkøbsordrer (IO'er).
- **Kreditorbud** – Få vist anmodninger om tilbud (tilbudsanmodninger) og reagere på dem ved at afgive bud.
- **Kreditoroplysninger** – Få vist eller opdatere kreditormasterdata.
- **Fakturering** – Arbejde med fakturaer. Dette emne dækker ikke arbejdsområdet **Fakturering**. Du kan finde flere oplysninger om dette arbejdsområde under [Arbejdsområde for kreditorsamarbejdsfakturering](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md).

Kreditorer kan også overvåge oplysninger om konsignationslager.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Arbejde med IO'er i arbejdsområdet Indkøbsordrebekræftelse

I **Indkøbsordrebekræftelse**-arbejdsområdet kan du reagere på de indkøbsordrer, der er sendt til gennemsyn. Det gør det også muligt at få vist oplysninger om indkøbsordrer, der afventer handling fra kunden, og indkøbsordrer, der er blevet bekræftet, men stadig er åbne.

Der findes tre lister i **Indkøbsordrebekræftelse**-arbejdsområdet:

- **Indkøbsordrer til gennemsyn** – Denne liste viser IO'er, der er blevet sendt til dig og afventer en reaktion fra dig. Når du har reageret, forsvinder IO'en fra listen. Hvis kunden sender dig en ny version af indkøbsordren, før du har reageret på den foregående, vises kun den nyeste version.
- **Afventer kundehandling** – På denne liste kan du se alle indkøbsordrer, du har reageret på, men som kunden endnu ikke har bekræftet. Hvis du accepterer en indkøbsordre, kan du overvåge den på denne liste, indtil status er skiftet til **Bekræftet**. Hvis du afviser en indkøbsordre eller accepterer den med ændringer, kan du overvåge den her, indtil kunden sender en ny version.
- **Åbn bekræftede indkøbsordrer** – Denne liste viser alle indkøbsordrer udstedt til din konto, der har status **Bekræftet**. Når produkter eller tjenester er fuldt modtaget mod indkøbsordren, forsvinder indkøbsordren fra listen.

Du kan bruge følgende sider til at arbejde med indkøbsordrer:

- **Indkøbsordrer til gennemsyn** – Denne side indeholder de samme oplysninger som listen **Indkøbsordrer til gennemsyn** i arbejdsområdet. Se beskrivelsen tidligere i dette emne.
- **Historik over bekræftelse af kreditor for indkøbsordre** – Denne side indeholder alle indkøbsordrer og alle versioner af indkøbsordrer, der er sendt til kreditoren. Den indeholder også alle de reaktioner, der er returneret fra kreditoren.
- **Åbn bekræftede indkøbsordrer** – Denne side indeholder de samme oplysninger som listen **Åbn bekræftede indkøbsordrer** i arbejdsområdet. Se beskrivelsen tidligere i dette emne.
- **Alle bekræftede indkøbsordrer** – Denne side indeholder alle indkøbsordrer, der er bekræftet. Indkøbsordrerne på denne side omfatter de indkøbsordrer, hvor produkter eller ydelser er modtaget. Du kan bruge denne liste til at overvåge de indkøbsordrer, du kan sende fakturaer for.

### <a name="responding-to-pos"></a>Reagere på indkøbsordrer

De indkøbsordrer, som debitoren sender dig til gennemsyn, vises i arbejdsområdet **Indkøbsordrebekræftelse** og på siden **Indkøbsordrer til gennemsyn**. Når du åbner en indkøbsordre, kan du acceptere den, afvise den eller acceptere den med ændringer. Der kan evt. være vedhæftede filer på indkøbsordren eller på de enkelte linjer. Du kan også tilknytte oplysninger til dit svar i indkøbsordrens hoved eller på de enkelte linjer. For eksempel kan du foreslå en erstatningsvare for en eller flere linjer.

Du kan se og udskrive indkøbsordren som en PDF-fil ved hjælp af **Vis/Udskriv**-indstillingen. Du kan også bruge handlingen **Vis dimensioner** til at skjule eller vise følgende dimensionskolonner: **Sted**, **Lagersted**, **Farve**, **Størrelse**, **Typografi** og **Konfiguration**. 

Hvis du bruger muligheden **Acceptér med ændringer**, kan du acceptere eller afvise individuelle linjer. Du kan også foretage følgende ændringer af linjer:

- Ændre datoer eller antal. Hvis du vil opdatere den bekræftede leveringsdato på alle linjer, skal du bruge **Opdater leveringsdato**-indstillingen i indkøbsordrens hoved.
- Opdel linjer for forskellige leveringsdatoer eller antal.
- Erstat en vare. I sektionen **Linjedetaljer** kan du angive en varebeskrivelse og varenummeret i feltet **Ekstern**.

Du kan ikke ændre prisoplysninger eller gebyrer, men du kan bruge noter til at komme med forslag til disse ændringer.

Hvis kunden sender dig en ny version af en indkøbsordre, har den et versionssuffiks, som angiver, at den er en ændret version af en tidligere sendt indkøbsordre. På siden **Historik over bekræftelse af kreditor for indkøbsordre** kan du holde styr på historikken for hver ordre.

## <a name="monitoring-consignment-inventory"></a>Overvågning af konsignationslager

Hvis du bruger konsignationslager, kan du bruge kreditorsamarbejde til at få vist oplysninger på de følgende sider:

- **Indkøbsordrer, der forbruger konsignationslager** – Indkøbsordrer for konsignationslager genereres, når kunden overtager ejerskabet af lageret. Disse konsignationsindkøbsordrer vises kun på denne side. De er ikke medtaget på siden **Alle bekræftede indkøbsordrer**.
- **Produkter, der er modtaget fra konsignationslager** – Denne side viser en liste over alle de transaktioner, hvor ejerskabet af produkter er blevet overført til den virksomhed, som forbruger af lageret. Du kan bruge disse oplysninger til at fakturere kunden.
- **Disponibelt konsignationslager** – Denne side viser det disponible konsignationslager, der ejes af din virksomhed, men som er disponibelt på kundens lagersted.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Arbejde med tilbudsanmodninger i arbejdsområdet Kreditorbud

I arbejdsområdet **Kreditorbud** kan du få vist de tilbudsanmodninger, som dit firma er blevet inviteret til at besvare. Du kan også besvare tilbudsanmodningerne. 

Arbejdsområdet viser også alle tilbudsanmodninger, du har tabt eller vundet. Hvis systemet er konfigureret til den offentlige sektor, viser arbejdsområdet de tilbudsanmodninger, der er offentligt tilgængelige.

### <a name="viewing-rfqs"></a>Visning af tilbudsanmodninger

Åbn arbejdsområdet **Kreditorbud** for at få adgang til følgende oplysninger:

- Vælg **Invitationer til nyt bud** for at se de tilbudsanmodninger, som dit firma er blevet inviteret til at besvare. Her kan du få vist en tilbudsanmodning og starte budprocessen. Du kan også se ændrede tilbudsanmodninger, der skal sendes et nyt bud for.
- Vælg **Returnerede bud** for at se de tilbudsanmodninger, kunden har returneret til dig, så du kan finde angive flere oplysninger eller opdatere buddet.
- Vælg **Igangværende bud** for at se de tilbudsanmodninger, som du eller en kontaktperson, der repræsenterer dit firma, har arbejdet på, men endnu ikke har sendt.
- Vælg **Tildelte bud** for at se, når kunden har tildelt mindst ét linjeelement i dit bud.
- Vælg **Tabte bud** for at se bud, hvor alle linjer er blevet afvist.
- Vælg linket **Tilbudsanmodning** for at se en liste over alle leverandørens invitationer til tilbudsanmodning og alle bud, der er afgivet. På siden **Tilbudsanmodning** kan du se alle de tilbudsanmodninger, som en leverandør er involveret i. Du kan søge ud fra status.
- Vælg linket **Afviste bud** for at se en liste over alle tilbudsanmodninger, hvor en leverandørs kontaktperson har afvist at byde.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Arbejde med tilbudsanmodninger, der er offentligt tilgængelige

Personer, der arbejder i den offentlige sektor, kan åbne og se udløbne tilbudsanmodninger, der er gjort tilgængelige for offentligheden.

- Vælg linket **Åbne publicerede tilbudsanmodninger** for at se en liste over åbne tilbudsanmodninger, der er tilgængelige for offentligheden. En åben tilbudsanmodning er en tilbudsanmodning, der endnu ikke er udløbet. Du kan finde udløbsdatoen og klokkeslættet i tilbudsanmodningshovedet.

    Hvis du er inviteret til at byde, kan du finde den samme tilbudsanmodning på siden **Invitationer til nyt bud**. Det kan ske, at du ønsker at byde på en tilbudsanmodning, som du ikke er inviteret til at byde på. I dette tilfælde kan du måske invitere dig selv, forudsat at kunden har aktiveret egen-invitation for tilbudsanmodningssagen.

    Du kan forbedre tilgængeligheden af linket **Åbn publicerede tilbudsanmodninger** ved at aktivere **Vis linket "Åbn publicerede tilbudsanmodninger" som en felt**-funktion. Denne funktion konverterer linket til et felt og flytter det til en fremtrædende placering, så det er nemt at finde det. (Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret.)

- Vælg linket **Lukkede publicerede tilbudsanmodninger** for at se en liste over lukkede tilbudsanmodninger, der er tilgængelige for offentligheden. En lukket tilbudsanmodning er en tilbudsanmodning, der er udløbet. Du kan finde udløbsdatoen og klokkeslættet i tilbudsanmodningshovedet.

    En lukket tilbudsanmodning viser alle kreditorbud helt ned på linjeniveau. Efterhånden som bud tildeles eller afvises, afspejles disse oplysninger i den lukkede tilbudsanmodning. Eventuelle vedhæftede filer, der indgår i et bud, er også tilgængelige.

> [!NOTE]
> Denne funktion er kun tilgængelig, hvis den offentlige sektor-konfiguration er aktiveret.

### <a name="bidding"></a>Afgivelse af bud

- Vælg **Bud** for at begynde at byde på en tilbudsanmodning.

    Når redigering er aktiveret for budfelterne i hovederne og linjerne i en tilbudsanmodning, kan du angive dit bud direkte i linjegitteret. Du skal også overveje, om der skal tilføjes eventuelle andre budoplysninger i linjedetaljerne.

    Når du begynder at arbejde på et bud, vises det i sektionen **Igangværende bud**.

    Du kan gemme et bud, når som helst før udløbsdatoen. Du kan derefter vende tilbage senere for at afslutte og afgive buddet. Når du har afgivet et bud, kan du tilbagekalde og opdatere det før udløbsdatoen.

- Vælg **Nulstil fra tilbudsanmodning** for at nulstille de data, du har angivet for et bud og vende tilbage til den oprindelige tilbudsanmodning. Du kan nulstille hovedet eller linjen.
- Vælg **Tilføj alternativ** eller **Fjern alternativ** i linjegitteret for at arbejde med alternativer.

    Nogle tilbudsanmodninger giver mulighed for alternative bud. Du kan kun angive alternative bud for linjer af typen **Kategori**, fordi bestemte varer ikke kan tilføjes som alternativer. 

- Vælg **Vedhæftet fil i tilbudsanmodning** eller **Tilbudsanmodningslinjer i vedhæftede filer** for at åbne en vedhæftet fil, som kunden har føjet til en tilbudsanmodning. Vælg **Bud i vedhæftede filer** eller **Budlinjer i vedhæftede filer** for at overføre vedhæftede filer sammen med buddet.

    Der kan være spørgeskemaer, som du skal besvare, før du kan sende et bud.

- Vælg **Afvis**, hvis du ikke vil byde. Når du har valgt **Afvis**, kan du ikke tilbagekalde handlingen og afgive et bud.

Hvis en tilbudsanmodning ændres, skal du angive et nyt bud. Du kan finde oplysninger om ændringen under fanen **Ændringer** på siden Tilbudsanmodning. Ændrede tilbudsanmodninger vises på siden **Invitationer til nyt bud**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Adgang til kreditormasterdata i arbejdsområdet Kreditoroplysninger

Som kreditor kan du få adgang til en del af de oplysninger, som kunden vedligeholder i kreditormasterposten. Derfor kan du holde oplysningerne opdateret. Når du vil opdatere oplysningerne, skal du have rollen kreditoradministrator (ekstern).

De tilgængelige oplysninger er kreditornavn, adresser, kontaktoplysninger, kontaktpersoner og deres kontaktoplysninger, id-numre, momsregistreringsnumre, indkøbskategorier, som kreditoren er godkendt til at sælge til kunden i, og oplysninger om certificeringer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]