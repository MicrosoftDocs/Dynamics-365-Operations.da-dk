---
title: Kampagnebannermodul
description: Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206577"
---
# <a name="promo-banner-module"></a>Kampagnebannermodul

[!include [banner](includes/banner.md)]

Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Kampagnebannermoduler bruges til at vise indbyggede informationsmeddelelser på en side. De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel. 

Kampagnebannermoduler understøtter en sms-besked og et link. Hvis der føjes flere meddelelser til et kampagnebannermodul, bliver det til et roterende banner, hvor du kan gå gennem alle meddelelserne. 

Kampagnebannermoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Anvendelseseksempler på kampagnebannere i e-handel

Kampagnebannere kan bruges i webstedets overskift til at vise kampagner eller meddelelser, der gælder for hele webstedet, som i følgende eksempler.

"Det årlige udsalg slutter om 10 dage"

"Store besparelser på skolestartudsalg. Køb nu".

"Butik for Thanksgiving-SALG!" 

Det følgende billede viser et eksempel på et reklamebanner.

![Eksempel på et reklamebannermodul](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Egenskaber for kampagnebannermodul

| Egenskabsbetegnelse             | Værdi                              | Beskrivende tekst |
|---------------------------|------------------------------------|-------------|
| Bannermeddelelser           | Tekst og link                     | En matrix af tekst og link. |
| Automatisk afspilning                  | **Sand** eller **Falsk**              | En værdi, der angiver, om meddelelser automatisk gennemløbes, hvis der er konfigureret flere meddelelser. |
| Interval for glidende interval | Et antal millisekunder (MS)      | Det interval, der bruges til at gå gennem meddelelser. |
| Tillad afvis             | **Sand** eller **Falsk**              | Hvis værdien er angivet til **Sand**, kan kunderne afvise påmindelsen. |
| Vis karruselslipper     | **Sand** eller **Falsk**              | En værdi, der angiver, om karruselslippere skal vises, så kunder kan gå gennem flere bannerelementer manuelt. |
| Tekstjustering            | **Højre**, **Venstre** eller **Centreret** | Tekstjusteringen i kampangebannermodulet. |
| Binding                      | En URL-adresse                              | URL-adressen for et valgfrit link. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Føj et kampangebannermodul til en ny side 

Hvis du vil føje et kampangebannermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv **Kampagnebannerskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.
1. Under **Sidedisposition** kan du føje et **Standardside** modul til **Brødtekst**-pladsen. 
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den. 
1. Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **Kampangebannermodul**. 
1. Tilføj et containermodul på pladsen **Hoved** på den nye side. 
1. Angiv værdien **Bredde** til **Fyld container** i ruden til højre.
1. Føj et kampangebannermodul til containermodulet under **Sidedisposition**.
1. Tilføj en eller flere bannermeddelelser i indstillingerne for bannermodulet. Hver meddelelse kan have tekst sammen med et link. Du kan redigere de andre egenskaber for at tilpasse modulet yderligere.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Øverst på siden vises en påmindelse med den tekst, du har tilføjet.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

> [!NOTE]
> Et kampagnebanner bruges typisk i sidehovedpladsen eller en underoverskriftplads.


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Karruselmodul](add-carousel.md)

[Tekstblokmodul](add-content-rich-block.md)

[Indholdsblokmodul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]