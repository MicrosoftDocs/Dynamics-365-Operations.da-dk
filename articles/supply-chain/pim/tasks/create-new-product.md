---
title: Oprette et nyt produkt
description: Dette emne beskriver, hvordan et nyt delt produkt oprettes.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844795"
---
# <a name="create-a-new-product"></a>Oprette et nyt produkt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne beskriver, hvordan et nyt delt produkt oprettes. Den udføres normalt af en produktdesigner. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.


## <a name="create-a-product"></a>Oprette et produkt
1. I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Produkter**.
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Produktnummer**. Hvis der ikke er konfigureret en nummerserie for produktnummeret, skal det angives manuelt.  
4. Skriv en værdi i feltet **Produktnavn**. Produktnavnet angives som standard til søgenavnet. Du kan ændre dette efter behov.  
5. Vælg **OK**.

## <a name="set-up-dimension-groups"></a>Konfigurere dimensionsgrupper
1. Vælg **Dimensionsgrupper** for at åbne dialogboksen.
2. Indtast eller vælg en værdi i feltet **Lagringsdimensionsgruppe**. Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner du skal angive for hver transaktion for produktet, og hvordan den spores på lageret.  
3. Indtast eller vælg en værdi i feltet **Sporingsdimensionsgruppe**. Lagringsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du skal angive for hver transaktion for produktet, og hvordan den håndteres på lageret.  
4. Vælg **OK**.

