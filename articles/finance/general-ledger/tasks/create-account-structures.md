---
title: Oprette kontostrukturer
description: Denne opgaveguide gennemgår oprettelse af en kontostruktur.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aece2b79633802d28ba3b4fd8b51788e26c17a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815158"
---
# <a name="create-account-structures"></a>Oprette kontostrukturer

[!include [banner](../../includes/banner.md)]

Denne opgaveguide gennemgår oprettelse af en kontostruktur. Der er brugt demodatafirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Finans > Kontoplan > Strukturer > Konfigurer kontostrukturer**.
2. Klik på **Ny** i **handlingsruden** for at åbne dialogboksen.
3. I feltet **Kontostruktur** skal du skrive et navn, som beskriver formålet med kontostrukturen.
4. I feltet **Beskrivelse** skal du indtaste et beskrivelse, som angiver formålet med kontostrukturen.
5. Klik på **Opret**.
6. Klik på **Tilføj segment** i **Segmenter og tilladte værdier**.
7. På listen over dimensioner skal du vælge den dimension, der skal føjes til kontostrukturen.
8. Klik på **Tilføj segment** nederst på listen.
9. Gentag trin 6 til 9 efter behov.
10. Vælg segmentet i sektionen i **Oplysninger om tilladt værdi** for at redigere de tilladte værdier.
    Klik f.eks. på feltet **Hovedkonto**.  
11. Vælg en indstilling i feltet **Operatør**, f.eks. er mellem og inkluderer.
12. Skriv en værdi i feltet **Værdi**. For eksempel 600000.  
13. Skriv en værdi i feltet **værdi**. For eksempel 699999.  
14. Klik på **Anvend** i sektionen **Oplysninger om tilladt værdi**.
15. Gentag trin 10 til 15 efter behov.  
16. Klik på **Tilføj nye kriterier** i sektionen **Oplysninger om tilladt værdi**.
17. Vælg en indstilling i feltet Operatør, f.eks. er mellem og inkluderer.
18. Skriv en værdi i feltet **Værdi**. For eksempel 033.  
19. Skriv en værdi i feltet **værdi**. For eksempel 034.  
20. Klik på **Anvend**.
21. Vælg segmentet i gitteret for at redigere de tilladte værdier. For eksempel Bærer.  
22. Skriv en værdi i feltet **CostCenter**. For eksempel 007..021.  
23. Klik på **Tilføj** i **Segmenter og tilladte værdier**.
24. Skriv en værdi i feltet **MainAccount**. For eksempel, 600000..699999  
25. Vælg segmentet i gitteret for at redigere de tilladte værdier. For eksempel Afdeling.  
26. Skriv en værdi i feltet Afdeling. For eksempel 032.  
27. Skriv en værdi i feltet CostCenter. For eksempel 086.  
28. Klik på **Valider** i **handlingsruden**.
29. Klik på **Aktivér** i **handlingsruden**.
30. Klik på **Aktiver**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]