---
title: Ekstra lokationszoner
description: Dette emne indeholder en oversigt over de nye lokationszoner, der er føjet til Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016296"
---
# <a name="additional-location-zones"></a>Ekstra lokationszoner

[!include [banner](../includes/banner.md)]

Der er tre nye zonefelter tilgængelige i Microsoft Dynamics 365 Supply Chain Management. Lagerstedschefer kan bruge dem til at definere yderligere lagerstedsorganisationer eller -layout. De nye zonefelter kan enten angives manuelt eller ved hjælp af guiden **Konfiguration af lokation**. De kan bruges i en forespørgsel eller filtrering, der bruger tabellen Lokationer.

Der kræves ikke yderligere konfiguration for at kunne bruge zonefelterne.

## <a name="turn-on-the-additional-location-zone-feature"></a>Aktivér funktionen Ekstra lokationszone

Før du kan bruge funktionen *Ekstra lokationszone* , skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Flere lokationszoner*

## <a name="use-location-zones"></a>Bruge lokationszoner

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Guiden Konfiguration af lokation**.
2. Angiv følgende værdier:

    - Vælg _62_ i feltet **Lagersted**.
    - Gå til feltet **Zone-id** , og vælg _PRODUKTION_.
    - Gå til feltet **Ekstra zone 1** , og vælg _PLUKZONE1_.
    - Gå til feltet **Ekstra zone 2** , og vælg _WEBBUTIK1_.
    - Gå til feltet **Lokationsprofil-id** , og vælg _PRODUKTION_.

3. Vælg linjen **Produktion**.
4. Gå til feltet **Fra nummer** , og angiv _1_. Gå til feltet **Til nummer** , og angiv _3_.
5. Vælg linjen **Gang**.
6. Gå til feltet **Fra nummer** , og angiv _1_. Gå til feltet **Til nummer** , og angiv _5_.
7. Vælg **Opret**.
8. Du modtager meddelelser om, at der er tilføjet nye lokationer. Vælg knappen **Vis meddelelser** for at få vist meddelelserne.
9. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**. De nye lokationer vises på listen, og alle zone felter er tilgængelige (dvs. det eksisterende zonefelt og de nye ekstra zonefelter).