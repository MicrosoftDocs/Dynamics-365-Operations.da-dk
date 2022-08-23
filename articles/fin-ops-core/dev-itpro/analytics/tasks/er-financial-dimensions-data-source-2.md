---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 2: Modeltilknytning)'
description: Denne artikel beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 2)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 0d2daedd38c93ff17ef39780140c9c28ece82736
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290808"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>ER Bruge økonomiske dimensioner som en datakilde (del 2: Modeltilknytning)

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter. Disse trin kan udføres i en hvilken som helst virksomhed.

For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 1: Design datamodel)".


## <a name="add-required-data-sources-to-model-mapping"></a>Føj nødvendige datakilder til modeltilknytning
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.
3. Klik på Designer.
4. Klik på Tilknyt model til datakilde.
5. Klik på Ny.
6. Vælg Post i feltet Definition.
7. Skriv 'Datatilknytning for dimensioner' i feltet Navn.
8. Skriv 'Datatilknytning for dimensioner' i feltet Beskrivelse.
9. Klik på Gem.
10. Klik på Designer.
11. Vælg 'Dynamics 365 for Operations\Tabel' i træet.
12. Klik på Tilføj rod.
13. Skriv "Firma" feltet Navn.
14. Skriv "CompanyInfo" i feltet Tabel.
15. Klik på OK.
16. Vælg 'Funktioner\Oplysninger om økonomiske dimensioner'.
17. Klik på Tilføj rod.
    * Denne datakilde angiver, hvordan omfanget af økonomiske dimensioner defineres for en rapport, der bruger denne model som datakilde.  
18. Skriv en værdi i feltet Navn.
19. Vælg Ja i feltet Spørg efter dimensioner.
    * Vælg Ja for at tillade brugeren at vælge dimensioner på kørselstidspunktet i formen Brugerdialogboks. Hvis indstillingen er angivet til Nej, bruges alle økonomiske dimensioner for den aktuelle forekomst som standard.  
20. Vælg 'Juridisk enhed' i feltet Valg af økonomiske dimensioner.
    * Vælg Alle for at tillade brugeren at vælge de ønskede dimensioner for den aktuelle forekomst i opslagsfeltet.  Vælg Juridisk enhed for at tillade brugeren at vælge dimensioner for firmaet i opslagsfeltet.  Vælg Dimension for at tillade brugeren at vælge dimensioner ved hjælp af et enkelt dimensionssæt.  
21. Vælg Ja i feltet Spørg efter hovedkonto.
    * Angiv 'Spørg efter hovedkonto' til Ja for at tillade brugere at vælge hovedkontoen som en del af listen over dimensioner.   Hvis indstillingen er angivet til Nej, inkluderes den primære konto ikke på listen over dimensioner, og indstillingen 'Er hovedkonto obligatorisk' er aktiveret. Hvis "Er hovedkonto obligatorisk" er angivet til Ja, skal du inkludere hovedkontoen på listen over dimensioner, uanset brugerens valg.  
22. Klik på OK.
![Detaljerne for egenskaberne for datakilden for økonomiske dimensioner-slide-out.](../media/er-financial-dimensions-guides-model-mapping1.png)
23. Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.
24. Klik på Tilføj rod.
25. Skriv "LedgerJournal" i feltet Navn.
26. Vælg Ja i feltet Spørg efter forespørgsel.
27. Skriv "LedgerJournalTable" i feltet Tabel.
28. Klik på OK.
![Model til tilknytningsdesigner, tabelposters datakildetype.](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>Tilknyt datamodelelementer til tilføjede datakilder
1. Udvid 'Kladde' i træet.
2. Udvid 'Kladde\Transaktion' i træet.
3. Udvid 'Kladde\Transaktion\Dimensionsdata' i træet.
4. Udvid eller skjul 'Dimensionsindstilling' i træet.
5. Udvid eller skjul 'LedgerJournal' i træet.
6. Udvid 'LedgerJournal\<Relations' i træet.
7. Udvid 'LedgerJournal\<Relations\LedgerJournalTrans' i træet.
8. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher' i træet.
9. Vælg 'Journal\Transaction\Voucher' i træet.
10. Klik på Bind.
11. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' i træet.
    * Bemærk, at for en hvilken som helst henvisning til økonomiske dimensioner, der f.eks. er angivet til LedgerDimension, er et tilsvarende datakildeelement tilgængeligt (LedgerDimension.Dimension). Dette datakildeelement indeholder de økonomiske dimensioner for de dimensioner, der er angivet som postens liste.  
12. Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' i træet.
13. Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner' i træet.
14. Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi' i træet.
15. Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Definition' i træet.
16. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Definition\Navn' i træet.
17. Vælg 'Kladde\Transaktion\Dimensionsdata\Navn' i træet.
18. Klik på Bind.
19. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi\Beskrivelse' i træet.
20. Vælg 'Kladde\Transaktion\Dimensionsdata\Beskrivelse' i træet.
21. Klik på Bind.
22. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi\Kode' i træet.
23. Vælg 'Kladde\Transaktion\Dimensionsdata\Kode' i træet.
24. Klik på Bind.
25. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner' i træet.
26. Vælg 'Kladde\Transaktion\Dimensionsdata' i træet.
27. Klik på Bind.
!Siden Modeltilknytningsdesigner, fanen Tilknytning, træet Datakilder.](../media/er-financial-dimensions-guides-model-mapping3.png)
28. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)' i træet.
29. Vælg 'Journal\Transaction\Debit' i træet.
30. Klik på Bind.
31. Vælg 'LedgerJournal\\<Relations\LedgerJournalTrans\Date(TransDate)' i træet.
32. Vælg 'Journal\Transaction\Date' i træet.
33. Klik på Bind.
34. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)' i træet.
35. Vælg 'Journal\Transaction\Currency' i træet.
36. Klik på Bind.
37. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)' i træet.
38. Vælg 'Journal\Transaction\Credit' i træet.
39. Klik på Bind.
40. Vælg 'LedgerJournal\<Relations\LedgerJournalTrans' i træet.
41. Vælg 'Journal\Transaction' i træet.
42. Klik på Bind.
43. Vælg "LedgerJournal\Journalbatchnummer(JournalNum)" i træet.
44. Vælg 'Journal\Batch' i træet.
45. Klik på Bind.
46. Vælg 'LedgerJournal' i træet.
47. Vælg 'Journal' i træet.
48. Klik på Bind.
49. Udvid 'Dimensions' i træet.
50. Udvid 'Dimensions\Hovedkonto og dimensioner' i træet.
51. Udvid 'Dimensions\Hovedkonto og dimensioner\Definition' i træet.
52. Vælg 'Dimensions\Hovedkonto og dimensioner\Definition\Navn' i træet.
53. Vælg 'Dimensionsindstilling\Kode' i træet.
54. Klik på Bind.
55. Vælg 'Dimensions\Hovedkonto og dimensioner\Definition\Navn på rapportkolonne' i træet.
56. Vælg 'Dimensionsindstilling\Navn' i træet.
57. Klik på Bind.
58. Vælg 'Dimensions\Hovedkonto og dimensioner' i træet.
59. Vælg 'Dimensionsindstilling' i træet.
60. Klik på Bind.
61. Vælg "Firma" i træet.
62. Klik på Rediger.
63. I feltet expressionAsStringText skal du skrive 'Company.'find()'.'name()''.
    * Company.'find()'.'name()'  
64. Klik på Gem.
![Side for ER-modeltilknytningsdesigner.](../media/er-financial-dimensions-guides-model-mapping4.png)
65. Luk siden.
66. Klik på Gem.
67. Luk siden.

## <a name="complete-this-draft-models-version"></a>Fuldfør denne version af kladdemodellen
1. Luk siden.
2. Luk siden.
3. Klik på Skift status.
4. Klik på Fuldført.
5. Klik på OK.
![Siden ER-konfigurationer.](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
