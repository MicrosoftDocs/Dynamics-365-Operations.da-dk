--- 
title: "Køre et format, der bruger vandret udvidelige områder til dynamisk at tilføje kolonnerne i Excel-rapporter til elektronisk rapportering (ER)"
description: "Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Køre et format, der bruger vandret udvidelige områder til dynamisk at tilføje kolonnerne i Excel-rapporter til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "Brug ER vandret udvidelige områder til dynamisk at tilføje kolonnerne i Excel-rapporter (del 1: Designformat)".

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


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
    * Gennemse det genererede output. Bemærk, at den netop oprettede Excel-fil indeholder det samme antal kolonner, der er valgt for økonomiske dimensioner. Rapporthovedet i disse kolonner repræsenterer navnene på økonomiske dimensioner. Transaktionslinjerne i disse kolonner repræsenterer økonomiske dimensioner. Kør denne rapport, og vælg forskellige dimensioner for at se, at rapporten ikke er afhængig af antallet af valgte dimensioner eller antallet af dimensioner, der er konfigureret for denne Dynamics 365 for Finance and Operations, Enterprise edition-forekomst.  

