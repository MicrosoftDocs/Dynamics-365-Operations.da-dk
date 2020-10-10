---
title: Betalingsmodul
description: Dette emne omhandler betalingsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818320"
---
# <a name="payment-module"></a>Betalingsmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler betalingsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Betalingsmodulet giver kunderne mulighed for at betale for ordrer med kreditkort eller debetkort. Integrationen af betalingsfunktioner i dette modul leveres af Dynamics 365-betalingsconnectoren til Adyen. Du kan finde flere oplysninger om, hvordan du opsætter og konfigurerer betalingsconnectoren i [Dynamics 365-betalingsconnector til Adyen](dev-itpro/adyen-connector.md).

Betalingsmodulet er vært for de betalingsoplysninger, der behandles via Adyen i en HTML-indbygget ramme (iFrame). Betalingsmodulet interagerer med modulet Commerce Scale Unit for at hente Adyens betalingsoplysninger. Som en del af interaktionen med Commerce Scale Unit kan betalingsmodulet tillade, at faktureringsadresseoplysninger enten vises i iframe eller som et separat modul. I Fabrikam-temaet vises faktureringsadressen i et separat modul. Denne fremgangsmåde muliggør fleksibel formatering, fordi adresselinjerne kan gengives, så de ligner linjerne i leveringsadressen.

I betalingsmodulet kan påloggede kunder også gemme deres betalingsoplysninger. Betalingsoplysningerne og faktureringsadressen gemmes og administreres via Adyen-betalingsconnectoren.

Betalingsmodulet dækker alle ordregebyrer, der ikke allerede er dækket af fordelskundepoint eller et gavekort. Hvis totalen for en ordre er fuldt dækket af fordelskundepoint eller gavekortkredit, vil betalingsmodulet være skjult, og kunden vil kunne afgive ordren uden at bruge det.

Adyen-betalingsconnectoren understøtter også effektiv kundegodkendelse (SCA). En del af EU Payment Services-direktivet 2.0 (PSD 2.0) kræver, at onlinekunder godkendes uden for deres onlineindkøbsløsning, når de bruger en elektronisk betalingsmåde. Under betalingsprocessen omdirigeres kunderne til deres banks websted. Efter godkendelsen omdirigeres de derefter tilbage til flowet for Commerce-betalingen. Under denne omdirigering vil de oplysninger, som en kunde har angivet i betalingsflowet (f.eks. leveringsadresse, leveringsindstillinger, oplysninger om gavekort og fordelskundeoplysninger) blive bevaret. Før du kan aktivere denne funktion, skal betalingsconnectoren konfigureres til SCA i Commerce Headquarters. Du kan finde flere oplysninger i [Effektiv kundegodkendelse ved hjælp af Adyen](adyen_redirect.md).

Følgende illustration viser et eksempel på moduler for gavekort, fordelskunde og betaling på en betalingsside.

![Eksempel på moduler for gavekort, fordelskunde og betaling på en betalingsside](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Egenskaber for betalingsmodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst | En valgfri overskrift til betalingsmodulet. |
| Højden på iFrame. | Pixels | Højden på iFrame i pixel. Højden kan dog justeres efter behov. |
| Vis faktureringsadresse | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vil faktureringsadressen blive betjent af Adyen i betalingsmodulets iFrame. Hvis den er indstillet til **Falsk**, betjenes faktureringsadressen ikke af Adyen, og en Commerce-bruger skal konfigurere et modul, der viser faktureringsadressen på betalingssiden. |
| Tilsidesæt betalingstype | Kode for overlappende typografiark (CSS) | Da betalingsmodulet er knyttet til en iframe, er der begrænsede formateringsfunktioner. Du kan foretage en del formatering ved hjælp af denne egenskab. Hvis du vil tilsidesætte webstedets typografier, skal du indsætte CSS-koden som værdien for denne egenskab. Webstedsgeneratorens CSS-tilsidesættelser og -typografier gælder ikke for dette modul. |

## <a name="billing-address"></a>Faktureringsadresse

Betalingsmodulet gør det muligt for kunderne at angive en faktureringsadresse til deres betalingsoplysninger. De kan også bruge deres leveringsadresse som faktureringsadresse, så betalingsflowet bliver lettere og hurtigere. Hvis egenskaben **Vis faktureringsadresse** er angivet til **Falsk**, skal betalingsmodulet konfigureres på betalingssiden.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Føje et betalingsmodul til en betalingsside og angive de krævede egenskaber

Et modul til at udføre betalingen kan kun føjes til et betalingsmodul. Du kan finde flere oplysninger om, hvordan du konfigurerer et betalingsmodul for en betalingsside, under [Betalingsmodul](add-checkout-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)

[Dynamics 365-betalingsconnector til Adyen](dev-itpro/adyen-connector.md)

[Effektiv kundegodkendelse (SCA) ved hjælp af Adyen](adyen_redirect.md)
