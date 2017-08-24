--- 
title: "Køre en rapport, der bruger økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f07e640d4b2a7f67d48df4c081819a55e7e68cda
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Køre en rapport, der bruger økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)". Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering. Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration. 


## <a name="run-report"></a>Kør rapporter
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.
3. Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.
4. Klik på Kør.
5. I feltet Dimensionens navn skal du angive eller vælge en værdi.
    * Hvis du vil vælge alle dimensioner i det aktuelle regnskab, skal du angive følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
6. Udvid posterne for at inkludere sektion.
7. Klik på Filtrér.
8. Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.
9. Skriv "00057" i feltet Kriterier.
10. Klik på OK.
11. Klik på OK.
    * Gennemse det genererede output. Bemærk, at for hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner. Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne Dynamics 365 for Finance and Operations, Enterprise edition-forekomst.  


