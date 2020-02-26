---
title: Konfigurere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002191"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurere vurderinger og anmeldelser


[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Vurderinger og anmeldelser på e-handels-websteder gør det lettere for kunder at få oplysninger om produkter, før de træffer en beslutning om køb, fordi de kan se, hvad andre kunder mener om disse produkter. På e-handelswebsteder fungerer vurderinger og anmeldelser også som en mekanisme til indsamling af kundefeedback om produkter. 

Vurderinger vises på produktlistesider, sider med kategorilister, søgeresultater og andre sider på webstedet. Vurderingshistogrammer og produktanmeldelser vises på sider med produktoplysninger (PDP'er). Ved hjælp af knappen **Skriv en anmeldelse** kan kunderne sende vurderinger og anmeldelser af et produkt.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Modul til vurderinger og anmeldelser på produktoplysningssider 

Tre moduler viser oversigten over vurderinger og anmeldelser på produktoplysningssider:

- Modul til skrivning af anmeldelser
- Modul med produktanmeldelseslister
- Vurderingshistogrammodul
 
Følgende illustration viser, hvordan vurderings- og anmeldelsesmodulerne ser ud på en side med produktoplysninger (PDP).

![Modul til vurderinger og anmeldelser på en produktoplysningsside](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Yderligere oplysninger om optimering af PDP-skabeloner og -layout med henblik på deling af konfigurationerne til vurderings- og anmeldelsesmoduler mellem flere PDP'er på dit e-handelswebsted, finder du under [Oversigt over skabeloner og layout](templates-layouts-overview.md).

I følgende illustration vises, hvordan dialogboksen **Tilføj modul** viser vurderings- og anmeldelsesmoduler i Dynamics 365 Commerce.

![Dialogboksen Tilføj modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Modul til skrivning af anmeldelser

Modulet til skrivning af anmeldelser omfatter knappen **Skriv en anmeldelse**, der giver brugere mulighed for at logge på, tildele en vurdering og skrive en anmeldelse af et produkt. I dette modul kan brugerne også redigere en vurdering eller en anmeldelse, som de tidligere har sendt. Dette modul vises typisk over modulerne med vurderings- og anmeldelseslister på en produktoplysningsside.

I følgende illustration vises dialogboksen **Skriv en anmeldelse**, der vises, når en kunde vælger **Skriv en anmeldelse**. Kunden kan bruge denne dialogboks til at sende en vurdering og en anmeldelse.

![Dialogboksen Skriv en anmeldelse](media/rnr-eCommerce-write-review-module.png)

Følgende tabel viser den egenskab for modulet til skrivning af anmeldelser, der skal konfigureres i oprettelsesværktøjet.

| Egenskabsbetegnelse | Værdi        | Beskrivelse af egenskab                 |
|---------------|--------------|--------------------------------------|
| Navn          | Skriv anmeldelse | Navnet på modulet til skrivning af anmeldelse. |

### <a name="ratings-histogram-module"></a>Vurderingshistogrammodul

Vurderingshistogrammodulet viser et histogram over vurderinger. Dette modul vises typisk mellem modulet til skrivning af anmeldelse og modulet med liste over produktanmeldelser på en produktoplysningsside (PDP).

Vurderingshistogrammodulet kræver ingen konfiguration. Du skal blot tilføje modulet i PDP-skabelonen. 

I følgende illustrationer vises, hvordan en PDP-skabelon ser ud i Dynamics 365 Commerce, når vurderings- og anmeldelsesmoduler er konfigureret til visning på PDP'er.

![PDP-skabelon, når vurderinger og anmeldelser er konfigureret til visning på PDP'er](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Modul med produktanmeldelseslister

Modulet med lister over produktanmeldelser viser en oversigt over produktanmeldelser sammen med indstillinger for sortering, filtrering og sideinddeling. Dette modul vises typisk efter vurderingshistogrammodulet på en PDP.

Følgende tabel viser de egenskaber for modulet med produktanmeldelseslister, der skal konfigureres i oprettelsesværktøjet.

| Egenskabsbetegnelse              | Værdi | Beskrivelse af egenskab |
|----------------------------|-------| ---------------------|
| Anmeldelser, der vises på hver side | 10    | Det antal anmeldelser, der skal vises ad gangen på en PDP. Knapperne **Næste** og **Forrige** er medtaget, så brugerne kan bevæge sig gennem siderne i en anmeldelse. |

#### <a name="ratings-histogram--summary-view"></a>Vurderingshistogram – oversigtsvisning

Modulet med produktanmeldelseslister indeholder en plads, hvor du kan tilføje et vurderingshistogrammodul. I følgende illustration vises, hvordan du kan tilføje et vurderingshistogrammodul i modulet med produktanmeldelseslister i Dynamics 365 Commerce.

![Tilføje et vurderingshistogrammodul i et modul med produktanmeldelseslister](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurere et websted til visning af vurderinger og anmeldelser

Konfigurationsværdier for vurderinger og anmeldelser, f.eks. leje-ID, anmeldelsers tekstlængde og længden af titler på anmeldelser, konfigureres på webstedsniveau. 

Udfør følgende trin for at konfigurere et websted til at vise vurderinger og anmeldelser. 

1. Gå til **Startside \> Websteder**.
1. Vælg navnet på dit websted. 
1. Gå til **Administration af websted \> Udvidelsesmuligheder**. 
1. Angiv det maksimale antal tegn som anmeldelsesteksten må have (f.eks. **1000**) i feltet **Anmeldelsens maksimale tekstlængde**. 
1. Angiv det maksimale antal tegn som anmeldelsestitler må have (f.eks. **55**) i feltet **Maksimal længde af anmeldelsestitel**. 
1. Vælg **Gem og udgiv**. 

I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.

![Konfiguration af et websted til visning af vurderinger og anmeldelser](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Sammenkæde en produktvurdering med anmeldelsessektionen på en PDP

En produktvurdering vises under produkttitlen øverst på PDP. Produktvurderingen kan konfigureres, så den sammenkædes med sektionen **Anmeldelser** på samme PDP. 

Hvis du vil knytte en produktvurdering til sektionen **Anmeldelser** på PDP'en, skal du følge disse trin.

1. Åbn PDP-skabelonen. 
1. Gå til **Indstillinger for købefeltcontainermodul**.
1. Vælg **Produktvurderinger** under **Købefelt**, og markér derefter afkrydsningsfeltet **Sammenkæd klik til modul med hele anmeldelsen**.

I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.

![Sammenkædning af en produktvurdering med anmeldelsessektionen på en PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurere linket til siden til beskyttelse af personlige oplysninger og politik

Følg disse trin for at konfigurere linket til siden om beskyttelse af personlige oplysninger og politik.

1. Gå til **Startside \> Websteder**.
1. Vælg navnet på dit websted. 
1. Gå til **Administration af websted \> Udvidelsesmuligheder**.
1. Vælg **Tilføj et link** under **RNR - beskyttelse af personlige oplysninger og politik** under fanen **Ruter**. Hvis der allerede er angivet et link, og du vil erstatte det, skal du markere linket. 
1. Vælg linket til siden om beskyttelse af personlige oplysninger og politik i dialogboksen **Tilføj et link**, og vælg derefter **OK**. 
1. Vælg **Gem og udgiv**. 

I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.

![Konfiguration af linket til siden til beskyttelse af personlige oplysninger og politik](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)
