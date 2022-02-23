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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683617"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Fejlfinding i forbindelse med problemer med dobbeltskrivningsmodulet i Finance and Operations-apps

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med **dobbeltskrivningsmodulet** i Finance and Operations-apps.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Du kan ikke indlæse dobbeltskrivningsmodulet i en Finance and Operations-app

Hvis du ikke kan åbne **Dobbeltskrivning**-siden ved at vælge titlen **Dobbeltskrivning** i **Datastyring**-arbejdsområdet, er dataintegrationstjenesten sandsynligvis nede. Opret en supportanmodning for at anmode om genstart af dataintegrationstjenesten.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Fejl, når du forsøger at oprette en ny tabeltilknytning

**Påkrævede legitimationsoplysninger for at løse problemet:** Den samme bruger, der har konfigureret dobbeltskrivning.

Du kan få vist følgende fejlmeddelelse, når du forsøger at konfigurere en ny enhed til dobbeltskrivning. Den eneste bruger, der kan oprette en tilknytning, er den bruger, der har konfigureret dobbeltskrivningsforbindelsen.

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 401 (uautoriseret)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fejl, når du åbner brugergrænsefladen til dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at få adgang til dobbeltskrivning fra arbejdsområdet **Datastyring**:

*login.microsoftonline.com afviste at oprette forbindelse.*

Du kan løse problemet ved at logge på ved hjælp af et InPrivate-vindue i Microsoft Edge, et incognito-vindue i Chromium eller et incognito-vindue i Google Chrome. Du skal også fjerne blokeringen af eller rydde tredjepartscookies.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Fejl under sammenkædning af miljøet ved dobbeltskrivning eller tilføjelse af en ny tabeltilknytning

**Påkrævet rolle for at løse problemet:** Systemadministrator i både Finance and Operations-apps og Dataverse.

Der kan opstå følgende fejl under sammenkædning eller oprettelse af tilknytninger:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 403 (tokenexchange).<br> Sessions-id: \<your session id\><br> Rodaktivitets-id: \<your root activity id\>*

Denne fejl kan forekomme, hvis du ikke har de nødvendige rettigheder til at sammenkæde dobbeltskrivning eller oprette tilknytninger. Denne fejl kan også opstå, hvis Dataverse-miljøet blev nulstillet uden at fjerne tilknytningen til dobbeltskrivning. Enhver bruger med rollen Systemadministrator i både Finance and Operations-apps og Dataverse kan sammenkæde miljøerne. Kun den bruger, der har konfigureret dobbeltskrivningsforbindelsen, kan tilføje nye tabeltilknytninger. Efter installationen kan enhver bruger med rollen Systemadministrator overvåge status og redigere tilknytningerne.

## <a name="error-when-you-stop-the-table-mapping"></a>Fejl, når du stopper tabeltilknytningen

Du kan få vist følgende fejlmeddelelse, når du forsøger at standse tabeltilknytninger:

*\[Forbudt\], \[{"status": 403, "kilde": "","meddelelse":"Fejl fra tokenudveksling: Brugeren har ikke adgang til forbindelsen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], fjernserveren returnerede en fejl: (403) forbudt.*

Denne fejl opstår, når det sammenkædede Dataverse-miljø ikke er tilgængeligt.

Du kan løse problemet ved at oprette en supportanmodning til dataintegrationsteamet. Tilknyt netværkssporingen, så dataintegrationsteamet kan markere tilknytningerne som **Kører ikke** i backend.

## <a name="error-while-trying-to-start-an-table-mapping"></a>Der opstod en fejl under forsøg på at starte en tabeltilknytning

Du kan få vist en fejl som følgende, når du forsøger at angive denne tilstand for en tilknytning til **Kører**:

*Den indledende datasynkronisering kan ikke fuldføres. Fejl: dobbeltskrivningsfejl - plugin-registrering mislykkedes: Der kan ikke oprettes metadata til dobbeltskrivningsopslag. Objektreference er ikke indstillet til en forekomst af et objekt.*

Rettelsen til denne fejl afhænger af årsagen til fejlen:

+ Hvis tilknytningen har afhængige tilknytninger, skal du sørge for at aktivere de afhængige tilknytninger for denne tabeltilknytning.
+ Tilknytningen mangler muligvis kilde- eller destinationsfelter. Hvis der mangler et felt i Finance and Operations-appen, skal du følge trinnene i afsnittet [Problemer med manglende enhedsfelter i tilknytninger](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). Hvis der mangler et felt i Dataverse, skal du klikke på knappen **Opdater tabeller** på tilknytningen, så felterne automatisk udfyldes i tilknytningen.
