---
title: Kampagnebannermodul
description: Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025614"
---
# <a name="promo-banner-module"></a>Kampagnebannermodul


[!include [banner](includes/banner.md)]

Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Kampagnebannermoduler bruges til at vise indbyggede informationsmeddelelser på en side. De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel. 

Kampagnebannermoduler understøtter en sms-besked og et link. Hvis der føjes flere meddelelser til et kampagnebannermodul, bliver det til et roterende banner, hvor du kan gå gennem alle meddelelserne. 

Kampagnebannermoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Anvendelseseksempler på kampagnebannere i e-handel

Kampagnebannere kan bruges i webstedets overskift til at vise kampagner eller meddelelser, der gælder for hele webstedet, som i følgende eksempler.

"Det årlige udsalg slutter om 10 dage"

"Store besparelser på skolestartudsalg. Køb nu".

## <a name="promo-banner-module-properties"></a>Egenskaber for kampagnebannermodul

| Egenskabsnavn             | Value                              | Beskrivelse |
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

1. Opret en sideskabelon med navnet **Kampangebannerskabelon**.
1. Under **Sidedisposition**kan du føje et **Standardside**modul til **Brødtekst**-pladsen. 
1. Tjek skabelonen ind, og publicer den. 
1. Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **Kampangebannermodul**. 
1. Tilføj et containermodul på pladsen **Hoved** på den nye side. 
1. Angiv værdien **Bredde** til **Fyld container** i ruden til højre.
1. Føj et kampangebannermodul til containermodulet under **Sidedisposition**.
1. Tilføj en eller flere bannermeddelelser i indstillingerne for bannermodulet. Hver meddelelse kan have tekst sammen med et link. Du kan redigere de andre egenskaber for at tilpasse modulet yderligere.
1. Gem siden, og se en forhåndsvisning af den. Øverst på siden vises en påmindelse med den tekst, du har tilføjet.
1. Afslut redigeringen af siden, og udgiv den. 

> [!NOTE]
> Et kampagnebanner bruges typisk i sidehovedpladsen eller en underoverskriftplads.


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Karruselmodul](add-carousel.md)

[Tekstblokmodul](add-content-rich-block.md)

[Indholdsblokmodul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
