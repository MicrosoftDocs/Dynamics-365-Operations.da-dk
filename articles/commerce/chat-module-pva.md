---
title: Commerce-chat med Power Virtual Agents-modul
description: Denne artikel beskriver Commerce-chat med Power Virtual Agents-modulet, der integrerer Microsoft Power Virtual Agents med websteder i Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691062"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Commerce-chat med Power Virtual Agents-modul

[!include [banner](includes/banner.md)]

Denne artikel beskriver Commerce-chat med Power Virtual Agents-modulet, der integrerer Microsoft Power Virtual Agents med websteder i Dynamics 365 Commerce.

Commerce-chat med funktionen Power Virtual Agents gør Dynamics 365-e-handelskunder i stand til at bruge Power Virtual Agents-chatrobotfunktioner til at håndtere deres forespørgsler. Fra og med Dynamics 365 Commerce version 10.0.30 kan denne funktion integreres i e-handelswebsteder ved hjælp af Commerce-chat med modulet Power Virtual Agents, som er en del af biblioteket i Commerce-modulet.

Commerce-chat med funktionen Power Virtual Agents hjælper virksomheder med at nå følgende mål:

- Øge tilpasset engagement med deres forbrugere og forbedre tilbageholdelse.
- Forbedre kundeservice ved hjælp af integration af selvbetjenings-chatrobotter.
- Forbedre den generelle kundetilfredshed og dermed øge salget.

> [!NOTE]
> Du kan få mere at vide om forskellene mellem Dynamics 365 Omnikanal til Customer Service og Power Virtual Agents-programmer i [Oversigt over Commerce-chatmoduler](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Forudsætninger for brug af Power Virtual Agents

Hvis du vil bruge Commerce-chat med funktionen Power Virtual Agents, skal du først oprette en Power Virtual Agents-chatrobot til dit e-handelswebsted. Du kan finde instruktioner under [Oprette en effektiv virtuel helpdesk-medarbejderrobot](/power-virtual-agents/authoring-first-bot).

Når du har konfigureret chatrobotten, skal du kopiere værdierne fra parametrene **Robot-id** og **Lejer-id** for at konfigurere Commerce-chatoplevelsen. Yderligere oplysninger om, hvordan du kopierer disse værdier, finder du under [Hente dine Power Virtual Agents-robotparametre](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Konfigurere dit e-handelswebsted 

En anbefalet måde at implementere chatoplevelsen på dit e-handelswebsted på er at føje Commerce-chat med Power Virtual Agents-modulet til det delte sidehovedfragment, der bruges på dine websider.

Følg disse trin, hvis du til tilføje chatmodulet til webstedets overskriftsfragment i Commerce-webstedsgenerator.

1. Gå til **Fragmenter** i Commerce-webstedsgeneratoren.
1. Vælg **Ny**.
1. I dialogboksen **Vælg et fragment** skal du vælge **Commerce-chat med Power Virtual Agents**-modulet, angive et navn til fragmentet og derefter vælge **OK**.
1. I dispositionsvisningen skal du vælge **Msdyn365 pva chat connector**.
1. Benyt følgende fremgangsmåde i ruden med egenskaber:

    1. Under **Robotparametre** skal du i feltet **Bot Framework Webchat Chat CDN-URL-adresse** bevare standardværdien (f.eks. `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. I feltet til **Bot Framework Direct Line-godkendelses-URL-adresse** skal du beholde standardværdien (f.eks. `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. Angiv i feltet **Robot-id** den Power Virtual Agents-værdi af **Robot-id**, du kopierede i afsnittet [Forudsætninger for brug af Power Virtual Agents](#prereq).
    1. I feltet **Lejer-id** skal du angive den værdi for **Lejer-id**, du har kopieret.

1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Gå til **Fragmenter**, og åbn overskriftsfragmentet for dit websted.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj fragment**.
1. Vælg det fragment for chat, du oprettede tidligere, i dialogboksen **Vælg moduler**, og vælg derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

## <a name="proactive-chat-parameters"></a>Proaktive chatparametre

Du kan få en komplet liste over proaktive parametre for chatkonfiguration i [Proaktive chatparametre til Commerce-chatmodulet](chat-proactive-chat-parameters.md).

> [!NOTE]
> I øjeblikket understøtter Power Virtual Agents ikke Azure Active Directory B2C (Azure AD B2C) som godkendelsesmetode. Det understøtter kun anonyme Retail Cloud Scale Unit-opkald (RCSU) for at få produkttilgængelighed eller interagere med andre anonyme API'er. Kald til godkendte API'er via Power Virtual Agents-chatrobotter kræver en eksplicit tilmelding af kunden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Commerce-chatfunktioner](commerce-chat-overview.md)

[Commerce-chat med Omnikanal til Customer Service-modulet](commerce-chat-module.md)

[Proaktive chatparametre til Commerce-chatmodulet](chat-proactive-chat-parameters.md)
