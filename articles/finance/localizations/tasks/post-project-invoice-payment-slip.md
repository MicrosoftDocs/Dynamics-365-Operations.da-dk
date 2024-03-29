---
title: Bogføre en projektfaktura med et indbetalingskort
description: Denne artikel forklarer, hvordan du kan bogføre en projektfaktura med et indbetalingskort i det angivne format.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, ProjProjectContractsListPage, ProjInvoiceTableCreate, ProjInvoiceTable, ProjProjectsListPage, ProjTableCreate, ProjGroupLookUp, ProjTable,  ProjTransOnAcc, ProjInvoiceProposalListPage, ProjInvoiceProposalCreateLines, ProjInvoiceProposalDetail, ProjInvoiceEditLines
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 644e72962f46e9990b6d336b67bb5e6259b86be7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871069"
---
# <a name="post-a-project-invoice-with-a-payment-slip"></a>Bogføre en projektfaktura med et indbetalingskort

[!include [banner](../../includes/banner.md)]

Du kan bogføre en projektfaktura med et vedhæftet indbetalingskort i det angivne format. Indbetalingskortet udskrives med kreditorens id-nummer og fakturanummeret, så indbetalingen kan identificeres.

Før du kan udføre denne procedure, skal du først oprette et indbetalingskortformat og oprette indbetalingskort til kundefakturaer. 



Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark. 

Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.

1. Gå til Debitor > Kunder > Alle kunder.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Vis eller skjul sektionen Faktura og levering.
5. Klik på Rediger.
6. I feltet På en projektfaktura skal du vælge en indstilling.
    * o    Ingen – Udskriv ikke et indbetalingskort. Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).   o    FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.   o FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.     
7. Klik på Gem.
8. Klik på fanen TabPageGrid.
9. Luk siden.
10. Gå til Projektstyring og regnskab > Projekter > Projektkontrakter.
11. Klik på Ny.
12. Skriv en værdi i feltet Navn.
13. Klik på rullelisten i feltet Finansieringskilde for at åbne opslaget.
14. Klik op linket i den valgte række på listen.
15. Klik på rullelisten i feltet Salgsvaluta for at åbne opslaget.
16. Find og vælg den ønskede post på listen.
17. Klik op linket i den valgte række på listen.
18. Klik på rullelisten i feltet Salgsvaluta for at åbne opslaget.
19. Find og vælg den ønskede post på listen.
    * Indbetalingskortet kan kun udskrives for en projektfaktura med valutaen danske kroner (DKK).  
20. Klik op linket i den valgte række på listen.
21. Klik på OK.
22. Klik på Gem.
23. Gå til Projektstyring og regnskab > Projekter > Alle projekter.
24. Klik på Ny.
25. Vælg en indstilling i feltet Projekttype.
26. Skriv en værdi i feltet Projektnavn.
27. Klik på rullelisten i feltet Projektgruppe for at åbne opslaget.
28. Klik op linket i den valgte række på listen.
29. Klik på rullelisten i feltet Projektkontrakt-id for at åbne opslaget.
30. Find og vælg den ønskede post på listen.
31. Klik op linket i den valgte række på listen.
32. Klik på Opret projekt.
33. Klik på Projekt i handlingsruden.
34. Klik på Projektstadie.
35. Klik på Under behandling.
36. Klik på OK.
37. Klik på Gem.
38. Klik på Administrer i handlingsruden.
39. Klik på Acontotransaktioner.
40. Klik på Ny.
41. Markér den valgte række på listen.
42. Angiv et tal i feltet Salgspris.
43. Klik på Gem.
44. Luk siden.
45. Klik på Administrer i handlingsruden.
46. Klik på Projektfakturaforslag.
47. Klik på Ny.
48. Klik på Fakturaforslag.
49. Klik på rullelisten i feltet Projekt for at åbne opslaget.
50. Luk siden.
51. Klik på rullelisten i feltet Projektkontrakt for at åbne opslaget.
52. Find og vælg den ønskede post på listen.
53. Klik op linket i den valgte række på listen.
54. Klik på OK.
55. Klik på Bogfør.
56. Klik på OK.
57. Klik på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
