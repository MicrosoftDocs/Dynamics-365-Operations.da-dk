---
title: Velkomstmail sendes ikke, når nye kunder oprettes
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der ikke sendes en velkomstbesked via mail, når der oprettes en ny kunde i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219398"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Velkomstmail sendes ikke, når nye kunder oprettes

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, hvis der ikke sendes en velkomstbesked via mail, når der oprettes en ny kunde i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivelse

Når der oprettes en ny kunde i Commerce Headquarters, sendes en velkomstmail ikke til kunden, selvom der er konfigureret en mailbesked for **Kunde er oprettet**-mailbeskedtypen.

## <a name="resolution"></a>Løsning

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Tilknytte en mailbeskedprofil under Handelsparametre

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Handelsparametre \> Generelt** i hovedkontoret.
2. På rullelisten **Profil til e-mail-besked** skal du vælge den mailbeskedprofil, der indeholder en tilknytning mellem den kundeoprettede beskedtype og en kundeoprettet mailskabelon.  

> [!NOTE] 
> Når du aktiverer beskeder, der er oprettet af kunder, vil kunder, der er oprettet i alle kanaler i den juridiske enhed,, modtage en kundeoprettet mail. Aktuelt kan kundeoprettede beskeder ikke være begrænset til en enkelt kanal.

Du kan få flere oplysninger i [Oprette mailskabeloner til transaktionshændelser](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en profil for mailbesked](../email-notification-profiles.md)
