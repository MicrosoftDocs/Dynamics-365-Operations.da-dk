---
title: Anvende visningsindstillinger for produktdimensioner
description: I dette emne beskrives visningsindstillingerne for produktdimensioner, og det beskrives, hvordan de anvendes i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80a0861c51ea14ddb6bce02d757667adac34e740cd04311e26211d9bdbae4ed8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716216"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Anvende visningsindstillinger for produktdimensioner

[!include [banner](includes/banner.md)]


I dette emne beskrives visningsindstillingerne for produktdimensioner, og det beskrives, hvordan de anvendes i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce understøtter størrelses-, typografi- og farvedimensioner for at skelne mellem produktvarianter. Dimensioner vises typisk som tekstværdier, for eksempel "Lille", "Mellem" og "Stor" for størrelser og "Sort" og "Brun" for farver. Men hvis et produkt understøtter mange variationer, kan det være vanskeligt at gennemse produktvarianter, da der skal foretages flere valg for at få vist billedet for de enkelte varianter. For at gøre det nemmere at gennemse produktvarianter kan version 10.0.20 af Commerce bruge billeder og hexadecimale (hex) koder til at vise dimensioner som prøver.

I Commerce-webstedsgenerator er dimensionsindtillingerne defineret i **Indstillinger for websted \> Udvidelser \> Dimensionsindstillinger**. I følgende illustration vises et eksempel på dimensionsindstillinger i webstedsgeneratoren.

![Eksempel på webstedsindstillinger i Commerce-webstedsgenerator.](./dev-itpro/media/swatch_site_settings.PNG)

Der er to tilgængelige dimensionsindstillinger:

- **Dimensioner, der skal vises som billede** – Angiv, hvilke dimensioner der skal vises som prøver på e-handelswebstedssider, for eksempel sider med produktoplysninger (PDP'er) og sider med lister over søgeresultater. Enhver kombination af farve-, størrelses- og typografidimensioner kan vises som en prøve. Hvis der vælges en dimension til visning som en prøve, søger Commerce-modulgengivelse efter en tilgængelig konfiguration af en hexkodeprøve. Hvis der ikke er konfigureret en hexkode, søger systemlogik efter en konfiguration af billedets URL-adresse til prøven. Hvis der hverken er konfigureret en hexkode eller en URL-adresse til et billede, vises der tekst.

    I følgende illustration vises et eksempel, hvor en PDP på et e-handelswebsted inkluderer farve- og størrelsesprøver. I dette eksempel konfigureres en hexkode for farvedimensionen. Derfor vises prøver som farver. Der er dog hverken konfigureret en hexkode eller en URL-adresse til et billede til størrelsesdimensionen. Derfor vises der tekst.

    ![Eksempel på den farvedimension, der vises som prøver på en side med oplysninger om e-handelsprodukter.](./dev-itpro/media/swatch_pdp.png)

- **Dimensioner, der skal vises på produktkortet** – Angiv, hvilke dimensioner der skal vises på produktkort, der vises på lister og på listesider. Før en dimension kan vises på et produktkort, skal denne indstilling aktiveres for den pågældende dimension. Indstillingen **Dimensioner, der skal vises som billede** skal også aktiveres. Funktionsmåden for valgt prøve på produktkort er optimeret til farvedimensionen. I forbindelse med andre dimensioner kan det være nødvendigt med en visningsudvidelse for at tilpasse funktionsmåden for valgt prøve.

    I følgende illustration vises et eksempel, hvor en listeside på et e-handelswebsted indeholder produktkort, der indeholder farveprøver.

    ![Eksempel på den farvedimension, der vises som prøver på en side med en e-handelsliste.](./dev-itpro/media/swatch_searchresults.PNG)

Du kan finde oplysninger om, hvordan du konfigurerer produktdimensioner, så de vises som prøver på webstedssider, under [Konfigurere produktdimensionsværdier, der skal vises som prøver](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Modul til søgeresultater](search-result-module.md)

[Boksmodul til køb](add-buy-box.md)

[Konfigurere produktdimensionsværdier, der skal vises som prøver](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
