---
title: "Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed"
description: "Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 672697254c1bf06e193a51c5c7c83c467a220ce8
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed

[!include[banner](../includes/banner.md)]


Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940. 

Brug følgende trin til at tilføje importenhed for bankkontoudtog, der understøtter formatet MT940.

1.  Kompilerer og synkroniserer følgende:
    -   Sammensat Entity\\BankStatementImportEntity
    -   Entity\\BankStatementBalanceEntity
    -   Entity\\BankStatementDocumentEntity
    -   Entity\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Tables\\BankStatementStaging

2.  Datastyring\\dataprojekter.
    1.  Indlæse MT940-importprojekter
        1.  Ændre XSLT.
            -   Klik på **Vis tilknytning**.
            -   Klik på **Vis tilknytning** på bankkontoudtogets dokumentet.
            -   Klik på **Transformationer**
            -   Slet filen BankReconiliation-to-Composite.xslt.
            -   Tilføj den nye version af BankReconiliation-to-Composite.xsl.

        2.  Vis **løbenummeret** på **kildedata**-layout.
            1.  Kildedataformat = XML-element.
            2.  Enhedsnavn = Bankkontoudtog.
            3.  Upload datafilen = ny version af SampleBankCompositeEntity.xml.
            4.  Klik på **Ja** for at overskrive den eksisterende fil.
            5.  Klik på **Ja** for at oprette en ny tilknytning.
            6.  Kontrollér, at S**equenceNumber** er tilknyttet.
                -   Klik på **Vis tilknytning** på bankkontoudtogets enhed.
                -   Kontrollér, at **SequenceNumber** er knyttet fra Kilde til Midlertidig.

3.  Importér det nye udtog.




