---
title: Foretage fejlfinding af problemer under den indledende opsætning
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration mellem Finance and Operations-apps og Common Data Service.
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
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172662"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Foretage fejlfinding af problemer under den indledende opsætning

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Du kan ikke sammenkæde en Finance and Operations-app med Common Data Service

**Påkrævede legitimationsoplysninger til opsætning af dobbeltskrivning:** Azure AD-lejeradministrator

Fejl på siden **Opsætning af sammenkædning til Common Data Service** er normalt forårsaget af ufuldstændige opsætnings- eller rettighedsproblemer. Kontroller, at hele tilstandskontrollen bliver gennemført tilfredsstillende på siden **Opsætning af sammenkædning til Common Data Service**, som vist i følgende illustration. Du kan ikke sammenkæde med Dobbeltskrivning, medmindre hele tilstandskontrollen gennemføres tilfredsstillende.

![Vellykket tilstandskontrol](media/health_check.png)

Du skal have rettigheder som Azure AD-lejeradministrator for at kunne sammenkæde Finance and Operations- og Common Data Service-miljøer. Når du har kædet miljøerne sammen, kan brugerne logge på ved hjælp af deres legitimationsoplysninger til deres konto og opdatere en eksisterende enhedstilknytning.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Fejl, når du åbner siden Sammenkædning med Common Data Service

**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator

Du kan få vist følgende fejlmeddelelse, når du åbner **Sammenkædning med Common Data Service** i en Finance and Operations-app:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 404 (Ikke fundet).*

Denne fejl opstår, når samtykketrinnet ikke blev fuldført. Hvis du vil validere, om samtykketrinnet er fuldført, skal du logge på portal.Azure.com ved hjælp af Azure AD-lejeradministratorkontoen og se, om den tredjepartsapp, der har id'et **33976c19-1db5-4c02-810e-c243db79efde**, vises på listen over Azure AD **virksomhedsprogrammer**. Hvis ikke, skal du give samtykke til appen.

Du kan give appsamtykke ved at følge disse trin.

1. Åbn følgende URL-adresse ved hjælp af dine administratorlegitimationsoplysninger. Du bliver bedt om at give dit samtykke.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Vælg **Accepter** for at angive, at du giver samtykke til at installere appen, der har id'et **33976c19-1db5-4c02-810e-c243db79efde** i din lejer.

    > [!TIP]
    > Denne app kræves for at kunne oprette sammenkæde Common Data Service- og Finance and Operations-apps. Hvis du har problemer med dette trin, skal du åbne browseren i Incognito-tilstand (i Google Chrome) eller i InPrivate-tilstand (i Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Kontrollere, at firmadata og dobbeltskrivningsteams er konfigureret korrekt under sammenkædning

For at sikre, at dobbeltskrivningen fungerer korrekt, oprettes de firmaer, du vælger under konfigurationen, i Common Data Service-miljøet. Disse firmaer er som standard skrivebeskyttede, og egenskaben **IsDualWriteEnable** er indstillet til **True**. Derudover oprettes standardejer-virksomhedsenheden og -teamet og inkluderer firmanavnet. Før du aktiverer tilknytningerne, skal du kontrollere, at standardteamejeren er angivet. Udfør følgende trin for at finde **Firmaer (CDM\_Company)**.

1. I den modelbaserede app i Dynamics 365 skal du vælge filteret i øverste højre hjørne.
2. Vælg **Firma** på rullelisten.
3. Vælg **Kør** for at få vist resultaterne.
4. Vælg det regnskab, der blev sammenkædet, da du konfigurerede dobbelt skrivning.
5. Kontroller, at der er en værdi i feltet **Standardejerteam**. I følgende illustration er **Standardejerteam**-feltet indstillet til **USMF Dual Write**.

    ![Kontrollere standardejerteamet](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Finde grænsen for antallet af juridiske enheder eller firmaer, der kan sammenkædes ved dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at aktivere tilknytninger:

*Fejl under dobbeltskrivning – plugin-registrering mislykkedes: \[(det er ikke muligt at hente partitionstilknytningen for projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Fejl: Overstiger det maksimale antal partitioner, der er tilladt for tilknytning af DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Der opstod en eller flere fejl.*

Den aktuelle grænse, når du sammenkæder miljøerne, er ca. 40 juridiske enheder. Denne fejl opstår, hvis du forsøger at aktivere tilknytninger, og mere end 40 juridiske enheder sammenkædes mellem miljøerne.
