---
title: Konfigurere ekspresbetalinger til PayPal
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurerer ekspresbetalinger til PayPal for at gøre det nemmere at foretage betaling ved kassen i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5fff17959e7ed9299df169c68b2ed07f6b7c7d2c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743566"
---
# <a name="configure-express-payments-for-paypal"></a>Konfigurere ekspresbetalinger til PayPal

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan konfigurerer ekspresbetalinger til PayPal for at gøre det nemmere at foretage betaling ved kassen i Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| PayPal-tegnebog | Den kundeoplevelse og integration, der understøttes af PayPal-connectoren. Det kaldes også knappen PayPal. |
| Tegnebog | En betalingstype, der ikke omfatter de traditionelle betalingskarakteristika som f.eks. BIN-området (Bank Identification Number) og udløbsdatoen, som bruges til at skelne mellem kredit- og debetkorttyper. |
| Ekspresbetaling | Et Commerce-modul, der understøtter en hurtigere betaling ved kassen, når der bruges understøttede betalingsmåder. Dette emne dækker brugen af betalingsekspresmodulet sammen med PayPal. |

Dynamics 365 Commerce tilbyder indbygget integration for PayPal-tegnebog. Når Dynamics 365 Payment Connector til PayPal er konfigureret, vises knappen PayPal som en betalingsmetode, der kan vælges, når onlineordren betales ved kassen. Når brugerne vælger PayPal, bliver de bedt om at fuldføre betalingen direkte via PayPal og returneres derefter til onlinebutikken for at fuldføre ordren. Ved kassen med PayPal-indkøbsvognen kan kunderne bruge deres betalingskontooplysninger til at udfylde formen til betaling ved kassen, så de hurtigere kan fuldføre processen til betaling ved kassen.

Commerce har tilføjet et betalingsekspresmodul, der gør det nemmere at betale ved kassen. Ekspresbetalingsmodulet kan bruges i et fragment, som kan medtages på en side i kassen eller indkøbsvognen. Når PayPal er konfigureret, bruges samme Dynamics 365 Payment Connector til PayPal-connector-referencen til både indstillingen for ekspresbetaling og den almindelige betaling ved kassen.

## <a name="paypal-checkout-in-commerce"></a>PayPal-betaling ved kassen i Commerce

### <a name="prerequisites"></a>Forudsætninger

Konfigurer PayPal-tegnebogen for dit miljø som beskrevet i [Dynamics 365 Payment Connector til PayPal](../paypal.md).

Hvis du bruger PayPal som en mulighed i det almindelige betalingsflow (hvor brugerne manuelt angiver deres kontooplysninger uden at bruge handlinger til ekspresbetaling med forhåndsudfyldning), skal du følge installationsinstruktionerne i [Betalingsmodulet](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Betalingsekspresmodul med PayPal

Ekspresbetalingsmodulet fungerer sammen med understøttende betalingsmåder for at give netkunder mulighed for at betale hurtigere ved at forhåndsudfylde deres betalingstjenestekontooplysninger under betalingsprocessen. Ekspresbetalingsmodulet bruger den konfigurerede betalings-connector til at forhåndsudfylde formen til betaling ved kassen med brugerkontooplysninger som f.eks. adresse, kontaktoplysninger og den valgte betalingsmåde.

Når der bruges PayPal-ekspresbetaling ved kassen, og en bruger vælger knappen PayPal i ekspresbetalingssektionen på siden til betaling ved kassen, åbnes et PayPal-betalingsvindue med iFrame. Derefter logger brugeren på sin PayPal-konto for at bruge kontoens leveringsadresse, faktureringsadresse, mailadresse og den valgte PayPal-betalingsmetode til at betale for transaktionen.

Når brugerne har fuldført handlingen i PayPal-vinduet, dirigeres de tilbage til siden til betaling ved kassen på Commerce-webstedet, hvor formen til betaling ved kassen er forhåndsudfyldt med de valgte oplysninger. I ekspresbetalingsflowet er den første leveringsmulighed, der er tilgængelig for den leveringsadresse, der returneres, forhåndsudfyldt for brugeren. Brugeren har derefter mulighed for at gennemse ordren og ændre betalingsoplysningerne ved kassen, før brugeren vælger **Afgiv ordre** for at færdiggøre ordren.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Tilføje betalingsekspresmodulet sammen med PayPal i et fragment

Følg disse trin, hvis du til tilføje betalingsekspresmodulet sammen med PayPal i et fragment i Commerce-webstedsgenerator.

1. Gå til dit websted.
1. Vælg **Fragmenter** i venstre navigationsrude, og vælg derefter **Nyt**.
1. Vælg modulet **Ekspresbetaling** i dialogboksen **Nyt fragment**, og angiv derefter et navn under **Fragmentets navn** (f.eks. **Ekspresbetaling**).
1. Vælg **OK** for at oprette fragmentet.
1. I dispositionsvisningen skal du vælge den plads til betalingsekspresmodulet, som du har oprettet.
1. Vælg **Overskrift** i egenskabsruden.
1. I feltet **Overskriftstekst** i dialogboksen **Overskrift** skal du indtaste den overskriftstekst, der skal vises for sektionen til ekspresbetaling på dit websted (f.eks. **Ekspresbetaling**).
1. Vælg overskriftsniveauet (f.eks. **H2**) under **Overskriftsniveau**.
1. Vælg **OK**.
1. I egenskabsruden skal du i feltet **Højde af iFrame** angive eller justere iFrame-elementets højde (f.eks. **60)**.
1. I feltet **Understøttede betalingsmiddeltyper** skal du angive **PayPal**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Føje betalingsekspresfragmentet til siden for betaling ved kassen

Udfør følgende trin for at føje betalingsekspresfragmentet til siden for betaling ved kassen i webstedsgeneratoren.

1. Gå til dit websted.
1. Vælg **Sider** i venstre navigationsrude, og vælg derefter siden til betaling ved kassen på dit websted.
1. Vælg **Rediger** for at redigere siden.
1. På pladsen **Hoved** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.

    > [!NOTE]
    > Hvis der allerede findes et containermodul, der indeholder et kassefragment, skal du flytte sektionen med ekspresbetaling, så den vises oven over eksisterende container til betaling ved kassen på pladsen **Hoved**. Sektionen for ekspresbetaling gengives derefter over den almindelige container til betaling ved kassen. Hvis du vil flytte et containermodul op eller ned, skal du vælge ellipseknappen (**...**) og vælge **Flyt op** eller **Flyt ned**.

1. I ruden **Containeregenskaber** anbefales det, at du konfigurerer egenskabsindstillingerne på følgende måde:

    - **Containerlayout** – Vælg **Stablet**.
    - **Bredde** – Vælg **Udfyld container**.
    - **Viste underordnede** – vælg **Tre**.

1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj fragment**.
1. I dialogboksen **Vælg et fragment** skal du finde og vælge det ekspresbetalingsfragment, som du har oprettet, og derefter vælge **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Føje betalingsekspresfragmentet til indkøbskurvens side

Udfør følgende trin for at føje betalingsekspresfragmentet til indkøbskurvens side i webstedsgeneratoren.

1. Gå til dit websted.
1. Vælg **Sider** i venstre navigationsrude, og vælg derefter indkøbskurvens side på dit websted.
1. Vælg **Rediger** for at redigere siden.
1. Find den container, der indeholder modulet **Indkøbskurv**, på pladsen **Hoved**. Modulet **Indkøbskurv** indeholder en plads til **Ekspresbetaling**.
1. På pladsen **Ekspresbetaling** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Ekspresbetaling** og derefter **OK**.
1. I egenskabsruden skal du i feltet **Understøttede betalingsmiddeltyper** angive **Paypal**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

### <a name="modes-of-delivery"></a>Leveringsmåder

Når modulet Ekspresbetaling er konfigureret til at bruge PayPal, udfyldes den første leveringsmulighed, der returneres for den leveringsadresse, der blev valgt til PayPal-kontoen, på forhånd. Brugerne kan ændre leveringsadressen, hvis de ønsker det.

Rækkefølgen for leveringsmåden er konfigureret i afsnittet **Leveringsmåder** for kanalen i Commerce headquarters. Du kan finde flere oplysninger i [Konfigurer leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

I modulet til betaling ved kassen bruges også modulet til leveringsindstillinger, når leveringsmåder gengives under betaling ved kassen. Der er flere oplysninger i [Leveringsindstillingsmodul](../delivery-options-module.md).

Leveringsmåder føjes til listen for onlinebutikken i Commerce headquarters. Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**, og vælg kanal-id'et for din butik. Vælg derefter **Konfiguration \> Leveringsmåder**. De modulleveringsmåder, der vises i konfigurationen, vises på samme måde på webstedet. Hvis du vil tilføje eller fjerne leveringsmåder for en detailkanal eller et produkt, skal du vælge **Administrer leveringsmåder** i handlingsruden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Ofte stillede spørgsmål om betalinger](payments-retail.md)

[Betalingsmodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)

[Konfigurer leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Leveringsindstillingsmodul](../delivery-options-module.md)
