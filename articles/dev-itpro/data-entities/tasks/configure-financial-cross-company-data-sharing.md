---
title: Konfigurere økonomisk datadeling på tværs af firmaer
description: Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551024"
---
# <a name="configure-financial-cross-company-data-sharing"></a>Konfigurere økonomisk datadeling på tværs af firmaer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder. Den anvender USMF-virksomheden og skabelonen til deling af økonomiske data.



Denne opgavevejledning kræver Dynamics AX-platform 7.1 eller nyere.

1. Gå til Systemadministration > Arbejdsområder > Datastyring.
2. Klik på Importer.
3. Skriv en værdi i feltet Navn.
4. Vælg typen Pakke i feltet Kildedataformat.
    * Klik på Overfør. Naviger til placeringen af pakkefilen for skabelonen til deling af økonomiske data, og vælg filen.  
5. Klik på Gem.
6. Markér den valgte række på listen.
    * Vælg den politik for datadeling, der netop er blevet oprettet.  
7. Klik på Importer.
8. Klik på Luk.
9. Opdater siden.
10. Luk siden.
11. Luk siden.
12. Luk siden.
13. Gå til Systemadministration > Konfiguration > Konfigurer datadeling på tværs af firma.
14. Find og vælg Betalingsdage på listen.
15. Klik på Tilføj.
16. Markér den valgte række på listen.
17. Skriv 'USSI' i feltet Firma.
18. Klik på Tilføj.
19. Skriv 'USMF' i feltet Firma.
20. Klik på Gem.
21. Klik på Enable.
22. Klik på Ja.
23. Klik på Find delingsproblemer.
24. Klik på Ja.
25. Klik på Opdater feltværdi.
26. Klik på Brug værdi fra firma 1.
27. Opdater siden.
28. Luk siden.

