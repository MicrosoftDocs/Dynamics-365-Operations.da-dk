---
title: Foretage fejlfinding af problemer under den indledende opsætning
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2b75155aac12d79b9d68cce3e066acaaf80d6764
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380182"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Foretage fejlfinding af problemer under den indledende opsætning

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Du kan ikke sammenkæde en Finance and Operations-app med Dataverse

**Påkrævet rolle for at konfigurere dobbeltskrivning:** Systemadministrator i Finance and Operations-apps og Dataverse.

Fejl på siden **Opsætning af sammenkædning til Dataverse** er normalt forårsaget af ufuldstændige opsætnings- eller rettighedsproblemer. Kontroller, at hele tilstandskontrollen bliver gennemført tilfredsstillende på siden **Opsætning af sammenkædning til Dataverse**, som vist i følgende illustration. Du kan ikke sammenkæde med Dobbeltskrivning, medmindre hele tilstandskontrollen gennemføres tilfredsstillende.

![Vellykket tilstandskontrol.](media/health_check.png)

Du skal have rettigheder som Azure AD-lejeradministrator for at kunne sammenkæde Finance and Operations- og Dataverse-miljøer. Når du har kædet miljøerne sammen, kan brugerne logge på ved hjælp af deres legitimationsoplysninger til deres konto og opdatere en eksisterende tabeltilknytning.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finde grænsen for antallet af juridiske tabeller eller firmaer, der kan sammenkædes ved dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at aktivere tilknytninger:

*Fejl under dobbeltskrivning – plugin-registrering mislykkedes: [(Kan ikke hente partitionstilknytning for projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Fejl: Overstiger det maksimale antal partitioner, der er tilladt for tilknytning af DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Der opstod en eller flere fejl.*

Den aktuelle grænse, når du sammenkæder miljøerne, er ca. 40 juridiske tabeller. Denne fejl opstår, hvis du forsøger at aktivere tilknytninger, og mere end 40 juridiske tabeller sammenkædes mellem miljøerne.

## <a name="connection-set-failed-while-linking-environment"></a>Forbindelsessættet mislykkedes under tilknytning af miljø

Under tilknytning af miljø for dobbeltskrivning mislykkes handlingen med en fejlmeddelelse:

*Lagring af forbindelsessættet mislykkedes! Der er allerede tilføjet en vare med samme nøgle.*

Dobbeltskrivning understøtter ikke flere juridiske enheder/firmaer med samme navn. Hvis du f.eks. har to firmaer med navnet "DAT" i Dataverse, vises denne fejlmeddelelse.

Hvis du vil fjerne spærringen af kunden, skal du fjerne identiske poster fra tabellen **cdm_company** i Dataverse. Hvis tabellen **cdm_company** indeholder poster med et tomt navn, skal du også fjerne eller rette de pågældende poster.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Fejl ved åbning af siden for dobbeltudskrivning i Finance and Operations-apps

Du kan modtage følgende fejlmeddelelse, når du forsøger at knytte et Dataverse-miljø til dobbeltskrivning:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 404 (Ikke fundet).*

Denne fejl opstår, når trinnet for appindhold ikke er fuldført. Du kan validere, om der er givet samtykke ved at logge på `portal.azure.com` med lejeradministratorens konto og kontrollere, om tredjepartsappen med id'et `33976c19-1db5-4c02-810e-c243db79efde` vises på AAD's Enterprise-programliste. Hvis ikke, skal du køre trinnet for samtykke igen som beskrevet i næste afsnit.

### <a name="providing-app-consent"></a>Give samtykke til app

+ Start følgende URL-adresse med administratorens legitimationsoplysninger.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Vælg **Acceptér** for at samtykke. Du giver dit samtykke til at installere appen (med `id=33976c19-1db5-4c02-810e-c243db79efde`) i din lejer.
+ Denne app skal bruges for Dataverse for at kommunikere med Finance and Operations-apps.

    ![Fejlfinding af opsætning af den første synkronisering.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Hvis det ikke fungerer, skal URL-adressen startes i privat tilstand i Microsoft Edge eller i inkognito-tilstand i Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations-miljø kan ikke findes

Du kan modtage følgende fejlmeddelelse:

*Finance and Operations-appmiljø \*\*\*.cloudax.dynamics.com kan ikke findes.*

Der er to ting, der kan medføre, at et problem med miljøet ikke bliver opdaget:

+ Den bruger, der skal logge på, er ikke i samme lejer som Finance and Operations-forekomsten.
+ Der er nogle ældre Finance and Operations-forekomster, som Microsoft var vært for, og som havde et problem med søgning. Du kan løse dette ved at opdatere Finance and Operations-forekomsten. Efter en opdatering kan miljøet findes.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
