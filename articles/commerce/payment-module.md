---
title: Betalingsmodul
description: Denne artikel omhandler betalingsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89ca5dd4f46611e75faccd3213028750fa48d35
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850269"
---
# <a name="payment-module"></a>Betalingsmodul

[!include [banner](includes/banner.md)]

Denne artikel omhandler betalingsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

Betalingsmodulet giver kunderne mulighed for at betale for ordrer med kreditkort eller debetkort. Integrationen af betalingsfunktioner i dette modul leveres af Dynamics 365-betalingsconnectoren til Adyen. Du kan finde flere oplysninger om, hvordan du opsætter og konfigurerer betalingsconnectoren i [Dynamics 365-betalingsconnector til Adyen](dev-itpro/adyen-connector.md).  

Fra og med Commerce Release 10.0.14 er betalingsmodulet også integreret med Dynamics 365-betalingsconnector til PayPal, hvilket giver kunderne mulighed for at betale ordrer ved hjælp af PayPal. Du kan finde flere oplysninger om, hvordan du konfigurerer Dynamics 365-betalingsconnector til PayPal, i [Dynamics 365-betalingsconnector til PayPal](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365-betalingsconnector til Adyen 

Betalingsmodulet er vært for de betalingsoplysninger, der behandles via Adyen i en HTML-indbygget ramme (iFrame). Betalingsmodulet interagerer med modulet Commerce Scale Unit for at hente Adyens betalingsoplysninger. Som en del af interaktionen med Commerce Scale Unit kan betalingsmodulet tillade, at faktureringsadresseoplysninger enten vises i iFrame via Adyen eller som et separat modul. I Fabrikam-temaet aktiveres faktureringsadressen som et separat modul. Denne fremgangsmåde muliggør fleksibel formatering, fordi adresselinjerne kan gengives, så de ligner linjerne i leveringsadressen.

I betalingsmodulet kan påloggede kunder også gemme deres betalingsoplysninger. Betalingsoplysningerne og faktureringsadressen gemmes og administreres via Adyen-betalingsconnectoren.

Betalingsmodulet dækker alle ordregebyrer, der ikke allerede er dækket af fordelskundepoint eller et gavekort. Hvis totalen for en ordre er fuldt dækket af fordelskundepoint eller gavekortkredit, vil betalingsmodulet være skjult, og kunden vil kunne afgive ordren uden at bruge det.

Adyen-betalingsconnectoren understøtter også effektiv kundegodkendelse (SCA). En del af EU Revised Payment Services-direktivet (PSD2) kræver, at onlinekunder godkendes uden for deres onlineindkøbsløsning, når de bruger en elektronisk betalingsmåde. Under betalingsprocessen ved kassen omdirigeres kunderne til deres banks websted, og efter godkendelsen bliver de igen omdirigeret til Commerce-betalingsflowet. Under denne omdirigering bliver de oplysninger, som en kunde har angivet i betalingsflowet (f.eks. leveringsadresse, leveringsindstillinger, oplysninger om gavekort og fordelskundeoplysninger) bevaret. Før du kan aktivere denne funktion, skal Adyen-betalingsconnectoren konfigureres til SCA i Commerce Headquarters. Du kan finde flere oplysninger i [Effektiv kundegodkendelse ved hjælp af Adyen](adyen_redirect.md). Denne funktion blev aktiveret i Commerce-version 10.0.12.

> [!NOTE]
> Med Adyen-betalingsconnectoren kan iFrame-modulet i betalingsmodulet kun gengives, hvis du føjer URL-adressen til Adyen til listen på dit websted over tilladte websteder. Hvis du vil udføre dette trin, skal du tilføje **\*.adyen.com** til dit websteds **child-src**, **connect-src**, **img-src**, **script-src** og **style-src** direktiver for sikkerhedspolitik. Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold](manage-csp.md). 

Følgende illustration viser et eksempel på moduler for gavekort, fordelskunde og Adyen-betaling på en betalingsside.

![Eksempel på moduler for gavekort, fordelskundepoint og Adyen-betaling på en betalingsside.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector til PayPal

Fra og med Commerce-version 10.0.14 er betalingsmodulet også integreret med Dynamics 365-betalingsconnector til PayPal. Du kan finde flere oplysninger om, hvordan du opsætter og konfigurerer denne betalingsconnector i [Dynamics 365-betalingsconnector til PayPal](paypal.md).
 
På betalingssiden kan du have både Adyen- og PayPal-connectorer konfigureret. Betalingsmodulet er blevet forbedret med yderligere egenskaber, der er med til at identificere, hvilken connector det skal fungere med. Du kan finde oplysninger i modulegenskaberne **Understøttede betalingsmiddeltyper** og **Er primære betaling** i følgende tabel.
  
Når betalingsmodulet er konfigureret til at bruge PayPal-betalingsconnectoren, vises en PayPal-knap på betalingssiden. Når betalingsmodulet startes af kunden, gengiver det en iFrame, der indeholder PayPal-oplysninger. Kunden kan logge på og angive PayPal-oplysninger i denne iFrame for at fuldføre transaktionen. Når en kunde vælger at betale med PayPal, debiteres den resterende saldo på ordren via PayPal.

PayPal-betalingsconnectoren kræver ikke noget faktureringsadressemodul, da alle fakturarelaterede oplysninger håndteres af PayPal i den pågældende iFrame. Modulerne for leveringsadresse og leveringsindstillinger er dog påkrævet.

I følgende illustration vises et eksempel på to betalingsmoduler på en betalingsside, én, der er konfigureret med Adyen-betalingsconnectoren og den anden med PayPal-betalingsconnectoren.
![Eksempel på Adyen-betalings- og PayPal-moduler på en betalingsside.](./media/ecommerce-paypal.png)

I følgende illustration vises et eksempel på den PayPal-iFrame, der aktiveres ved hjælp af knappen PayPal. 
![Eksempel på Paypal iFrame på en betalingsside.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Egenskaber for betalingsmodul

| Egenskabsbetegnelse | Værdier | Betegnelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst | En valgfri overskrift til betalingsmodulet. |
| Højden på iFrame. | Pixels | Højden på iFrame i pixel. Højden kan dog justeres efter behov. |
| Vis faktureringsadresse | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vil faktureringsadressen blive betjent af Adyen i betalingsmodulets iFrame. Hvis indstillet til **Falsk**, betjenes faktureringsadressen ikke af Adyen, og en Commerce-bruger skal konfigurere et modul, der viser faktureringsadressen på betalingssiden. For PayPal-betalingsconnectoren har dette felt ingen indflydelse, da faktureringsadressen håndteres fuldt ud i PayPal. |
| Tilsidesæt betalingstype | Kode for overlappende typografiark (CSS) | Da betalingsmodulet er knyttet til en iframe, er der begrænsede formateringsfunktioner. Du kan foretage en del formatering ved hjælp af denne egenskab. Hvis du vil tilsidesætte webstedets typografier, skal du indsætte CSS-koden som værdien for denne egenskab. Webstedsgeneratorens CSS-tilsidesættelser og -typografier gælder ikke for dette modul. |
|Understøttede betalingsmiddeltyper| Streng| Hvis der er konfigureret flere betalingsconnectorer, skal du angive strengen for understøttede betalingsmiddeltype, som defineret i konfigurationen af Commerce Headquarters-betalingsconnectoren (se følgende billede). Hvis feltet er tomt, anvendes som standard Adyen-betalingsconnectoren. Tilføjet i Commerce version 10.0.14.|
|Er primær betaling|  **Sand** eller **Falsk** | Hvis **Sand**, genereres eventuelle fejlmeddelelser fra den primære betalingsconnector på betalingssiden. Hvis både Adyen- og PayPal-betalingsconnectorer er konfigureret, skal du indstille Adyen til **Sand**, som blev tilføjet i Commerce-version 10.0.14.|
|Brug connector-id| **Sand** eller **Falsk** | Brug denne egenskab, hvis der er konfigureret flere betalingsconnectorer for webstedet. Hvis **Sand**, skal connectorer bruge connector-id'et til betalingskorrelation.|
|Brug browserangivet sprogkode til iFrame|  **Sand** eller **Falsk** | (Kun Adyen) Hvis **Sand** vil Adyen iFrame gengive sproget baseret på webstedsbrugerens browserkontekst i stedet for at bruge sprogkoden for den Commerce-kanal, der er konfigureret for webstedet. Tilføjet i Commerce version 10.0.27.|

I følgende illustration vises et eksempel på den værdi for **Understøttede betalingsmiddeltype**, der er indstillet til "PayPal" i konfigurationen for betalingsconnectoren i Commerce Headquarters.
![Eksempel på understøttede betalingsmiddeltyper i Commerce Headquarters.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Faktureringsadresse

Et faktureringsadressemodul kan bruges på betalingssiden, hvis faktureringsadresselinjerne i Adyen-betalingsconnectoren ikke i tilstrækkelig omfang stemmer overens med resten af webstedet. 

Hvis du vil bruge et faktureringsadressemodul på betalingssiden, når betalingsmodulet er integreret med Adyen-betalingsconnectoren, skal du indstille egenskaben **Vis faktureringsadresse** til **Falsk**, så der kan bruges et dedikeret faktureringsadressemodul i stedet for Adyen-standardfaktureringsadressen. I dette tilfælde skal webstedets forfatter inkludere et faktureringsadressemodul på betalingssiden. Adyen-betalingsconnectoren giver også mulighed for at bruge leveringsadressen som faktureringsadresse for at minimere antallet af trin for brugeren af webstedet.

I lighed med betalingsmoduler er der føjet en egenskab for **Understøttede betalingsmiddeltyper** til faktureringsadressemodulet i Commerce Release 10.0.14. Værdien af denne egenskab skal være identisk med den værdi, der er angivet i betalingsmodulet, for at sikre, at de fungerer sammen. I Adyen-betalingsconnectoren skal denne værdi være tom (standardtilstanden) i både betalingsmodulet og faktureringsadressemodulet. For PayPal-connectoren kræves der ikke et dedikeret faktureringsadressemodul. Ved andre typer betalingsconnectorer skal strengen angives som konfigureret i Commerce Headquarters.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Føje et betalingsmodul til en betalingsside og angive de krævede egenskaber

Et modul til at udføre betalingen kan kun føjes til et betalingsmodul. Du kan finde flere oplysninger om, hvordan du konfigurerer et betalingsmodul for en betalingsside, under [Betalingsmodul](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Konfigurere Adyen- og PayPal-betalingsconnectorer, når de begge bruges

Hvis både Adyen- og PayPal-betalingsconnectorer bruges til dit websted, skal du følge disse trin i Commerce-webstedsgenerator for at tilføje betalingsmoduler for hver connector i kassemodulet og derefter konfigurere egenskaberne for hvert modul.

1. Benyt følgende fremgangsmåde i egenskabsruden til PayPal-betalingsmodulet:

    1. I feltet for egenskaben **Understøttede betalingsmiddeltyper** skal du angive **PayPal**.
    1. Fjern markeringen i afkrydsningsfeltet for egenskaben **Er primær betaling**.
    1. Markér afkrydsningsfeltet for egenskaben **Brug connector-id**.

1. Benyt følgende fremgangsmåde i egenskabsruden til Adyen-betalingsmodulet:

    1. Lad feltet for egenskaben **Understøttede betalingsmiddeltyper** være tomt.
    1. Markér afkrydsningsfeltet for egenskaben **Er primær betaling**.
    1. Markér afkrydsningsfeltet for egenskaben **Brug connector-id**.

> [!NOTE]
> Når du konfigurerer Adyen- og PayPal-connectorerne til at blive brugt sammen, skal **Dynamics 365 Payment Connector til Adyen**-konfigurationen være på den første position i onlinekanalens connector-konfiguration af **Betalingskonti** i Commerce Headquarters. Hvis du vil bekræfte eller ændre connectorrækkefølgen, skal du gå til **Onlinebutikker** og vælge kanalen til dit websted. Derefter skal du under **Connector** i oversigtspanelet **Betalingskonti** under fanen **Opsætning** sikre, at **Dynamics 365 Payment Connector for Adyen**-konfigurationen er på den første position (dvs. på den øverste linje), og at **Dynamics 365 Payment Connector til PayPal**-konfigurationen er på den anden linje. Tilføj eller fjern connectorer efter behov for at prioritere dem.

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)

[Dynamics 365-betalingsconnector til Adyen](dev-itpro/adyen-connector.md)

[Dynamics 365-betalingsconnector til PayPal](paypal.md)

[Effektiv kundegodkendelse (SCA) ved hjælp af Adyen](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
