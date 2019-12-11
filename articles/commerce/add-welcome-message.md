---
title: Tilføj en velkomstmeddelelse
description: Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697376"
---
# <a name="add-a-welcome-message"></a>Tilføj en velkomstmeddelelse

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du føjer en velkomstmeddelelse til dit Microsoft Dynamics 365 Commerce-websted.

## <a name="overview"></a>Oversigt

En velkomstmeddelelse på dit e-handelswebsted kan informere de besøgende om igangværende salg, webstedsopdateringer, eller at sæsonens kollektioner er tilgængelige. Velkomstmeddelelsen konfigureres ved hjælp af påmindelsesmodulet.

Påmindelsesmodulet skal føjes til pladsen **Fejl-/oplysningsmeddelelser** i sidehovedfragmentet. Med påmindelsesmodulet kan du angive den tekst, der skal vises, tekstfarven og justeringen. Det giver dig også mulighed for at angive, om besøgende på webstedet skal kunne afvise meddelelsen.

Når en velkomstmeddelelse føjes til et delt sidehovedfragment, vises det på hver side, der bruger den skabelon, hvor det delte sidehovedfragment bruges.

Hvis du vil føje en velkomstmeddelelse til dit websted, skal du følge disse trin.

1. Gå til dit websted i Dynamics 365 Commerce.
1. Vælg **Fragmenter**.
1. Vælg det sidehovedfragment, som meddelelsen skal føjes til.
1. Udvid **Fejl-/oplysningsmeddelelser** i dispositionstræet.
1. Vælg påmindelsesmodulet.

    Hvis der endnu ikke findes et påmindelsesmodul, skal du vælge ellipseknappen (**...**) ud for **Fejl-/oplysningsmeddelelser** og derefter vælge **Tilføj modul**. Vælg påmindelsesmodulet, og vælg derefter **OK**.

1. Vælg **Tilføj datakilde** under fanen **Data** i egenskabsruden til højre, og vælg derefter **Indhold**.
1. Skriv teksten til velkomstmeddelelsen i feltet **Inputtekst**.
1. Gem sidehovedfragmentet, check det ind, og publicer det.

Velkomstmeddelelsen vises nu øverst på alle de webstedssider, der bruger det valgte sidehovedfragment.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføj et logo](add-logo.md)

[Vælg et tema for webstedet](select-site-theme.md)

[Tilføj en favicon](add-favicon.md)

[Tilføj en copyright-meddelelse](add-copyright-notice.md)

[Føje sprog til webstedet](add-languages-to-site.md)

[Tilføje scriptkode til sider på websteder for at understøtte telemetri](add-telemetry.md)

