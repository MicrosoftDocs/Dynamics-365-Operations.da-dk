---
title: Betalingsmodul
description: I dette emne beskrives det, hvordan du føjer et købefeltmodul til en side og angiver de påkrævede egenskaber.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697077"
---
# <a name="checkout-module"></a>Betalingsmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives det, hvordan du føjer et købefeltmodul til en side og angiver de påkrævede egenskaber.

## <a name="overview"></a>Oversigt

Et betalingsmodul er en særlig container, der er vært for alle de moduler, som skal bruges til at oprette en ordre. Et betalingsmodul kan omfatte moduler, der håndterer leveringsadressen, leveringsmetoderne, faktureringsoplysningerne, ordreoversigten og andre oplysninger, der er relateret til en kundeordre. Den indeholder en trinvis proces, som en kunde bruger til at angive alle de relevante oplysninger for at foretage et køb.

Et betalingsmodul gengiver data på basis af indkøbsvogn-id'et. Dette indkøbsvogn-id gemmes som en browsercookie. Der kræves et indkøbsvogn-id for at gengive oplysninger i betalingsmodulet, f. eks. varerne i ordren, det samlede beløb og rabatterne.

## <a name="checkout-module-properties"></a>Egenskaber for betalingsmodul

Et betalingsmodul indeholder et sæt moduler, som det er vært for. En breddeegenskab giver dig mulighed for at angive, om elementerne i betalingsmodulet skal tilpasses dets bredde eller udfylde skærmen.

Et betalingsmodul har flere pladser, f.eks. pladsen **Betalingsoplysninger**, pladsen **Ordreoversigt** og pladsen **Afgiv ordre**. Hver plads understøtter et sæt moduler, der vises i et bestemt layout på siden. Pladsen **Betalingsoplysninger** indeholder f.eks. alle de moduler, der kræves for at udløse en betaling, f. eks. moduler for leveringsadressen og betalingsmåden. Pladsen **Ordreoversigt** viser en ordreoversigt og understøtter handlingen til afgivelse af ordren. Pladsen **Afgiv ordre** understøtter ligeledes handlingen til afgivelse af ordren. Ordreafgivelsesmoduler kan defineres på to pladser for at optimere processen til ordreafgivelse fra forskellige platforme.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduler, der kan bruges i betalingsmodulet

- **Leveringsadresse** – dette modul giver en kunde mulighed for at tilføje eller vælge en leveringsadresse for en ordre. Hvis kunden er logget på, vises eventuelle adresser, der tidligere er blevet gemt for den pågældende kunde. Kunden kan derefter vælge blandt disse adresser. Kunden kan også tilføje en ny adresse. Leveringsadressen bruges til alle varer i ordren, der kræver levering. Den kan ikke tilpasses for individuelle linjevarer. Der er defineret leveringsadresseformater for hvert land eller område, og dette modul gennemtvinger de lande-/områdespecifikke regler. Selvom dette modul ikke indeholder adressevalidering, kan adressevalidering implementeres ved hjælp af tilpasning. Hvis ordren kun omfatter varer, der afhentes i butikken, skjules dette modul automatisk.
- **Leveringsindstillinger** – dette modul giver en kunde mulighed for at vælge en leveringsindstilling for en ordre. Leveringsindstillingerne er baseret på leveringsadressen. Hvis leveringsadressen ændres, skal leveringsindstillingerne hentes igen. Hvis ordren kun omfatter varer, der afhentes i butikken, skjules dette modul automatisk.
- **Container til betalingssektion** – dette modul er en container, hvor du kan placere flere moduler for at oprette en sektion i betalingsprocessen. Du kan f. eks. indsætte alle betalingsrelaterede moduler i denne container for at få dem vist som én sektion. Dette modul påvirker kun processens layout.
- **Gavekort** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af et gavekort. Den understøtter kun Microsoft Dynamics 365 Commerce-gavekort. Der kan anvendes ét eller flere gavekort til en ordre. Hvis gavekortets saldoen ikke dækker beløbet i indkøbsvognen, kan gavekortet kombineres med en anden betalingsmåde. Gavekort kan kun indløses, hvis kunden er logget på.
- **Fordelskundepoint** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af fordelskundepoint. Den giver en oversigt over tilgængelige point og udløbssteder, og giver kunden mulighed for at vælge det antal point, der skal indløses. Hvis kunden ikke er logget på eller ikke er fordelskunde, eller hvis det samlede beløb i indkøbsvognen er 0 (nul), skjules dette modul automatisk.
- **Kreditkort** – dette modul giver en kunde mulighed for at betale en ordre ved hjælp af et kreditkort. Hvis det samlede beløb i indkøbsvognen dækkes af fordelskundepoint eller et gavekort, eller hvis det er 0 (nul), skjules dette modul automatisk. Integration af kreditkort leveres af Adyen-betalingsconnectoren. Yderligere oplysninger om, hvordan denne connector bruges, finder du ved at gå til [Adyen Payment Connector](https://).
- **Faktureringsadresse** – dette modul giver en kunde mulighed for at angive faktureringsoplysninger. Disse oplysninger behandles sammen med kreditkortoplysningerne af Adyen. Dette modul omfatter en indstilling, som gør det muligt for kunderne at bruge deres faktureringsadresse som leveringsadresse.
- **Kontaktoplysninger** – dette modul giver en kunde mulighed for at tilføje eller ændre kontaktoplysningerne (mailadressen) for en ordre.
- **Afgiv ordre** – dette modul giver en kunde mulighed for at afgive en ordre.
- **Indholdsrig blok** – dette modul indeholder alle de meddelelser, der styres af CMS (Content Management System). Det kan f. eks. indeholde meddelelsen "Kontakt 1-800-FABRIKAM", hvis der er problemer med ordren". 
- **Ordreoversigt** – dette modul viser omkostningsfordelingen for en ordre.
- **Ordrelinjevarer** – dette modul viser en oversigt over de varer, der medtages i en ordre.

## <a name="retail-server-interaction"></a>Interaktion med Retail Server

De fleste betalingsoplysninger, f. eks. leveringsadressen og leveringsmåden, gemmes i indkøbsvognen og behandles som en del af ordren. Den eneste undtagelse er kreditkortoplysningerne. Disse oplysninger behandles direkte ved hjælp af Adyen-betalingsconnectoren. Betalingen er godkendt, men opkræves ikke.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Føje et betalingsmodul til en ny side og angive de påkrævede egenskaber

Hvis du vil føje et betalingsmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Fragment \> Nyt fragment**, og navngiv det nye fragment **Betalingsfragment**.
1. Føj et betalingsmodul til fragmentet.
1. Føj en overskrift til betalingsmodulet.
1. Tilføj leveringsadresse-, leveringsindstillinger- og container til betalingssektion-modulerne på pladsen **Betalingsoplysninger**. Der er nu fire sektioner på pladsen **Betalingsoplysninger**.
1. Tilføj gavekort-, fordelskundepoint og kreditkortmodulerne i betalingssektionen. På denne måde sikrer du dig, at alle betalingsmåderne vises sammen i en sektion.
1. På pladsen **Ordreoversigt** kan du tilføje ordreoversigt-, afgiv ordre- og indholdsrig blok-modulerne.
1. Tilføj følgende tekst i indholdsrig blok-modulet: **Kontakt 1-800-FABRIKAM", hvis der er problemer med ordren.**
1. Tilføj et afgiv ordre-modul på pladsen **Ordreoversigt**.
1. Vælg **Gem**. Nogle moduler gengives muligvis ikke i eksemplet, fordi de ikke har en indkøbsvognkontekst.
1. Tjek fragmentet ind, og publicer det.
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
