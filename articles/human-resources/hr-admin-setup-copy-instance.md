---
title: Kopiér en forekomst
description: Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40ca0a4d9733fc2a163daa4ea1c27a3bfae6d3bf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527831"
---
# <a name="copy-an-instance"></a>Kopiér en forekomst

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø. Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.

Hvis du vil kopiere en forekomst, skal du huske at følge nedenstående tip:

- Den forekomst af Personale, du vil overskrive, skal være et sandkassemiljø.

- De miljøer, du kopierer fra og til, skal være i samme område. Du kan ikke kopiere på tværs af områder.

- Du skal være administrator i destinationsmiljøet, så du kan logge på, når du har kopieret forekomsten.

- Når du kopierer Personale-databasen, kopierer du ikke de elementer (apps eller data), der er indeholdt i et Microsoft Power Apps-miljø. Yderligere oplysninger om kopiering af elementer i et Power Apps-miljø finder du i [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment). Det Power Apps-miljø, du vil overskrive, skal være et sandkassemiljø. Du skal være global lejeradministrator for at kunne ændre et Power Apps-produktionsmiljø til et sandkassemiljø. Yderligere oplysninger om ændring af et Power Apps-miljø finder du [Skifte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance)forekomst.

- Hvis du kopierer en forekomst til dit sandkassemiljø og vil integrere dit sandkassemiljø med Common Data Service, skal du genanvende brugerdefinerede felter på Common Data Service-objekter. Se [Anvende brugerdefinerede felter i Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Virkninger af kopiering af en Personale-database

Følgende hændelser indtræffer, når du kopierer en Personale-database:

- Kopieringsprocessen sletter den eksisterende database i destinationsmiljøet. Når kopieringsprocessen er fuldført, kan du ikke gendanne den eksisterende database.

- Destinationsmiljøet vil ikke være tilgængeligt, før kopieringsprocessen er fuldført.

- Dokumenter i Microsoft Azure Blob-lager kopieres ikke fra ét miljø til et andet. Eventuelle dokumenter og skabeloner, der er vedhæftet, kopieres derfor ikke men forbliver i kildemiljøet.

- Alle brugere undtagen administratorbrugere og andre interne tjenestebrugerkonti er derfor ikke tilgængelige. Administratorbrugeren kan derfor slette eller sløre data, før andre brugere får adgang til systemet igen.

- Administratorbrugeren skal foretage påkrævede konfigurationsændringer, f.eks. genoprette forbindelse mellem integrationsslutpunkter og bestemte tjenester eller URL-adresser.

## <a name="copy-the-human-resources-database"></a>Kopiere Personale-databasen

Hvis du vil fuldføre denne opgave, skal du først kopiere en forekomst og derefter logge på Microsoft Power Platform Administration for at kopiere dit Power Apps-miljø.

> [!WARNING]
> Når du kopierer en forekomst, slettes databasen i destinationsforekomsten. Destinationsforekomsten er ikke tilgængelig under denne proces.

1. Log på LCS, og vælg det LCS-projekt, der indeholder den forekomst, du vil kopiere.

2. I LCS-projektet skal du vælge feltet **Administration af Personale-app**.

3. Vælg den forekomst, der skal kopieres, og vælg derefter **Kopier**.

4. I opgaveruden **Kopier en forekomst** skal du markere den forekomst, der skal overskrives, og derefter vælge **Kopier**. Vent, indtil værdien i feltet **Kopieringsstatus** opdateres til **Fuldført**.

   ![[Vælg forekomst, der skal overskrives](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Vælg **Power Platform**, og log på Microsoft Power Platform Administration.

   ![[Vælg Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Vælg det Power Apps-miljø, der skal kopieres, og vælg derefter **Kopier**.

7. Når kopieringsprocessen er fuldført, skal du logge på destinationsforekomsten og aktivere Common Data Service-integration. Du kan finde flere oplysninger og instruktioner under [Konfigurere Common Data Service-integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Dataelementer og statusser

Følgende dataelementer kopieres ikke, når du kopierer en forekomst af Personale:

- E-mailadresser i tabellen **LogisticsElectronicAddress**

- Historikken for batchjobbet i tabellerne **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory**

- SMTP-adgangskoden (Simple Mail Transfer Protocol) i tabellen **SysEmailSMTPPassword**

- SMTP-Relay-serveren i tabellen **SysEmailParameters**

- Indstillinger for Udskriftsstyring i tabellerne **PrintMgmtSettings** og **PrintMgmtDocInstance**

- Miljøspecifikke poster i tabellerne **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**

- Vedhæftede dokumenter i tabellen DocuValue. Disse vedhæftede filer kan omfatte eventuelle Microsoft Office-skabeloner, der er overskrevet i kildemiljøet

- Forbindelsesstrengen i tabellen **PersonnelIntegrationConfiguration**

Nogle af disse elementer kopieres ikke, fordi de er miljøspecifikke. Eksempler omfatter posterne **BatchServerConfig** og **SysCorpNetPrinters**. Andre elementer kopieres ikke på grund af antallet af supportanmodninger. F.eks.:

- Der kan sendes duplikerede mails, fordi SMTP stadig er aktiveret i miljøet til test af brugeraccept (sandkasse).

- Der kan sendes ugyldige integrationsmeddelelser, fordi batchjobbene stadig er aktiveret.

- Brugere kan være aktiveret, før administratorer kan udføre oprydningshandlinger efter opdatering.

Følgende statusser ændres også, når du kopierer en forekomst:

- Alle brugere undtagen administrator angives til **Deaktiveret**.

- Alle batchjob, bortset fra visse systemjob, angives til **Tilbagehold.**

## <a name="environment-admin"></a>Miljøadmin

Alle brugere i destinationens sandkassemiljøet, herunder administratorer, erstattes af brugerne af kildemiljøet. Før du kopierer en forekomst, skal du sikre dig, at du er administrator i kildemiljøet. Er du ikke det, kan du ikke logge på destinationens sandkassemiljø, når kopieringen er fuldført.

Alle brugere, der ikke er administratorer i destinationens sandkassemiljø, er deaktiveret for at forhindre uønsket logon i sandkassemiljøet. Administratorer kan genaktivere brugerne, hvis det er nødvendigt.

## <a name="apply-custom-fields-to-common-data-service"></a>Anvende brugerdefinerede felter i Common Data Service

Hvis du kopierer en forekomst til dit sandkassemiljø og vil integrere dit sandkassemiljø med Common Data Service, skal du genanvende brugerdefinerede felter på Common Data Service-objekter.

Udfør følgende trin for hvert brugerdefineret felt, der vises i Common Data Service-objekter:

1. Gå til det brugerdefinerede felt, og vælg **Rediger**.

2. Fjern markeringen i feltet **Aktiveret** for hver cdm_*-enhed, som det brugerdefinerede felt er aktiveret i.

3. Vælg **Anvend ændringer**.

4. Vælg **Rediger** igen.

5. Vælg feltet **Aktiveret** for hver cdm_*-enhed, som det brugerdefinerede felt er aktiveret i.

6. Vælg **Anvend ændringer** igen.

Ved at fravælge, anvende ændringer, vælge igen og genanvende ændringer vil det skema, der opdateres i Common Data Service, indeholde de brugerdefinerede felter.

Du kan finde flere oplysninger om brugerdefinerede felter under [Oprette og arbejde med brugerdefinerede felter](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).

## <a name="see-also"></a>Se også

[Klargør Human Resources](hr-admin-setup-provision.md)</br>
[Fjern en forekomst](hr-admin-setup-remove-instance.md)</br>
[Opdater proces](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]