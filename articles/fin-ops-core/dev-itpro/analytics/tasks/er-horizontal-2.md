---
title: 'ER Bruge vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk (del 2: Kørselsformat)'
description: Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66c2a97a068ed83f93699f14e827bdc2fb580d93
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141827"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER Bruge vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk (del 2: Kørselsformat)

[!include [banner](../../includes/banner.md)]

Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "Brug ER vandret udvidelige områder til dynamisk at tilføje kolonnerne i Excel-rapporter (del 1: Designformat)".

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="find-created-format"></a>Find oprettet format
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Eksempelmodel til økonomiske dimensioner' i træet.
3. Vælg 'Eksempelmodel til økonomiske dimensioner\Eksempel på rapport med vandret områder, der kan udvides' i træet.

## <a name="execute-format-to-create-excel-output"></a>Udfør format for at oprette Excel-output
1. Klik på Kør.
2. Skriv 'BusinessUnit;CostCenter;Department' i feltet Dimensionens navn.
    * Indtast eller vælg en værdi i feltet Dimensionens navn.  Hvis du vil vælge alle dimensioner for det aktuelle regnskab, skal du angive følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Udvid posterne for at inkludere sektion.
4. Klik på Filtrér.
5. Vælg rækken for tabellen Finanskladde og feltet Kladdebatchnummer.
6. Skriv '00057..00058' i feltet Kriterier.
    * 00057..00058  
7. Klik på OK.
8. Klik på OK.
    * Gennemse det genererede output. Bemærk, at den netop oprettede Excel-fil indeholder det samme antal kolonner, der er valgt for økonomiske dimensioner. Rapporthovedet i disse kolonner repræsenterer navnene på økonomiske dimensioner. Transaktionslinjerne i disse kolonner repræsenterer økonomiske dimensioner. Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne forekomst.  

