---
title: Oprette kriterier for valg af salgspris
description: Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8c60b188b7c7090546e8367455e0f58ce9359b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147681"
---
# <a name="create-sales-price-selection-criteria"></a>Oprette kriterier for valg af salgspris

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller. Denne procedure kræver, at der er mindst én tilgængelig salgspris. I dette eksempel bruges prismodellen for salgsprismodellen for højttalerløsningen i demodatafirmaet USMF. Normalt bruger en produktchef denne procedure.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Tilføj et nyt kriterium for en eksisterende salgsprismodel
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktkonfigurationsmodeller.
3. På listen skal du vælge rækken for produktmodellen for højttalerløsningen, men ikke klikke på linket for modelnavnet.
4. Klik på Model i handlingsruden.
5. Klik på Prismodelkriterier.
6. Klik på Ny.
7. Skriv 'Kundegruppe 10' i feltet Navn.
    * Navnet på prismodelkriteriet bruges til at identificere de underliggende udvælgelseskriterier.  
8. Indtast eller vælg en værdi i feltet Prismodel.
9. I feltet Ordretype skal du vælge "Salgsordre".
    * Ordretypen bestemmer de databasefelter, der er tilgængelige for valgforespørgslen.  
10. Indtast en dato i feltet Gyldig fra.
11. Angiv en dato i feltet Udløber senest.
12. Klik på Gem.

## <a name="create-the-query-for-the-selection-criteria"></a>Opret forespørgslen for udvælgelseskriterierne
1. Klik på Rediger.
2. Vælg Kunder i feltet Tabel. 
3. Vælg Kundegruppe i feltet Felt.
    * I dette eksempel bruger vi en specifik kundegruppe til udvælgelseskriterierne.  
4. Vælg Kundegruppe 10 i feltet Kriterier. 
5. Klik på OK.

