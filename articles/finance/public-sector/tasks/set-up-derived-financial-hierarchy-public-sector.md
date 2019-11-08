---
title: Konfigurere et afledt finansielt hierarki i den offentlige sektor
description: For at opfylde CGAC-krav (Government-wide Accounting Classification) skal organisationer i den offentlige sektor bruge afledte finansielle hierarkier for at indsamle og analysere bogførte posteringsdata for specifikke hovedkontonumre, fulde kontonumre og økonomiske dimensionsværdier.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, LedgerDerivedFinHierarchyLegalEntities, LedgerDerivedFinHierarchies
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 872f3a69d76d485138c4793b71d22f043539dfb2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174587"
---
# <a name="set-up-a-derived-financial-hierarchy-in-the-public-sector"></a>Konfigurere et afledt finansielt hierarki i den offentlige sektor

[!include [task guide banner](../../includes/task-guide-banner.md)]

For at opfylde CGAC-krav (Government-wide Accounting Classification) skal organisationer i den offentlige sektor bruge afledte finansielle hierarkier for at indsamle og analysere bogførte posteringsdata for specifikke hovedkontonumre, fulde kontonumre og økonomiske dimensionsværdier. Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.


## <a name="create-a-category-hierarchy"></a>Opret et kategorihierarki
1. Gå til administration af produktoplysninger > Opsætning af > Kategorier og attributter > Kategorihierarkier.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Opret.
6. Klik på Ny kategorinode.
7. Skriv en værdi i feltet Navn.
8. Skriv en værdi i feltet Kode.
9. Klik på Ny kategorinode.
10. Skriv en værdi i feltet Navn.
11. Skriv en værdi i feltet Kode.
    * (Valgfrit) Tilføj yderligere underordnede noder, eller angiv yderligere indstillinger for de noder, du har oprettet.  
12. Klik på Gem.

## <a name="assign-the-derived-financial-hierarchy-category-type"></a>Tildele det afledte økonomiske hierarkis kategoritype
1. Gå til administration af produktoplysninger > Opsætning > Kategorier og attributter > Tilknytninger af kategorihierarkiroller.
2. Klik på Ny.
3. Vælg "Afledt økonomisk hierarki" i feltet Kategori for hierarkitype.
4. Klik på rullelisten i feltet Kategorihierarki for at åbne opslaget.
5. Klik på kategorihierarkiet, der skal knyttes til typen af afledt økonomisk hierarki, på listen.
6. Klik på Gem.

## <a name="associate-the-derived-financial-hierarchy-with-a-legal-entity"></a>Tilknytte det afledte økonomiske hierarki med en juridisk enhed
1. Gå til Finans > Diagram over konti > Dimensioner > Tilknyt økonomiske hierarkier.
2. Klik på Ny.
3. Klik på rullelisten i feltet Juridisk enhed for at åbne opslaget.
4. Vælg den juridiske enhed, som skal tilknyttes det afledte økonomiske hierarki, på listen.
5. Klik på rullelisten i feltet Afledt økonomisk hierarki for at åbne opslaget.
6. Vælg det afledte økonomiske hierarki, som skal tilknyttes den juridiske enhed, på listen.
7. Klik på Gem.

## <a name="create-filter-rules-for-the-derived-financial-hierarchy"></a>Oprette filterregler for det afledte økonomiske hierarki
1. Gå til Finans > Diagram over konti > Dimensioner > Afledte økonomiske hierarkier.
2. Klik på rullelisten i feltet Afledt økonomisk hierarki for at åbne opslaget.
3. Klik på det hierarki, du vil oprette filterregler for, på listen.
4. Vælg "Vælg en underordnet node i træet" i træet.
5. Klik på Rediger filter.
    * Klik på Tilføj nye kriterier for at begynde at tilføje regler til filteret. Når du har tilføjet alle kriterierne, skal du klikke på Aktivér filter.  
