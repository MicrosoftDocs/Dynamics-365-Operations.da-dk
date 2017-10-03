--- 
title: Oprette en formatkonfiguration til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c46b222cb12d0432609c47f89afc522e02c41ab6
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Oprette en formatkonfiguration til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER). Denne formatkonfiguration definerer formatet af elektroniske dokumenter, der bruges til behandling af betalinger. I dette eksempel skal du oprette en formatkonfiguration for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Tilknyt model til markerede datakilder".


## <a name="create-a-new-format-configuration"></a>Opret en ny formatkonfiguration
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Vælg "Betalinger (forenklet mode)" i træet.
4. Klik på Opret konfiguration for at åbne dialogboksen.
5. Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.
6. Skriv "BACS (UK-fiktiv) i feltet Navn.
    * BACS (UK-fiktiv)  
7. Skriv "'BACS kreditorbetalingsformat (UK-fiktiv)" i feltet Beskrivelse.
    * BACS kreditorbetalingsformat (UK-fiktiv)  
    * Den aktive konfigurationsudbyder indsættes automatisk her. Denne udbyder vil kunne vedligeholde denne konfiguration. Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.  
    * Du kan definere et bestemt format for det elektroniske dokument. Lad feltet være tomt, hvis du vil vælge et format på kørselstidspunktet.  
8. Indtast eller vælg en værdi i feltet Definition af datamodel.
9. Klik på Opret konfiguration.
    * En ny konfiguration er oprettet. Kladdeversionen kan bruges til at gemme designformatet til håndtering af elektroniske dokumenter.  

## <a name="design-format-of-electronic-document"></a>Designformat for elektronisk dokument
1. Klik på Designer.
2. Klik på Tilføj rod for at åbne dialogboksen.
3. Vælg "Common\File" i træet.
4. Skriv "Xml" i feltet Navn.
    * Xml  
5. Skriv "UTF-8" i feltet Kodning.
    * UTF-8  
6. Klik på OK.
7. Klik på Tilføj for at åbne dialogboksen.
8. Vælg "XML\Element'' i træet.
9. Skriv "Meddelelse" i feltet Navn.
    * Melding  
10. Klik på OK.
11. Vælg "Xml\Meddelelse" i træet.
12. Klik på Tilføj element.
13. Skriv "ProcessingDate" i feltet Navn.
    * ProcessingDate  
14. Klik på OK.
15. Klik på Tilføj element.
16. Skriv "MessageId" i feltet Navn.
    * MessageId  
17. Klik på OK.
18. Klik på Tilføj element.
19. Skriv "Betalinger" i feltet Navn.
    * Betalinger  
20. Klik på OK.
21. Vælg "Xml\Meddelelse\Betalinger" i træet.
22. Klik på Tilføj element.
23. Skriv "Vare" i feltet Navn.
    * Post  
24. Klik på OK.
25. Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.
26. Klik på Tilføj for at åbne dialogboksen.
27. Vælg "XML\Attribut" i træet.
28. Skriv "Id" i feltet Navn.
    * Id  
29. Klik på OK.
30. Klik på Tilføj for at åbne dialogboksen.
31. Vælg "XML\Element'' i træet.
32. Skriv "Kreditor" i feltet Navn.
    * Leverandør  
33. Klik på OK.
34. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor" i træet.
35. Klik på Tilføj element.
36. Skriv "Navn" i feltet Navn.
    * Navn  
37. Klik på OK.
38. Klik på Tilføj element.
39. Skriv "Bank" i feltet Navn.
    * Pengeinstitut  
40. Klik på OK.
41. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.
42. Klik på Tilføj element.
43. Skriv "RoutingNumber" i feltet Navn.
    * RoutingNumber  
44. Klik på OK.
45. Klik på Tilføj element.
46. Skriv "AccountNumber" i feltet Navn.
    * AccountNumber  
47. Klik på OK.
48. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor" i træet.
49. Klik på Kopiér.
50. Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.
51. Klik på Sæt ind.
52. Skriv "Betaler" i feltet Navn.
    * Betaler  
53. Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.
54. Klik på Tilføj element.
55. Skriv "Valuta" feltet Navn.
    * Valuta  
56. Klik på OK.
57. Klik på Tilføj element.
58. Skriv "Beskrivelse" i feltet Navn.
    * Betegnelse  
59. Klik på OK.
60. Klik på Tilføj element.
61. Skriv "TransDate" i feltet Navn.
    * TransDate  
62. Klik på OK.
63. Klik på Tilføj element.
64. Skriv "Beløb" i feltet Navn.
    * Beløb  
65. Klik på OK.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Klargør formatkomponenter til tilknytning til datamodelelementer
1. Vælg "Xml\Meddelelse\ProcessingDate" i træet.
2. Klik på Tilføj for at åbne dialogboksen.
3. Vælg "Tekst\DateTime" i træet.
4. Skriv 'åååå-MM-dd' i feltet Format.
    * åååå-MM-dd  
5. Klik på OK.
6. Vælg "Xml\Meddelelse\Betalinger\TransDate" i træet.
7. Klik på Tilføj DateTime.
8. Skriv 'åååå-MM-dd' i feltet Format.
    * åååå-MM-dd  
9. Vælg "Date" i feltet DateTime-type.
10. Klik på OK.
11. Vælg "Xml\Meddelelse\MessageId" i træet.
12. Klik på Tilføj for at åbne dialogboksen.
13. Vælg "Tekst\Streng" i træet.
14. Klik på OK.
15. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn" i træet.
16. Klik på Tilføj streng.
17. Klik på OK.
18. Vælg "Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\RoutingNumber" i træet.
19. Klik på Tilføj streng.
20. Klik på OK.
21. Vælg "Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\AccountNumber" i træet.
22. Klik på Tilføj streng.
23. Klik på OK.
24. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Navn" i træet.
25. Klik på Tilføj streng.
26. Klik på OK.
27. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber" i træet.
28. Klik på Tilføj streng.
29. Klik på OK.
30. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber" i træet.
31. Klik på Tilføj streng.
32. Klik på OK.
33. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\Valuta" i træet.
34. Klik på Tilføj streng.
35. Klik på OK.
36. Vælg "Xml\Meddelelse\Betalinger\Vare\Beskrivelse" i træet.
37. Klik på Tilføj streng.
38. Klik på OK.
39. Vælg "Xml\Meddelelse\Betalinger\Vare\Beløb" i træet.
40. Klik på Tilføj streng.
41. Klik på OK.
42. Klik på Gem.
43. Luk siden.


