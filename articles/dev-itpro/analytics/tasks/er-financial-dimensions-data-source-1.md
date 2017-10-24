--- 
title: "Designe datamodel til at bruge økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en systemadministrator eller udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d8a03c4b85666975a7b42d46f3afdd35019e9b93
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Designe datamodel til at bruge økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en systemadministrator eller udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter. Disse trin kan udføres i en hvilken som helst virksomhed.

Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.


## <a name="create-a-new-data-model"></a>Opret en ny datamodel
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at udbyderen "Litware, Inc." er tilgængelig og markeret som aktiv.  
2. Klik på Rapporteringskonfigurationer.
3. Klik på Opret konfiguration for at åbne dialogboksen.
4. Skriv 'Eksempelmodel til økonomiske dimensioner' i feltet Navn.
5. Klik på Opret konfiguration.
6. Klik på Designer.
7. Klik på Ny for at åbne dialogboksen Fjern.
8. Skriv 'Post' et navn i feltet Navn.
9. Klik på Tilføj.
10. Klik på Ny for at åbne dialogboksen Fjern.
11. Skriv "Firma" feltet Navn.
12. Klik på Tilføj.
    * Vi vil føje en ny liste over poster til vores model. Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) indstillingerne for den valgte økonomiske dimension. Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens indstilling.  
13. Klik på Ny for at åbne dialogboksen Fjern.
14. Skriv 'Dimensionsindstilling' i feltet Navn.
15. Vælg "Liste over poster" i feltet Varetype.
16. Klik på Tilføj.
17. Klik på Ny for at åbne dialogboksen Fjern.
18. Skriv 'Kode' i feltet Navn.
19. Vælg "Streng" i feltet Varetype.
20. Klik på Tilføj.
21. Klik på Ny for at åbne dialogboksen Fjern.
22. Skriv "Navn" i feltet Navn.
23. Klik på Tilføj.
24. Vælg 'Post' i træet.
25. Klik på Ny for at åbne dialogboksen Fjern.
26. Skriv 'Journal' i feltet Navn.
27. Vælg "Liste over poster" i feltet Varetype.
28. Klik på Tilføj.
29. Klik på Ny for at åbne dialogboksen Fjern.
30. Skriv 'Batch' i feltet Navn.
31. Vælg "Streng" i feltet Varetype.
32. Klik på Tilføj.
33. Klik på Ny for at åbne dialogboksen Fjern.
34. Skriv "Transaktion" i feltet Navn.
35. Vælg "Liste over poster" i feltet Varetype.
36. Klik på Tilføj.
37. Klik på Ny for at åbne dialogboksen Fjern.
38. Skriv 'Dato' i feltet Navn.
39. Vælg "Dato" i feltet Varetype.
40. Klik på Tilføj.
41. Klik på Ny for at åbne dialogboksen Fjern.
42. Skriv 'Debet' i feltet Navn.
43. Vælg "Kommatal" i feltet Varetype.
44. Klik på Tilføj.
45. Klik på Ny for at åbne dialogboksen Fjern.
46. Skriv "Kredit" i feltet Navn.
47. Klik på Tilføj.
48. Klik på Ny for at åbne dialogboksen Fjern.
49. Skriv "Valuta" feltet Navn.
50. Vælg "Streng" i feltet Varetype.
51. Klik på Tilføj.
52. Klik på Ny for at åbne dialogboksen Fjern.
53. Skriv 'Bilag' i feltet Navn.
54. Klik på Tilføj.
55. Klik på Ny for at åbne dialogboksen Fjern.
56. Skriv 'Dimensionsdata' i feltet Navn.
57. Vælg "Liste over poster" i feltet Varetype.
58. Klik på Tilføj.
    * Vi har føjet en ny liste over poster til vores model. Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) værdierne for den valgte økonomiske dimension. Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens værdier. Dimensionsnavnet præsenteres også i denne post som et felt, der skal bruges, hvis det er nødvendigt med henblik på valg.  
59. Klik på Ny for at åbne dialogboksen Fjern.
60. Skriv 'Kode' i feltet Navn.
61. Vælg "Streng" i feltet Varetype.
62. Klik på Tilføj.
63. Klik på Ny for at åbne dialogboksen Fjern.
64. Skriv "Beskrivelse" i feltet Navn.
65. Klik på Tilføj.
66. Klik på Ny for at åbne dialogboksen Fjern.
67. Skriv "Navn" i feltet Navn.
68. Klik på Tilføj.
69. Klik på Gem.
70. Luk siden.


