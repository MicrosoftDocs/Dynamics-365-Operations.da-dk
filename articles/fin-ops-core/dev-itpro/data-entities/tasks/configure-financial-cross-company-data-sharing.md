---
title: Konfigurere økonomisk datadeling på tværs af firmaer
description: Denne procedure viser, hvordan du kan konfigurere, aktivere, validere og løse konflikter ved deling af data mellem virksomheder.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2caaa971790c31ed4c88bd0b2365179fb22b644e3d4512f4f06bb33bd29f8d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736272"
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]