---
title: Betalingsmodul
description: Denne artikel beskriver, hvordan du føjer et købefeltmodul til en side og angiver de påkrævede egenskaber.
author: anupamar-ms
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 295b99c7012e35a40af34d454ff7082d4100c74a
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746219"
---
# <a name="checkout-module"></a>Betalingsmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver, hvordan du føjer et købefeltmodul til en side og angiver de påkrævede egenskaber.

Et betalingsmodul er en særlig container, der er vært for alle moduler, som skal bruges til at oprette en ordre. Den indeholder en trinvis proces, som en kunde bruger til at angive alle de relevante oplysninger for at foretage et køb. Det henter leveringsadresse, forsendelsesmetode og faktureringsoplysninger. Den indeholder også en ordreoversigt og andre oplysninger vedrørende en kundeordre.

Et betalingsmodul gengiver data på basis af indkøbsvogn-id'et. Dette indkøbsvogn-id gemmes som en browsercookie. Der kræves et indkøbsvogn-id for at gengive oplysninger i betalingsmodulet, f. eks. varerne i ordren, det samlede beløb og rabatterne. 

Det følgende billede viser et eksempel på et Fabrikam-betalingsmodul på en betalingsside.

![Eksempel på et betalingsmodul.](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Egenskaber for betalingsmodul

Et udtjekningsmodul viser en ordreoversigt og giver mulighed for at afgive en ordre. Hvis du vil indsamle alle de kundeoplysninger, der kræves, før en ordre kan placeres, skal der føjes yderligere moduler til udtjekningsmodulet. Detailhandlere har derfor fleksibilitet til at føje brugerdefinerede moduler til udtjekningen eller til at udelukke moduler ud fra behovene.

| Egenskabsbetegnelse | Værdier | Beskrivelse |
|----------------|--------|-------------|
| Overskrift til udtjekning | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En overskrift til betalingsmodulet. |
| Overskrift til Ordreoversigt | Overskriftstekst | En overskrift til sektionen Ordreoversigt i modulet. |
| Overskrift til linjeelementer i indkøbsvogn | Overskriftstekst | En overskrift til de linjeelementer i kurven, som vises i betalingsmodulet. |
| Vis forsendelsesgebyrer for linjeelement | **Sand** eller **Falsk** | Hvis denne egenskab angives til **Sand**, vil forsendelsesgebyrer, der gælder for linjeelementer, blive vist på linjer i indkøbsvognen. Hvis funktionen **Overskrift til gebyr uden forholdsberegning** er aktiveret i Commerce Headquarters, vil forsendelsesgebyret blive anvendt til hovedniveauet og ikke linjeniveauet. Denne funktion blev tilføjet i Commerce version 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduler, der kan bruges i betalingsmodulet

- **Leveringsadresse** – dette modul giver en kunde mulighed for at tilføje eller vælge en leveringsadresse for en ordre. Yderligere oplysninger om dette modul finder du i [Leveringsadressemodul](ship-address-module.md).

    Det følgende billede viser et eksempel på et leveringsadressemodul på en betalingsside.

    ![Eksempel på et leveringsadressemodul.](./media/ecommerce-shippingaddress.PNG)

- **Leveringsindstillinger** – Dette modul giver en kunde mulighed for at vælge en leveringsmåde for en ordre. Yderligere oplysninger om dette modul finder du i [Leveringsindstillingsmodul](delivery-options-module.md).

    Det følgende billede viser et eksempel på et leveringsindstillingsmodul på en betalingsside.
 
    ![Eksempel på et leveringsindstillingsmodul.](./media/ecommerce-deliveryoptions.PNG)

- **Container til betalingssektion** – dette modul er en container, hvor du kan placere flere moduler for at oprette en sektion i betalingsprocessen. Du kan f. eks. indsætte alle betalingsrelaterede moduler i denne container for at få dem vist som én sektion. Dette modul påvirker kun processens layout.

- **Gavekort** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af et gavekort. Yderligere oplysninger om dette modul finder du i [Gavekortmodul](add-giftcard.md).

- **Fordelskundepoint** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af fordelskundepoint. Den giver en oversigt over tilgængelige point og udløbssteder, og giver kunden mulighed for at vælge det antal point, der skal indløses. Hvis kunden ikke er logget på eller ikke er fordelskunde, eller hvis det samlede beløb i indkøbsvognen er 0 (nul), skjules dette modul automatisk.

- **Betaling** – Dette modul giver en kunde mulighed for at betale en ordre med kreditkort eller debetkort. Kunder kan også angive en faktureringsadresse for den valgte betalingsmulighed. Yderligere oplysninger om dette modul finder du i [Betalingsmodul](payment-module.md).

    Det følgende billede viser et eksempel på moduler for gavekort, fordelskundepoint og betaling på en betalingsside.

    ![Eksempel på moduler for gavekort, fordelskundepoint og betaling på en betalingsside.](./media/ecommerce-payments.PNG)

- **Kontaktoplysninger** – dette modul giver en kunde mulighed for at tilføje eller ændre kontaktoplysningerne (mailadressen) for en ordre.

- **Tekstblok** – Dette modul indeholder alle de meddelelser, der styres af CMS (Content Management System). Det kan f. eks. indeholde meddelelsen "Kontakt 1-800-Fabrikam, hvis der er problemer med ordren". 

- **Vilkår og betingelser for betaling** – Dette modul indeholder RTF-tekst med vilkår og betingelser og et afkrydsningsfelt til kundeinput. Afkrydsningsfeltet er valgfrit og kan konfigureres. Input hentes af modulet og kan bruges som en kontrol, inden ordren sendes, men de indgår ikke i ordreoversigtens oplysninger. Dette modul kan føjes til pladsen for betalingscontaineren, containeren for betalingssektionen eller vilkår og betingelser, afhængigt af virksomhedens behov. Hvis det føjes til pladsen for betalingscontaineren eller containeren for betalingssektionen, vises det som et trin i betalingsprocessen. Hvis det føjes til pladsen for vilkår og betingelser, vises det tæt på knappen for ordreafgivelse.

    Følgende billede viser et eksempel på vilkår og betingelser på en betalingsside.

    ![Eksempel på vilkår og betingelser på en betalingsside.](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

De fleste betalingsoplysninger, f. eks. leveringsadressen og leveringsmåden, gemmes i indkøbsvognen og behandles som en del af ordren. Den eneste undtagelse er kreditkortoplysningerne. Disse oplysninger behandles direkte ved hjælp af Adyen-betalingsconnectoren. Betalingen er godkendt, men den debiteres først, når ordren er leveret.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Føje et betalingsmodul til en side og angive de påkrævede egenskaber

Hvis du vil føje et betalingsmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. Vælg modulet **Betaling** i dialogboksen **Vælg fragment**.
1. Under **Fragmentnavn** skal du angive navnet **Betalingsfragment** og derefter vælge **OK**.
1. Vælg pladsen **Betalingsmodul**.
1. Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.
1. På pladsen **Betalingsoplysninger** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulerne **Leveringsadresse**, **Leveringsindstillinger**, **Container til betalingssektion** og **Kontaktoplysninger** og derefter vælge **OK**.
1. I modulet **Container til betalingssektion** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulerne **Gavekort**, **Fordelskunde** og **Betaling** og derefter **OK**. På denne måde sikrer du dig, at alle betalingsmåderne vises sammen i en sektion.
1. I pladsen for **Vilkår og betingelser** skal du tilføje modulet **Vilkår og betingelser for betaling**, hvis det er nødvendigt. I ruden Egenskaber for modulet skal du konfigurere teksten for vilkårene og betingelserne efter behov.
1. Vælg **Gem** og derefter **Vis** for at få vist fragmentet. Nogle moduler, som ikke har en indkøbsvognkontekst, gengives muligvis ikke i eksemplet.
1. Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Opret en skabelon, der bruger det nye betalingsfragment.
1. Opret en betalingsside, der bruger den nye skabelon.

> [BEMÆRK] Når du bruger enkeltbetalingsgodkendelse som beskrevet i [Udvidede betalinger ved kassen i storefront](./dev-itpro/enhanced-sca.md), skal du i sektionen **Oplysninger om udtjekning** på betalingssiden bekræfte, at containeren i betalingssektionen er placeret sidst. Derved sikres, at alle nødvendige oplysninger indsamles på siden til betaling ved kassen, før handlingerne til endelig betaling og ordreudførelse fuldføres. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Indkøbskurvsmodul](add-cart-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
