---
title: Oversigt over teknisk ændringsstyring
description: Dette emne giver en oversigt over teknisk ændringsstyring, som hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947514"
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

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Aktivere funktionerne til styring af tekniske ændringer og versionsdimension for systemet

Før du kan bruge styring af tekniske ændringer, skal du aktivere både funktionen *Styring af tekniske ændringer* og dens konfigurationsnøgle. Hvis du også vil spore versionsdimensionen for produkter i transaktioner (valgfrit), skal du også aktivere funktionen *Produktversionsdimension* og dens konfigurationsnøgle.

Du skal først aktivere disse funktioner ved at følge disse trin.

1. Gå til arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Søg efter opdateringer.
1. Aktivér den funktion, der hedder **Teknisk ændringsstyring**.
1. Hvis du vil bruge den, skal du også aktivere funktionen med navnet **Produktdimensionsversion**.

Du skal derefter aktivere konfigurationsnøglerne ved at følge disse trin.

1. Sæt systemet i vedligeholdelsestilstand som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
1. Udvid noden **Handel**.
1. Aktiver konfigurationsnøglen for hovedfunktionen ved at markere afkrydsningsfeltet **Styring af tekniske ændringer**. (Det er ikke nødvendigt at udvide noden, medmindre du også vil deaktivere en eller begge af dens underfunktioner.)
1. Hvis du også vil bruge versionsdimensionen, skal du markere afkrydsningsfeltet **Produktdimension - Version**. (Dette afkrydsningsfelt er placeret længere nede på listen og er ikke indlejret under noden **Styring af tekniske ændringer**.)
1. Slå vedligeholdelsestilstand fra som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Fra april 2022 vil licensnøglerne til både **Styring af tekniske ændringer** og **Produktdimension – Version** som standard være aktiveret for alle nye installationer, men du vil stadig kunne deaktivere dem, hvis det er nødvendigt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
