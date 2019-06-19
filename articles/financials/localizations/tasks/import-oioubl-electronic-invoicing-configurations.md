---
title: Importere konfigurationer for elektronisk OIOUBL-fakturering
description: Denne procedure viser, hvordan du importerer elektroniske OIOUBL-fakturakonfigurationer.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15e0b2db7c5c014910890ff9b466bf674695c5ad
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561001"
---
# <a name="import-oioubl-electronic-invoicing-configurations"></a>Importere konfigurationer for elektronisk OIOUBL-fakturering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du importerer elektroniske OIOUBL-fakturakonfigurationer. 



Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.



Det er den første af seks opgaver, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer. Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Vælg Microsoft på listen over konfigurationsudbydere.
3. Klik på Angiv som aktiv.
4. Klik på Lagre.
5. Klik på Åbn.
6. Klik på Vis filtre.
7. Anvend følgende filtre: Angiv filterværdien "OIOUBL salgsfaktura" i feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatoren "begynder med"
8. Klik på Importer.
9. Klik på Ja.
10. Anvend følgende filtre: Angiv filterværdien "OIOUBL kreditnota" i feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatoren "begynder med"
11. Klik på Importer.
12. Klik på Ja.
13. Anvend følgende filtre: Angiv filterværdien "OIOUBL projektfaktura" i feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatoren "begynder med"
14. Klik på Importer.
15. Klik på Ja.
16. Anvend følgende filtre: Angiv filterværdien "OIOUBL projektkreditnota" i feltet "Konfigurationsnavn" ved hjælp af filteroperatoren "starter med"
17. Klik på Importer.
18. Klik på Ja.

