---
title: Moduler til bedømmelser og anmeldelser
description: Denne artikel beskriver de vurderinger og vurderingsmoduler, der bruges på siderne med produktdetaljer i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ede42caac78dc48fa6315a2d3c22f1e0f12f0810
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283581"
---
# <a name="ratings-and-reviews-modules"></a>Moduler til bedømmelser og anmeldelser

[!include [banner](includes/banner.md)]

Denne artikel beskriver de vurderinger og vurderingsmoduler, der bruges på siderne med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.

Vurderinger og anmeldelser på e-Commerce-websteder gør det lettere for kunder at få oplysninger om produkter, før de træffer en beslutning om køb, og er også en mekanisme til at indsamle kundefeedback om produkter. 

Vurderinger vises på produktlistesider, sider med kategorilister, søgeresultater og andre sider på webstedet. 

Vurderingshistogrammer og produktanmeldelser vises på PDP'er. Ved hjælp af knappen **Skriv en anmeldelse** kan kunderne sende vurderinger og anmeldelser af et produkt. Disse PDP-funktioner styres af klassifikations- og evalueringsmoduler.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Modul til vurderinger og anmeldelser på produktoplysningssider 

Tre moduler viser oversigten over vurderinger og anmeldelser på produktoplysningssider:
- Modul til skrivning af anmeldelser
- Modul med produktanmeldelseslister
- Vurderingshistogrammodul
 
Følgende illustration viser, hvordan vurderings- og anmeldelsesmodulerne ser ud på en side med produktoplysninger (PDP).

![Moduler til vurderinger og anmeldelser på en produktoplysningsside.](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Yderligere oplysninger om optimering af PDP-skabeloner og -layout med henblik på deling af konfigurationerne til vurderings- og anmeldelsesmoduler mellem flere PDP'er på dit e-handelswebsted, finder du under [Oversigt over skabeloner og layout](templates-layouts-overview.md).

I følgende illustration vises, hvordan dialogboksen **Tilføj modul** viser vurderings- og anmeldelsesmoduler i Dynamics 365 Commerce.
![Dialogboksen Tilføj modul.](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Modul til skrivning af anmeldelser

Modulet til skrivning af anmeldelser omfatter knappen **Skriv en anmeldelse**, der giver brugere mulighed for at logge på, tildele en vurdering og skrive en anmeldelse af et produkt. I dette modul kan brugerne også redigere en vurdering eller en anmeldelse, som de tidligere har sendt. Dette modul vises typisk over modulerne med vurderings- og anmeldelseslister på en produktoplysningsside.
I følgende illustration vises dialogboksen **Skriv en anmeldelse**, der vises, når en kunde vælger **Skriv en anmeldelse**. Kunden kan bruge denne dialogboks til at sende en vurdering og en anmeldelse.

![Dialogboksen Skriv en anmeldelse.](media/rnr-eCommerce-write-review-module.png)

Følgende tabel viser den egenskab for modulet til skrivning af anmeldelser, der skal konfigureres i oprettelsesværktøjet.

| Egenskabsbetegnelse | Værdi        | Beskrivelse af egenskab                 |
|---------------|--------------|--------------------------------------|
| Navn          | Skriv anmeldelse | Navnet på modulet til skrivning af anmeldelse. |

### <a name="ratings-histogram-module"></a>Vurderingshistogrammodul

Vurderingshistogrammodulet viser et histogram over vurderinger. Dette modul vises typisk mellem modulet til skrivning af anmeldelse og modulet med liste over produktanmeldelser på en produktoplysningsside (PDP).
Vurderingshistogrammodulet kræver ingen konfiguration. Du skal blot tilføje modulet i PDP-skabelonen. I følgende illustrationer vises, hvordan en PDP-skabelon ser ud i Dynamics 365 Commerce, når vurderings- og anmeldelsesmoduler er konfigureret til visning på PDP'er.
![PDP-skabelon, når vurderinger og anmeldelser er konfigureret til visning på PDP'er.](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Modul med produktanmeldelseslister

Modulet med lister over produktanmeldelser viser en oversigt over produktanmeldelser sammen med indstillinger for sortering, filtrering og sideinddeling. Dette modul vises typisk efter vurderingshistogrammodulet på en PDP.
Følgende tabel viser de egenskaber for modulet med produktanmeldelseslister, der skal konfigureres i oprettelsesværktøjet.

| Egenskabsbetegnelse              | Værdi | Beskrivelse af egenskab |
|----------------------------|-------| ---------------------|
| Anmeldelser, der vises på hver side | 10    | Det antal anmeldelser, der skal vises ad gangen på en PDP. Knapperne **Næste** og **Forrige** er medtaget, så brugerne kan bevæge sig gennem siderne i en anmeldelse. |

#### <a name="ratings-histogram--summary-view"></a>Vurderingshistogram – oversigtsvisning

Modulet med produktanmeldelseslister indeholder en plads, hvor du kan tilføje et vurderingshistogrammodul. I følgende illustration vises, hvordan du kan tilføje et vurderingshistogrammodul i modulet med produktanmeldelseslister i Dynamics 365 Commerce.

![Tilføje et vurderingshistogrammodul i et modul med produktanmeldelseslister.](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
