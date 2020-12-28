---
title: Skjule leveringsmåder uden fragtmand i forsendelsesindstillingerne i POS
description: Dette emne beskriver en konfigurationsindstilling, der kan forhindre leveringsmåder uden fragtmand i at blive vist som valgmulighed, når der oprettes forsendelsesordrer i POS.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411167"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Skjule leveringsmåder uden fragtmand i forsendelsesindstillingerne i POS


[!include [banner](includes/banner.md)]

Dette emne beskriver en konfigurationsindstilling, der er tilgængelig for POS-programmet. Denne konfigurationsindstilling ændrer funktionaliteten af den valgte leveringsmåde, når der oprettes forsendelsesordrer i POS.

Når brugere opretter kundeforsendelsesordrer i POS, kan de vælge en leveringsmåde for forsendelsen. Denne funktionalitet er tilgængelig, uanset om hele ordren leveres eller kun udvalgte linjer.

Som standard viser dialogboksen, hvor der vælges leveringsmåde, alle de gyldige leveringsmåder for kombinationen af en kanal, en vare og en leveringsadresse. Disse leveringsmåder defineres på siden **Leveringsmåder** i Headquarters (**Salg og marketing \> Opsætning \> Fordeling \> Leveringsmåder**). Leveringsmåder uden fragtmand som f.eks. **Udfør** eller **Afhentning** kan også vises som valg i dialogboksen.

Der er dog tilføjet en funktion, som giver dig mulighed for at skjule leveringsmåder uden fragtmand i dialogboksen. Hvis du vil aktivere denne funktion, skal du på siden **Commerce-parametre** under fanen **Kundeordrer** angive indstillingen **Vis kun fragtmandstilstande for indstillingen forsendelsesordrer** til **Ja**. Når du har aktiveret denne funktion og kører de relevante distributionsjob for at synkronisere oplysningerne til kanaldatabasen, vises leveringsmåder uden fragtmand ikke som muligt valg under processen til oprettelse af forsendelsesordrer i POS.
