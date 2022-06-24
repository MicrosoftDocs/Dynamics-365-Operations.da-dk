---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)'
description: Denne artikel beskriver, hvordan du konfigurerer et format for elektronisk rapportering til optælling og opsummering baseret på data fra det allerede genererede tekstoutput. (Del 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c708a6da7d5f37571d3e4fc8587beb4c30f33784
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895331"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 1: Oprettelsesformat)".

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Opret en formatkonfiguration for at tilføje optællings- og sammenlægningsdetaljer
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Udvid 'Intrastat-model' i træet.
4. Vælg 'Intrastat-model\Intrastat (DE)' i træet.
    * Antag, at du skal tilpasse det format, der leveres af Microsoft, ved at tilføje linjer med oversigtsdetaljerne i slutningen af Intrastat-rapporten. Det skal du gøre ved at aflede din egen forekomst af Intrastat-konfigurationen fra Microsofts forekomst for at foretage ændringer.  
5. Klik på Opret konfiguration for at åbne dialogboksen.
6. Skriv 'Afled fra navn: Intrastat (DE), Microsoft' i feltet Ny.
7. Skriv 'Intrastat (DE) med optælling og sammenlægning' i feltet Navn.
8. Klik på Opret konfiguration.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Konfigurer denne rapport til at udføre optælling og sammenlægning baseret på oplysninger om output
1. Klik på Designer.
2. Vælg Ja i feltet Detaljer om indsamlingsoutput.
    * Dette flag aktiverer på kørselstidspunktet processen til indsamling af outputdetaljer til generering af Intrastat-filen.  
    * Du skal foretage optælling for forskellige Intrastat-retninger, så føj en dedikeret modeloptælling til datakildernes liste over denne formatkonfiguration.  
3. Klik på fanen Tilknytning.
4. Klik på Tilføj rod for at åbne dialogboksen.
5. Vælg 'Datamodel\Optælling' i træet.
6. Skriv 'Retning' i feltet Navn.
7. Indtast eller vælg en værdi i feltet Modelfasttekst.
    * Vælg værdien Retning.  
8. Klik på OK.
9. Klik på Tilføj rod for at åbne dialogboksen.
10. Vælg "Funktioner\Beregnet felt" i træet.
11. Skriv '$BlockName' i feltet Navn.
12. Klik på Rediger formel.
13. Skriv "bloker" i feltet Formel.
14. Klik på Gem.
15. Luk siden.
16. Klik på OK.
17. Klik på Tilføj rod for at åbne dialogboksen.
18. Vælg "Funktioner\Beregnet felt" i træet.
19. Skriv '$RecName' i feltet Navn.
20. Klik på Rediger formel.
21. Skriv "post" i feltet Formel.
22. Klik på Gem.
23. Luk siden.
24. Klik på OK.
25. Klik på Tilføj rod for at åbne dialogboksen.
26. Vælg "Funktioner\Beregnet felt" i træet.
27. Skriv '$InvName' i feltet Navn.
28. Klik på Rediger formel.
29. Skriv '"InvoicedAmountEUR"' i feltet Formel.
30. Klik på Gem.
31. Luk siden.
32. Klik på OK.
33. Vælg 'Intrastat\Data' i træet.
34. Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'
35. Klik på Tilføj datakilde.
    * $BlockName  
36. Klik på Gem.
37. Luk siden.
38. Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.
39. Skriv 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")' i feltet Formel.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Klik på Gem.
41. Luk siden.
    * Tæl linjerne i denne rækkefølge. Resultaterne skal bruges sammen med navnet "bloker" separat for forskellige retninger. "Import" vil blive brugt til enhver Intrastat-postering for indførsel. Værdien "Eksport" vil blive brugt til enhver Intrastat-postering for udførsel. Overvej at bruge et virtuelt Excel-regneark. For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.  
42. Udvid 'Intrastat\Data: Sequence' i træet.
43. Vælg 'Intrastat\Data: Sequence\Arrivals?' i træet.
44. Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.
    * Tæl linjerne i denne rækkefølge. Resultaterne huskes med navnet "post".  
45. Vælg '$RecName' i træet.
46. Klik på Tilføj datakilde.
47. Klik på Gem.
48. Luk siden.
49. Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'
50. Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.
51. Klik på Gem.
52. Luk siden.
    * Tæl linjerne i denne rækkefølge. Resultaterne skal bruges sammen med navnet "post" separat for forskellige varekoder. Overvej at bruge et virtuelt Excel-regneark. For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksporter" i overensstemmelse hermed, og den anden blok "post"udfyldes med varekodeværdien.  
53. Vælg 'Intrastat\Data: Sequence\Dispatches?' i træet.
54. Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'
55. Vælg '$RecName' i træet.
56. Klik på Tilføj datakilde.
57. Klik på Gem.
58. Luk siden.
59. Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.
60. Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.
61. Klik på Gem.
62. Luk siden.
63. Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?' i træet.
64. Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord' i træet.
65. Klik på fanen Format.
66. Vælg 'Intrastat\Data\Dispatches\Record\Fakturabeløb EUR' i træet.
67. Klik på fanen Tilknytning.
68. Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.
69. Vælg '$InvName' i træet.
70. Klik på Tilføj datakilde.
71. Klik på Gem.
72. Luk siden.
    * Sammenlæg de fakturerede beløbsværdier for linjerne i denne rækkefølge. Resultaterne skal bruges sammen med navnet "InvoicedAmountEUR" separat for forskellige Intrastat-retninger og varekoder. Overvej at bruge et virtuelt Excel-regneark. For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed. Den anden blok "post" udfyldes med varekodeværdien, og den tredje kolonne "InvoicedAmountEUR" udfyldes med en fakturabeløbsværdien.  
73. Udvid 'Intrastat\Data\Arrivals?' i træet.
74. Udvid 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord' i træet.
75. Klik på fanen Format.
76. Vælg 'Intrastat\Data\Arrivals\Record\Fakturabeløb EUR' i træet.
77. Klik på fanen Tilknytning.
78. Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.
79. Vælg '$InvName' i træet.
80. Klik på Tilføj datakilde.
81. Klik på Gem.
82. Luk siden.
83. Klik på Gem.
84. Luk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]