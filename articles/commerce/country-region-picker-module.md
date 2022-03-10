---
title: Modul til pluk af land/område
description: Dette emne omhandler plukmoduler til land/område og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
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
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 1a8eebb589372051272573895a0ae5b4203eef62
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109775"
---
# <a name="countryregion-picker-module"></a>Modul til pluk af land/område

[!include [banner](includes/banner.md)]

Dette emne omhandler plukmoduler til land/område og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

I modulet til plukker af land/område bruges [registrerings- og omdirigerelsesfunktionen](geo-detection-redirection.md) i Dynamics 365 Commerce til at vise anbefalede URL-adresser til kunder, der anmoder om en URL-adresse til e-handelswebstedet, der ikke er tilknyttet deres land eller område.

En kunde i Canada anmoder f.eks. om en URL-adresse til webstedet, som ikke er knyttet til Canada. I dette tilfælde viser modulet til valg af land/region en dialogboks, hvor du anbefales URL-adresser til websteder, der er tilknyttet Canada. I følgende illustration vises et eksempel på dialogboksen pluk land/område.

![Eksempel på en dialogboks til pluk af land/område på en startside.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Modulegenskaber til pluk af land/område

| Egenskabsbetegnelse              | Værdi       | Betegnelse |
| -------------------------- | ----------- | ----------- |
| Overskrift                    | Tekst        | Den overskrift, der vises øverst i dialogboksen. |
| Underoverskrift                 | Tekst        | Underoverskriften, der vises under overskriften. |
| Land: Visningsstreng    | Tekst        | Det viste navn for en URL-indstilling (f.eks. "Canada"). |
| Land: Visningsunderstreng | Tekst        | En valgfri visningsunderstreng til en URL-indstilling (f.eks. "Engelsk" eller "Fransk"). |
| Land: Billede af land     | Medieaktiv | Et valgfrit billede, der er knyttet til en URL-indstilling (f.eks. et billede af det canadiske flag). |
| Land: URL-adresse for land       | Tekst        | Den URL-adresse, der svarer til den kanal og landeindstilling, der er konfigureret for landet eller området på siden **Kanaler** i Commerce Site Builder (**Webstedsindstillinger \> Kanaler**). Denne URL-adresse skal være nøjagtig den samme som den URL-adresse, der er konfigureret på siden **Kanaler**. |
| Handlingslink                | Handlingslink | Et valgfrit link, der vises nederst i dialogboksen. Dette link kan f.eks. pege på en intern side med en liste over alle lande og områder, som webstedet understøtter. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Tilføj et modul til pluk af land/område på en side

Modulet til plukker for land/region kan føjes til hovedmodulet enten direkte eller via et delt modul. Yderligere oplysninger om sidehovedmoduler finder du i [Sidehovedmodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurere modulet til plukker for land/region i Commerce site builder

> [!NOTE]
> De URL-adresser, du anbefaler til kunderne, skal konfigureres som landeobjekter i modulet til lande-/områdeplukkere.

For hver URL-adresse, du vil vise og anbefale til kunder, skal du følge disse trin i Commerce Site Builder.

1. Vælge plads til modul til pluk af land/område.
1. Vælg Tilføj land under **Tilføj land** i egenskabsruden **Landeliste**.
1. Vælg det nye felt **Land**.
1. I feltet **Vis streng** skal du angive et visningsnavn (f.eks. **Canada**).
1. Valgfrit: I feltet **Vis understreng** skal du angive en understring for visning (f.eks. **fransk** eller **fr-ca**).
1. Valgfrit: Vælg et billede fra mediebiblioteket.
1. Skriv URL-adresse i feltet **Lande-URL**. Denne URL-adresse skal være nøjagtig den samme som den URL-adresse, der vises på siden **Kanaler**, og som er knyttet til kanalen, herunder den landestandard, der er tilknyttet til landet eller området.
1. Vælg **OK**.
1. Gentag disse trin for alle de andre URL-adresser i landet, som modulet til plukker af land/område skal vises i.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere registrering og omdirigeret registrering](geo-detection-redirection.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Sidehovedmodul](author-header-module.md)

[Webstedsvælgermodul](site-selector.md)

[Brødkrummemodul](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
