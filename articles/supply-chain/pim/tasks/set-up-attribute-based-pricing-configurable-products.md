---
title: Konfigurere attributbaseret prissætning for konfigurerbare produkter
description: I dette emne beskrives, hvordan du opretter attributbaserede priser.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4acd7b423396124dd1059602f5aa6460ec5e259
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578146"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Konfigurere attributbaseret prissætning for konfigurerbare produkter

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan du opretter attributbaserede priser. Som en forudsætning skal du have en produktkonfigurationsmodel, der har en eller flere komponenter og attributter. I dette eksempel bruges Højttaler af topkvalitet-modellen i demodatafirmaet USMF. Normalt bruger en produktchef denne procedure.


## <a name="create-a-new-price-model"></a>Opret en ny prismodel

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.
1. På listen skal du vælge linjen **Højttaler af topkvalitet**, men vælg ikke linket for navnet.
1. Vælg **Model** i handlingsruden.
1. Vælg **Prismodeller**.
1. Vælg **Ny**.
1. Angiv en værdi i feltet **Navn på prismodel**. Brug et navn, der gør det nemt at identificere modellen.  
1. Indtast en værdi i feltet **Beskrivelse**.
1. Vælg **Gem**.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]