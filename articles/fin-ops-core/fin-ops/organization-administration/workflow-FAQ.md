---
title: Ofte stillede spørgsmål om arbejdsproces
description: Denne artikel besvarer ofte stillede spørgsmål om arbejdsprocessystemet.
author: ChrisGarty
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a72fd141bb1178a3a83385c512d1a655064d5b00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896573"
---
# <a name="workflow-faq"></a>Ofte stillede spørgsmål om arbejdsproces

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikel besvarer ofte stillede spørgsmål om arbejdsprocessystemet.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvorfor modtages flere beskeder, når en workflowopgave afvises?
Når en workflowopgave afvises, fuldføres den som afvist. Der oprettes en anden workflowopgave, som tildeles til igangsætteren. Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning". 

Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring. Vi ser på forskellige måder at forbedre dette i en senere version.

## <a name="why-are-my-workflow-exports-failing"></a>Hvorfor mislykkes eksporten af mine arbejdsgange?
Der er i øjeblikket en begrænsning i funktionen til eksport af arbejdsgange, som forhindrer, at arbejdsgangens navne overstiger 48 tegn. Hvis du bruger et navn, der er længere end 48 tegn, kan det resultere i, at fejlen "Serveren kunne ikke godkende anmodningen", og/eller forhindre, at en fil kan eksporteres uden en filtype. Følgende blogindlæg indeholder flere detaljer [Fejlfinding i forbindelse med eksport af arbejdsgang](https://community.dynamics.com/365/financeandoperations/b/elandaxdynamicsaxupgradesanddevelopment/posts/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Kan afsenderen af en arbejdsgang også godkende arbejdsgangen?
Ja, en afsender af en arbejdsgang kan også godkende arbejdsgangen, hvis den er konfigureret på denne måde. Hvis du vil undgå dette, skal du angive **Systemadministration > Arbejdsgang > Arbejdsgangsparametre > Generelt > Godkender > Tillad ikke afsenders godkendelse** til **Ja**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Kan jeg føje påmindelser til arbejdsgange for at sende beskeder til brugerne?
Her er nogle få nøgleområder, du kan bemærke om tilføjelse af påmindelser til arbejdsgange for at give beskeder:
- Påmindelser for mekanismer til arbejdsgangsbeskeder
    - Påmindelser kan konfigureres til postændringer. Arbejdsgange ændrer poster, så det er muligt at oprette en påmindelse, der relaterer til en post, der er blevet ændret pga. en arbejdsgang. Men da arbejdsgange har forskellige indbyggede beskedindstillinger, er brug af påmindelser ikke ideel.
- Standardbeskeder fra arbejdsgange 
    - Arbejdsgange har indbyggede mailbeskeder. En kunde kan konfigurere beskederne, så brugerne sendes som mails. Disse beskeder resulterer ikke i Handlingscenter-meddelelser for brugere.
    - I en fremtidig opdatering vil vi tilføje en Handlingscenter-meddelelse, så en bruger får tildelt et arbejdsgangsopgave. 
- Føje beskeder til arbejdsgange
    - Handlingscenter-meddelelser kan oprettes for bestemte brugere, f.eks. en meddelelse, der er oprettet fra en arbejdsgang i X++.
    - [Arbejdsgange har forretningshændelser](../../dev-itpro/business-events/business-events-workflow.md), som kunden kan bruge til at udløse flows, har de beskeder, de søger efter.   

Hvis en bruger kort sagt ikke får den rigtige besked fra Handlingscenter, når vedkommende er blevet tildelt en arbejdsgangsopgave, så brug [Arbejdsgangsforretningshændelser](../../dev-itpro/business-events/business-events-workflow.md) med Microsoft Power Automate til at give flere eller andre beskeder.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Hvorfor kan arbejdsgangseditor ikke starte under AD FS?
Når du kører arbejdsproceseditoren under Active Directory Federation Services (ADFS) i et opgraderet miljø, kan den have problemer med at starte. Hvis den gør det, skal du sørge for, at URL-adressen "https://dynamicsaxworkfloweditor/" er tilføjet til egenskaben **Microsoft Dynamics 365 for Operations i Det lokale miljø - Arbejdsgang - Forudinstalleret program** i ADFS-indstillingerne.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Hvorfor får jeg vist SQL-deadlock ved arbejdsgangsbehandling? 
Standardfeltværdien for **Antal af arbejdsgangsvarer pr. batch** på siden **Arbejdsgangparametre** er 0. En værdi på 0 gør, at standarden ændres til 20 varer pr. batch. Vær forsigtig, når du justerer denne værdi, fordi et stort antal varer pr. batch (> 40) kan forårsage SQL-deadlock.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Hvad er den arbejdsgangsforbedrede fejlfunktion?
Den arbejdsgangsforbedrede fejlfunktion i version 10.0.13 tilføjer fejlkoder for at differentiere forskellige klasser af arbejdsgangsfejl. De rapporterede fejlmeddelelser er overvejende ens med mindre forskelle for at gøre dem tydeligere.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
