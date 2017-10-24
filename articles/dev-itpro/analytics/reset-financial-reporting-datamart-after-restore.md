---
title: "Nulstil økonomirapporterings-datacenteret efter gendannelse af en database"
description: "Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Finance and Operations-database."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Nulstil økonomirapporterings-datacenteret efter gendannelse af en database

[!include[banner](../includes/banner.md)]


Dette emne beskriver, hvordan du nulstiller økonomirapporterings-datacenteret efter gendannelse af en Microsoft Dynamics 365 for Finance and Operations-database.

Hvis du på et tidspunkt vil gendanne din Finance and Operations-database fra en sikkerhedskopi eller kopiere databasen fra et andet miljø, skal du følge trinnene i dette emne for at sikre, at datacenteret for økonomirapportering bruger den gendannede Finance and Operations-database korrekt. 
> [!Note] 
> Trinene i processen understøttes for Dynamics 365 for Operations maj 2016 udgaven (App build 7.0.1265.23014 og økonomirapportering build 7.0.10000.4) og nyere versioner. Hvis du har en tidligere udgave af Dynamics 365 for Finance and Operations, skal du kontakte vores supportteam for at få hjælp.

## <a name="export-report-definitions"></a>Eksporter rapportdefinitioner
Først skal du eksportere de rapportdesigns, der er placeret i Report Designer, ved hjælp af følgende trin:

1.  I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.
2.  Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**. 

    > [!Note] 
    > Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.
    
3.  Vælg de rapportdefinitioner, der skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinitioner og de tilhørende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du klikke på den relevante fane og derefter vælge de elementer, der skal eksporteres. Tryk på og hold Ctrl-tasten nede for at vælge flere elementer på en fane. Når du vælger rapporter til eksport, vælges de tilknyttede rækker, kolonner, træer og dimensionsopsætninger.

4.  Klik på **Eksporter**.
5.  Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.
6.  Klik på **Gem**.

Filen kan kopieres eller overføres til et sikkert sted, så den kan importeres til et andet miljø på et senere tidspunkt. Du kan finde oplysninger om brug af en Microsoft Azure-lagerkonto i [Overfør data med AzCopy-kommandolinjeværktøjet](/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft leverer ikke en lagerkonto som en del af din Finance and Operations-aftale. Du skal købe en lagerkonto eller bruge en lagerkonto fra et separat Azure-abonnement. 
> [!WARNING]
> Vær opmærksom på funktionen af D-drevet på virtuelle Azure-maskiner. Opbevar ikke dine eksporterede komponentgrupper her permanent. Du kan finde flere oplysninger om midlertidige drev i [Om de midlertidige drev på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stop tjenester
Brug Fjernskrivebord til at oprette forbindelse til alle computere i miljøet, og stop følgende tjenester i Windows ved hjælp af services.msc:

-   Tjenesten World Wide Web Publishing (på alle AOS-computere)
-   Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)
-   Tjenesten Management Reporter 2012 Process (kun på BI-computere)

Disse tjenester har åbne forbindelser til Dynamics 365 for Finance and Operations-databasen.

## <a name="reset"></a>Nulstil
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Find og hent den nyeste MinorVersionDataUpgrade.zip-pakke

Find den nyeste MinorVersionDataUpgrade.zip-pakke ved hjælp af vejledningen i [Hent den nyeste installerbare dataopgraderingspakke](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Vejledningen beskriver, hvordan du finder og henter den korrekte version af dataopgraderingspakken. Der kræves ikke en opgradering for at hent pakken MinorVersionDataUpgrade.zip. Du behøver kun at udføre trinnene i afsnittet "Hent den nyeste installerbare dataopgraderingspakke" uden at udføre nogen af de øvrige trin i artiklen for at hente en kopi af MinorVersionDataUpgrade.zip-pakken.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Udfør scripts mod Finance and Operations-databasen

Kør følgende scripts mod Finance and Operations-databasen (ikke mod økonomirapporteringsdatabasen).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse scripts sikrer, at brugerne, rollerne og indstillingerne for sporing af ændringer er korrekte.

### <a name="execute-powershell-command-to-reset-database"></a>Udfør PowerShell-kommando for at nulstille databasen

På AOS-computeren skal du udføre følgende kommandoer i PowerShell som administrator for at nulstille integrationen mellem Finance and Operations og økonomirapporteringen:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Når du har udført kommandoerne, bliver du bedt om at indtaste "Y" for at bekræfte.

Forklaring af parametrene:

-   De gyldige værdier for -Reason er: SERVICING, BADDATA, OTHER.
-   Parameteren -ReasonDetail er fri tekst.
-   Årsag og reasonDetail registreres i telemetri/miljø overvågningen.

## <a name="start-services"></a>Start tjenester
Brug services.msc til at genstarte de tjenester, som du tidligere har stoppet:

-   Tjenesten World Wide Web Publishing (på alle AOS-computere)
-   Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)
-   Tjenesten Management Reporter 2012 Process (kun på BI-computere)

## <a name="import-report-definitions"></a>Importer rapportdefinitioner
Importer dine rapportdesigns fra Report Designer ved hjælp af den fil, der oprettes under eksporten:

1.  I Report Designer skal du gå til **Regnskab** &gt; **Komponentgruppe**.
2.  Vælg den komponentgruppe, der skal eksporterer, og klik på **Eksporter**. 

    > [!NOTE]
    > Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.
    
3.  Vælg komponenten **Standard**, og klik på **Importer**.
4.  Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og klik på **Åbn**.
5.  I dialogboksen Importér skal du vælge de rapportdefinitioner, der skal importeres:
    -   Hvis du vil importere alle rapportdefinitioner og de understøttende komponenter, skal du klikke på **Marker alt**.
    -   Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsopsætninger, der skal importeres.

6.  Klik på **Importer**.





