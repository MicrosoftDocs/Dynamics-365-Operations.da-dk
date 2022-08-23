---
title: Fejlfinde problemer under den indledende opsætning
description: Denne artikel indeholder oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289508"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Fejlfinde problemer under den indledende opsætning

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder fejlfindingsoplysninger for dobbeltskrivning mellem programmer til finans og drift og Dataverse. Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.

> [!IMPORTANT]
> Nogle af de problemer, som denne artikel vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Du kan ikke oprette et link mellem et program til finans og drift og Dataverse

**Påkrævet rolle for at konfigurere dobbeltskrivning:** Systemadministrator i programmer til finans og drift og Dataverse.

Fejl på siden **Opsætning af sammenkædning til Dataverse** er normalt forårsaget af ufuldstændige opsætnings- eller rettighedsproblemer. Kontroller, at hele tilstandskontrollen bliver gennemført tilfredsstillende på siden **Opsætning af sammenkædning til Dataverse**, som vist i følgende illustration. Du kan ikke sammenkæde med Dobbeltskrivning, medmindre hele tilstandskontrollen gennemføres tilfredsstillende.

![Vellykket tilstandskontrol.](media/health_check.png)

Du skal have legitimationsoplysninger som Azure AD-lejeradministrator for at kunne sammenkæde programmer til finans og drift og Dataverse-miljøer. Når du har kædet miljøerne sammen, kan brugerne logge på ved hjælp af deres legitimationsoplysninger til deres konto og opdatere en eksisterende tabeltilknytning.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finde grænsen for antallet af juridiske tabeller eller firmaer, der kan sammenkædes ved dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at aktivere tilknytninger:

*Fejl under dobbeltskrivning – plugin-registrering mislykkedes: [(Kan ikke hente partitionstilknytning for projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Fejl: Overstiger det maksimale antal partitioner, der er tilladt for tilknytning af DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Der opstod en eller flere fejl.*

Den aktuelle grænse, når du sammenkæder miljøerne, er ca. 40 juridiske tabeller. Denne fejl opstår, hvis du forsøger at aktivere tilknytninger, og mere end 40 juridiske tabeller sammenkædes mellem miljøerne.

## <a name="connection-set-failed-while-linking-environment"></a>Forbindelsessættet mislykkedes under tilknytning af miljø

Under tilknytning af miljø for dobbeltskrivning mislykkes handlingen med en fejlmeddelelse:

*Lagring af forbindelsessættet mislykkedes! Der er allerede tilføjet en vare med samme nøgle.*

Dobbeltskrivning understøtter ikke flere juridiske enheder/firmaer med samme navn. Hvis du f.eks. har to firmaer med navnet "DAT" i Dataverse, vises denne fejlmeddelelse.

Hvis du vil fjerne spærringen af kunden, skal du fjerne identiske poster fra tabellen **cdm_company** i Dataverse. Hvis tabellen **cdm_company** indeholder poster med et tomt navn, skal du også fjerne eller rette de pågældende poster.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Fejl ved åbning af dobbeltskrivningsside i programmer til finans og drift

Du kan modtage følgende fejlmeddelelse, når du forsøger at knytte et Dataverse-miljø til dobbeltskrivning:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 404 (Ikke fundet).*

Denne fejl opstår, når trinnet for appindhold ikke er fuldført. Du kan validere, om der er givet samtykke ved at logge på `portal.azure.com` med lejeradministratorens konto og kontrollere, om tredjepartsappen med id'et `33976c19-1db5-4c02-810e-c243db79efde` vises på AAD's Enterprise-programliste. Hvis ikke, skal du køre trinnet for samtykke igen som beskrevet i næste afsnit.

### <a name="providing-app-consent"></a>Give samtykke til app

+ Start følgende URL-adresse med administratorens legitimationsoplysninger.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Vælg **Acceptér** for at samtykke. Du giver dit samtykke til at installere appen (med `id=33976c19-1db5-4c02-810e-c243db79efde`) i din lejer.
+ Denne app skal bruges til Dataverse for at kommunikere med programmer til finans og drift.

    ![Fejlfinding af opsætning af den første synkronisering.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Hvis det ikke fungerer, skal URL-adressen startes i privat tilstand i Microsoft Edge eller i inkognito-tilstand i Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finans og driftsmiljø kan ikke registreres

Du kan modtage følgende fejlmeddelelse:

*Programmer til finans og drift-miljø \*\*\*.cloudax.dynamics.com kan ikke findes.*

Der er to ting, der kan medføre, at et problem med miljøet ikke bliver opdaget:

+ Den bruger, der skal logge på, er ikke i samme lejer som finans og driftsforekomsten.
+ Der er nogle ældre forekomster af finans og drift, som Microsoft var vært for, og som havde et problem med produktopdagelse. Du kan løse dette ved at opdatere forekomsten af finans og drift. Efter en opdatering kan miljøet findes.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>Fejlen 403 (forbudt) mens der oprettes forbindelser

Som en del af processen til sammenkædning af dobbeltskrivning oprettes der to Power Apps-forbindelser (også kaldet *Apihub*-forbindelser) på vegne af brugeren i det tilknyttede Dataverse-miljø. Hvis kunden ikke har en licens til Power Apps-miljøet, mislykkes oprettelsen af ApiHub-forbindelser, og der vises en fejl 403 (forbudt). Her er et eksempel på fejlmeddelelsen:

> MSG=\[Der blev ikke konfigureret et dobbeltskrivningsmiljø. Fejloplysninger: Svarstatuskoden tyder ikke på, at handlingen lykkedes: 403 (forbudt). - Svarstatuskoden tyder ikke på, at handlingen lykkedes: 403 (forbudt).\] STACKTRACE=\[   at Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() i X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- Slut på stakspor fra forrige lokation, hvor undtagelse opstod --- ved System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() ved System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) ved Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() i X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

Denne fejl opstår pga. manglende Power Apps-licens. Tildel brugeren en passende licens (f.eks. Power Apps Prøve 2-plan), så brugeren har tilladelse til at oprette forbindelser. Hvis kunden vil kontrollere licensen, kan kunden gå til webstedet [Min konto](https://portal.office.com/account/?ref=MeControl#subscriptions) for at se de licenser, der aktuelt er tildelt brugeren.

Du kan finde flere oplysninger om Power Apps-licens i følgende artikler:

- [Tildele brugere licenser](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Køb Power Apps til din organisation](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

