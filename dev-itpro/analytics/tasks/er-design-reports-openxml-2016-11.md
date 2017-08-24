--- 
title: Designe en konfiguration til generering af rapporter i OpenXML-format til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d552dbcf932813de4d060b4f2190cf388eddb1bf
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Designe en konfiguration til generering af rapporter i OpenXML-format til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format. Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.



I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.



Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin. Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen. Denne fil kan åbnes fra: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx


## <a name="upload-the-payments-data-model-configuration"></a>Overføre konfiguration for betalingsdatamodel
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
2. Markér den valgte række på listen.
    * Vælg konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".  
3. Klik på Angiv som aktiv.
4. Klik på Lagre.
    * Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt. Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.  
5. Klik på Tilføj for at åbne dialogboksen.
6. Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.
7. Klik på Opretlager.
8. Klik på OK.
9. Klik på Åbn.
10. Vælg 'Betalingsmodel' i træet.
11. Klik på Importer.
    * Importér denne datamodel. Den bruges som en datakilde i en ny formatkonfiguration. Spring dette trin over, hvis denne konfiguration allerede er importeret.  
12. Klik på Ja.
13. Luk siden.
14. Luk siden.

## <a name="create-a-new-format-configuration"></a>Opret en ny formatkonfiguration
1. Klik på Rapporteringskonfigurationer.
2. Vælg 'Betalingsmodel' i træet.
3. Klik på Opret konfiguration for at åbne dialogboksen.
4. Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.
    * Opret et format, der er baseret på PaymentModel-datamodellen.  
5. Skriv 'Eksempel på regnearksrapport' i feltet Navn.
    * Eksempel på regnearksrapport  
6. Skriv 'Eksempel på regnearksrapport for kreditorers betalinger' i feltet Beskrivelse.
    * Eksempel på regnearksrapport for kreditorers betalinger  
7. Indtast eller vælg en værdi i feltet Definition af datamodel.
    * Vælg 'CustomerCreditTransferInitiation'-definitionen.  
8. Klik på Opret konfiguration.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Designe et nyt dokument i OPENXML-regnearksformat
1. Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.
2. Klik på Designer.
3. Klik på Importér i handlingsruden.
4. Klik på Importér fra Excel.
5. Klik på Vedhæftede filer.
    * Vedhæft det eksisterende Excel-dokument som en skabelon.  
6. Klik på Ny.
7. Klik på Filer.
    * Peg på den eksisterende Excel-fil.  
8. Luk siden.
9. Indtast eller vælg en værdi i feltet Skabelon.
    * Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.  
10. Klik på OK.
    * Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Oprette en ny datakilde for at beregne totaler efter valutakoder
1. Klik på fanen Tilknytning.
2. Klik på Tilføj rod for at åbne dialogboksen.
3. Vælg 'Funktioner\Gruppér efter' i træet.
4. Skriv 'PaymentByCurrency' i feltet Navn.
    * PaymentByCurrency  
5. Klik på Rediger gruppe efter.
6. Udvid 'model' i træet.
7. Vælg "model\Betalinger" i træet.
8. Klik på Tilføj et felt til.
9. Klik på Hvad skal grupperes.
10. Udvid 'model\Betalinger' i træet.
11. Vælg 'model\Betalinger\Valuta' i træet.
12. Klik på Tilføj et felt til.
13. Klik på Grupperede felter.
14. Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.
15. Klik på Tilføj et felt til.
16. Klik på Aggregeringsfelter.
17. Vælg en indstilling i feltet Metode.
    * Vælg sammenlægningsfunktionen SUM.  
18. Skriv 'TotalInstructuredAmount' i feltet Navn.
    * TotalInstructuredAmount  
19. Klik på Gem.
20. Luk siden.
21. Klik på OK.

## <a name="map-format-components-to-data-sources"></a>Knytte formatkomponenter til datakilder
1. Udvid 'model' i træet.
2. Udvid 'model\Betalinger' i træet.
3. Udvid 'model\Betalinger\Initierende part(InitiatingParty)' i træet.
4. Vælg 'model\Betalinger\Initierende part(InitiatingParty)\Navn' i træet.
5. Udvid "Excel\ReportHeader" i træet.
6. Vælg "Excel\ReportHeader\CompanyName" i træet.
7. Klik på Bind.
8. Udvid "model\Betalinger\Kreditor" i træet.
9. Udvid 'model\Betalinger\Kreditor\Identifikation' i træet.
10. Vælg 'model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)' i træet.
11. Udvid "Excel\PaymLines" i træet.
12. Vælg "Excel\PaymLines\VendAccountName" i træet.
13. Klik på Bind.
14. Vælg "model\Betalinger\Kreditor\Navn" i træet.
15. Vælg "Excel\PaymLines\VendName" i træet.
16. Klik på Bind.
17. Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.
18. Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Navn' i træet.
19. Vælg "Excel\PaymLines\Bank" i træet.
20. Klik på Bind.
21. Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)' i træet.
22. Vælg "Excel\PaymLines\RoutingNumber" i træet.
23. Klik på Bind.
24. Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.
25. Udvid 'model\Payments\Creditor Account(CreditorAccount)\Identification' i træet.
26. Vælg 'model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\IBAN' i træet.
27. Vælg "Excel\PaymLines\AccountNumber" i træet.
28. Klik på Bind.
29. Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.
30. Vælg "Excel\PaymLines\Debit" i træet.
31. Klik på Bind.
32. Udvid "model\Betalinger\Kreditor" i træet.
33. Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.
34. Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.
35. Vælg 'model\Betalinger\Valuta' i træet.
36. Vælg "Excel\PaymLines\Currency" i træet.
37. Klik på Bind.
38. Udvid 'PaymentByCurrency' i træet.
39. Udvid 'PaymentByCurrency\grouped' i træet.
40. Vælg 'PaymentByCurrency\grouped\Valuta' i træet.
41. Udvid "Excel\SummaryLines" i træet.
42. Vælg "Excel\SummaryLines\SummaryCurrency" i træet.
43. Klik på Bind.
44. Udvid 'PaymentByCurrency\aggregated' i træet.
45. Vælg 'PaymentByCurrency\aggregated\TotalInstructuredAmount' i træet.
46. Vælg "Excel\SummaryLines\SummaryAmount" i træet.
47. Klik på Bind.
48. Vælg 'PaymentByCurrency' i træet.
49. Vælg "Excel\SummaryLines" i træet.
50. Klik på Bind.
51. Vælg "model\Betalinger" i træet.
52. Vælg "Excel\PaymLines" i træet.
53. Klik på Bind.
54. Klik på Gem.
55. Luk siden.

## <a name="use-the-created-configuration-for-payments-processing"></a>Bruge den oprettede konfiguration til behandling af betalinger
1. Klik på Skift status.
2. Klik på Fuldført.
3. Klik på OK.
4. Luk siden.
5. Luk siden.
6. Gå til Kreditor > Opsætning af betaling > Betalingsmåder.
7. Brug Quick Filter til at filtrere på feltet Betalingsmåde med værdien "Elektronisk".
    * Elektronisk  
8. Klik på Rediger.
9. Udvid sektionen Filformater.
10. Vælg Ja i feltet Generisk elektronisk indberetning.
11. Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.
    * Vælg konfigurationen 'Eksempel på regnearksrapport'.  
12. Klik på Gem.
13. Luk siden.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Bruge den oprettede konfiguration til at teste betalingskladdebehandling
1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
    * Opret en ny betalingskladde.  
3. Skriv VendPay i feltet Navn.
    * VendPay  
4. Klik på Linjer.
5. I feltet Konto skal du angive værdierne 'GB_SI_000001'.
    * GB_SI_000001  
6. Angiv Debet til '1000'.
7. Klik på Ny.
8. I feltet Konto skal du angive værdierne 'GB_SI_000005'.
    * GB_SI_000005  
9. Angiv Debet til '2000'.
10. Skriv 'EUR' i feltet Valuta.
    * EUR  
11. I feltet Modkonto skal du angive værdierne 'GBSI OPER'.
    * GBSI OPER  
12. Skriv 'Elektronisk' i feltet Betalingsmåde.
    * Elektronisk  
13. Klik på Gem.
14. Klik på Generer betalinger.
15. Skriv 'Elektronisk' i feltet Betalingsmåde.
    * Elektronisk  
16. Skriv "Betalinger" i feltet Filnavn.
    * Skriv f.eks. Betalinger.  
17. Skriv 'GBSI OPER' i feltet Bankkonto.
    * GBSI OPER  
18. Klik på OK.
19. Klik på OK.
    * Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.  


