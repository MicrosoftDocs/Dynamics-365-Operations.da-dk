---
title: Tilføje en velkomstmeddelelse
description: Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797377"
---
# <a name="add-a-welcome-message"></a>Tilføje en velkomstmeddelelse

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.

En velkomstmeddelelse på dit e-handelswebsted kan informere de besøgende om igangværende salg, webstedsopdateringer, eller at sæsonens kollektioner er tilgængelige. Velkomstmeddelelsen konfigureres ved hjælp af påmindelsesmodulet.

Påmindelsesmodulet skal føjes til pladsen **Fejl-/oplysningsmeddelelser** i sidehovedfragmentet. Med påmindelsesmodulet kan du angive den tekst, der skal vises, tekstfarven og justeringen. Det giver dig også mulighed for at angive, om besøgende på webstedet skal kunne afvise meddelelsen.

Når en velkomstmeddelelse føjes til et delt sidehovedfragment, vises det på hver side, der bruger den skabelon, hvor det delte sidehovedfragment bruges.

Hvis du vil føje en velkomstmeddelelse til dit websted, skal du følge disse trin.

1. Naviger til dit websted i Commerce-webstedsgeneratoren.
1. Vælg **Fragmenter**.
1. Vælg det sidehovedfragment, som meddelelsen skal føjes til.
1. Udvid **Fejl-/oplysningsmeddelelser** i dispositionstræet.
1. Vælg påmindelsesmodulet, og vælg derefter **OK**. Hvis der endnu ikke findes et påmindelsesmodul, skal du først vælge ellipseknappen (**...**) ud for **Fejl-/oplysningsmeddelelser** og derefter vælge **Tilføj modul**.
1. Vælg **Tilføj datakilde** under fanen **Data** i egenskabsruden til højre, og vælg derefter **Indhold**.
1. Skriv teksten til velkomstmeddelelsen i feltet **Inputtekst**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke sidehovedfragmentet ind, og vælg derefter **Publicer** for at publicere det. 

Velkomstmeddelelsen vises nu øverst på alle de webstedssider, der bruger det valgte sidehovedfragment.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføj et logo](add-logo.md)

[Vælg et tema for webstedet](select-site-theme.md)

[Arbejd med CSS-tilsidesættelsesfiler](css-override-files.md)

[Tilføj en favicon](add-favicon.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
