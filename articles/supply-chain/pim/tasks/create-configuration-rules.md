---
title: Oprette konfigurationsregler
description: Denne procedure opretter variantregler, der kan bruges til dimensionsbaseret konfiguration for at gennemtvinge eller forhindre bestemte kombinationer af styklistelinjer.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d75e9ecaa814085e8fce1836125553511cf4f48b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999725"
---
# <a name="create-configuration-rules"></a>Oprette konfigurationsregler

[!include [banner](../../includes/banner.md)]

Denne procedure opretter variantregler, der kan bruges til dimensionsbaseret konfiguration for at gennemtvinge eller forhindre bestemte kombinationer af styklistelinjer. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den syvende procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration.

1. Gå til Administration af produktoplysninger > Styklister og formler > Styklister.
2. Find og vælg den ønskede post på listen.
    * Find og vælg stykliste for dimensionsbaseret konfiguration.  
3. Klik på Indstillinger i handlingsruden.
4. Klik på Skift visning.
5. Klik på Overskriftsvisning.
    * Åbn Overskriftsvisning for at åbne oversigtspanelet Variantrute.  
6. Vis eller skjul sektionen Variansrute.
    * Oversigtspanelet Variantrute skal være i udvidet tilstand.  
7. Klik på Konfigurationsregler.
8. Klik på Ny.
9. Markér den valgte række på listen.
10. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
    * Varerne i den aktuelle variantgruppe vises. Vælg den, der repræsenterer betingelsen i reglen.  
11. Klik op linket i den valgte række på listen.
12. Vælg en indstilling i feltet Metode.
    * Det er muligt at gennemtvinge enten en markering eller et fravalg af en vare fra en anden variantgruppe.  
13. Klik på rullelisten i feltet Afledt gruppe for at åbne opslaget.
14. Find og vælg den ønskede post på listen.
15. Klik op linket i den valgte række på listen.
    * Vælg den ønskede variantgruppe.  
16. Klik på rullelisten i feltet Afledt varenummer for at åbne opslaget.
17. Klik op linket i den valgte række på listen.
    * Vælg det varenummer, der skal vælges eller fravælges afhængigt af den valgte metode.  
18. Luk siden.

