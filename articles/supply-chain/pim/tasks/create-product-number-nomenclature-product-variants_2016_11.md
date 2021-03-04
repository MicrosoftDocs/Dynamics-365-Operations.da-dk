---
title: Oprette et produktnummernomenklatur for konfigurerede produktvarianter
description: Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f75d7e493255b9c09c10b121f388854861cb0fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424625"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Oprette et produktnummernomenklatur for konfigurerede produktvarianter

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres. Denne fremgangsmåde viser også, hvordan du kan opbygge en konfigurationsnomenklatur en produktkonfigurations modelkomponent. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Den nye nomenklatur for produktnumre er knyttet til produktmasteren D0004. Denne opgave udføres normalt af en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opret en nomenklatur for produktnummer
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktnomenklatur.
3. Klik på Ny.
4. Skriv en værdi i feltet Navn.
5. Skriv en værdi i feltet Beskrivelse.
6. Klik på Tilføj.
7. Klik på Produktmasternummer.
8. Klik på Tilføj.
9. Klik på Tekstkonstant.
10. Markér den valgte række på listen.
11. Skriv en værdi i feltet Tekst.
12. Klik på Tilføj.
13. Klik på Konfiguration.
14. Luk siden.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tildel nomenklaturen for produktnummer til en produktmaster
1. Klik på Produktmastere.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Produktnummer med værdien "D".
3. Klik op linket i den valgte række på listen.
4. Klik på Rediger.
5. Vælg Ja i feltet Brug nomenklatur.
6. Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.
7. Luk siden.
8. Luk siden.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Opret nomenklatur for en komponent i en produktkonfigurationsmodel
1. Klik på Produktkonfigurationsmodeller.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Klik på Rediger.
5. Vælg Ja i feltet Brug konfigurationsnomenklatur.
6. Klik på Tilføj.
7. Klik på Attributværdi.
8. Markér den valgte række på listen.
9. Indtast eller vælg en værdi i feltet Attribut.
10. Klik på Tilføj.
11. Klik på Tekstkonstant.
12. Markér den valgte række på listen.
13. Skriv en værdi i feltet Tekst.
14. Klik på Tilføj.
15. Klik på Attributværdi.
16. Markér den valgte række på listen.
17. Indtast eller vælg en værdi i feltet Attribut.
18. Klik på Tilføj.
19. Klik på Tekstkonstant.
20. Markér den valgte række på listen.
21. Skriv en værdi i feltet Tekst.
22. Klik på Tilføj.
23. Klik på Attributværdi.
24. Markér den valgte række på listen.
25. Indtast eller vælg en værdi i feltet Attribut.
26. Klik på Tilføj.
27. Klik på Tekstkonstant.
28. Markér den valgte række på listen.
29. Skriv en værdi i feltet Tekst.
30. Klik på Tilføj.
31. Klik på Attributværdi.
32. Markér den valgte række på listen.
33. Indtast eller vælg en værdi i feltet Attribut.
34. Klik på Tilføj.
35. Klik på Tekstkonstant.
36. Markér den valgte række på listen.
37. Skriv en værdi i feltet Tekst.
38. Klik på Tilføj.
39. Klik på Nummerserieværdi.
40. Markér den valgte række på listen.
41. Skriv eller vælg en værdi i feltet Nummerserie.
42. Luk siden.
43. Luk siden.
44. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]