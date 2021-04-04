---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)'
description: Dette emne beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7cc1a60234ef09b80950cbf0c7f18b0d65709d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565208"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER Bruge økonomiske dimensioner som en datakilde (del 4: Kør rapporten)

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 3: Design rapporten)". Du skal også konfigurere standarddokumenttyper på siden Parametre til elektronisk rapportering. Standarddokumenttyper angives også, når du henter og importerer en ER-konfiguration. 


## <a name="run-report"></a>Kør rapporter
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.
3. Vælg 'Eksempelmodel til økonomiske dimensioner\Finanskladderapport' i træet.
4. Klik på Kør.
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run1.png)
5. Indtast eller vælg en værdi i feltet Dimensionens navn.
    * Hvis du vil vælge alle dimensioner i det aktuelle firma, skal du angive følgende oplysninger: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run2.png)
6. Udvid posterne for at inkludere sektion.
7. Klik på Filtrér.
8. Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.
9. Skriv "00057" i feltet Kriterier.
10. Klik på OK.
11. Klik på OK.
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run3.png)
    * Gennemse det genererede output. For hver transaktion for det markerede batch vises de økonomiske dimensioner fra det tilsvarende sæt dimensioner. Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.  
![Siden ER-konfigurationer](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]