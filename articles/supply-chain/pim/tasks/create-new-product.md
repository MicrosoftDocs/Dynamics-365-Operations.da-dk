---
title: Opret et nyt produkt
description: Denne opgave viser, hvordan du opretter et nyt delt produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548410"
---
# <a name="create-a-new-product"></a>Opret et nyt produkt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgave viser, hvordan du opretter et nyt delt produkt. Den udføres normalt af en produktdesigner. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.

1. Gå til Administration af produktoplysninger > Produkter > Produkter.

## <a name="create-a-product"></a>Oprette et produkt
1. Klik på Ny.
2. Skriv en værdi i feltet Produktnummer.
    * Hvis der ikke er konfigureret en nummerserie for produktnummeret, skal det angives manuelt.  
3. Angiv en værdi i feltet Produktnavn.
    * Produktnavnet angives som standard til søgenavnet. Du kan ændre dette efter behov.  
4. Klik på OK.

## <a name="set-up-dimension-groups"></a>Konfigurere dimensionsgrupper
1. Klik på Dimensionsgrupper for at åbne dialogboksen.
2. Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.
    * Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner du skal angive for hver transaktion for produktet, og hvordan den spores på lageret.  
3. Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.
    * Lagringsdimensionsgruppen bestemmer, hvilke sporingsdimensioner du skal angive for hver transaktion for produktet, og hvordan den håndteres på lageret.  
4. Klik på OK.

