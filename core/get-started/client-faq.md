---
title: "Dynamics 365 for operationer klienten ofte stillede spørgsmål"
description: "Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics-365 for klient operationer."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 2c99b2e1f7ddecb61be62832ca1a8d3ac1fd21a8
ms.lasthandoff: 03/31/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Dynamics 365 for operationer klienten ofte stillede spørgsmål

Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics-365 for klient operationer.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Hvorfor ikke symboler indlæses, når jeg bruger Dynamics 365 for operationer?
-----------------------------------------------------------------

Sikkerhedsindstillingerne i din browser kan forhindre, at symbolerne indlæses korrekt. Hvis du vil løse dette problem, kan du prøve følgende trin:

-   Hvis du oplever dette problem i Internet Explorer, skal du klikke på **Tools**, og klik derefter på **Internet-indstillinger**.  I dialogboksen Internetindstillinger på den **beskyttelse af personlige oplysninger**, og klik på **Brugerdefineret niveau**, og Kontroller, at den **skrifttype download** indstilling er valgt.
-   Ellers skal du muligvis føje Dynamics-365 for operationer websted til listen over websteder, du har tillid til.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg beholde handlingsruden faner åbne hele tiden?
Vi planlægger at implementere denne funktion snart. Brugerne vil derefter kunne vælge at beholde fanerne på Handlingsruder åben hele tiden. Ellers skjules fanerne, når de ikke bruges, for at give mere skærmplads til siden.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Hvorfor kan jeg nogle gange se forskellige genvejsmenuer når jeg rightclick?
Hvis du højreklikker på et redigerbart felt (eller hvis tekst er markeret), vises genvejsmenuen i browseren. Denne menu giver dig adgang til kommandoerne **Klip**, **Kopiér** og **Sæt ind** kommandoer. Vi kan ikke integrere disse kommandoer i Dynamics-365 for operationer genvejsmenuer, fordi af sikkerhedsmæssige årsager ikke browsere giver os mulighed for automatisk at få adgang til Udklipsholder.

Hvis du højreklikker på en feltetiket eller værdien af et skrivebeskyttet kontrolelement, får du vist Dynamics-365 for operationer genvejsmenuen.

Nemmere Tastaturadgang, planlægger vi at implementere en tastaturgenvej i fremtiden, som skal åbne Dynamics-365 for operationer genvejsmenuen.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Hvor er funktionen Vis detaljer i Dynamics 365 for operationer?
Indstillingen **Vis detaljer** er tilgængelig på flere måder:

-   Hvis et kontrolelement har funktionaliteten **Vis detaljer**, og hvis kontrolelementet har en værdi, vises denne værdi som et hyperlink. Du kan klikke på hyperlinket for at åbne en side, der indeholder yderligere oplysninger.
-   **Få vist oplysninger om** er også en indstilling på Dynamics 365 for operationer genvejsmenuer. Yderligere oplysninger om, hvornår Dynamics 365 for operationer genvejsmenuer vises, når du højreklikker på, finder du i det forrige afsnit.



