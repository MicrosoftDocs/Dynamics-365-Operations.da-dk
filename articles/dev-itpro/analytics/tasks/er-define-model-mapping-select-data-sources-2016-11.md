---
title: Definere ER-modeltilknytninger og vælge datakilder til dem
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan vælge datakilder til en datamodel for elektronisk rapportering.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5f2f2c699514d723f42f5d1fb25724f46dfc4f4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551385"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>Definere ER-modeltilknytninger og vælge datakilder til dem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan vælge datakilder til en datamodel for elektronisk rapportering (ER). Datakilderne skal være bundet til enkelte komponenter i den valgte datamodel i designfasen og udfylde forretningsoplysninger til denne datamodel på kørselstidspunktet. I dette eksempel skal du vælge datakilder til en eksisterende datamodel, der er oprettet for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Oprette en ny datamodel".


## <a name="open-the-electronic-reporting-configurations-tree"></a>Åbn træet til elektroniske rapporteringskonfigurationer
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Klik på Rapporteringskonfigurationer.

## <a name="insert-a-new-model-mapping"></a>Indsæt en ny modeltilknytning
1. Vælg "Betalinger (forenklet mode)" i træet.
2. Klik på Designer.
3. Klik på Tilknyt model til datakilde.
4. Klik på Ny.
    * Derved oprettes en ny post, der knytter datamodellen til datakilder. I dette eksempel skal du knytte datamodellen til datakilder for den ønskede betalingstype: overførsel.     Det er muligt at udforme mere end én tilknytning til en bestemt datamodel. For eksempel kan du oprette en tilknytning til de forskellige typer betalinger, såsom direkte debitering eller krediteringsoverførsler. I dette eksempel skal du oprette en tilknytning til overførsler.  
5. Skriv CT-tilknytning" i feltet Navn.
    * CT-tilknytning  
6. Skriv "Betalingsmodel tilknytning CT" i feltet Beskrivelse.
    * Betalingsmodel tilknytning CT  
7. Skriv "CustomerCreditTransferInitiation" i feltet Definition.
    * Vælg CustomerCreditTransferInitiation  
8. ResolveChanges definitionen.
9. Klik på Gem.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Definer påkrævede datakilder for den aktuelle modeltilknytning
1. Klik på Designer.
2. Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.
3. Klik på Tilføj rod.
    * Angiv denne datakilde for at få adgang til betalingstransaktioner.  
4. Skriv "Transaktioner" i feltet Navn.
    * Poster  
5. Angiv "Transaktioner" i feltet Etiket.
    * Poster  
6. Angiv "Finansjournallinjer" i feltet Hjælp.
    * Finansjournallinjer  
7. Vælg Ja i feltet Spørg efter forespørgsel.
    * Vælg Ja.  
8. Skriv "LedgerJournalTrans" i feltet Tabel.
    * LedgerJournalTrans  
9. Klik på OK.
    * Vælg LedgerJournalTrans-tabellen som en datakilde for den aktuelle datamodel.  
10. Vælg "Funktioner\Beregnet felt" i træet.
11. Klik på Tilføj.
    * Klik på Tilføj for at tilføje et nyt beregnet felt.  
12. Skriv "$EndToEndID" i feltet Navn.
    * $EndToEndID  
13. Klik på Rediger formel.
14. Vælg '"Streng\SAMMENKÆD" i træet.
15. Klik på Tilføj funktion.
16. Udvid "Transaktioner" i træet.
17. Vælg "Transaktioner\Bilag" i træet.
18. Klik på Tilføj datakilde.
19. Skriv "CONCATENATE(Transaktioner.Bilag, "-", " i feltet Formel.
    * Skriv [, "-",] i slutningen af formlen.  
20. Vælg "Streng\TEKST" i træet.
21. Klik på Tilføj funktion.
22. Vælg "Transaktioner\Post-ID(RecId)' i træet.
23. Klik på Tilføj datakilde.
24. Skriv "CONCATENATE(Transaktioner.Bilag, "-", TEXT(Transaktioner.RecId))" i feltet Formel.
    * Skriv [))] i slutningen af formlen.  
25. Klik på Gem.
    * Sørg for, at ingen fejl er fundet for den formel, der er oprettet. Se fanen FEJL under formelkontrolelementet.  
26. Luk siden.
27. Klik på OK.
    * Føj det beregnede felt til denne datakilde.  
28. Klik på Tilføj.
    * Klik på Tilføj for at tilføje et nyt beregnet felt.  
29. Skriv "$Amount" i feltet Navn.
    * $Amount  
30. Klik på Rediger formel.
31. Udvid "Transaktioner" i træet.
32. Vælg "Transaktioner\Debit(AmountCurDebit)" i træet.
33. Klik på Tilføj datakilde.
34. Skriv "Transaktioner.AmountCurDebit - " i feltet Formel.
    * Skriv [ - ] i slutningen af formlen.  
35. Vælg "Transaktioner\Credit(AmountCurCredit)" i træet.
36. Klik på Tilføj datakilde.
37. Klik på Gem.
38. Luk siden.
39. Klik på OK.
    * Dette føjer det $Amount-beregnede felt til den valgte datakilde for den aktuelle datamodel.  
40. Vælg "Transaktioner\$Amount" i træet.
41. Udvid "Transaktioner" i træet.
42. Udvid eller skjul "Transaktioner\$Amount" i træet.
43. Udvid eller skjul "Transaktioner" i træet.
44. Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.
45. Klik på Tilføj rod.
    * Angiv denne datakilde for at få adgang til oplysninger om firmaets bankkonto.  
46. Skriv "BankAccount" i feltet Navn.
    * BankAccount  
47. Angiv "Bankkonto" i feltet Etiket.
    * Bankkonto  
48. Angiv "Bankkonto" i feltet Hjælp.
    * Bankkonto  
49. Vælg Ja i feltet Spørg efter forespørgsel.
    * Vælg Ja.  
50. Skriv "BankAccountTable" i feltet Tabel.
    * BankAccountTable  
51. Klik på OK.
    * Vælg BankAccountTable-tabellen som en datakilde for den aktuelle datamodel.  
52. Klik på Tilføj rod.
    * Angiv denne datakilde for at få adgang til oplysninger om firmaets forudsætninger.  
53. Skriv "Firma" feltet Navn.
    * Regnskab  
54. Skriv en værdi i feltet Etiket.
    * Firmaoplysninger  
55. Skriv "Firmaoplysninger" i feltet Hjælp.
    * Firmaoplysninger  
56. Vælg Ja i feltet Spørg efter forespørgsel.
    * Vælg Ja.  
57. Skriv "CompanyInfo" i feltet Tabel.
    * CompanyInfo  
58. Klik på OK.
    * Vælg CompanyInfo-tabellen som en datakilde for den aktuelle datamodel.  
59. Vælg "Funktioner\Beregnet felt" i træet.
60. Klik på Tilføj rod.
    * Indsæt et beregnet felt som en ny datakilde.  
61. Skriv "ProcessingDateTime" i feltet Navn.
    * ProcessingDateTime  
62. Skriv "Afviklingsdato og -klokkeslæt" i feltet Etiket.
    * Behandlingsdato og -klokkeslæt  
63. Klik på Rediger formel.
64. Vælg "Dato/klokkeslæt\SESSIONNOW".
65. Klik på Tilføj funktion.
66. Klik på Gem.
67. Luk siden.
68. Klik på OK.
    * Føj det ProcessingDateTime-beregnede som en datakilde til den aktuelle datamodel.  
69. Klik på Gem.
70. Luk siden.
71. Luk siden.
72. Luk siden.

