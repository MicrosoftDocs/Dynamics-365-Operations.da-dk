---
title: Modulet Social deling
description: Dette emne omhandler moduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795351"
---
# <a name="social-share-module"></a>Modul til deling på sociale medier

[!include [banner](includes/banner.md)]

Dette emne omhandler moduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Med moduler til social deling kan brugerne dele URL-adresser på et e-handels-websted på sociale medier som Facebook, Twitter, Pinterest og LinkedIn. URL-adresser til websider kan også deles via mail. Moduler til social deling bruges ofte på sider med produktoplysninger (PDP-filer), som hjælper brugerne med at dele produktoplysninger.

Hvert modul til social deling er en container for elementmoduler til social deling. Hvert elementmodul til social deling kan konfigureres til at pege på et bestemt websted med sociale medier. Integration med Facebook, Twitter, Pinterest, LinkedIn og mail understøttes som standard. Når en bruger af webstedet vælger et socialt mediesymbol, startes en HTML-IFrame for det pågældende websted med sociale medier. I iFrame kan brugeren logge på og bogføre sideindholdet, som de fik vist.

De enkelte sociale medieplatforme kan registrere cookies, så dette modul kræver, at brugerne af webstedet accepterer beskeden om samtykke til cookie. Når cookie-samtykke ikke accepteres, vil modulet være skjult på siden. Du kan få flere oplysninger under [Cookieoverholdelse](cookie-compliance.md).

I følgende illustration fremhæves et eksempel på et modul til social deling, der bruges på en side med produktdetaljer.

![Eksempel på et modul til social deling](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Egenskaber for modul til social deling

| Egenskabsbetegnelse             | Værdi                 | Beskrivelse |
|---------------------------|-----------------------|-------------|
| Overskrift                  | Tekst | Denne egenskab angiver en titel til modulet. |
| Retning | **Lodret** eller **Vandret**  | Denne egenskab definerer layoutretningen for sociale mediers elementer. |

## <a name="social-share-item-module-properties"></a>Egenskaber for elementmodul til social deling
| Egenskabsbetegnelse             | Værdi                 | Beskrivelse |
|---------------------------|-----------------------|-------------|
| Sociale medier              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail** | En rullemenu med en liste over sociale mediers platforme. |
| Ikon |Billede    | Dette er det billede, der vil blive vist for de respektive sociale medier. Som bedste fremgangsmåde kan du se sociale medieplatformes SDK for at få det anbefalede billede til hver platform. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Tilføje et modul til social deling i et købefeltmodul

Følg disse trin for at tilføje et modul til social deling i et købefeltmodul.

1. Vælg **Sider** på webstedet Fabrikam, og vælg derefter siden **DefaultPDP** for at åbne siden med produktdetaljer. 
1. På pladsen **Købefelt (påkrævet)** skal du vælge ellipsen (**...**) og derefter vælge **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Social deling** og derefter **OK**.
1. På pladsen **Social deling** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **SocialShare** og derefter **OK**.
1. Vælg **Vandret** under **Retning** i ruden Egenskaber for modulet **SocialShare**. Tilføj eventuelt en billedtekst.
1. På pladsen **SocialShare** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **SocialShareItem** og derefter **OK**.
1. I ruden Egenskaber for modulet **SocialShareItem** skal du under **Sociale medier** vælge **Facebook**.
1. I ruden Egenskaber for modulet **SocialShareItem** skal du under **Ikon** vælge **+ Tilføj et billede**.
1. I dialogboksen **Medievælger** skal du vælge Facebook-logobilledet og derefter **OK**. Hvis der ikke findes et Facebook-logo, skal du vælge **Upload nyt medieelement** for at uploade det.
1. Tilføj og konfigurer yderligere **SocialShareItem**-moduler efter behov.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Siden viser modulet til social deling.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Cookieoverholdelse](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]