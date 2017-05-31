---
title: "Ofte stillede spørgsmål om Dynamics 365 for Operations-klient"
description: "Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics 365 for Operations-klienten."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7e8f09b965403298630460ccb6669fd82abb0e8c
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Ofte stillede spørgsmål om Dynamics 365 for Operations-klient

[!include[banner](../includes/banner.md)]


Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics 365 for Operations-klienten.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Hvorfor indlæses symboler ikke, når jeg bruger Dynamics 365 for Operations?
-----------------------------------------------------------------

Sikkerhedsindstillingerne i din browser kan forhindre, at symbolerne indlæses korrekt. Hvis du vil løse dette problem, kan du prøve følgende trin:

-   Hvis du oplever dette problem i Internet Explorer, skal du klikke på **Funktioner**, og klik derefter på **Internetindstillinger**.  I dialogboksen Internetindstillinger under fanen **Beskyttelse af personlige oplysninger** skal du klikke på **Brugerdefineret niveau** og kontrollere, at indstillingen **Overførsel af skrifttyper** er markeret.
-   Ellers skal du muligvis føje Dynamics 365 for Operations-webstedet til listen over websteder, du har tillid til.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg lade faner i handlingsruden være åbne hele tiden?
Vi planlægger at implementere denne funktion snart. Brugerne vil herefter kunne vælge at beholde fanerne i Handlingsruder åbne hele tiden. Ellers skjules fanerne, når de ikke bruges, for at give mere skærmplads til siden.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Hvorfor kan jeg nogle gange se forskellige genvejsmenuer når jeg højreklikker?
Hvis du højreklikker på et redigerbart felt (eller hvis tekst er markeret), vises genvejsmenuen i browseren. Denne menu giver dig adgang til kommandoerne **Klip**, **Kopiér** og **Sæt ind** kommandoer. Vi kan ikke integrere disse kommandoer i genvejsmenuer i Dynamics 365 for Operations af sikkerhedsmæssige årsager, da browsere ikke giver os mulighed for automatisk at få adgang til systemets Udklipsholder.

Hvis du højreklikker på en feltetiket eller værdien af et skrivebeskyttet kontrolelement, vises genvejsmenuen Dynamics 365 for Operations.

For at gøre tastaturadgang nemmere, planlægger vi at implementere en tastaturgenvej i fremtiden, som vil åbne genvejsmenuen til Dynamics 365 for Operations.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Hvor er funktionen Vis detaljer i Dynamics 365 for Operations?
Indstillingen **Vis detaljer** er tilgængelig på flere måder:

-   Hvis et kontrolelement har funktionaliteten **Vis detaljer**, og hvis kontrolelementet har en værdi, vises denne værdi som et hyperlink. Du kan klikke på hyperlinket for at åbne en side, der indeholder yderligere oplysninger.
-   **Vis detaljer** er også en indstilling i genvejsmenuer i Dynamics 365 for Operations. Du kan finde flere oplysninger om, hvornår genvejsmenuer i Dynamics 365 for Operations vises, når du højreklikker, i det forrige afsnit.





