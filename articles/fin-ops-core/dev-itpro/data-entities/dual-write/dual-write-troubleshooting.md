---
title: Generel fejlfinding
description: Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.
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
ms.openlocfilehash: 779cc80d4cb510e79885919f1c705824ab6ad58b3e2fe1bab7bbec0511d08951
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736296"
---
# <a name="general-troubleshooting"></a>Generel fejlfinding

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emne indeholder generelle fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Når du forsøger at installere dobbeltskrivningspakken ved hjælp af værktøjet Package Deployer, vises der ingen tilgængelige løsninger

Nogle versioner af Package Deployer-værktøjet er inkompatible med pakken til dobbeltskrivningsløsninger. For at installere pakken korrekt skal du sørge for at bruge [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller nyere af Package Deployer-værktøjet.

Når du har installeret Package Deployer-værktøjet, skal du installere løsningspakken ved at følge disse trin.

1. Hent den seneste fil med løsningspakken fra Yammer.com. Når zip-filen med pakken er hentet, skal du højreklikke på den og vælge **Egenskaber**. Markér afkrydsningsfeltet **Ophæv blokering**, og vælg derefter **Anvend**. Hvis du ikke kan se afkrydsningsfeltet **Ophæv blokering**, er blokeringen af zip-filen allerede fjernet, og du kan springe dette trin over.

    ![Dialogboksen Egenskaber.](media/unblock_option.png)

2. Udpak zip-filen med pakken, og kopier alle filerne i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![Indhold af mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.](media/extract_package.png)

3. Indsæt alle de kopierede filer i mappen **Tools** i Package Deployer-værktøjet. 
4. Kør **PackageDeployer.exe** for at vælge Dataverse-miljøet og installere løsningerne.

    ![Indhold af mappen Tools.](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivere og åbne plug-in-sporingslogge i Dataverse for at få vist oplysninger om fejl

**Følgende rolle er påkrævet for at kunne aktivere sporingsloggen og få vist fejl:** systemadministrator

Udfør følgende trin for at aktivere sporingsloggen.

1. Log på Customer Engagement-appen, åbn siden **Indstillinger**, og vælg derefter **Administration** under **System**.
2. På siden **Administration** skal du vælge **Systemindstillinger**.
3. Under fanen **Tilpasning** i kolonnen **Plug-in og brugerdefineret sporing af arbejdsgangsaktivitet** skal du vælge **Alle** for at aktivere sporingslogfilen for plug-in'en. Hvis du kun vil logføre sporingslogge, når der opstår undtagelser, kan du vælge **Undtagelse** i stedet.


Udfør følgende trin for at få vist sporingsloggen.

1. Log på Customer Engagement-appen, åbn siden **Indstillinger**, og vælg derefter **Plug-in-sporingslogfil** under **Tilpasning**.
2. Find sporingslogfilerne, hvor kolonnen **Typenavn** er indstillet til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dobbeltklik på et element for at få vist hele loggen, og gennemse derefter **Message Block**-teksten i oversigtspanelet **Udførelse**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivere fejlfindingstilstand for at foretage fejlfinding af problemer med direkte synkronisering i Finance and Operations-apps

**Påkrævet rolle for at få vist fejl**: Dobbeltskrivningsfejl i systemadministrationen, der stammer fra Dataverse, kan vises i appen Finance and Operations. I nogle tilfælde er den fulde tekst i fejlmeddelelsen ikke tilgængelig, fordi meddelelsen er for lang eller indeholder personligt identificerbare oplysninger (PII). Du kan aktivere detaljeret logføring for fejl ved at følge disse trin.

1. Alle projektkonfigurationer i Finance and Operations-apps har egenskaben **IsDebugMode** i tabellen **DualWriteProjectConfiguration**. Åbn tabellen **DualWriteProjectConfiguration** ved hjælp af tilføjelsesprogrammet til Excel.

    > [!TIP]
    > Du kan nemt åbne tabellen ved at slå **Design**-tilstand til i Excel-tilføjelsesprogrammet og derefter tilføje **DualWriteProjectConfigurationEntity** i regnearket. Du kan finde flere oplysninger under [Åbne tabeldata i Excel og opdatere dem ved hjælp af tilføjelsesprogrammet til Excel](../../office-integration/use-excel-add-in.md).

2. Indstil egenskaben **IsDebugMode** til **Ja** for projektet.
3. Kør det scenario, der genererer fejl.
4. De detaljerede logfiler er tilgængelige i tabellen DualWriteErrorLog. Hvis du vil slå data op i tabelbrowseren, skal du bruge følgende URL-adresse (Erstat **XXX** efter behov):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontrollere synkroniseringsfejl på den virtuelle maskine for Finance and Operations-appen

**Påkrævet rolle for at få vist fejl:** Systemadministrator

1. Log på Microsoft Dynamics LifeCycle Services (LCS).
2. Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstesten for.
3. Vælg titlen **Skybaserede miljøer**.
4. Brug Fjernskrivebord til at logge på den virtuelle maskine (VM) for Finance and Operations-appen. Brug den lokale konto, der vises i LCS.
5. Åbn Logbog.
6. Vælg **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**.
7. Gennemse listen over seneste fejl.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Fjerne sammenkædning og sammenkæde med et andet Dataverse-miljø fra en Finance and Operations-app

**Påkrævet rolle for at fjerne miljøtilknytningen:** Systemadministrator for enten Finance and Operations-app eller Dataverse.

1. Log på Finance and Operations-appen.
2. Gå til **Arbejdsområder \> Datastyring**, og vælg feltet **Dobbeltskrivning**.
3. Vælg alle kørende tilknytninger, og vælg derefter **Stop**.
4. Vælg **Ophæv sammenkædning af miljø**.
5. Vælg **Ja** for at bekræfte operationen.

Nu kan du sammenkæde et nyt miljø.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Kan ikke se linjeoplysningsformularen for salgsordren 

Når du opretter en salgsordre i Dynamics 365 Sales, kan klik på **+ Tilføj produkter** omdirigere dig til ordrelinjeformen i Dynamics 365 Project Operations. Du kan ikke få vist formularen for salgsordrelinjens **Oplysninger** på denne måde. Indstillingen for **Oplysninger** vises ikke på rullelisten under **Ny ordrelinje**. Dette sker, fordi Project Operations er installeret i dit miljø.

Hvis du vil aktivere formularindstillingen **Oplysninger** igen, skal du følge disse trin:
1. Naviger til tabellen **Ordrelinje**.
2. Find formularen **Oplysninger** under formularernoden. 
3. Vælg formularen **Oplysninger**, og klik på **Aktivér sikkerhedsroller**. 
4. Ret sikkerhedsindstillingen til **Vis for alle**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]