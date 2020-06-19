---
title: Betalingsmodul
description: I dette emne beskrives det, hvordan du føjer et købefeltmodul til en side og angiver de påkrævede egenskaber.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411178"
---
# <a name="checkout-module"></a>Betalingsmodul


[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du føjer et købefeltmodul til en side og angiver de påkrævede egenskaber.

## <a name="overview"></a>Oversigt

Et betalingsmodul er en særlig container, der er vært for alle moduler, som skal bruges til at oprette en ordre. Den indeholder en trinvis proces, som en kunde bruger til at angive alle de relevante oplysninger for at foretage et køb. Det henter leveringsadresse, forsendelsesmetode og faktureringsoplysninger. Den indeholder også en ordreoversigt og andre oplysninger vedrørende en kundeordre.

Et betalingsmodul gengiver data på basis af indkøbsvogn-id'et. Dette indkøbsvogn-id gemmes som en browsercookie. Der kræves et indkøbsvogn-id for at gengive oplysninger i betalingsmodulet, f. eks. varerne i ordren, det samlede beløb og rabatterne. 

Det følgende billede viser et eksempel på et Fabrikam-betalingsmodul på en betalingsside.

![Eksempel på et betalingsmodul](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Egenskaber for betalingsmodul

Et udtjekningsmodul viser en ordreoversigt og giver mulighed for at afgive en ordre. Hvis du vil indsamle alle de kundeoplysninger, der kræves, før en ordre kan placeres, skal der føjes yderligere moduler til udtjekningsmodulet. Detailhandlere har derfor fleksibilitet til at føje brugerdefinerede moduler til udtjekningen eller til at udelukke moduler ud fra behovene.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduler, der kan bruges i betalingsmodulet

- **Leveringsadresse** – dette modul giver en kunde mulighed for at tilføje eller vælge en leveringsadresse for en ordre. Hvis kunden er logget på, vises eventuelle adresser, der tidligere er blevet gemt for den pågældende kunde. Kunden kan derefter vælge blandt disse adresser. Kunden kan også tilføje en ny adresse. Leveringsadressen bruges til alle varer i ordren, der kræver levering. Den kan ikke tilpasses for individuelle linjevarer. Der er defineret leveringsadresseformater for hvert land eller område, og dette modul gennemtvinger de lande-/områdespecifikke regler. Selvom dette modul ikke indeholder adressevalidering, kan adressevalidering implementeres ved hjælp af tilpasning. Hvis ordren kun omfatter varer, der afhentes i butikken, skjules dette modul automatisk.

    Det følgende billede viser et eksempel på et leveringsadressemodul på en betalingsside.

    ![Eksempel på et leveringsadressemodul](./media/ecommerce-shippingaddress.PNG)

- **Leveringsindstillinger** – dette modul giver en kunde mulighed for at vælge en leveringsindstilling for en ordre. Leveringsindstillingerne er baseret på leveringsadressen. Hvis leveringsadressen ændres, skal leveringsindstillingerne hentes igen. Hvis ordren kun omfatter varer, der afhentes i butikken, skjules dette modul automatisk.

    Det følgende billede viser et eksempel på et leveringsindstillingsmodul på en betalingsside.

    ![Eksempel på et leveringsindstillingsmodul](./media/ecommerce-deliveryoptions.PNG)

- **Container til betalingssektion** – dette modul er en container, hvor du kan placere flere moduler for at oprette en sektion i betalingsprocessen. Du kan f. eks. indsætte alle betalingsrelaterede moduler i denne container for at få dem vist som én sektion. Dette modul påvirker kun processens layout.
- **Gavekort** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af et gavekort. Den understøtter kun Microsoft Dynamics 365 Commerce-gavekort. Der kan anvendes ét eller flere gavekort til en ordre. Hvis gavekortets saldoen ikke dækker beløbet i indkøbsvognen, kan gavekortet kombineres med en anden betalingsmåde. Gavekort kan kun indløses, hvis kunden er logget på.
- **Fordelskundepoint** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af fordelskundepoint. Den giver en oversigt over tilgængelige point og udløbssteder, og giver kunden mulighed for at vælge det antal point, der skal indløses. Hvis kunden ikke er logget på eller ikke er fordelskunde, eller hvis det samlede beløb i indkøbsvognen er 0 (nul), skjules dette modul automatisk.
- **Betaling** – Dette modul giver en kunde mulighed for at betale en ordre ved hjælp af et kreditkort. Hvis det samlede beløb i indkøbsvognen dækkes af fordelskundepoint eller et gavekort, eller hvis det er 0 (nul), skjules dette modul automatisk. Integration af kreditkort leveres af Adyen-betalingsconnectoren til dette modul. Du kan flere oplysninger om, hvordan denne connector bruges, i [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).
- **Faktureringsadresse** – dette modul giver en kunde mulighed for at angive faktureringsoplysninger. Disse oplysninger behandles sammen med kreditkortoplysningerne af Adyen. Dette modul omfatter en indstilling, som gør det muligt for kunderne at bruge deres faktureringsadresse som leveringsadresse.

    Det følgende billede viser et eksempel på moduler for gavekort, fordelskundepoint, betaling og faktureringsadresse på en betalingsside.

    ![Eksempel på moduler for gavekort, fordelskundepoint, betaling og faktureringsadresse](./media/ecommerce-payments.PNG)

- **Kontaktoplysninger** – dette modul giver en kunde mulighed for at tilføje eller ændre kontaktoplysningerne (mailadressen) for en ordre.

- **Tekstblok** – Dette modul indeholder alle de meddelelser, der styres af CMS (Content Management System). Det kan f. eks. indeholde meddelelsen "Kontakt 1-800-Fabrikam, hvis der er problemer med ordren". 

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

De fleste betalingsoplysninger, f. eks. leveringsadressen og leveringsmåden, gemmes i indkøbsvognen og behandles som en del af ordren. Den eneste undtagelse er kreditkortoplysningerne. Disse oplysninger behandles direkte ved hjælp af Adyen-betalingsconnectoren. Betalingen er godkendt, men opkræves ikke.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Føje et betalingsmodul til en side og angive de påkrævede egenskaber

Hvis du vil føje et betalingsmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Sidefragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. Vælg modulet **Betaling** i dialogboksen **Nyt sidefragment**.
1. Under **Sidefragmentsnavn** skal du angive navnet **Betalingsfragment** og derefter vælge **OK**.
1. Vælg pladsen **Betalingsmodul**.
1. Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.
1. På pladsen **Betalingsoplysninger** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulerne **Leveringsadresse**, **Leveringsindstillinger**, **Container til betalingssektion** og **Kontaktoplysninger** og derefter vælge **OK**.
1. I modulet **Container til betalingssektion** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulerne **Gavekort**, **Fodelskunde** og **Betaling** og derefter **OK**. På denne måde sikrer du dig, at alle betalingsmåderne vises sammen i en sektion.
1. Vælg **Gem** og derefter **Vis** for at få vist fragmentet. Nogle moduler, som ikke har en indkøbsvognkontekst, gengives muligvis ikke i eksemplet.
1. Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Opret en skabelon, der bruger det nye betalingsfragment.
1. Opret en betalingsside, der bruger den nye skabelon.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbsvognmodul](add-cart-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
