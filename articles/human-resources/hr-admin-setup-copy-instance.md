---
title: Kopiér en forekomst
description: Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: e8385b7dfcd1d7294542c7f54f609b26b7988ac4
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431239"
---
# <a name="copy-an-instance"></a>Kopiér en forekomst

Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø. Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.

Hvis du vil kopiere en forekomst, skal du sikre dig følgende:

- Den forekomst af Personale, du vil overskrive, skal være et sandkassemiljø.

- De miljøer, du kopierer fra og til, skal være i samme område. Du kan ikke kopiere på tværs af områder.

- Du skal være administrator i destinationsmiljøet, så du kan logge på, når du har kopieret forekomsten.

- Når du kopierer Personale-databasen, kopierer du ikke de elementer (apps eller data), der er indeholdt i et Microsoft PowerApps-miljø. Yderligere oplysninger om kopiering af elementer i et PowerApps-miljø finder du i [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment). Det PowerApps-miljø, du vil overskrive, skal være et sandkassemiljø. Du skal være global lejeradministrator for at kunne ændre et PowerApps-produktionsmiljø til et sandkassemiljø. Yderligere oplysninger om ændring af et PowerApps-miljø finder du [Skifte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance)forekomst.

## <a name="effects-of-copying-a-human-resources-database"></a>Virkninger af kopiering af en Personale-database

Følgende hændelser indtræffer, når du kopierer en Personale-database:

- Kopieringsprocessen sletter den eksisterende database i destinationsmiljøet. Når kopieringsprocessen er fuldført, kan du ikke gendanne den eksisterende database.

- Destinationsmiljøet vil ikke være tilgængeligt, før kopieringsprocessen er fuldført.

- Dokumenter i Microsoft Azure Blob-lager kopieres ikke fra ét miljø til et andet. Eventuelle dokumenter og skabeloner, der er vedhæftet, kopieres derfor ikke men forbliver i kildemiljøet.

- Alle brugere undtagen administratorbrugere og andre interne tjenestebrugerkonti er derfor ikke tilgængelige. Administratorbrugeren kan derfor slette eller sløre data, før andre brugere får adgang til systemet igen.

- Administratorbrugeren skal foretage påkrævede konfigurationsændringer, f.eks. genoprette forbindelse mellem integrationsslutpunkter og bestemte tjenester eller URL-adresser.

## <a name="copy-the-human-resources-database"></a>Kopiere Personale-databasen

Hvis du vil fuldføre denne opgave, skal du først kopiere en forekomst og derefter logge på Microsoft Power Platform Administration for at kopiere dit PowerApps-miljø.

> [!WARNING]
> Når du kopierer en forekomst, slettes databasen i destinationsforekomsten. Destinationsforekomsten er ikke tilgængelig under denne proces.

1. Log på LCS, og vælg det LCS-projekt, der indeholder den forekomst, du vil kopiere.

2. I LCS-projektet skal du vælge feltet **Administration af Personale-app**.

3. Vælg den forekomst, der skal kopieres, og vælg derefter **Kopier**.

4. I opgaveruden **Kopier en forekomst** skal du markere den forekomst, der skal overskrives, og derefter vælge **Kopier**. Vent, indtil værdien i feltet **Kopieringsstatus** opdateres til **Fuldført**.

   ![[Vælg en forekomst, der skal overskrives](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Vælg **Power Platform**, og log på Microsoft Power Platform Administration.

   ![[Vælg Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Vælg det PowerApps-miljø, der skal kopieres, og vælg derefter **Kopier**.

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

Nogle af disse elementer kopieres ikke, fordi de er miljøspecifikke. Eksempler omfatter posterne **BatchServerConfig** og **SysCorpNetPrinters**. Andre elementer kopieres ikke på grund af antallet af supportanmodninger. Der kan f.eks. sendes duplikerede e-mails, fordi SMTP stadig er aktiveret i testmiljøet til brugeraccept (sandkasse), der kan blive sendt ugyldige integrationsmeddelelser, fordi batchjobbene stadig er aktiveret, og brugerne kan være aktiverede, før administratorer kan udføre handlinger til oprydning efter opdatering.

Følgende statusser ændres desuden, når du kopierer en forekomst:

- Alle brugere undtagen administrator angives til **Deaktiveret**.

- Alle batchjob, bortset fra visse systemjob, angives til **Tilbagehold.**

## <a name="environment-admin"></a>Miljøadmin

Alle brugere i destinationens sandkassemiljøet, herunder administratorer, erstattes af brugerne af kildemiljøet. Før du kopierer en forekomst, skal du sikre dig, at du er administrator i destinationsmiljøet. Er du ikke det, kan du ikke logge på destinationens sandkassemiljø, når kopieringen er fuldført.

Alle brugere, der ikke er administratorer i destinationens sandkassemiljø, er deaktiveret for at forhindre uønsket logon i sandkassemiljøet. Administratorer kan genaktivere brugerne, hvis det er nødvendigt.
