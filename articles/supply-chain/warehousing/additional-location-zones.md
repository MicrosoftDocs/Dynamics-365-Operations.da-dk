---
title: Ekstra lokationszoner
description: Denne artikel indeholder en oversigt over de nye lokationszoner, der er føjet til Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c20225cfb3c44fff955d0ad4e96c7fecf0ddf715
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900645"
---
# <a name="additional-location-zones"></a>Ekstra lokationszoner

[!include [banner](../includes/banner.md)]

Der er tre nye zonefelter tilgængelige i Microsoft Dynamics 365 Supply Chain Management. Lagerstedschefer kan bruge dem til at definere yderligere lagerstedsorganisationer eller -layout. De nye zonefelter kan enten angives manuelt eller ved hjælp af guiden **Konfiguration af lokation**. De kan bruges i en forespørgsel eller filtrering, der bruger tabellen Lokationer.

Der kræves ikke yderligere konfiguration for at kunne bruge zonefelterne.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Slå funktionen Flere lokationszoner til eller fra

Fra og med Supply Chain Management version 10.0.25 er denne funktion som standard aktiveret. Administratorer kan aktivere eller deaktivere denne funktion ved at søge efter funktionen *Flere lokationszoner* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="use-location-zones"></a>Bruge lokationszoner

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Guiden Konfiguration af lokation**.
2. Angiv følgende værdier:

    - Vælg _62_ i feltet **Lagersted**.
    - Gå til feltet **Zone-id**, og vælg _PRODUKTION_.
    - Gå til feltet **Ekstra zone 1**, og vælg _PLUKZONE1_.
    - Gå til feltet **Ekstra zone 2**, og vælg _WEBBUTIK1_.
    - Gå til feltet **Lokationsprofil-id**, og vælg _PRODUKTION_.

3. Vælg linjen **Produktion**.
4. Gå til feltet **Fra nummer**, og angiv _1_. Gå til feltet **Til nummer**, og angiv _3_.
5. Vælg linjen **Gang**.
6. Gå til feltet **Fra nummer**, og angiv _1_. Gå til feltet **Til nummer**, og angiv _5_.
7. Vælg **Opret**.
8. Du modtager meddelelser om, at der er tilføjet nye lokationer. Vælg knappen **Vis meddelelser** for at få vist meddelelserne.
9. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**. De nye lokationer vises på listen, og alle zone felter er tilgængelige (dvs. det eksisterende zonefelt og de nye ekstra zonefelter).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]