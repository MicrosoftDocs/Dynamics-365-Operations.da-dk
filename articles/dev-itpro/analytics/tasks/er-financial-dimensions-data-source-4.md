--- 
title: "Køre rapporter, der bruger økonomiske dimensioner som datakilder"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6569f9b97d5d15bf74b8b3882bf4bab50970dd0f
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="run-reports-that-use-financial-dimensions-as-data-sources"></a>Køre rapporter, der bruger økonomiske dimensioner som datakilder

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    * Gennemse det genererede output. Bemærk, at for hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner. Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne Dynamics 365 for Finance and Operations-forekomst.  


