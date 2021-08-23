---
title: Ofte stillede spørgsmål om klienter
description: Denne artikel indeholder svar på ofte stillede spørgsmål om Finance and Operations-klienten.
author: jasongre
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05ebc55b55a40b09c825d2c93e10bb7ff38185473204b9bc7d130e81f6c419a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750504"
---
# <a name="client-faq"></a>Ofte stillede spørgsmål om klienter

[!include [banner](../includes/banner.md)]

Denne artikel indeholder svar på ofte stillede spørgsmål om Finance and Operations-klienten.

## <a name="why-arent-symbols-loaded"></a>Hvorfor indlæses symboler ikke?

Sikkerhedsindstillingerne i din browser kan forhindre, at symbolerne indlæses korrekt. Hvis du vil løse dette problem, kan du prøve følgende trin:

- Hvis du oplever dette problem i Internet Explorer, skal du klikke på **Funktioner**, og klik derefter på **Internetindstillinger**. I dialogboksen Internetindstillinger under fanen **Beskyttelse af personlige oplysninger** skal du klikke på **Brugerdefineret niveau** og kontrollere, at indstillingen **Overførsel af skrifttyper** er markeret.
- Ellers skal du muligvis føje appwebstedet til listen over websteder, du har tillid til.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Jeg savner båndet fra Dynamics AX 2012. Kan jeg lade faner i handlingsruden være åbne hele tiden?

Vi planlægger at implementere denne funktion snart. Brugerne vil herefter kunne vælge at beholde fanerne i Handlingsruder åbne hele tiden. Ellers skjules fanerne, når de ikke bruges, for at give mere skærmplads til siden.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Hvorfor kan jeg nogle gange se forskellige genvejsmenuer, når jeg højreklikker?

Hvis du højreklikker på et redigerbart felt (eller hvis tekst er markeret), vises genvejsmenuen i browseren. Denne menu giver dig adgang til kommandoerne **Klip**, **Kopiér** og **Sæt ind** kommandoer. Vi kan ikke integrere disse kommandoer i genvejsmenuer af sikkerhedsmæssige årsager, da browsere ikke giver os mulighed for automatisk at få adgang til systemets Udklipsholder.

Hvis du højreklikker på en feltetiket eller værdien af et skrivebeskyttet kontrolelement, vises genvejsmenuen.

For at gøre tastaturadgang nemmere planlægger vi at implementere en tastaturgenvej i fremtiden, som vil åbne genvejsmenuen.

## <a name="where-is-the-view-details-functionality"></a>Hvor er funktionen Vis detaljer?

Indstillingen **Vis detaljer** er tilgængelig på flere måder:

- Hvis et kontrolelement har funktionaliteten **Vis detaljer**, og hvis kontrolelementet har en værdi, vises denne værdi som et hyperlink. Du kan klikke på hyperlinket for at åbne en side, der indeholder yderligere oplysninger.
- **Vis detaljer** er også en indstilling i genvejsmenuer. Du kan finde flere oplysninger om, hvornår genvejsmenuer vises, når du højreklikker, i det forrige afsnit.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]