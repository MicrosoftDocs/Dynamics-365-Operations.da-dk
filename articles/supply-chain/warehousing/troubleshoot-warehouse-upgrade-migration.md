---
title: Foretage fejlfinding af opgradering og migrering til avanceret lokationsstyring
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du opgraderer og overfører til avanceret lokationsstyring.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907881"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Foretage fejlfinding af opgradering og migrering til avanceret lokationsstyring

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du opgraderer og overfører til avanceret lokationsstyring.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Jeg får vist følgende fejlmeddelelse: "java.security.cert.certPathValidatorException: Tillidsanker for certificeringsstien blev ikke fundet".

### <a name="issue-description"></a>Problembeskrivelse

Du modtager denne fejlmeddelelse i mobilappen Lokationsstyring, fordi der ikke er tillid til selvsignerede certifikater på Android 8 + i lokale miljøer.

### <a name="issue-resolution"></a>Problemløsning

Brug et eksternt (offentligt) nøglecenter. Der findes en rettelse til dette problem i version 1.9.0.0 af lagerstedsappen. Du kan finde flere oplysninger om dette problem, og hvordan det løses, under [Foretage fejlfinding af problemer med forbindelsen til mobilappen Lokationsstyring](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Hvad er den godkendte proces for flytning fra grundlæggende lagerstyring til avanceret lagerstyring?

### <a name="issue-description"></a>Problembeskrivelse

Du kører i øjeblikket under lagerbeholdning/lagerstyring og bruger grundlæggende lagerbeholdningsfunktioner, og du vil flytte til avanceret lagerstyring for at udnytte mobilenheder, -bølger og -arbejde. Der opstår dog problemer, når du forsøger at flytte. Du kan f.eks. ikke ændre dine produkter, så de bruger lagringsdimensioner (sted, lagersted og lokation), da produkterne har transaktioner for dem. Derfor skal du kende den godkendte proces for flytning fra grundlæggende lagerstyring til avanceret lagerstyring.

### <a name="issue-resolution"></a>Problemløsning

Du kan finde flere oplysninger om processen for flytning fra grundlæggende lagerstyring til avanceret lagerstyring i følgende blogindlæg og dokumentation:

- [Aktivere lokationsstyringsproces for eksisterende varer og lagersteder](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Migrering af Microsoft Dynamics AX WMS til nye R3-lagersteds- og transportfunktioner](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2-varemigrering](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Opgradere lokationsstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]