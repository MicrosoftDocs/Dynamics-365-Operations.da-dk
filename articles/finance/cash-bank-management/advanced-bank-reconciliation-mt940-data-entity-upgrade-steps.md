---
title: Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed
description: Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c891a5139ff7de85e6762513f57236e24f1644529d7825c9ce5e1dfda50fbad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739377"
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
            6.  Kontrollér, at S **equenceNumber** er tilknyttet.
                -   Klik på **Vis tilknytning** på bankkontoudtogets enhed.
                -   Kontrollér, at **SequenceNumber** er knyttet fra Kilde til Midlertidig.

3.  Importér det nye udtog.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]