---
title: Kopiér en forekomst
description: Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 935c2e6cb45df193e6cbf70634f3561154c6fe38
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178527"
---
# <a name="copy-an-instance"></a>Kopiér en forekomst

_**Anvendes på:** Human Resources i enkeltstående infrastruktur_ 

> [!NOTE]
> Fra og med juni 2022 kan Personale-miljøer kun implementeres på infrastrukturen i program til finans og drift-infrastruktur. Du kan finde flere oplysninger i [Klargøre Human Resources i infrastruktur til finans og drift](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finans og drift-infrastrukturen understøtter ikke en funktion til kopieringsforekomst. Du kan implementere nye miljøer og bruge databasebevægelser til at oprette kopier. Du kan finde flere oplysninger om opsætning af medarbejderselvbetjening i [Oversigt over medarbejder- og lederselvbetjening](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Yderligere oplysninger om databasebevægelser på infrastrukturen i finans og operationer finder du på [startsiden for databasebevægelsesoperationer](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø. Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.

Hvis du vil kopiere en forekomst, skal du huske at følge nedenstående tip:

- Den forekomst af Human Resources, du vil overskrive, skal være et sandkassemiljø.

- De miljøer, du kopierer fra og til, skal være i samme område. Du kan ikke kopiere på tværs af områder.

- Du skal være administrator i destinationsmiljøet, så du kan logge på, når du har kopieret forekomsten.

- Når du kopierer Human Resources-databasen, kopierer du ikke de elementer (apps eller data), der er indeholdt i et Microsoft Power Apps-miljø. Yderligere oplysninger om kopiering af elementer i et Power Apps-miljø finder du i [Kopiere et miljø](/power-platform/admin/copy-environment). Det Power Apps-miljø, du vil overskrive, skal være et sandkassemiljø. Du skal være global lejeradministrator for at kunne ændre et Power Apps-produktionsmiljø til et sandkassemiljø. Yderligere oplysninger om ændring af et Power Apps-miljø finder du [Skifte en forekomst](/dynamics365/admin/switch-instance)forekomst.

- Hvis du kopierer en forekomst til dit sandkassemiljø og vil integrere dit sandkassemiljø med Dataverse, skal du genanvende brugerdefinerede felter på Dataverse-tabeller. Se [Anvende brugerdefinerede felter i Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Virkninger af kopiering af en Human Resources-database

Følgende hændelser indtræffer, når du kopierer en Human Resources-database:

- Kopieringsprocessen sletter den eksisterende database i destinationsmiljøet. Når kopieringsprocessen er fuldført, kan du ikke gendanne den eksisterende database.

- Destinationsmiljøet vil ikke være tilgængeligt, før kopieringsprocessen er fuldført.

- Dokumenter i Microsoft Azure Blob-lager kopieres ikke fra ét miljø til et andet. Eventuelle dokumenter og skabeloner, der er vedhæftet, kopieres derfor ikke men forbliver i kildemiljøet.

- Alle brugere med undtagelse af dem, der har sikkerhedsrollen "Systemadministrator" og andre interne tjenestebrugerkonti, vil ikke være tilgængelige. Administratorbrugeren kan derfor slette data, før andre brugere får adgang til systemet igen.

- Enhver bruger med sikkerhedsrollen "Systemadministrator" skal foretage påkrævede konfigurationsændringer, f.eks. genoprette forbindelse mellem integrationsslutpunkter og bestemte tjenester eller URL-adresser.

## <a name="copy-the-human-resources-database"></a>Kopiere Human Resources-databasen

Hvis du vil fuldføre denne opgave, skal du først kopiere en forekomst og derefter logge på Microsoft Power Platform Administration for at kopiere dit Power Apps-miljø.

> [!WARNING]
> Når du kopierer en forekomst, slettes databasen i destinationsforekomsten. Destinationsforekomsten er ikke tilgængelig under denne proces.

1. Log på LCS, og vælg det LCS-projekt, der indeholder den forekomst, du vil kopiere.

2. I LCS-projektet skal du vælge feltet **Administration af Human Resources-app**.

3. Vælg den forekomst, der skal kopieres, og vælg derefter **Kopier**.

4. I opgaveruden **Kopier en forekomst** skal du markere den forekomst, der skal overskrives, og derefter vælge **Kopier**. Vent, indtil værdien i feltet **Kopieringsstatus** opdateres til **Fuldført**.

   ![[Vælg forekomst, der skal overskrives.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Vælg **Power Platform**, og log på Microsoft Power Platform Administration.

   ![[Vælg Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Vælg det Power Apps-miljø, der skal kopieres, og vælg derefter **Kopier**.

Du kan finde flere oplysninger om kopiering af Power Apps-miljøer i [Kopier et miljø](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Når kopieringsprocessen er fuldført, skal du logge på destinationsforekomsten og aktivere Dataverse-integration. Du kan finde flere oplysninger og instruktioner under [Konfigurere Dataverse-integration](./hr-admin-integration-common-data-service.md).

## <a name="data-elements-and-statuses"></a>Dataelementer og statusser

Følgende dataelementer kopieres ikke, når du kopierer en forekomst af Human Resources:

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

- Alle brugere med undtagelse af dem, der har sikkerhedsrollen "Systemadministrator", er angivet til **Deaktiveret**.

- Alle batchjob, bortset fra visse systemjob, angives til **Tilbagehold.**

## <a name="environment-admin"></a>Miljøadmin

Alle brugere i destinationens sandkassemiljøet, herunder administratorer, erstattes af brugerne af kildemiljøet. Før du kopierer en forekomst, skal du sikre dig, at du er administrator i kildemiljøet. Er du ikke det, kan du ikke logge på destinationens sandkassemiljø, når kopieringen er fuldført.

Alle brugere, der ikke er administratorer i destinationens sandkassemiljø, er deaktiveret for at forhindre uønsket logon i sandkassemiljøet. Administratorer kan genaktivere brugerne, hvis det er nødvendigt.

## <a name="apply-custom-fields-to-dataverse"></a>Anvende brugerdefinerede felter i Dataverse

Hvis du kopierer en forekomst til dit sandkassemiljø og vil integrere dit sandkassemiljø med Dataverse, skal du genanvende brugerdefinerede felter på Dataverse-tabeller.

Udfør følgende trin for hvert brugerdefineret felt, der vises i Dataverse-tabeller:

1. Gå til det brugerdefinerede felt, og vælg **Rediger**.

2. Fjern markeringen i feltet **Aktiveret** for hver cdm_*-enhed, som det brugerdefinerede felt er aktiveret i.

3. Vælg **Anvend ændringer**.

4. Vælg **Rediger** igen.

5. Vælg feltet **Aktiveret** for hver cdm_*-enhed, som det brugerdefinerede felt er aktiveret i.

6. Vælg **Anvend ændringer** igen.

Ved at fravælge, anvende ændringer, vælge igen og genanvende ændringer vil det skema, der opdateres i Dataverse, indeholde de brugerdefinerede felter.

Du kan finde flere oplysninger om brugerdefinerede felter under [Oprette og arbejde med brugerdefinerede felter](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Se også

[Klargør Human Resources](hr-admin-setup-provision.md)</br>
[Fjern en forekomst](hr-admin-setup-remove-instance.md)</br>
[Opdater proces](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
