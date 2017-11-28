---
title: "Ofte stillede spørgsmål til Finance and Operations-klient"
description: "Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics 365 for Finance and Operations-klienten."
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 658d5a1a031f2292dbd445fa7fb345be01c61947
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="finance-and-operations-client-faq"></a>Ofte stillede spørgsmål til Finance and Operations-klient

[!include[banner](../includes/banner.md)]


Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics 365 for Finance and Operations-klienten.

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>Hvorfor indlæses symboler ikke, når jeg bruger Finance and Operations?
-----------------------------------------------------------------

Sikkerhedsindstillingerne i din browser kan forhindre, at symbolerne indlæses korrekt. Hvis du vil løse dette problem, kan du prøve følgende trin:

-   Hvis du oplever dette problem i Internet Explorer, skal du klikke på **Funktioner**, og klik derefter på **Internetindstillinger**.  I dialogboksen Internetindstillinger under fanen **Beskyttelse af personlige oplysninger** skal du klikke på **Brugerdefineret niveau** og kontrollere, at indstillingen **Overførsel af skrifttyper** er markeret.
-   Ellers skal du muligvis føje Finance and Operations-webstedet til listen over websteder, du har tillid til.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg lade faner i handlingsruden være åbne hele tiden?
Vi planlægger at implementere denne funktion snart. Brugerne vil herefter kunne vælge at beholde fanerne i Handlingsruder åbne hele tiden. Ellers skjules fanerne, når de ikke bruges, for at give mere skærmplads til siden.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Hvorfor kan jeg nogle gange se forskellige genvejsmenuer, når jeg højreklikker?
Hvis du højreklikker på et redigerbart felt (eller hvis tekst er markeret), vises genvejsmenuen i browseren. Denne menu giver dig adgang til kommandoerne **Klip**, **Kopiér** og **Sæt ind** kommandoer. Vi kan ikke integrere disse kommandoer i genvejsmenuer i Finance and Operations af sikkerhedsmæssige årsager, da browsere ikke giver os mulighed for automatisk at få adgang til systemets Udklipsholder.

Hvis du højreklikker på en feltetiket eller værdien af et skrivebeskyttet kontrolelement, vises genvejsmenuen Finance and Operations.

For at gøre tastaturadgang nemmere, planlægger vi at implementere en tastaturgenvej i fremtiden, som vil åbne genvejsmenuen til Finance and Operations.

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Hvor er funktionen Vis detaljer i Finance and Operations?
Indstillingen **Vis detaljer** er tilgængelig på flere måder:

-   Hvis et kontrolelement har funktionaliteten **Vis detaljer**, og hvis kontrolelementet har en værdi, vises denne værdi som et hyperlink. Du kan klikke på hyperlinket for at åbne en side, der indeholder yderligere oplysninger.
-   **Vis detaljer** er også en indstilling i genvejsmenuer i Finance and Operations. Du kan finde flere oplysninger om, hvornår genvejsmenuer i Finance and Operations vises, når du højreklikker, i det forrige afsnit.





