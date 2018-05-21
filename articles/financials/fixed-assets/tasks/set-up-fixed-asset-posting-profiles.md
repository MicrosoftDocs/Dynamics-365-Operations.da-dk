--- 
title: "Oprette posteringsprofiler for anlægsaktiver"
description: "Denne opgaveguide konfigurerer posteringsprofiler for bogføring af anlægsaktiver."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Oprette posteringsprofiler for anlægsaktiver

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide konfigurerer posteringsprofiler for bogføring af anlægsaktiver.  Den bruger rollen Revisor og demodata for den juridiske enhed USMF.  Eksemplerne i opgaveguiden er for en grundlæggende posteringsprofil, men posteringsprofiler skal oprettes for din specifikke kontoplan og krav til finansiel rapportering.

1. Gå til Anlægsaktiver > Opsætning > Posteringsprofiler for anlægsaktiver.
2. Klik på Ny.
3. Skriv en værdi i feltet Posteringsprofil.
4. Skriv en værdi i feltet Beskrivelse.
    * Du skal oprette en posteringsprofil til hver transaktionstype for anlægsaktiver, som du vil bruge, når du arbejder med anlægsaktiver.  Denne opgaveguide starter med transaktionstypen Anskaffelse.  
5. Klik på Tilføj.
6. Indtast eller vælg en værdi i feltet Bog.
    * I feltet Grupperinger kan du definere posteringsprofilen ned til tabellen (én konto konfigureret for hvert anlægsaktiv) eller gruppe (én konto konfigureret for hver anlægsaktivgruppe).  Til denne opgaveguide er værdien angivet til "Alle" for at gælde for alle anlægsaktiver med den angivne bog.  
7. Angive de ønskede værdier i feltet Hovedkonto.
    * Du kan for Anskaffelser angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.    
8. Vælg "Anskaffelsesregulering" i feltet Transaktionstype.
    * Til posteringer til anskaffelsesreguleringer bruger vi de samme konti som anvendt til anskaffelsesposteringer.  
9. Klik på Tilføj.
10. Indtast eller vælg en værdi i feltet Bog.
11. Angive de ønskede værdier i feltet Hovedkonto.
    * Du kan for anskaffelsesreguleringer angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.    
12. Vælg "Afskrivning" i feltet Transaktionstype.
13. Klik på Tilføj.
14. Indtast eller vælg en værdi i feltet Bog.
15. Angive de ønskede værdier i feltet Hovedkonto.
16. I feltet Modkonto skal du specificere de ønskede værdier.
17. Vælg "Afskrivningsregulering" i feltet Transaktionstype.
    * Til posteringer til afskrivningsreguleringer bruger vi de samme konti som anvendt til afskrivningsposteringer.  
18. Klik på Tilføj.
19. Indtast eller vælg en værdi i feltet Bog.
20. Angive de ønskede værdier i feltet Hovedkonto.
21. I feltet Modkonto skal du specificere de ønskede værdier.
22. Vælg "Kassation – salg" i feltet Transaktionstype.
23. Klik på Tilføj.
24. Indtast eller vælg en værdi i feltet Bog.
25. Angive de ønskede værdier i feltet Hovedkonto.
    * Du kan for Kassation angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.  
26. Vælg "Kassation – spild" i feltet Transaktionstype.
    * Vi bruger de samme konti til kassation-salg og kassation-spild.  
27. Klik på Tilføj.
28. Indtast eller vælg en værdi i feltet Bog.
29. Angive de ønskede værdier i feltet Hovedkonto.
    * Du kan for Kassation angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.  
30. Udvid sektionen Kassation.
    * Du skal konfigurere posteringsprofiler for både salg og skrot.  Vi starter med salgstransaktioner for kassation.  
31. Klik på Tilføj.
32. Indtast eller vælg en værdi i feltet Bog.
33. Vælg "Anskaffelsesværdi" i feltet Bogfør værdi.
    * Anskaffelsesværdi håndterer anskaffelse og anskaffelsesreguleringsværdier for alle år.  Du kan også definere konti for disse posteringstyper separat.  
    * Du kan angive, at kassationsprocessen skal bruge forskellige konti, afhængigt af om kassationen resulterer i tab eller vinding.  Jeg vil angive værditypen til "Alle" for at bruge de samme konti til alle former for kassation.  
34. Angive de ønskede værdier i feltet Hovedkonto.
35. I feltet Modkonto skal du specificere de ønskede værdier.
36. Klik på Tilføj.
37. Indtast eller vælg en værdi i feltet Bog.
    * Vælg "Afskrivning (foregående år)" i feltet Bogfør værdi.  
38. Angive de ønskede værdier i feltet Hovedkonto.
39. I feltet Modkonto skal du specificere de ønskede værdier.
40. Klik på Tilføj.
41. Indtast eller vælg en værdi i feltet Bog.
42. Vælg "Afskrivning (indeværende år)" i feltet Bogfør værdi.
43. Angive de ønskede værdier i feltet Hovedkonto.
44. I feltet Modkonto skal du specificere de ønskede værdier.
45. Klik på Tilføj.
46. Indtast eller vælg en værdi i feltet Bog.
47. Vælg "Reguleringer af afskrivning (foregående år)" i feltet Bogfør værdi.
48. Angive de ønskede værdier i feltet Hovedkonto.
49. I feltet Modkonto skal du specificere de ønskede værdier.
50. Klik på Tilføj.
51. Indtast eller vælg en værdi i feltet Bog.
52. Vælg "Reguleringer af afskrivning (indeværende år)" i feltet Bogfør værdi.
53. Angive de ønskede værdier i feltet Hovedkonto.
54. I feltet Modkonto skal du specificere de ønskede værdier.
55. Klik på Tilføj.
56. Indtast eller vælg en værdi i feltet Bog.
57. Vælg "Bogført nettoværdi" i feltet Bogfør værdi.
58. Angive de ønskede værdier i feltet Hovedkonto.
59. I feltet Modkonto skal du specificere de ønskede værdier.
60. Vælg "Spild" i feltet Salg eller spild.
61. Klik på Tilføj.
62. Indtast eller vælg en værdi i feltet Bog.
63. Vælg "Anskaffelsesværdi" i feltet Bogfør værdi.
64. Angive de ønskede værdier i feltet Hovedkonto.
65. I feltet Modkonto skal du specificere de ønskede værdier.
66. Klik på Tilføj.
67. Indtast eller vælg en værdi i feltet Bog.
    * Vælg "Afskrivning (foregående år)" i feltet Bogfør værdi.  
68. Angive de ønskede værdier i feltet Hovedkonto.
69. I feltet Modkonto skal du specificere de ønskede værdier.
70. Klik på Tilføj.
71. Indtast eller vælg en værdi i feltet Bog.
72. Vælg "Afskrivning (indeværende år)" i feltet Bogfør værdi.
73. Angive de ønskede værdier i feltet Hovedkonto.
74. I feltet Modkonto skal du specificere de ønskede værdier.
75. Klik på Tilføj.
76. Indtast eller vælg en værdi i feltet Bog.
77. Vælg "Reguleringer af afskrivning (foregående år)" i feltet Bogfør værdi.
78. Angive de ønskede værdier i feltet Hovedkonto.
79. I feltet Modkonto skal du specificere de ønskede værdier.
80. Klik på Tilføj.
81. Indtast eller vælg en værdi i feltet Bog.
82. Vælg "Reguleringer af afskrivning (indeværende år)" i feltet Bogfør værdi.
83. Angive de ønskede værdier i feltet Hovedkonto.
84. I feltet Modkonto skal du specificere de ønskede værdier.
85. Klik på Tilføj.
86. Indtast eller vælg en værdi i feltet Bog.
87. Vælg "Bogført nettoværdi" i feltet Bogfør værdi.
88. Angive de ønskede værdier i feltet Hovedkonto.
89. I feltet Modkonto skal du specificere de ønskede værdier.


