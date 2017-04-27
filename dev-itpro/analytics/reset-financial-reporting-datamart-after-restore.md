---
title: "Nulstil økonomirapporterings-datacenteret efter gendannelse af en database"
description: "Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Operations-database."
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

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Nulstil økonomirapporterings-datacenteret efter gendannelse af en database

Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Operations-database. 

Der findes flere situationer, hvor du muligvis er nødt til at gendanne Dynamics 365 for Operations-databasen fra en sikkerhedskopi eller kopierer databasen fra et andet miljø. Når dette sker, skal du også følge de relevante trin for at sikre, at økonomirapporterings-datacenteret bruger den gendannede Dynamics 365 for Operations-database korrekt. Hvis du har spørgsmål til nulstilling af økonomirapporterings-datacenteret af andre årsager end gendannelse af en Dynamics 365 for Operations-database, kan du finde yderligere oplysninger i [Nulstilling af Management Reporter-datacenteret](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/). Bemærk, at trinene i processen understøttes for Dynamics 365 for Operations maj 2016 udgaven (App build 7.0.1265.23014 og økonomirapportering build 7.0.10000.4) og nyere versioner. Hvis du har en tidligere udgave af Dynamics 365 for Operations, skal du kontakte vores supportteam for at få hjælp.

## <a name="export-report-definitions"></a>Eksporter rapportdefinitioner
Først skal du eksportere de rapportdesigns, der er placeret i Report Designer, ved hjælp af følgende trin:

1.  I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.
2.  Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**. **Bemærk:** I Dynamics 365 for Operations understøttes kun én komponentgruppe, **Standard**.
3.  Vælg de rapportdefinitioner, der skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres. Tryk på og hold Ctrl-tasten nede for at vælge flere elementer på en fane. Når du vælger rapporter, der skal eksporteres, markeres de tilknyttede rækker, kolonner, træer og dimensionssæt.

4.  Klik på **Eksporter**.
5.  Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.
6.  Klik på **Gem**.

Filen kan kopieres eller overføres til et sikkert sted, så den kan importeres til et andet miljø på et senere tidspunkt. Du kan finde oplysninger om brug af en Microsoft Azure-lagerkonto i [Overfør data med AzCopy-kommandolinjeværktøjet](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Bemærk!** Microsoft leverer ikke en lagerkonto som en del af din Dynamics 365 for Operations-aftale. Du skal købe en lagerkonto eller bruge en lagerkonto fra et separat Azure-abonnement. **Vigtigt:** Være opmærksom på funktionen af D-drevet på virtuelle Azure-maskiner. Opbevar ikke dine eksporterede komponentgrupper her permanent. Du kan finde flere oplysninger om midlertidige drev i [Om de midlertidige drev på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stop tjenester
Brug Fjernskrivebord til at oprette forbindelse til alle computere i miljøet, og stop følgende tjenester i Windows ved hjælp af services.msc:

-   Tjenesten World Wide Web Publishing (på alle AOS-computere)
-   Tjenesten Microsoft Dynamics 365 for Operations Batch Management (kun på ikke-private AOS-computere)
-   Tjenesten Management Reporter 2012 Process (kun på BI-computere)

Disse tjenester har åbne forbindelser til Dynamics 365 for Operations-databasen.

## <a name="reset"></a>Nulstil
#### <a name="locate-the-latest-dataupgradezip-package"></a>Find den nyeste DataUpgrade.zip-pakke

Find den nyeste DataUpgrade.zip-pakke ved hjælp af vejledningen i [Hent scriptet DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). Vejledningen beskriver, hvordan du finder den korrekte version af dataopgraderingspakken til dit miljø.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Udfør scripts mod Dynamics 365 for Operations-databasen

Kør følgende scripts mod Dynamics 365 for Operations-databasen (ikke mod økonomirapporteringsdatabasen).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse scripts sikrer, at brugerne, rollerne og indstillingerne for sporing af ændringer er korrekte.

#### <a name="execute-powershell-command-to-reset-database"></a>Udfør PowerShell-kommando for at nulstille databasen

Følgende kommando skal udføres direkte på AOS-computeren for at nulstille integrationen mellem Dynamics 365 for Operations og økonomirapporteringen:

1.  Åbn Windows PowerShell som administrator.
2.  Udfør: F:
3.  Udfør: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Udfør: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Udfør: Reset-DatamartIntegration -Reason OTHER -ReasonDetail "&lt;min årsag til nulstilling&gt;"
    -   Du bliver bedt om at indtaste "Y" for at bekræfte.

Forklaring af parametrene:

-   De gyldige værdier for -Reason er: SERVICING, BADDATA, OTHER.
-   Parameteren -ReasonDetail er fri tekst.
-   Årsag og reasonDetail registreres i telemetri/miljø overvågningen.

## <a name="start-services"></a>Start tjenester
Brug services.msc til at genstarte de tjenester, som du tidligere har stoppet:

-   Tjenesten World Wide Web Publishing (på alle AOS-computere)
-   Tjenesten Microsoft Dynamics 365 for Operations Batch Management (kun på ikke-private AOS-computere)
-   Tjenesten Management Reporter 2012 Process (kun på BI-computere)

## <a name="import-report-definitions"></a>Importer rapportdefinitioner
Importer dine rapportdesigns fra Report Designer ved hjælp af den fil, der oprettes under eksporten:

1.  I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.
2.  Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**. **Bemærk:** I Dynamics 365 for Operations understøttes kun én komponentgruppe, **Standard**.
3.  Vælg komponenten **Standard**, og klik på **Importer**.
4.  Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og klik på **Åbn**.
5.  I dialogboksen Importér skal du vælge de rapportdefinitioner, der skal importeres:
    -   Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.

6.  Klik på **Importer**.



