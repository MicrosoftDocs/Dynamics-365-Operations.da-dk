---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 4: Kørselsformat)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "336192"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a>ER Konfigurere format for at udføre optælling og sammenlægning (del 4: Kørselsformat)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet. Disse trin kan udføres i DEMF-virksomheden.

For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 3: Brug beregninger til at oprette output)".

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Test denne konfiguration til oprettelse af Intrastat-rapporter
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.
3. Udvid 'Intrastat-model' i træet.
4. Udvid 'Intrastat-model\Intrastat (DE)' i træet.
5. Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.
6. Klik på Konfigurationer i handlingsruden.
7. Klik på Brugerparametre.
8. Vælg Ja i feltet Indstillinger for kørsel.
9. Klik på OK.
10. Klik på Rediger.
11. Vælg Ja i feltet Udkast til kørsel.
12. Klik på Gem.
13. Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.
14. Udvid sektionen Elektronisk rapportering.
15. Vælg konfigurationen "Intrastat (DE) med optælling og sammenlægning".
16. Vælg konfigurationen "Intrastat (DE) med optælling og sammenlægning".
17. Klik på Gem.
18. Luk siden.
19. Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.
20. Klik på Output.
21. Klik på Rapport.
    * Kør processen til oprettelse af Intrastat-rapport.  
22. I feltet Fra dato skal du angive datoen til "2000-01-01".
    * Definer start- og slutdatoer for af rapporteringsperioden, som omfatter de eksisterende posteringer i formen.  
23. I feltet Til dato skal du angive datoen til "2022-12-31".
    * Definer start- og slutdatoer for af rapporteringsperioden, som omfatter de eksisterende posteringer i formen.  
24. Vælg 'Indførsel' i feltet Retning.
25. Vælg Ja i feltet Generer fil.
26. Klik på OK.
    * Få vist oprettet output med oversigtslinjer i slutningen.  
27. Klik på Ny.
28. Markér den valgte række på listen.
29. Vælg 'Udførsel' i feltet Retning.
30. Indtast eller vælg en værdi i feltet Varenummer.
31. Indtast eller vælg en værdi i feltet Vare.
32. Angiv Vægt til 10
33. Angiv Fakturabeløb til '10000'.
34. Angiv Statistisk beløb til '10000'.
35. Klik på Output.
36. Klik på Rapport.
37. Vælg 'Udførsel' i feltet Retning.
38. Klik på OK.
    * Få vist oprettet output med oversigtslinjer i slutningen. Bemærk, at det er blevet ændret sammenlignet med den første kørsel.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Kør denne konfiguration i fejlfindingstilstand for at gennemse indsamlede optællings- og sammenlægningsdata
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Udvid 'Intrastat-model' i træet.
3. Udvid 'Intrastat-model\Intrastat (DE)' i træet.
4. Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.
5. Klik på Konfigurationer i handlingsruden.
6. Klik på Brugerparametre.
7. Vælg Ja i feltet Kør i fejlfindingstilstand.
8. Klik på OK.
9. Luk siden.
10. Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.
11. Klik på Output.
12. Klik på Rapport.
13. Klik på OK.
14. Luk siden.
15. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
16. Udvid 'Intrastat-model' i træet.
17. Udvid 'Intrastat-model\Intrastat (DE)' i træet.
18. Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.
19. Klik på Fejlfindingslogfiler.
    * Bemærk, at der er oprettet en fejlfindingslogpost for kørselsprocessen for den valgte konfiguration.  
20. Klik på Vedhæft.
21. Klik på Åbn.
    * Gennemse den XML-fil, der indeholder optællings- og sammenlægningsdetaljer, der er indsamlet under kørsel af den valgte konfiguration.  

