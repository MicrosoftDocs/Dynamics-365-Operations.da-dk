---
title: Påmindelsesmodul
description: Dette emne omhandler påmindelsesmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785346"
---
# <a name="alert-module"></a>Påmindelsesmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler påmindelsesmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et påmindelsesmodul bruges til at vise indbyggede informationsmeddelelser på en side. Påmindelsesmoduler understøtter en sms-besked og et link. De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel. 

Påmindelsesmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Eksempler på påmindelsesmoduler i e-handel

Påmindelsesmoduler kan bruges i webstedets sidehoved til at angive kampagner eller meddelelser for hele webstedet. Her er nogle eksempler:

"Det årlige udsalg slutter om 10 dage"

"Store besparelser på skolestartudsalg. Køb nu".

## <a name="alert-module-properties"></a>Egenskaber for påmindelsesmodul

| Egenskabsbetegnelse  | Værdi                              | Beskrivelse |
|----------------|------------------------------------|-------------|
| Tekst           | Tekst                               | Den tekstmeddelelse, der vises i påmindelsesmodulet. |
| Tekstjustering | **Højre**, **Venstre** eller **Centreret** | En værdi, der definerer, hvordan tekst justeres i påmindelsesmodulet. |
| Påmindelse for afvisning  | **Sand** eller **Falsk**              | Hvis værdien er angivet til **Sand**, kan kunden afvise påmindelsen. |
| Binding           | URL-adresse                                | URL-adressen for et valgfrit link. |

## <a name="add-an-alert-module-to-a-page"></a>Føj et påmindelsesmodul til en side 

Hvis du vil føje et påmindelsesmodul til en side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **påmindelsesskabelon**.
1. Tilføj et påmindelsesmodul på pladsen **Hoved** på standardsiden.
1. Tjek skabelonen ind, og publicer den. 
1. Brug den påmindelsesskabelon, som du netop har oprettet, til at oprette en side med navnet **påmindelsesside**. 
1. Tilføj et påmindelsesmodul på pladsen **Hoved** på den nye side.
1. Angiv påmindelsesteksten i indstillingerne for påmindelsesmodulet. Du kan redigere de andre egenskaber, hvis du vil tilpasse påmindelsesmodulet yderligere.
1. Gem siden, og se en forhåndsvisning af den. Øverst på siden kan du se en påmindelse med den tekst, du har tilføjet.
1. Tjek siden ind, og publicer den. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Karruselmodul](add-carousel.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-modul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
