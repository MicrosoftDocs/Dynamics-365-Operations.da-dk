---
title: Konfigurere økonomisk datadeling på tværs af firmaer
description: Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98eeae9f50238aae172e4a217d40be39ee46a0b8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142955"
---
# <a name="configure-financial-cross-company-data-sharing"></a>Konfigurere økonomisk datadeling på tværs af firmaer

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder. Den anvender USMF-virksomheden og skabelonen til deling af økonomiske data.

Denne opgavevejledning kræver Dynamics AX-platform 7.1 eller nyere.

1. Gå til **Navigationsrude > Moduler > Systemadministration > Arbejdsområder > Datastyring**.
2. Klik på **Importér**.
3. Skriv en værdi i feltet **Navn**.
4. Vælg typen 'Pakke' i feltet **Kildedataformat**. Klik på **Overfør**. Naviger til placeringen af pakkefilen for skabelonen til deling af økonomiske data, og vælg filen.
5. Klik på **Gem**.
6. Markér den valgte række på listen. Vælg den politik for datadeling, der netop er blevet oprettet.  
7. Klik på **Importér**.
8. Klik på **Luk**.
9. Opdater siden.
10. Luk siden.
11. Luk siden.
12. Luk siden.
13. Gå til **Navigationsrude > Moduler > Systemadministration > Opsætning > Konfigurer datadeling på tværs af firma**.
14. Find og vælg **Betalingsdage** på listen.
15. Klik på **Tilføj**.
16. Markér den valgte række på listen.
17. Skriv 'USSI' i feltet **Firma**.
18. Klik på **Tilføj**.
19. Skriv 'USMF' i feltet **Firma**.
20. Klik på **Gem**.
21. Klik på **Aktivér**.
22. Klik på **Ja**.
23. Klik på **Find delingsproblemer**.
24. Klik på **Ja**.
25. Klik på **Opdater feltværdi**.
26. Klik på **Brug værdi fra firma 1**.
27. Opdater siden.
28. Luk siden.

