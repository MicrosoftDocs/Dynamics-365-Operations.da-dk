---
title: Skjule leveringsmåder uden fragtmand i forsendelsesindstillingerne i POS
description: Denne artikel beskriver en konfigurationsindstilling, der kan forhindre leveringsmåder uden fragtmand i at blive vist som valgmulighed, når der oprettes forsendelsesordrer i POS.
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 469e6ebb8afed26a6bf25f4c9c3ab8f7f4ac78ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896999"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Skjule leveringsmåder uden fragtmand i forsendelsesindstillingerne i POS


[!include [banner](includes/banner.md)]

Denne artikel beskriver en konfigurationsindstilling, der er tilgængelig for POS-programmet. Denne konfigurationsindstilling ændrer funktionaliteten af den valgte leveringsmåde, når der oprettes forsendelsesordrer i POS.

Når brugere opretter kundeforsendelsesordrer i POS, kan de vælge en leveringsmåde for forsendelsen. Denne funktionalitet er tilgængelig, uanset om hele ordren leveres eller kun udvalgte linjer.

Som standard viser dialogboksen, hvor der vælges leveringsmåde, alle de gyldige leveringsmåder for kombinationen af en kanal, en vare og en leveringsadresse. Disse leveringsmåder defineres på siden **Leveringsmåder** i Headquarters (**Salg og marketing \> Opsætning \> Fordeling \> Leveringsmåder**). Leveringsmåder uden fragtmand som f.eks. **Udfør** eller **Afhentning** kan også vises som valg i dialogboksen.

Der er dog tilføjet en funktion, som giver dig mulighed for at skjule leveringsmåder uden fragtmand i dialogboksen. Hvis du vil aktivere denne funktion, skal du på siden **Commerce-parametre** under fanen **Kundeordrer** angive indstillingen **Vis kun fragtmandstilstande for indstillingen forsendelsesordrer** til **Ja**. Når du har aktiveret denne funktion og kører de relevante distributionsjob for at synkronisere oplysningerne til kanaldatabasen, vises leveringsmåder uden fragtmand ikke som muligt valg under processen til oprettelse af forsendelsesordrer i POS.


[!INCLUDE[footer-include](../includes/footer-banner.md)]