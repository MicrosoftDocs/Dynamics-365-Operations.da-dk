---
title: Velkomstmail sendes ikke, når nye kunder oprettes
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der ikke sendes en velkomstbesked via mail, når der oprettes en ny kunde i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349947"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Velkomstmail sendes ikke, når nye kunder oprettes

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der ikke sendes en velkomstbesked via mail, når der oprettes en ny kunde i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivelse

Når der oprettes en ny kunde i Commerce-hovedkontoret, sendes en velkomstmail ikke til kunden, selvom der er konfigureret en mailbesked for **Kunde er oprettet**-mailbeskedtypen.

## <a name="resolution"></a>Løsning

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Angiv den korrekte værdi for mail-id'et for mailbeskedtypen Kunde er oprettet

Hvis du vil angive den korrekte værdi for **Mail-id** for **Kunde er oprettet** i mailbeskedtype i hovedkontoret, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.
1. Vælg mailbeskedprofilen i navigationsruden til venstre.
1. Angiv feltet **Mail-id** til **NewCust** under **Indstillinger for hændelsesbesked** for **Kunde er oprettet**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en profil for mailbesked](../email-notification-profiles.md)
