--- 
title: "Designe en rapport til at bruge økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter."
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
ms.openlocfilehash: c67bf235f3514a19893bcefcaae6e3bb11bbb151
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Designe en rapport til at bruge økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 2: Modeltilknytning)".


## <a name="design-a-report-to-present-financial-dimensions"></a>Opret en rapport til visning af økonomiske dimensioner
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.
3. Klik på Opret konfiguration for at åbne dialogboksen.
4. Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.
    * Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.  
5. Skriv "Finanskladderapport" i feltet Navn.
6. Vælg Post i feltet Definition.
7. Klik på Opret konfiguration.
8. Klik på Designer.
9. Klik på Tilføj rod for at åbne dialogboksen.
10. Vælg "XML\Element'' i træet.
11. Skriv 'Root' i feltet Navn.
12. Klik på OK.
13. Klik på Tilføj for at åbne dialogboksen.
14. Vælg "XML\Attribut" i træet.
15. Skriv "Firma" feltet Navn.
16. Klik på OK.
17. Klik på Tilføj for at åbne dialogboksen.
18. Vælg "XML\Element'' i træet.
19. Skriv 'Journal' i feltet Navn.
20. Klik på OK.
21. Vælg 'Root: XML Element\Journal: XML-element' i træet.
22. Klik på Tilføj for at åbne dialogboksen.
23. Vælg "XML\Attribut" i træet.
24. Skriv 'Batch' i feltet Navn.
25. Klik på OK.
26. Klik på Tilføj for at åbne dialogboksen.
27. Vælg "XML\Element'' i træet.
28. Skriv "Transaktion" i feltet Navn.
29. Klik på OK.
30. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.
31. Klik på Tilføj for at åbne dialogboksen.
32. Vælg "XML\Attribut" i træet.
33. Skriv 'Bilag' i feltet Navn.
34. Klik på OK.
35. Klik på Tilføj attribut.
36. Skriv 'Dato' i feltet Navn.
37. Klik på OK.
38. Klik på Tilføj attribut.
39. Skriv "Valuta" feltet Navn.
40. Klik på OK.
41. Klik på Tilføj attribut.
42. Skriv 'Dt' i feltet Navn.
43. Klik på OK.
44. Klik på Tilføj attribut.
45. Skriv 'Ct' i feltet Navn.
46. Klik på OK.
47. Klik på Tilføj for at åbne dialogboksen.
48. Vælg "XML\Element'' i træet.
49. Skriv 'Dimensioner' i feltet Navn.
50. Klik på OK.
51. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.
52. Klik på Tilføj for at åbne dialogboksen.
53. Vælg "XML\Attribut" i træet.
54. Skriv 'Kode' i feltet Navn.
55. Klik på OK.
56. Klik på Tilføj attribut.
57. Skriv 'Værdi' i feltet Navn.
58. Klik på OK.
59. Klik på Tilføj attribut.
60. Skriv 'Desc' i feltet Navn.
61. Klik på OK.

## <a name="map-report-elements-to-data-sources"></a>Knyt rapportelementer til datakilder
1. Klik på fanen Tilknytning.
2. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.
3. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.
4. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.
5. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.
6. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Desc: XML-attribut' i træet.
7. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Beskrivelse: Streng' i træet.
8. Klik på Bind.
9. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Værdi: XML-attribut' i træet.
10. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.
11. Klik på Bind.
12. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Kode: XML-attribut' i træet.
13. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Navn: Streng' i træet.
14. Klik på Bind.
15. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.
16. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.
17. Klik på Bind.
18. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Ct: XML-attribut' i træet.
19. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.
20. Klik på Bind.
21. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dt: XML-attribut' i træet.
22. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.
23. Klik på Bind.
24. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Valuta: XML-attribut' i træet.
25. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.
26. Klik på Bind.
27. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Data: XML-attribut' i træet.
28. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.
29. Klik på Bind.
30. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Bilag: XML-attribut' i træet.
31. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.
32. Klik på Bind.
33. Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.
34. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.
35. Klik på Bind.
36. Vælg 'Root: XML-element\Journal: XML-element\Batch: XML-attribut' i træet.
37. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.
38. Klik på Bind.
39. Vælg 'Root: XML Element\Journal: XML-element' i træet.
40. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.
41. Klik på Bind.
42. Vælg 'Root: XML-element\Firma: XML-attribut' i træet.
43. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.
44. Klik på Bind.
45. Klik på Gem.
46. Luk siden.


