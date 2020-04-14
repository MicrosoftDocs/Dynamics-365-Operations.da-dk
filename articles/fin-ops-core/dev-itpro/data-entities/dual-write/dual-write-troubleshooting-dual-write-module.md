---
title: Fejlfinding i forbindelse med problemer med dobbeltskrivningsmodulet i Finance and Operations-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med dobbeltskrivningsmodulet i Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172754"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Fejlfinding i forbindelse med problemer med dobbeltskrivningsmodulet i Finance and Operations-apps

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med **dobbeltskrivningsmodulet** i Finance and Operations-apps.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Du kan ikke indlæse dobbeltskrivningsmodulet i en Finance and Operations-app

Hvis du ikke kan åbne **Dobbeltskrivning**-siden ved at vælge titlen **Dobbeltskrivning** i **Datastyring**-arbejdsområdet, er dataintegrationstjenesten sandsynligvis nede. Opret en supportanmodning for at anmode om genstart af dataintegrationstjenesten.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Fejl, når du forsøger at oprette en ny enhedstilknytning

**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator

Du kan få vist følgende fejlmeddelelse, når du forsøger at konfigurere en ny enhed til dobbeltskrivning:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 401 (uautoriseret)*

Denne fejl opstår, fordi det kun er en Azure AD-lejeradministrator, der kan tilføje en ny enhedstilknytning.

Du kan løse problemet ved at logge på Finance and Operations-appen som Azure AD-lejeradministrator. Du skal også gå til web.PowerApps.com og validere forbindelsen igen.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fejl, når du åbner brugergrænsefladen til dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at få adgang til dobbeltskrivning fra arbejdsområdet **Datastyring**:

*login.microsoftonline.com afviste at oprette forbindelse.*

Du kan løse problemet ved at logge på ved hjælp af et InPrivate-vindue i Microsoft Edge, et incognito-vindue i Chromium eller et incognito-vindue i Google Chrome. Du skal også fjerne blokeringen af eller rydde tredjepartscookies.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Fejl under sammenkædning af miljøet ved dobbeltskrivning eller tilføjelse af en ny enhedstilknytning

**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator

Der kan opstå følgende fejl under sammenkædning eller oprettelse af tilknytninger:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 403 (tokenexchange).<br> Sessions-id: \<dit sessions-id\><br> Rodaktivitets-id: \<dit rod-aktivitets-id\>*

Denne fejl kan forekomme, hvis du ikke har de nødvendige rettigheder til at sammenkæde dobbeltskrivning eller oprette tilknytninger. Du skal bruge en Azure AD-lejeradministratorkonto for at kunne sammenkæde miljøer og tilføje nye enhedstilknytninger. Men når du har udført installationen, kan du bruge en ikke-administratorkonto til at overvåge status og redigere tilknytningerne.

## <a name="error-when-you-stop-the-entity-mapping"></a>Fejl, når du stopper tilknytningen af enheder

Du kan få vist følgende fejlmeddelelse, når du forsøger at standse tilknytninger af enheder:

*\[Forbudt\], \[{"status": 403, "kilde": "","meddelelse":"Fejl fra tokenudveksling: Brugeren har ikke adgang til forbindelsen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], fjernserveren returnerede en fejl: (403) forbudt.*

Denne fejl opstår, når det sammenkædede Common Data Service-miljø ikke er tilgængeligt.

Du kan løse problemet ved at oprette en supportanmodning til dataintegrationsteamet. Tilknyt netværkssporingen, så dataintegrationsteamet kan markere tilknytningerne som **Kører ikke** i backend.
