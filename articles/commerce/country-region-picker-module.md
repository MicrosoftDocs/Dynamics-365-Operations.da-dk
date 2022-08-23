---
title: Modul til pluk af land/område
description: Denne artikel omhandler plukmoduler til land/område og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 203a8e17e075f15b7ae3cceb98d24ced75539a01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270285"
---
# <a name="countryregion-picker-module"></a>Modul til pluk af land/område

[!include [banner](includes/banner.md)]

Denne artikel omhandler plukmoduler til land/område og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.

I vælgermodulet til land/område bruges [registrerings- og omdirigeringsfunktionen](geo-detection-redirection.md) i Dynamics 365 Commerce til at vise anbefalede websteder til kunder, der anmoder om en URL-adresse til e-handelswebstedet, der ikke er tilknyttet deres land eller område.

En kunde i Canada anmoder f.eks. om en URL-adresse til webstedet, som ikke er knyttet til noget andet land end Canada. I dette tilfælde viser modulet til valg af land/region en dialogboks, hvor du anbefales URL-adresser til websteder, der er tilknyttet Canada. 

## <a name="how-it-works"></a>Sådan fungerer det

Når geografisk registrering og omdirigering aktiveres for et websted, og en kunde anmoder om en URL-adresse til webstedet, bliver det land, der er registreret for kunden, og den URL-adresse, de har anmodet om, brugt til at finde ud af, om URL-adressen er knyttet til det land, hvor kunden er. Tilknytningen mellem URL-adresser og lande defineres på siden **Kanaler** under **Indstillinger for websted** i Commerce-webstedsgenerator. 

Hvis URL-adressen til anmodningen ikke stemmer overens med en URL-adresse, der er knyttet til kundens land, returneres listen over en eller flere URL-adresser, der er knyttet til landet, i svaret. Lande-/områdevælgeren sammenligner hver URL-adresse på den pågældende liste med de URL-adresser, der er konfigureret i modulet land/område. For hvert nøjagtigt match, der findes, viser lande-/områdevælgeren visningsoverskriften, underoverskriften og billedet for den pågældende URL-adresse, og hyperlinks til disse elementer ved hjælp af URL-adressen.

Når en kunde angiver en indstilling i vælgeren for land/område, føres de til URL-adressen i hyperlinket. Denne URL-adresse skrives til cookien **\_msdyn365\_\_\_site\_**, så den kan bruges som kundens præference for websted. Næste gang kunden anmoder om den URL-adresse, som ikke er tilknyttet deres land eller område, bliver kunden automatisk omdirigeret til sit foretrukne land. Det anbefales derfor, at du også bruger [webstedsvælgermodulet](site-selector.md) på dit e-handelswebsted, så kunderne kan tilsidesætte eller opdatere deres præference for websted. 

Hvis en kunde lukker vælgerdialogboksen til land/område, skrives der ingen cookies, og kunden forbliver på det aktuelle websted. 

I følgende illustration vises et eksempel på dialogboksen pluk land/område.

![Eksempel på en dialogboks til pluk af land/område på en startside.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Modulegenskaber til pluk af land/område

| Egenskabsbetegnelse              | Værdi       | Betegnelse                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Overskrift                    | Tekst        | Den overskrift, der vises øverst i dialogboksen.       |
| Underoverskrift                 | Tekst        | Underoverskriften, der vises under overskriften.               |
| Land: Visningsstreng    | Tekst        | Det viste navn for en URL-indstilling (f.eks. "Canada").   |
| Land: Visningsunderstreng | Tekst        | En valgfri visningsunderstreng til en URL-indstilling (f.eks. "Engelsk" eller "Fransk"). |
| Land: Billede af land     | Medieaktiv | Et valgfrit billede, der er knyttet til en URL-indstilling (f.eks. et billede af det canadiske flag). |
| Land: URL-adresse for land       | Tekst        | URL-adressen på webstedet for det land/område, der konfigureres. Denne URL-adresse skal være nøjagtig den samme som den URL-adresse, du har angivet for dette land/område på siden **Kanaler** under **Indstillinger for websted** i Commerce-webstedsgenerator. Desuden skal domænet for URL-adressen være det brugerdefinerede domæne, der er angivet i feltet **Match domæne** på siden **Kanaler**, ikke arbejdsadressen på det websted, som Commerce leverer, når du opretter dit e-handelsmiljø (f.eks. URL-adressen `https://<yourcompany>.commerce.dynamics.com/`). |
| Handlingslink                | Handlingslink | Et valgfrit link, der vises nederst i dialogboksen. Dette link kan f.eks. pege på en intern side med en liste over alle lande og områder, som webstedet understøtter. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Tilføj et modul til pluk af land/område på en side

Modulet til plukker for land/region kan føjes til hovedmodulet enten direkte eller via et delt modul. Yderligere oplysninger om sidehovedmoduler finder du i [Sidehovedmodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurere modulet til plukker for land/region i Commerce site builder

> [!NOTE]
> De URL-adresser, du anbefaler til kunderne, skal konfigureres som landeobjekter i modulet til lande-/områdeplukkere.

For hvert websteds URL-adresse, som du vil vise og anbefale til kunder, skal du følge disse trin i Commerce-webstedsgenerator.

1. Vælge plads til modul til pluk af land/område.
1. Vælg Tilføj land under **Tilføj land** i egenskabsruden **Landeliste**.
1. Vælg det nye felt **Land**.
1. I feltet **Vis streng** skal du angive et visningsnavn (f.eks. **Canada**).
1. Valgfrit: I feltet **Vis understreng** skal du angive en understring for visning (f.eks. **fransk** eller **fr-ca**).
1. Valgfrit: Vælg et billede fra mediebiblioteket.
1. Skriv URL-adresse i feltet **Lande-URL**. Denne URL-adresse skal være nøjagtig den samme som den URL-adresse, der vises på siden **Kanaler**, og som er knyttet til kanalen, herunder den landestandard, der er tilknyttet landet eller området. 
1. Vælg **OK**.
1. Gentag disse trin for alle de andre URL-adresser i landet, som modulet til plukker af land/område skal vises i.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere registrering og omdirigeret registrering](geo-detection-redirection.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Sidehovedmodul](author-header-module.md)

[Webstedsvælgermodul](site-selector.md)

[Brødkrummemodul](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
