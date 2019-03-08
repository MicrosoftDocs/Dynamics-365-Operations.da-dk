---
title: Konfigurere attributbaseret prissætning for konfigurerbare produkter
description: Denne procedure viser, hvordan du opretter attributbaserede priser.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8568b5f4933ae58bc2d55a169c798668e03bed2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "333777"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Konfigurere attributbaseret prissætning for konfigurerbare produkter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter attributbaserede priser. Som en forudsætning skal du have en produktkonfigurationsmodel, der har en eller flere komponenter og attributter. I dette eksempel bruges Højttaler af topkvalitet-modellen i demodatafirmaet USMF. Normalt bruger en produktchef denne procedure.


## <a name="create-a-new-price-model"></a>Opret en ny prismodel
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktkonfigurationsmodeller.
3. På listen skal du vælge linjen Højttaler af topkvalitet, men ikke klikke på linket for navnet.
4. Klik på Model i handlingsruden.
5. Klik på Prismodeller.
6. Klik på Ny.
7. Angiv en værdi i feltet Prismodel.
    * Brug et navn, der gør det nemt at identificere modellen.  
8. Skriv en værdi i feltet Beskrivelse.
9. Klik på Gem.

## <a name="add-price-elements"></a>Tilføj priselementer
1. Klik på Rediger.
    * Hver komponent i en produktmodel kan have et basispriselement og et vilkårligt antal prisudtryksregler. Du kan også tilføje priser i forskellige valutaer.  
2. Indtast en værdi i feltet Basisprisudtryk.
    * Skriv for eksempel 100.   En basisprisudtryk kan være en numerisk værdi, eller det kan bestå af en matematisk beregning, der omfatter en eller flere attributter.  
3. Klik på Tilføj.
4. Skriv 'Rosewood' i feltet Navn.
    * Navnet på prisudtrykket hjælper med at identificere, hvad priselementet repræsenterer. I dette eksempel opretter vi priselementet for indstillingen Kabinetfinish til Rosewood-højttaler.  
5. Klik på Rediger betingelse.
    * En prisbetingelse hjælper med at sikre, at prisudtrykselementet kun er inkluderet i salgsprisen, hvis der findes en bestemt kombination af attributter.  
6. I feltet ConstraintBody skal du angive 'CabinetFinish=="Rosewood"'.
7. Klik på OK.
8. Skriv en værdi i feltet Udtryk.
    * Skriv for eksempel 50.  
9. Luk siden.
10. Luk siden.

