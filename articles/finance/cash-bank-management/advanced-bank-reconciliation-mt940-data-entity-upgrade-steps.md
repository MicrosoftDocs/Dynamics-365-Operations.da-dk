---
title: Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed
description: Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188458"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed

[!include [banner](../includes/banner.md)]

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



