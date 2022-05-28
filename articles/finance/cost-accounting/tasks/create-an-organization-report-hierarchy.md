---
title: Oprette et organisationsrapporthierarki
description: Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering.
author: twheeloc
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e247ad7ac79607ce5f7209c343aabc5e3b66163a
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734713"
---
# <a name="create-an-organization-report-hierarchy"></a>Oprette et organisationsrapporthierarki

[!include [banner](../../includes/banner.md)]

Du kan bruge denne procedure til at oprette et rapporthierarki til organisationsrapportering. Formålet med denne registrering er at føre dig gennem dimensionshierarkiet, så du kan fortsætte, indtil rapporteringsstrukturen for hele organisationen er oprettet. Denne registrering bruger USP2-demodatafirmaet.

1. Gå til **Omkostningsregnskab > Dimensioner > Dimensionshierarkier**.
2. Klik på **Ny**.
3. Vælg 'Klassifikationshierarki for dimension' i feltet **HierarchyTypeComboBox**.
    * Vælg Klassifikationshierarki for dimension. Klassifikationshierarki for dimension-typen bruges til at definere regler og til rapporteringsformål. Den understøtter alle dimensioner, f.eks. omkostningsobjekter, omkostningselementer og statistiske dimensioner.  
4. Klik på **Opret**.
5. Skriv 'Organisation USP2' i feltet **Navn på dimensionshierarki**.
6. Indtast eller vælg en værdi i feltet **Dimension**.
    * Vælg Bærere.  
7. Klik på **Gem**.
8. Klik på **Vis hierarki**.
9. Klik på **Ny**.
10. Skriv 'Administrerende direktør' i feltet **Nodenavn**.
11. Klik på **Gem**.
12. Klik på **Ny**.
13. Skriv 'Bærere for administrerende direktør' i feltet **Nodenavn**.
14. Klik på **Gem**.
15. Klik på **Ny**.
16. Skriv 'Region Øst' i feltet **Nodenavn**.
17. Klik på **Gem**.
18. Klik på **Ny**.
19. Markér den valgte række på listen.
20. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Vælg det dimensionsmedlem, der svarer til noden.  
21. Klik på **Gem**.
22. Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.
23. Klik på **Ny**.
24. Skriv 'Region Vest' i feltet **Nodenavn**.
25. Klik på **Gem**.
26. Klik på **Ny**.
27. Markér den valgte række på listen.
28. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Vælg det dimensionsmedlem, der svarer til noden.  
29. Klik på **Gem**.
30. Vælg 'Organisation USP2\Administrerende direktør' i træet.
31. Klik på **Ny**.
32. Skriv 'Bærere for regnskabsdirektør' i feltet **Nodenavn**.
33. Klik på **Gem**.
34. Klik på **Ny**.
35. Skriv 'Marketingkampa' i feltet **Nodenavn**.
36. Skriv 'Marketingkampagne' i feltet **Nodenavn**.
37. Klik på **Gem**.
38. Klik på **Ny**.
39. Markér den valgte række på listen.
40. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Vælg det dimensionsmedlem, der svarer til noden.  
41. Klik på **Gem**.
42. Vælg 'Organisation USP2\Administrerende direktør\Bærere for administrerende direktør' i træet.
43. Klik på **Ny**.
44. Skriv 'Messer' i feltet **Nodenavn**.
45. Klik på **Gem**.
46. Klik på **Ny**.
47. Markér den valgte række på listen.
48. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Vælg det dimensionsmedlem, der svarer til noden.  
49. Klik på **Gem**.
50. Vælg 'Organisation USP2\Administrerende direktør' i træet.
51. Skriv 'Bærere for informationschef' i feltet **Nodenavn**.
52. Klik på **Gem**.
53. Klik på **Ny**.
54. Skriv 'Call centre' i feltet **Nodenavn**.
55. Klik på **Gem**.
56. Klik på **Ny**.
57. Markér den valgte række på listen.
58. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Vælg det dimensionsmedlem, der svarer til noden.  
59. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
