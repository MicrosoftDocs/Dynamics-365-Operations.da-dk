---
title: Oprette en ER-formatkonfiguration (november 2016)
description: Denne artikel forklarer, hvordan du opretter en formatkonfiguration til elektronisk rapportering (ER).
author: kfend
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: 3c705add64a46c4cce5127f16fae45edba1bc001
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290718"
---
# <a name="er-create-a-format-configuration-november-2016"></a>Oprette en ER-formatkonfiguration (november 2016)

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER). Denne formatkonfiguration definerer formatet af elektroniske dokumenter, der bruges til behandling af betalinger. I dette eksempel skal du oprette en formatkonfiguration for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Tilknyt model til markerede datakilder".


## <a name="create-a-new-format-configuration"></a>Opret en ny formatkonfiguration
1. Gå til **Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.
2. Klik på **Rapporteringskonfigurationer**.
3. Vælg **Betalinger (forenklet mode)** i træet.
4. Klik på **Opret konfiguration** for at åbne dialogboksen.

 > [!NOTE]
 > Hvis du ikke kan se **Opret konfiguration**, skal du aktivere designtilstand på siden **Parametre til elektronisk rapportering**. 
 
5. Skriv **Format baseret på datamodel PaymentModel** i feltet **Ny**.
6. Skriv **BACS (UK-fiktiv)** i feltet **Navn**.
7. Skriv **BACS kreditorbetalingsformat (UK-fiktiv)** i feltet **Beskrivelse**.
    * Den aktive konfigurationsudbyder indsættes automatisk her. Denne udbyder vil kunne vedligeholde denne konfiguration. Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.  
    * Du kan definere et bestemt format for det elektroniske dokument. Lad feltet være tomt, hvis du vil vælge et format på kørselstidspunktet.  
8. Indtast eller vælg en værdi i feltet **Definition af datamodel**.
9. Klik på **Opret konfiguration**. En ny konfiguration er oprettet. Kladdeversionen kan bruges til at gemme designformatet til håndtering af elektroniske dokumenter.  

## <a name="design-the-format-of-an-electronic-document"></a>Designformatet for et elektronisk dokument
1. Klik på **Designer**.
2. Klik på **Tilføj rod** for at åbne dialogboksen.
3. Vælg **Common\File** i træet.
4. Skriv **Xml** i feltet **Navn**.
5. Skriv **UTF-8** i feltet **Kodning**.
6. Klik på **OK**.
7. Klik på **Tilføj**.
8. Vælg **XML\Element** i træet.
9. Skriv **Meddelelse** i feltet **Navn**.
10. Klik på **OK**.
11. Vælg **Xml\Meddelelse** i træet.
12. Klik på **Tilføj element**.
13. Skriv **ProcessingDate** i feltet **Navn**.
14. Klik på **OK**.
15. Klik på **Tilføj element**.
16. Skriv **MessageId** i feltet Navn.
17. Klik på **OK**.
18. Klik på **Tilføj element**.
19. Skriv **Betalinger** i feltet **Navn**.
20. Klik på **OK**.
21. Vælg **Xml\Meddelelse\Betalinger** i træet.
22. Klik på **Tilføj element**.
23. Skriv **Vare** i feltet **Navn**.
24. Klik på **OK**.
25. Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.
26. Klik på **Tilføj**.
27. Vælg **XML\Attribut** i træet.
28. Skriv **Id** i feltet Navn.
29. Klik på **OK**.
30. Klik på **Tilføj**.
31. Vælg **XML\Element** i træet.
32. Skriv **Kreditor** i feltet Navn.
33. Klik på **OK**.
34. Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor** i træet.
35. Klik på **Tilføj element**.
36. Skriv **Navn** i feltet Navn.
37. Klik på **OK**.
38. Klik på **Tilføj element**.
39. Skriv **Bank** i feltet **Navn**.
40. Klik på **OK**.
41. Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank** i træet.
42. Klik på **Tilføj element**.
43. Skriv **RoutingNumber** i feltet **Navn**.
44. Klik på **OK**.
45. Klik på **Tilføj element**.
46. Skriv **AccountNumber** i feltet **Navn**.
47. Klik på **OK**.
48. Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor** i træet.
49. Klik på **Kopiér**.
50. Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.
51. Klik på **Sæt ind**.
52. Skriv **Betaler** i feltet **Navn**.
53. Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.
54. Klik på **Tilføj element**.
55. Skriv **Valuta** feltet **Navn**.
56. Klik på **OK**.
57. Klik på **Tilføj element**.
58. Skriv **Beskrivelse** i feltet **Navn**.
59. Klik på **OK**.
60. Klik på **Tilføj element**.
61. Skriv **TransDate** i feltet Navn.
62. Klik på **OK**.
63. Klik på **Tilføj element**.
64. Skriv **Beløb** i feltet Navn.
65. Klik på **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Klargør formatkomponenter til tilknytning til datamodelelementer
1. Vælg **Xml\Meddelelse\ProcessingDate** i træet.
2. Klik på **Tilføj** for at åbne dialogboksen.
3. Vælg **Tekst\DateTime** i træet.
4. Skriv **åååå-MM-dd** i feltet **Format**.
5. Klik på **OK**.
6. Vælg **Xml\Meddelelse\Betalinger\TransDate** i træet.
7. Klik på **Tilføj DateTime**.
8. Skriv **åååå-MM-dd** i feltet **Format**.
9. Vælg **Date** i feltet **DateTime**-type.
10. Klik på **OK**.
11. Vælg **Xml\Meddelelse\MessageId** i træet.
12. Klik på **Tilføj** for at åbne dialogboksen.
13. Vælg **Tekst\Streng** i træet.
14. Klik på **OK**.
15. Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn** i træet.
16. Klik på **Tilføj streng**.
17. Klik på **OK**.
18. Vælg **Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i træet.
19. Klik på **Tilføj streng**.
20. Klik på **OK**.
21. Vælg **Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\AccountNumber** i træet.
22. Klik på **Tilføj streng**.
23. Klik på **OK**.
24. Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Navn** i træet.
25. Klik på **Tilføj streng**.
26. Klik på **OK**.
27. Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber** i træet.
28. Klik på **Tilføj streng**.
29. Klik på **OK**.
30. Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber** i træet.
31. Klik på **Tilføj streng**.
32. Klik på **OK**.
33. Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\Valuta** i træet.
34. Klik på **Tilføj streng**.
35. Klik på **OK**.
36. Vælg **Xml\Meddelelse\Betalinger\Vare\Beskrivelse** i træet.
37. Klik på **Tilføj streng**.
38. Klik på **OK**.
39. Vælg **Xml\Meddelelse\Betalinger\Vare\Beløb** i træet.
40. Klik på **Tilføj streng**.
41. Klik på **OK**.
42. Klik på **Gem**.
43. Luk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
