---
title: Generel fejlfinding
description: Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.
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
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172685"
---
# <a name="general-troubleshooting"></a>Generel fejlfinding

[!include [banner](../../includes/banner.md)]



Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Når du forsøger at installere dobbeltskrivningspakken ved hjælp af værktøjet Package Deployer, vises der ingen tilgængelige løsninger

Nogle versioner af Package Deployer-værktøjet er inkompatible med pakken til dobbeltskrivningsløsninger. For at installere pakken korrekt skal du sørge for at bruge [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller nyere af Package Deployer-værktøjet.

Når du har installeret Package Deployer-værktøjet, skal du installere løsningspakken ved at følge disse trin.

1. Hent den seneste fil med løsningspakken fra Yammer.com. Når zip-filen med pakken er hentet, skal du højreklikke på den og vælge **Egenskaber**. Markér afkrydsningsfeltet **Ophæv blokering**, og vælg derefter **Anvend**. Hvis du ikke kan se afkrydsningsfeltet **Ophæv blokering**, er blokeringen af zip-filen allerede fjernet, og du kan springe dette trin over.

    ![Dialogboksen Egenskaber](media/unblock_option.png)

2. Udpak zip-filen med pakken, og kopier alle filerne i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![Indhold af mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. Indsæt alle de kopierede filer i mappen **Tools** i Package Deployer-værktøjet. 
4. Kør **PackageDeployer.exe** for at vælge Common Data Service-miljøet og installere løsningerne.

    ![Indhold af mappen Tools](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Aktivere og åbne plug-in-sporingslogge i Common Data Service for at få vist oplysninger om fejl

**Følgende rolle er påkrævet for at kunne aktivere sporingsloggen og få vist fejl:** systemadministrator

Udfør følgende trin for at aktivere sporingsloggen.

1. Log på Finance and Operations-appen, åbn siden **Indstillinger**, og vælg derefter **Administration** under **System**.
2. På siden **Administration** skal du vælge **Systemindstillinger**.
3. Under fanen **Tilpasning** i feltet **Plug-in og brugerdefineret sporing af arbejdsgangsaktivitet** skal du vælge **Alle** for at aktivere sporingslogfilen for plug-in'en. Hvis du kun vil logføre sporingslogge, når der opstår undtagelser, kan du vælge **Undtagelse** i stedet.


Udfør følgende trin for at få vist sporingsloggen.

1. Log på Finance and Operations-appen, åbn siden **Indstillinger**, og vælg derefter **Plug-in-sporingslogfil** under **Tilpasning**.
2. Find sporingslogfilerne, hvor feltet **Typenavn** er indstillet til **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.
3. Dobbeltklik på et element for at få vist hele loggen, og gennemse derefter **Message Block**-teksten i oversigtspanelet **Udførelse**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivere fejlfindingstilstand for at foretage fejlfinding af problemer med direkte synkronisering i Finance and Operations-apps

**Påkrævet rolle for at få vist fejl** : Systemadministrator

Dobbeltskrivningsfejl, der stammer fra Common Data Service, kan forekomme i Finance and Operations-appen. I nogle tilfælde er den fulde tekst i fejlmeddelelsen ikke tilgængelig, fordi meddelelsen er for lang eller indeholder personligt identificerbare oplysninger (PII). Du kan aktivere detaljeret logføring for fejl ved at følge disse trin.

1. Alle projektkonfigurationer i Finance and Operations-apps har egenskaben **IsDebugMode** i enheden **DualWriteProjectConfiguration**. Åbn enheden **DualWriteProjectConfiguration** ved hjælp af tilføjelsesprogrammet til Excel.

    > [!TIP]
    > En nem måde at åbne objektet på er at slå **Design**-tilstand til i Excel-tilføjelsesprogrammet og derefter tilføje **DualWriteProjectConfigurationEntity** i regnearket. Du kan finde flere oplysninger under [Åbne enhedsdata i Excel og opdatere dem ved hjælp af tilføjelsesprogrammet til Excel](../../office-integration/use-excel-add-in.md).

2. Indstil egenskaben **IsDebugMode** til **Ja** for projektet.
3. Kør det scenario, der genererer fejl.
4. De detaljerede logfiler er tilgængelige i tabellen DualWriteErrorLog. Hvis du vil slå data op i tabelbrowseren, skal du bruge følgende URL-adresse (Erstat **XXX** efter behov):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontrollere synkroniseringsfejl på den virtuelle maskine for Finance and Operations-appen

**Påkrævet rolle for at få vist fejl** : Systemadministrator

1. Log på Microsoft Dynamics LifeCycle Services (LCS).
2. Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstesten for.
3. Vælg titlen **Skybaserede miljøer**.
4. Brug Fjernskrivebord til at logge på den virtuelle maskine (VM) for Finance and Operations-appen. Brug den lokale konto, der vises i LCS.
5. Åbn Logbog.
6. Vælg **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**.
7. Gennemse listen over seneste fejl.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Fjerne sammenkædning og sammenkæde med et andet Common Data Service-miljø fra en Finance and Operations-app

**Påkrævede legitimationsoplysninger for at fjerne sammenkædningen af miljøet**: Azure AD-lejeradministrator

1. Log på Finance and Operations-appen.
2. Gå til **Arbejdsområder \> Datastyring**, og vælg feltet **Dobbeltskrivning**.
3. Vælg alle kørende tilknytninger, og vælg derefter **Stop**.
4. Vælg **Ophæv sammenkædning af miljø**.
5. Vælg **Ja** for at bekræfte operationen.

Nu kan du sammenkæde et nyt miljø.
