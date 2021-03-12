---
title: Oversigt over teknisk ændringsstyring
description: Dette emne giver en oversigt over teknisk ændringsstyring, som hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b081cd8d56217b8cf76db824c29482d453fc9ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001942"
---
# <a name="engineering-change-management-overview"></a>Oversigt over teknisk ændringsstyring

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Oversigt over funktioner

Moderne producenter kræver omfattende administration af produktdata, versionsstyring og styring af teknisk ændring for at opnå succes i en verden med konstant kortere produktlivscyklusser, højere kvalitets- og pålidelighedskrav og større fokus på produktsikkerhed.

Styring af tekniske ændringer bringer strukturen og disciplinen til administrationsprocessen for produktdata og gør det muligt at definere, frigive og revidere produkter på en kontrolleret måde, der understøttes af arbejdsprocesser. Ved hjælp af produktversioner og styring af tekniske ændringer kan du dokumentere, vurdere virkningen af og anvende tekniske ændringer under hele et produkts livscyklus.

Teknisk ændringsstyring hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer. Her er en oversigt over dens hovedfunktioner:

- Produktversioner
- Forbedrede produktudgivelsesfunktioner, der giver dig mulighed for at vedligeholde produktmasterdata i én juridisk enhed (den tekniske virksomhed) og publicere det fuldt konfigurerede, frigivne produkt til andre juridiske enheder
- Regler for validering af, at nødvendige oplysninger angives, før en produktversion aktiveres (parathedskontrol)
- Forbedret administration af produktets levetid med detaljeret styring af, hvornår et frigivet produkt kan bruges i bestemte forretningsprocesser
- Tekniske ændringsanmodninger, der understøttes af arbejdsprocesser
- Tekniske ændringsordrer, der understøttes af arbejdsprocesser

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Den foregående video ([Styring af ændringer i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="turn-on-engineering-change-management-for-your-system"></a>Aktivere styring af tekniske ændringer for systemet

Du skal først aktivere styring af tekniske ændringer ved at følge disse trin.

1. Gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Søg efter opdateringer.
1. Aktivér den funktion, der hedder **Teknisk ændringsstyring**.

Derefter skal du aktivere **Teknisk ændringsstyring**-konfigurationsnøglen ved at følge disse trin.

1. Sæt systemet i vedligeholdelsestilstand som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
1. Udvid **Handel**-noden, og markér afkrydsningsfeltet **Teknisk ændringsstyring**.
1. Slå vedligeholdelsestilstand fra som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
