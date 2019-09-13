---
title: Konfigurere attributbaseret prissætning for konfigurerbare produkter
description: I dette emne beskrives, hvordan du opretter attributbaserede priser.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914693"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Konfigurere attributbaseret prissætning for konfigurerbare produkter

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives, hvordan du opretter attributbaserede priser. Som en forudsætning skal du have en produktkonfigurationsmodel, der har en eller flere komponenter og attributter. I dette eksempel bruges Højttaler af topkvalitet-modellen i demodatafirmaet USMF. Normalt bruger en produktchef denne procedure.


## <a name="create-a-new-price-model"></a>Opret en ny prismodel
1. Vælg **Definition af produktvariantmodel** på startsiden.
2. Vælg **Produktkonfigurationsmodeller** i sektionen **Links**.
3. På listen skal du vælge linjen **Højttaler af topkvalitet**, men vælg ikke linket for navnet.
4. Vælg **Model** i handlingsruden.
5. Vælg **Prismodeller**.
6. Vælg **Ny**.
7. Angiv en værdi i feltet **Navn på prismodel**. Brug et navn, der gør det nemt at identificere modellen.  
8. Indtast en værdi i feltet **Beskrivelse**.
9. Vælg **Gem**.

## <a name="add-price-elements"></a>Tilføj priselementer
1. Vælg **Rediger**. Hver komponent i en produktmodel kan have et basispriselement og et vilkårligt antal prisudtryksregler. Du kan også tilføje priser i forskellige valutaer.  
2. Indtast en værdi i feltet **Basisprisudtryk**. Skriv for eksempel 100. En basisprisudtryk kan være en numerisk værdi, eller det kan bestå af en matematisk beregning, der omfatter en eller flere attributter.  
3. Vælg **Tilføj**.
4. Skriv `Rosewood` i feltet **Navn**. Navnet på prisudtrykket hjælper med at identificere, hvad priselementet repræsenterer. I dette eksempel opretter vi priselementet for indstillingen Kabinetfinish til Rosewood-højttaler.  
5. Vælg **Rediger betingelse**. En prisbetingelse hjælper med at sikre, at prisudtrykselementet kun er inkluderet i salgsprisen, hvis der findes en bestemt kombination af attributter.  
6. Angiv `CabinetFinish=="Rosewood"` i feltet **ConstraintBody**.
7. Vælg **OK**.
8. Skriv en værdi i feltet **Udtryk**. Skriv f.eks. `50`. 
9. Luk siden.

