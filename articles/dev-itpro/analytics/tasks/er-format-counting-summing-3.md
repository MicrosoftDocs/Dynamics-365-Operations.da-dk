--- 
title: "Bruge beregninger til fremstille output til optælling og opsummering"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5b7f0cc5b94ab7be11a013ef3e5909d84847e885
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing"></a>Bruge beregninger til fremstille output til optælling og opsummering 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 2: Konfigurer beregninger)".

Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Konfigurer denne rapport til at bruge optællings- og sammenlægningsinfo
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Udvid 'Intrastat-model' i træet.
4. Udvid 'Intrastat-model\Intrastat (DE)' i træet.
5. Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.
6. Klik på Designer.
7. Klik på fanen Tilknytning.
8. Klik på Tilføj rod for at åbne dialogboksen.
    * Tilføj en ny datakilde for at hente en liste over huskede blokke.  
9. Vælg "Funktioner\Beregnet felt" i træet.
10. Skriv '$BlocksList' i feltet Navn.
    * $BlocksList  
11. Klik på Rediger formel.
12. Vælg 'Datasamlingsfunktioner\COLLECTEDLIST' i træet.
13. Klik på Tilføj funktion.
14. Klik på Tilføj datakilde.
15. Skriv 'COLLECTEDLIST('$BlockName', ' i feltet Formel.
    * COLLECTEDLIST('$BlockName',  
16. Skriv 'COLLECTEDLIST('$BlockName', "*")' i feltet Formel.
    * COLLECTEDLIST('$BlockName', "*")  
17. Klik på Gem.
    * Mønsteret "*" betyder, at alle blokke medtages på listen til denne post.  
18. Luk siden.
19. Klik på OK.
20. Klik på fanen Format.
21. Vælg 'Intrastat\Data' i træet.
22. Klik på Tilføj for at åbne dialogboksen.
23. Vælg 'Text\Sequence' i træet.
24. Skriv 'Totaler efter blokke' i feltet Navn.
    * Totaler efter blokke  
25. Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.
26. Klik på OK.
27. Vælg 'Intrastat\Data\Totaler efter blokke' i træet.
28. Klik på Tilføj for at åbne dialogboksen.
29. Vælg "Tekst\Streng" i træet.
30. Skriv 'Blokkode' i feltet Navn.
    * Bloker kode  
31. Klik på OK.
32. Klik på Tilføj streng.
33. Skriv 'Linjeoptælling' i feltet Navn.
    * Linjeoptælling  
34. Klik på OK.
35. Klik på Tilføj streng.
36. Skriv "Samlet beløb" i feltet Navn.
    * Totalbeløb  
37. Klik på OK.
38. Klik på fanen Tilknytning.
39. Vælg '$BlocksList' i træet.
40. Klik på Bind.
    * Opret en oversigtslinje for hver huskede blok.  
41. Klik på fanen Format.
42. Vælg 'Intrastat\Data\Totaler efter blokke\Blokkode' i træet.
43. Klik på fanen Tilknytning.
44. Klik på Rediger formel.
45. Skriv "Blok-id: " & ' i feltet Formel.
    * "Blok-id: " &  
46. Udvid '$BlocksList' i træet.
47. Vælg '$BlocksList\Value' i træet.
48. Klik på Tilføj datakilde.
49. Klik på Gem.
50. Luk siden.
51. Klik på fanen Format.
52. Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling' i træet.
53. Klik på fanen Tilknytning.
54. Klik på Rediger formel.
    * Opret output for antallet af linjer for hver blok, der vises i denne rapport.  
55. Skriv '"Antal linjer i denne blok: " & ' i feltet Formel.
    * "Antal linjer i denne blok: " &  
56. Skriv '"Antal linjer i denne blok: " & TEXT(' i feltet Formel.
    * "Antal linjer i denne blok: " & TEXT(  
57. Vælg 'Datasamlingsfunktioner\COUNTIFS' i træet.
58. Klik på Tilføj funktion.
59. Klik på Tilføj datakilde.
60. Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', ' i feltet Formel.
    * "Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName',  
61. Udvid '$BlocksList' i træet.
62. Vælg '$BlocksList\Value' i træet.
63. Klik på Tilføj datakilde.
64. Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i feltet Formel.
    * "Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Vælg '$RecName' i træet.
66. Klik på Tilføj datakilde.
67. Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))' i feltet Formel.
    * "Antal linjer i denne blok:" & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Klik på Gem.
69. Luk siden.
70. Klik på fanen Format.
71. Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling\Samlet beløb' i træet.
72. Klik på fanen Tilknytning.
73. Klik på Rediger formel.
    * Opret output, der er summen af det fakturerede beløb for hver blok, der vises i denne rapport.  
74. Skriv '"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))' i feltet Formel.
    * "Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Klik på Gem.
76. Luk siden.
77. Klik på Gem.
78. Luk siden.


