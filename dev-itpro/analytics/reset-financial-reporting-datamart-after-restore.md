---
title: Nulstil finansiel rapportering datamarkedet efter gendannelse af en database
description: Dette emne beskriver, hvordan du nulstille finansiel rapportering datamarkedet efter gendannelse af en Microsoft Dynamics-365 for operationer database.
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Nulstil finansiel rapportering datamarkedet efter gendannelse af en database

Dette emne beskriver, hvordan du nulstille finansiel rapportering datamarkedet efter gendannelse af en Microsoft Dynamics-365 for operationer database. 

Der findes flere situationer, hvor du muligvis gendanne dine Dynamics 365 for operationer-databasen fra en sikkerhedskopi eller kopierer databasen fra et andet miljø. Når dette sker, skal du også følge de relevante trin for at sikre, at finansielle rapportering datamarkedet korrekt med den gendannede Dynamics 365 for operationer database. Hvis du har spørgsmål om at nulstille finansiel rapportering datamarkedet af årsager uden for gendannelse af en Dynamics 365 for operationer-database, kan du referere til den [nulstille datamarkedet Management Reporter](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for yderligere oplysninger. Bemærk, at trin i processen understøttes for Dynamics 365 for Operation maj 2016 frigivelse (App build 7.0.1265.23014 og finansiel rapportering build 7.0.10000.4) og nyere versioner. Hvis du har en tidligere udgave af Dynamics 365 for operationer, skal du kontakte vores supportteam for at få hjælp.

## <a name="export-report-definitions"></a>Eksportere rapportdefinitioner
Først eksportere rapporten design i rapportdesigner, ved hjælp af følgende trin:

1.  I rapportdesigner, gå til **virksomhed**&gt;**dokumentkomponent grupper**.
2.  Vælg dokumentkomponent gruppen til at eksportere, og klik på **eksportere**. **Bemærk:** For Dynamics 365 for operationer, understøttes kun én dokumentkomponent af typen gruppe, **standard**.
3.  Vælg rapportdefinitionerne, der skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres. Tryk på og hold Ctrl-tasten nede for at vælge flere elementer på en fane. Når du vælger rapporter til at eksportere, vælges den tilknyttede rækker, kolonner, træer og dimensionsopsætninger.

4.  Klik på **eksportere**.
5.  Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.
6.  Click **Save**.

Filen kan kopieres eller overføres til et sikkert sted, så den kan importeres til et andet miljø på et senere tidspunkt. Du kan finde oplysninger om brug af en konto til Microsoft Azure storage i [overføre data med AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Bemærk:** Microsoft ikke levere en storage-konto som en del af din Dynamics 365 til operationer aftale. Du skal købe en storage-konto eller bruge en storage-konto fra en separat Azure abonnement. **Vigtigt:** være opmærksom på funktionen af D-drev på Azure virtuelle maskiner. Opbevar ikke dine eksporterede dokumentkomponent grupper her permanent. Finde flere oplysninger om midlertidige drev [om midlertidig drevet på Windows Azure virtuelle maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stoppe tjenester
Du kan bruge Fjernskrivebord til at oprette forbindelse til alle computere i miljøet og stopper følgende tjenester i Windows ved hjælp af services.msc:

-   World wide Web-udgivelse service (på alle AOS-computere)
-   Microsoft Dynamics 365 for operationer Batch Management-tjenesten (på ikke-private AOS-computere kun)
-   Management Reporter 2012 proces-tjenesten (på kun BI-computere)

Disse tjenester har åbne forbindelser, til Dynamics-365 for operationer database.

## <a name="reset"></a>Nulstil
#### <a name="locate-the-latest-dataupgradezip-package"></a>Find de nyeste DataUpgrade.zip-pakke

Find den nyeste DataUpgrade.zip-pakke ved hjælp af vejledningen findes i [hente scriptet DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). Vejledningen beskriver, hvordan at finde den korrekte version af data opgraderingspakke til dit miljø.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Udføre scripts mod Dynamics 365 for operationer database

Kør følgende scripts mod Dynamics-365 for operationer databasen (ikke mod finansielle rapporteringsdatabasen).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse scripts sikrer, at de brugere, roller og ændre indstillinger for opfølgning er korrekte.

#### <a name="execute-powershell-command-to-reset-database"></a>Udfør PowerShell-kommando for at nulstille databasen

Følgende kommando skal udføres direkte på AOS-computeren til at nulstille integration mellem Dynamics 365 for operationer og regnskabsaflæggelse:

1.  Åbn Windows PowerShell som Administrator.
2.  Udfør: F:
3.  Udfør: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Udfør: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Udfør: Nulstilling af DatamartIntegration-anden årsag - ReasonDetail "&lt;min årsag til nulstilling af&gt;"
    -   Du bliver bedt om at indtaste "Y" for at bekræfte.

Forklaring af parametrene:

-   De gyldige værdier for - årsagen er: vedligeholdelse, BADDATA, andre.
-   Parameteren - ReasonDetail er fri tekst.
-   Årsag og reasonDetail registreres i overvågning af fjernmåling/miljø.

## <a name="start-services"></a>Start af tjenester
Du kan bruge services.msc genstarte de tjenester, som du tidligere har stoppet:

-   World wide Web-udgivelse service (på alle AOS-computere)
-   Microsoft Dynamics 365 for operationer Batch Management-tjenesten (på ikke-private AOS-computere kun)
-   Management Reporter 2012 proces-tjenesten (på kun BI-computere)

## <a name="import-report-definitions"></a>Importere rapportdefinitioner
Importere dine designs med rapporten fra rapportdesigner, ved hjælp af den fil, der oprettes under eksporten:

1.  I rapportdesigner, gå til **virksomhed**&gt;**dokumentkomponent grupper**.
2.  Vælg dokumentkomponent gruppen til at eksportere, og klik på **eksportere**. **Bemærk:** For Dynamics 365 for operationer, understøttes kun én dokumentkomponent af typen gruppe, **standard**.
3.  Vælg den **standard** opbygning blok, og klik på **Import**.
4.  Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og klik på **åbne**.
5.  I dialogboksen Importér skal du vælge de rapportdefinitioner, der skal importeres:
    -   Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.

6.  Click **Import**.



