---
title: Tilknyt ER-komponenter i det oprettede format til datamodelelementer (november 2016)
description: Følgende procedure viser, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan knytte datamodelelementer til komponenter i den oprettede ER-konfiguration (elektroniske rapportering), der definerer et elektronisk dokumentformat for betalingsvirksomhedens domæne.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e77de79113e3f44da1d7f92f17a446df86f6852e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143024"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>Tilknyt ER-komponenter i det oprettede format til datamodelelementer (november 2016)

[!include [banner](../../includes/banner.md)]

Følgende procedure viser, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan knytte datamodelelementer til komponenter i den oprettede ER-konfiguration (elektroniske rapportering), der definerer et elektronisk dokumentformat for betalingsvirksomhedens domæne. Dette format bruges senere til at generere elektroniske dokumenter til behandling af betalinger. I dette eksempel skal du oprette en formatkonfiguration til eksempelfirmaet 'Litware Inc.'. Disse trin kan udføres i alle firmaer, da ER-konfigurationer deles mellem alle firmaer. For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "Opret en formatkonfiguration".


## <a name="select-a-format-configuration"></a>Vælg en formatkonfiguration
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Udvid 'Betalinger (forenklet model)' i træet.
4. Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.
5. Klik på Designer.

## <a name="map-format-components-to-data-model-elements"></a>Tilknyt formatkomponenter til datamodelelementer
1. Klik på Udvid/skjul.
2. Klik på fanen Tilknytning.
3. Udvid 'model' i træet.
4. Vælg "Xml\Meddelelse\ProcessingDate\DateTime" i træet.
5. Vælg "model\ProcessingDateTime" i træet.
6. Klik på Bind.
7. Vælg "Xml\Meddelelse\MessageId\Streng" i træet.
8. Vælg "model\MessageIdentification" i træet.
9. Klik på Bind.
10. Udvid 'model\Betalinger' i træet.
11. Vælg "Xml\Meddelelse\Betalinger\Vare\Beløb\Streng" i træet.
12. Vælg "model\Betalinger\InstructedAmount" i træet.
13. Klik på Bind.
14. Vælg "Xml\Meddelelse\Betalinger\TransDate\DateTime" i træet.
15. Vælg "model\Betalinger\TransactionDate" i træet.
16. Klik på Bind.
17. Vælg "Xml\Meddelelse\Betalinger\Vare\Beskrivelse\Streng" i træet.
18. Vælg "model\Betalinger\Beskrivelse" i træet.
19. Klik på Bind.
20. Vælg "Xml\Meddelelse\Betalinger\Vare\Valuta\Streng" i træet.
21. Vælg 'model\Betalinger\Valuta' i træet.
22. Klik på Bind.
23. Vælg "Xml\Meddelelse\Betalinger\Vare\Id" i træet.
24. Vælg "model\Betalinger\End2EndID" i træet.
25. Klik på Bind.
26. Udvid "model\Betalinger\Kreditor" i træet.
27. Udvid 'model\Betalinger\Kreditor\Konto' i træet.
28. Udvid "model\Betalinger\Kreditor\Speditør" i træet.
29. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn\Streng" i træet.
30. Vælg "model\Betalinger\Kreditor\Navn" i træet.
31. Klik på Bind.
32. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\RoutingNumber\Streng" i træet.
33. Vælg "model\Betalinger\Kreditor\Agent\RoutingNumber" i træet.
34. Klik på Bind.
35. Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\AccountNumber\Streng" i træet.
36. Vælg "model\Betalinger\Kreditor\Konto\Nummer" i træet.
37. Klik på Bind.
38. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Navn\Streng" i træet.
39. Udvid "model\Betalinger\Debitor" i træet.
40. Udvid 'model\Betalinger\Debitor\Konto' i træet.
41. Udvid "model\Betalinger\Debitor\Speditør" i træet.
42. Vælg "model\Betalinger\Debitor\Navn" i træet.
43. Klik på Bind.
44. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber\Streng" i træet.
45. Vælg "model\Betalinger\Kreditor\Agent\RoutingNumber" i træet.
46. Klik på Bind.
47. Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber\Streng" i træet.
48. Vælg "model\Betalinger\Debitor\Konto\Nummer" i træet.
49. Klik på Bind.
50. Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.
51. Vælg "model\Betalinger" i træet.
52. Klik på Bind.
53. Klik på Gem.

## <a name="validate-format-mapping"></a>Valider formattilknytning
1. Klik på Valider.
    * Valider den nye tilknytning for at sikre, at alle bindinger er i orden.  
2. Luk siden.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Ændr status for den aktuelle version af formatkonfiguration
I de næste trin skal du ændre status for formatkonfigurationen fra Udkast til Fuldført for at gøre den tilgængelig for generering af betalingsdokumenter.  
1. Klik på Skift status.
2. Klik på Fuldført.
3. Skriv en værdi i feltet Beskrivelse.
    * For eksempel "version 1".  
4. Klik på OK.
5. Vælg den færdige version af den aktuelle konfiguration.
    * Bemærk, at konfigurationen gemmes som fuldført version 1.1: Dette er version 1 af det format, der er baseret på version 1 af datamodellen.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Definer ikrafttrædelsesdatoen for færdig version af format
Hver formatversion kan konfigureres som tilgængelig for brug fra en bestemt dato. Når der er mere end én formatversion aktiv på en bestemt dato, vælges det nyeste format (baseret på versionsnummer) til anvendelse. Sessionens datoværdi bruges til valg af korrekt version.  

## <a name="restrict-access-to-created-format-from-companies"></a>Begræns adgang til oprettet format fra firmaer
1. Udvid sektionen ISO-land/områdekoder.
    * Hver formatadgang kan begrænses ved at identificere bestemte lande/områder, hvori et format er gældende. Hvis listen over lande/områder for det pågældende format er tom, kan dette format bruges i ethvert firma. Når der indsættes nogle ISO-lande/-områdekoder på denne liste over lande/områder, kan dette format kun bruges i firmaer, hvis den primære adresse er i landet/området.  

