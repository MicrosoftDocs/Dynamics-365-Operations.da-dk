---
title: Konfigurere Apple Pay med Adyen i Dynamics 365 Commerce
description: I denne artikel beskrives det, hvordan du konfigurerer Apple Pay med Adyen i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 896847cee696e221b2114f7f28a0b56e73fc911b
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838223"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Konfigurere Apple Pay med Adyen i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

I denne artikel beskrives det, hvordan du konfigurerer Apple Pay med Adyen i Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Apple Pay | Kaldes også for Apple Pay-"knappen", og Apple Pay er et betalingstilbud, der understøttes via Adyen-connector. Det aktiverer kundeoplevelse og integration, der understøttes af Microsoft Dynamics 365 Apple Pay-connectoren. |
| Tegnebog | En betalingstype, der ikke omfatter de traditionelle betalingskarakteristika som f.eks. BIN-intervaller (Bank Identification Number)-området og udløbsdatoen, som bruges til at skelne mellem kredit- og debetkorttyper. |

Dynamics 365 Commerce tilbyder integration uden for feltet for Apple Pay, når Adyen- betalings-gateway-tjenesten bruges. Apple Pay er en digital betalingsmåde, der bruger en Apple Pay-forhandlerkonto, der fungerer som overensstemmelse med betalingstjenesten Adyen. Når den er konfigureret, er knappen Apple Pay tilgængelig som en betalingsmåde, der er en del af butikkers onlineordrer på betalingssiden. Knappen Apple Pay vises kun som en betalingsmåde for understøttede Apple Pay-enheder. Når brugere vælger **Apple Pay** i en understøttet browser eller enhed, bliver de afledt til at gennemføre deres betaling direkte med Apple Pay-tjenesten. De returneres derefter til onlinebutikken for at fuldføre ordren.

Dynamics 365 Payment Connector til Apple Pay-connector-referencen bruges ud over Dynamics 365 Payment Connector til Adyen til at aktivere Apple Pay og kreditkortbetalinger på et websted. Apple Pay kan også konfigureres til brug i butikker, der har Adyen-betalingsterminaler, der bruger Dynamics 365 Payment Connector for Adyen sammen med Commerce-POS. I dette tilfælde håndterer Dynamics 365 Payment Connector for Adyen tapen til Betalingsenhedstryk ved hjælp af terminalen.

## <a name="prerequisites"></a>Forudsætninger

Der kræves en Apple-forhandlerkonto for at bruge Apple Pay med Adyen i Commerce. Du kan finde flere oplysninger om, hvordan du konfigurerer Apple Pay i dit testkundeområde, i [Integration med Apple Pay Drop-in](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Du kan finde oplysninger om, hvad du skal gøre, når du er klar til at gå i gang i produktionsmiljøet, under [Going live](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Apple Pay-metoden skal også integreres med din Adyen-konto. Adyen kan hjælpe dig med at konfigurere betalingsmetoden og kan også hjælpe med at sikre, at de domæner, du vil bruge certifikatet til, er tildelt til brug med certifikatet.

Du kan aktivere udvidet kontantbetaling i Commerce headquarters ved at gå til **Workspaces \> Feature management**, og søge efter funktionen **Forbedrede understøttelser af tegnebog og betalingsforbedringer**. Vælg funktionen, og vælg derefter **Aktivér**. Når funktionen er aktiveret, skal du køre **1110**-fordelingsplanen for at gøre ændringen tilgængelig i alle kanaler.

## <a name="map-the-apple-pay-payment-method"></a>Tilknytte Apple Pay-betalingsmetoden

Apple Pay er en digital betalingsmåde. Du kan finde flere oplysninger om, hvordan du konfigurerer betalingstilknytning for Apple Pay, i [Betalingssupport til kontantbetaling](../wallets.md).

Benyt denne fremgangsmåde for at tilknytte Apple Pay-betalingsmetoden i Commerce headquarters.

1. Gå til **Detail og handel \> Konfiguration af kanal \> Betalingsmetoder \> Korttyper**.
1. Vælg **Ny** for at tilføje en linje til Apple Pay, og angiv følgende værdier:

    - **ID:** ApplePay
    - **Navn på elektronisk betaling:** Apple Pay
    - **Type:** Tegnebog
    - **Udsteder:** Apple

1. Vælg **Processortilknytning** for at åbne dialogboksen **Tilknytning af processorbetalingsmåder**. Kolonnen **Ikke-tilknyttede betalingsmåder** viser understøttede betalingsmåder for hvert tilgængeligt connector (Adyen, PayPal og Apple).
1. Tilknyt de understøttede betalingsmetoder, du vil bruge til både **Dynamics 365 Payment Connector til Adyen**-connectoren (til brug i POS) og **Dynamics 365 Payment Connector til Apple Pay**-connectoren (til onlinekanalen).
1. For hver tilknytningslinje i kolonnen **Ikke tilknyttede processorbetalingsmetoder** skal du markere den linje, der skal understøttes, og vælg **Tilføj** for at flytte dine valg til **Tilknyttede processorbetalingsmetoder**-kolonnen.
1. Vælg **OK**, og vælg derefter **Gem** på siden **Korttyper**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Konfigurere Apple Pay-certifikater til dit websted

For hvert websted skal du overføre domænesammenknytningsfilen (også kendt som Apple Pay-certifikat), som beskrevet i [dokumentationen til Adyen Apple Pay](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Du kan bruge Commerce Site Builder til at overføre domænesammenknytningsfilen til webstedets mediebibliotek.

Hvis du vil konfigurere Apple Pay-certifikatet i Site Builder, skal du følge disse trin.

1. Hent certifikatet (domænesammenknytningsfilen) fra [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Føj .txt-filtypen til domænesammenknytningsfilen.
1. I Site Builder skal du [overføre](../upload-serve-static-files.md) domænesammenknytningsfilen til webstedets mediebibliotek.
1. Gå til **URL**.
1. Vælg **Ny \> Ny URL-adresse**.
1. Vælg **Mediebiblioteksaktiv** i dialogboksen **Ny URL-adresse**.
1. Angiv URL-stien i **URL-sti** (hvis den ikke allerede er angivet). Når URL-adressen til domænets basisadresse er indtastet, skal du angive følgende påkrævede Apple-streng: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Vælg **Næste**. Mediebiblioteket viser alle overførte medieaktiver for den **dokument** (txt)-typen.
1. Vælg den domænetilknytningsfil, der skal anvendes til anmodninger til den URL-adresse, du har defineret tidligere.
1. Vælg **Opret**.

På dette tidspunkt er den URL-adresse, du har oprettet, i kladdetilstand. Publicer URL-adressen for at fuldføre processen. Den fil, som URL-adressen peger på, bliver ikke returneret, før du publicerer URL-adressen.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Konfigurere en Commerce online butik for Apple Pay

Hvis du vil konfigurere en Commerce online butik til at bruge Apple Pay, skal du følge disse trin.

1. Gå til **Detail og Commerce \> Kanaler \> Online-butikker** i Commerce headquarters.
1. Vælg værdien for **Detailkanal-id** til den onlinebutikskanal, der er knyttet til dit websted.
1. I oversigtspanelet **Betalingskonti** kan du tilføje **Dynamics 365 Payment Connector til Adyen**-connector, hvis det ikke allerede er konfigureret, ved at følge instruktionerne i [Konfigurere Dynamics 365 Payment Connector til Adyen](adyen-connector-setup.md).
1. Når Adyen-connectoren er konfigureret, skal du vælge **Tilføj** for at tilføje **Dynamics 365 Payment Connector til Apple Pay**-connectoren.
1. Angiv værdier for connector-forhandleregenskaber.

    | Egenskab               | Beskrivende tekst | Obligatorisk | Indstil automatisk | Eksempelværdi |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Navn på assembly          | Assembly-navn for Dynamics 365 Payment Connector til Apple Pay. | Ja | Ja | Binært navn |
    | Tjenestekonto-id     | Det entydige id for opsætningen af forhandleregenskaber. Dette id påstemples på betalingstransaktioner og identificerer de handlendes egenskaber, som downstream-processer (som f.eks. fakturering) skal bruge. | Ja | Ja | Guid |
    | Forhandlerkonto-id    | Indtast et entydigt Adyen forhandler-id Denne værdi kan du få, når du tilmelder dig Adyen som beskrevet i [Tilmelding til Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ja | Nej | MerchantIdentifier |
    | API-nøgle til skyen          | Angiv Adyen API-nøgle til skyen. Du kan hente denne nøgle ved at følge instruktionerne i [Sådan henter du API-nøglen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ja | Nej | abcdefg |
    | Gatewaymiljø    | Angiv det Adyen gateway-miljø, der skal knyttes til. Mulige værdier er **Test** og **Live**. Du skal kun indstille dette felt til **Live** for produktionsenheder og transaktioner. | Ja | Ja | Aktiv |
    | Understøttede valutaer   | Angiv de valutaer, som connectoren skal behandle. I scenarier, der indeholder kort, kan Adyen understøtte yderligere valutaer via [dynamisk valutaomregning](https://www.adyen.com/pos-payments/dynamic-currency-conversion), efter at transaktionsanmodningen er sendt til betalingsterminalen. Kontakt Adyen Support for at få en liste over understøttede valutaer. | Ja | Ja | USD;EUR |
    | Understøttede betalingsmiddeltyper | Angiv de betalingstyper, som connectoren skal behandle. | Ja | Ja | ApplePay |

1. Når der er angivet oplysninger om den handlende, skal du køre distributionstidsplanen **1070**-kanalkonfiguration.


### <a name="configure-content-security-policies-in-site-builder"></a>Konfigurere sikkerhedspolitikker for indhold i Site Builder

Før du konfigurerer dine fragmenter eller sider med Apple Pay, skal du sikre dig, at sikkerhedspolitikkerne (CPS) er konfigureret i Commerce-webstedsgenerator for dit websted.

Benyt følgende fremgangsmåde for at konfigurere sikkerhedspolitikkerne for indhold i Site Builder.

1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. På fanen **Sikkerhedspolitik for indhold** vælges **Tilføj** for at tilføje en linje, der har `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` til sektionerne **child-src**, **connect-scr**, **frame-src**, **img-src**, **script-src** og **style-src**.
1. Når du er færdig, skal du vælge **Gem og publicer** for at bekræfte ændringerne.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Konfigurere Apple Pay som betalingsmåde ved kassen

Hvis du vil konfigurere Apple Pay til betaling ved kassen som en betalingsmåde ved kassen på webstedets (ikke-express) betalingsside, skal du følge disse trin.

1. Vælg **Fragmenter** i webstedsgenerator, og vælg derefter fragmentet til betaling ved kassen på dit websted.
1. Vælg **Rediger**.
1. I modulet **Container til betalingssektion** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Apple Pay** og derefter **OK**.
1. Vælg **Gem**.
1. Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

Indstillinger for modulet **Apple Pay** er indbygget i modulet og er forbundet med det konfigurerede Dynamics 365 Payment Connector til Apple Pay-connector, der er konfigureret for onlinekanalen i Commerce Headquarters.

### <a name="apple-pay-payment-behavior"></a>Funktionsmåde for Apple Pay-betaling

Knappen til betaling **Apple Pay** vises kun på understøttede Apple Pay-enheder (iPhones, iPads og Safari-browsere, der understøtter Apple Pay). Hvis en bruger ikke bruger en af disse enheder, skjules betalingsknappen **Apple Pay**, så den ikke vises.

Når en bruger markerer betalingsknappen **Apple Pay**, vises dialogboksen **Apple Pay**. Her kan brugeren godkendes mod sin Apple Pay-enhed eller browser. Dialogboksen **Apple Pay** viser en oversigt over ordrebeløbet og den betalingsmåde, som brugeren har konfigureret i forhold til Apple Wallet. Brugeren kan gennemse disse oplysninger og derefter vælge **Betal** for at fuldføre betalingen. Når betalingen er fuldført, dirigeres brugeren til siden **Ordre fuldført** på webstedet, der indeholder en detaljeret ordreoversigt for den fuldførte transaktion.

## <a name="configure-commerce-pos-for-apple-pay"></a>Konfigurer Apple Pay for Commerce POS

POS-konfigurationen bruger konfigurationen i hardwareprofilens **EFT-servicefelt** til Dynamics 365 Payment Connector for Adyen. Du skal konfigurere den elektroniske pengeoverførselstjeneste (EFT) til Dynamics 365 Payment Connector for Adyen i Commerce Headquarters, som beskrevet i [Konfigurere en Dynamics 365 POS-hardwareprofil](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Sørg for, at du føjer **ApplePay** til listen over betalingsmiddeltyper i feltet **Understøttede betalingsmiddeltyper**. Brug semikolon (;) for at adskille betalingsmiddeltyper på listen.

Processortilknytningen for Adyen-connector vil registrere de kontantkorttyper, som Apple Pay bruger på POS-terminalen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Ofte stillede spørgsmål om betalinger](payments-retail.md)

[Betalingsmodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
