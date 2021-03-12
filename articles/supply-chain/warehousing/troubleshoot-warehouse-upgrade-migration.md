---
title: Foretage fejlfinding af opgradering og migrering til avanceret lokationsstyring
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du opgraderer og overfører til avanceret lokationsstyring.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993862"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Foretage fejlfinding af opgradering og migrering til avanceret lokationsstyring

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du opgraderer og overfører til avanceret lokationsstyring.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Jeg får vist følgende fejlmeddelelse: "java.security.cert.certPathValidatorException: Tillidsanker for certificeringsstien blev ikke fundet".

### <a name="issue-description"></a>Problembeskrivelse

Du modtager denne fejlmeddelelse i lagerstedsappen, fordi der ikke er tillid til selvsignerede certifikater på Android 8 + i lokale miljøer.

### <a name="issue-resolution"></a>Problemløsning

Brug et eksternt (offentligt) nøglecenter. Der findes en rettelse til dette problem i version 1.9.0.0 af lagerstedsappen. Du kan finde flere oplysninger om dette problem, og hvordan det løses, under [Foretage fejlfinding af problemer med forbindelsen til lagerstedsappen](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Hvad er den godkendte proces for flytning fra grundlæggende lagerstyring til avanceret lagerstyring?

### <a name="issue-description"></a>Problembeskrivelse

Du kører i øjeblikket under lagerbeholdning/lagerstyring og bruger grundlæggende lagerbeholdningsfunktioner, og du vil flytte til avanceret lagerstyring for at udnytte mobilenheder, -bølger og -arbejde. Der opstår dog problemer, når du forsøger at flytte. Du kan f.eks. ikke ændre dine produkter, så de bruger lagringsdimensioner (sted, lagersted og lokation), da produkterne har transaktioner for dem. Derfor skal du kende den godkendte proces for flytning fra grundlæggende lagerstyring til avanceret lagerstyring.

### <a name="issue-resolution"></a>Problemløsning

Du kan finde flere oplysninger om processen for flytning fra grundlæggende lagerstyring til avanceret lagerstyring i følgende blogindlæg og dokumentation:

- [Aktivere lokationsstyringsproces for eksisterende varer og lagersteder](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Migrering af Microsoft Dynamics AX WMS til nye R3-lagersteds- og transportfunktioner](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2-varemigrering](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Opgradere lokationsstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
