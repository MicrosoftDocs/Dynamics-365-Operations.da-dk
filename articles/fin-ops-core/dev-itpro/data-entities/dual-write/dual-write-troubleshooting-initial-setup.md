---
title: Foretage fejlfinding af problemer under den indledende opsætning
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første opsætning af dobbeltskrivningsintegration.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c641849b2aec76124b6661f339175325a312efce
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350830"
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

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Fejl, når du åbner siden Sammenkædning med Dataverse

**Påkrævede legitimationsoplysninger for at løse problemet**: Azure AD-lejeradministrator

Du kan få vist følgende fejlmeddelelse, når du åbner **Sammenkædning med Dataverse** i en Finance and Operations-app:

*Svarstatuskoden tyder ikke på, at handlingen lykkedes: 404 (Ikke fundet).*

Denne fejl opstår, når samtykketrinnet ikke blev fuldført. Hvis du vil validere, om samtykketrinnet er fuldført, skal du logge på portal.Azure.com ved hjælp af Azure AD-lejeradministratorkontoen og se, om den tredjepartsapp, der har id'et **33976c19-1db5-4c02-810e-c243db79efde**, vises på listen over Azure AD **virksomhedsprogrammer**. Hvis ikke, skal du give samtykke til appen.

Du kan give appsamtykke ved at følge disse trin.

1. Åbn følgende URL-adresse ved hjælp af dine administratorlegitimationsoplysninger. Du bliver bedt om at give dit samtykke.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Vælg **Accepter** for at angive, at du giver samtykke til at installere appen, der har id'et **33976c19-1db5-4c02-810e-c243db79efde** i din lejer.

    > [!TIP]
    > Denne app kræves for at kunne oprette sammenkæde Dataverse- og Finance and Operations-apps. Hvis du har problemer med dette trin, skal du åbne browseren i Incognito-tilstand (i Google Chrome) eller i InPrivate-tilstand (i Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Kontrollere, at firmadata og dobbeltskrivningsteams er konfigureret korrekt under sammenkædning

For at sikre, at dobbeltskrivningen fungerer korrekt, oprettes de firmaer, du vælger under konfigurationen, i Dataverse-miljøet. Disse firmaer er som standard skrivebeskyttede, og egenskaben **IsDualWriteEnable** er indstillet til **True**. Derudover oprettes standardejer-virksomhedsenheden og -teamet og inkluderer firmanavnet. Før du aktiverer tilknytningerne, skal du kontrollere, at standardteamejeren er angivet. Udfør følgende trin for at finde tabellen **Firmaer (CDM\_Firma)**.

1. I den modelbaserede app i Dynamics 365 skal du vælge filteret i øverste højre hjørne.
2. Vælg **Firma** på rullelisten.
3. Vælg **Kør** for at få vist resultaterne.
4. Vælg det regnskab, der blev sammenkædet, da du konfigurerede dobbelt skrivning.
5. Kontroller, at der er en værdi i kolonnen **Standardejerteam**. I følgende illustration er kolonnen **Standardejerteam** indstillet til **USMF-dobbeltskrivning**.

    ![Kontrollere standardejerteamet.](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finde grænsen for antallet af juridiske tabeller eller firmaer, der kan sammenkædes ved dobbeltskrivning

Du kan få vist følgende fejlmeddelelse, når du forsøger at aktivere tilknytninger:

*Fejl under dobbeltskrivning – plugin-registrering mislykkedes: \[(det er ikke muligt at hente partitionstilknytningen for projekt DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Fejl: Overstiger det maksimale antal partitioner, der er tilladt for tilknytning af DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Der opstod en eller flere fejl.*

Den aktuelle grænse, når du sammenkæder miljøerne, er ca. 40 juridiske tabeller. Denne fejl opstår, hvis du forsøger at aktivere tilknytninger, og mere end 40 juridiske tabeller sammenkædes mellem miljøerne.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]