---
title: Velkomstmail sendes ikke, når nye kunder oprettes
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der ikke sendes en velkomstbesked via mail, når der oprettes en ny kunde i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853677"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Velkomstmail sendes ikke, når nye kunder oprettes

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der ikke sendes en velkomstbesked via mail, når der oprettes en ny kunde i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivelse

Når der oprettes en ny kunde i Commerce Headquarters, sendes en velkomstmail ikke til kunden, selvom der er konfigureret en mailbesked for **Kunde er oprettet**-mailbeskedtypen.

## <a name="resolution"></a>Løsning

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Angiv den korrekte værdi for mail-id'et for mailbeskedtypen Kunde er oprettet

Hvis du vil angive den korrekte værdi for **Mail-id** for **Kunde er oprettet** i mailbeskedtype i hovedkontoret, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.
1. Vælg mailbeskedprofilen i navigationsruden til venstre.
1. Angiv feltet **Mail-id** til **NewCust** under **Indstillinger for hændelsesbesked** for **Kunde er oprettet**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en profil for mailbesked](../email-notification-profiles.md)
