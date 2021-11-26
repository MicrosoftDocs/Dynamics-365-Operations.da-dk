---
title: Foretage fejlfinding af problemer med dobbeltskrivning i Finance and Operations-apps
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med dobbeltskrivningsmodulet i Finance and Operations-apps.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 3caf3f18718fd6bee20232a0200d421b9c9ef22c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781192"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Foretage fejlfinding af problemer med dobbeltskrivning i Finance and Operations-apps

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med **dobbeltskrivningsmodulet** i Finance and Operations-apps.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Du kan ikke indlæse dobbeltskrivningsmodulet i en Finance and Operations-app

Hvis du ikke kan åbne **Dobbeltskrivning**-siden ved at vælge titlen **Dobbeltskrivning** i **Datastyring**-arbejdsområdet, er dataintegrationstjenesten sandsynligvis nede. Opret en supportanmodning for at anmode om genstart af dataintegrationstjenesten.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Fejl, når du forsøger at oprette en ny tabeltilknytning

**Påkrævede legitimationsoplysninger for at løse problemet:** Den samme bruger, der har konfigureret dobbeltskrivning.

Du kan få vist følgende fejlmeddelelse, når du forsøger at konfigurere en ny tabel til dobbeltskrivning. Den eneste bruger, der kan oprette en tilknytning, er den bruger, der har konfigureret dobbeltskrivningsforbindelsen.

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 401 (uautoriseret).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Fejl, når du åbner brugergrænsefladen til dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at få adgang til dobbeltskrivning fra arbejdsområdet **Datastyring**:

*login.microsoftonline.com afviste at oprette forbindelse.*

Du kan løse problemet ved at logge på ved hjælp af et InPrivate-vindue i Microsoft Edge, et incognito-vindue i Chromium eller et incognito-vindue i Google Chrome. Du skal også fjerne blokeringen af eller rydde tredjepartscookies.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Fejl under sammenkædning af miljøet ved dobbeltskrivning eller tilføjelse af en ny tabeltilknytning

**Påkrævet rolle for at løse problemet:** Systemadministrator i både Finance and Operations-apps og Dataverse.

Der kan opstå følgende fejl under sammenkædning eller oprettelse af tilknytninger:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Denne fejl kan forekomme, hvis du ikke har de nødvendige rettigheder til at sammenkæde dobbeltskrivning eller oprette tilknytninger. Denne fejl kan også opstå, hvis Dataverse-miljøet blev nulstillet uden at fjerne tilknytningen til dobbeltskrivning. Enhver bruger med rollen Systemadministrator i både Finance and Operations-apps og Dataverse kan sammenkæde miljøerne. Kun den bruger, der har konfigureret dobbeltskrivningsforbindelsen, kan tilføje nye tabeltilknytninger. Efter installationen kan enhver bruger med rollen Systemadministrator overvåge status og redigere tilknytningerne.

## <a name="error-when-you-stop-the-table-mapping"></a>Fejl, når du stopper tabeltilknytningen

Du kan få vist følgende fejlmeddelelse, når du forsøger at standse tabeltilknytninger:

*\[Forbudt\], \[{"status": 403, "kilde": "","meddelelse":"Fejl fra tokenudveksling: Brugeren har ikke adgang til forbindelsen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], fjernserveren returnerede en fejl: (403) forbudt.*

Denne fejl opstår, når det sammenkædede Dataverse-miljø ikke er tilgængeligt.

Du kan løse problemet ved at oprette en supportanmodning til dataintegrationsteamet. Tilknyt netværkssporingen, så dataintegrationsteamet kan markere tilknytningerne som **Kører ikke** i backend.

## <a name="errors-while-trying-to-start-a-table-mapping"></a>Der opstod fejl under forsøg på at starte en tabeltilknytning

### <a name="unable-to-complete-initial-data-sync"></a>Den første datasynkronisering kunne ikke fuldføres

Du kan få vist en fejlmeddelelse som den følgende, når du forsøger at køre den første synkronisering:

*Den indledende datasynkronisering kan ikke fuldføres. Fejl: dobbeltskrivningsfejl - plugin-registrering mislykkedes: Der kan ikke oprettes metadata til dobbeltskrivningsopslag. Objektreference er ikke indstillet til en forekomst af et objekt.*

Når du forsøger at angive denne tilstand for en tilknytning til **Kører**, kan du modtage denne fejlmeddelelse: Rettelsen afhænger af årsagen til fejlen:

+ Hvis tilknytningen har afhængige tilknytninger, skal du sørge for at aktivere de afhængige tilknytninger for denne tabeltilknytning.
+ Tilknytningen mangler muligvis kilde- eller destinationskolonner. Hvis der mangler en kolonne i Finance and Operations-appen, skal du følge trinnene i afsnittet [Problemer med manglende tabelkolonner i tilknytninger](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Hvis der mangler en kolonne i Dataverse, skal du klikke på knappen **Opdater tabeller** på tilknytningen, så kolonnerne automatisk udfyldes i tilknytningen.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Fejl pga. uoverensstemmelse mellem versioner og opgradering af dobbeltskrivningsløsninger

Du kan få vist følgende fejlmeddelelser, når du forsøger at køre tabeltilknytningerne:

+ *Debitorgrupper (msdyn_customergroups): Fejl under dobbeltskrivning - Dynamics 365 for Sales-løsningen 'Dynamics365Company har uoverensstemmelse mellem versioner. Version: '2.0.2.10' Påkrævet version: '2.0.133'*
+ *Dynamics 365 for Sales-løsningen 'Dynamics365FinanceExtended' har uoverensstemmelse mellem versioner. Version: '1.0.0.0' Påkrævet version: '2.0.227'*
+ *Dynamics 365 for Sales-løsningen 'Dynamics365FinanceAndOperationsCommon' har uoverensstemmelse mellem versioner. Version: '1.0.0.0' Påkrævet version: '2.0.133'*
+ *Dynamics 365 for Sales-løsningen 'CurrencyExchangeRates' har uoverensstemmelse mellem versioner. Version: '1.0.0.0' Påkrævet version: '2.0.133'*
+ *Dynamics 365 for Sales-løsningen 'Dynamics365SupplyChainExtended' har uoverensstemmelse mellem versioner. Version: '1.0.0.0' Påkrævet version: '2.0.227'*

Du kan løse problemerne ved at opdatere løsningerne til dobbeltskrivning i Dataverse. Sørg for at opgradere til den seneste løsning, som svarer til den ønskede løsningsversion.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
