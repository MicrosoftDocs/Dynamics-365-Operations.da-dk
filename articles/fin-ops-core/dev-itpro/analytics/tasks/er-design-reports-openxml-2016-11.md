---
title: Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)
description: Denne artikel beskriver, hvordan du opretter en ny konfiguration af elektronisk rapportering, der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b2325a5389e0bfe1efff17e5cd117ad8dbcd65d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908407"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format. Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.

I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.

Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin. Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen. Denne fil kan åbnes fra [Skabelon for betalingsrapport](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).


## <a name="upload-the-payments-data-model-configuration"></a>Overføre konfiguration for betalingsdatamodel
1. Gå i navigationsruden til **Moduler > Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.
2. Markér konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. på listen. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren [Oprette konfigurationsudbydere og markere dem som aktiv](er-configuration-provider-mark-it-active-2016-11.md).
3. Vælg **Angiv aktive**.
4. Vælg **Lagre**. Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt. Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.  
5. Vælg **Tilføj** for at åbne dialogboksen.
6. Skriv `Operations resourcesdd` i feltet **Konfigurationslagertype**.
7. Vælg **Opret lager**.
8. Vælg **OK**.
9. Vælg **Åbn**.
10. Vælg **Betalingsmodel** i træet.
11. Vælg **Importér**. Importér denne datamodel. Den bruges som en datakilde i en ny formatkonfiguration. Spring dette trin over, hvis denne konfiguration allerede er importeret.  
12. Vælg **Ja**.
13. Luk siderne, indtil du vender tilbage til den elektroniske rapporteringsside.

## <a name="create-a-new-format-configuration"></a>Opret en ny formatkonfiguration
1. Vælg **Rapporteringskonfigurationer**.
2. Vælg **Betalingsmodel** i træet.
3. Vælg **Opret konfiguration** for at åbne dialogboksen.
4. Angiv `Format based on data model PaymentModel` i feltet **Ny**. Opret et format, der er baseret på PaymentModel-datamodellen.
5. Skriv `Sample worksheet report` i feltet **Navn**. Eksempel på regnearksrapport  
6. Skriv `Sample worksheet report for vendors' payments` i feltet **Beskrivelse**. Eksempel på regnearksrapport for kreditorers betalinger.  
7. Indtast eller vælg en værdi i feltet **Definition af datamodel**. Vælg definitionen **CustomerCreditTransferInitiation**.  
8. Vælg **Opret konfiguration**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Designe et nyt dokument i OPENXML-regnearksformat
1. Vælg **Betalingsmodel\Eksempel på regnearksrapport** i træet.
2. Vælg **Designer**.
3. Vælg **Importér** i handlingsruden.
4. Vælg **Importér fra Excel**.
5. Vælg **Vedhæftede filer**. Vedhæft det eksisterende Excel-dokument som en skabelon.  
6. Vælg **Ny**.
7. Vælg **Fil**. Peg på den eksisterende Excel-fil.  
8. Luk siden.
9. Indtast eller vælg en værdi i feltet **Skabelon**. Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.  
10. Vælg **OK**. Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Oprette en ny datakilde for at beregne totaler efter valutakoder
1. Vælg fanen **Tilknytning**.
2. Vælg **Tilføj rod** for at åbne dialogboksen.
3. Vælg **Funktioner\Gruppér efter** i træet.
4. Skriv `PaymentByCurrency` i feltet **Navn**.
5. Vælg **Rediger gruppe efter**.
6. Udvid **model** i træet, og vælg derefter **model\Betalinger**.
7. Vælg **Føj felt til**.
8. Vælg **Hvad skal grupperes**.
9. Udvid **model\Betalinger** i træet, og vælg derefter **model\Betalinger\Valuta**.
10. Vælg **Føj felt til**.
11. Vælg **Grupperede felter**.
12. Vælg **model\Betalinger\Instrueret beløb(InstructedAmount)** i træet.
13. Vælg **Føj felt til**, og vælg derefter **Aggregeringsfelter**.
14. Vælg en indstilling i feltet **Metode**. Vælg aggregeringsfunktionen **SUM**.  
15. Skriv `TotalInstructuredAmount` i feltet **Navn**.
16. Vælg **Gem**.
17. Luk siden.
18. Vælg **OK**.

## <a name="map-format-components-to-data-sources"></a>Knytte formatkomponenter til datakilder
1. Vælg **model\Betalinger\Initierende part(InitiatingParty)\Navn** og **Excel\ReportHeader\CompanyName** i træet.
2. Vælg **Bind**.
3. Vælg **model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)** og **Excel\PaymLines\VendAccountName** i træet.
4. Vælg **Bind**.
5. Vælg **model\Betalinger\Kreditor\Navn** og **Excel\PaymLines\VendName** i træet.
6. Vælg **Bind**.
7. Vælg **model\Betalinger\Kreditagent(CreditorAgent)\Navn** og **Excel\PaymLines\Bank** i træet.
8. Vælg **Bind**.
9. Vælg **model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)** og **Excel\PaymLines\RoutingNumber** i træet.
10. Vælg **Bind**.
11. Vælg **model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\Nummer** og **Excel\PaymLines\AccountNumber** i træet.
12. Vælg **Bind**.
13. Vælg **model\Betalinger\Instrueret beløb(InstructedAmount)** og **Excel\PaymLines\Debit** i træet.
14. Vælg **Bind**.
15. Vælg **model\Betalinger\Valuta** og **Excel\PaymLines\Currency** i træet.
16. Vælg **Bind**.
17. Vælg **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency** i træet.
18. Vælg **Bind**.
19. Vælg **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount**  i træet.
20. Vælg **Bind**.
21. Vælg **PaymentByCurrency** og **Excel\SummaryLines** i træet.
22. Vælg **Bind**.
23. Vælg **model\Betalinger** og **Excel\PaymLines** i træet.
24. Vælg **Bind**.
25. Vælg **Gem**, og luk derefter siden.

## <a name="use-the-created-configuration-for-payments-processing"></a>Bruge den oprettede konfiguration til behandling af betalinger
1. Vælg **Skift status**.
2. Vælg **Fuldfør**.
3. Vælg **OK**.
4. I navigationsruden skal du gå til **Moduler > Kreditor > Betalingsopsætning > Betalingsmåder**.
5. Brug Quick Filter til at filtrere på feltet **Betalingsmåde** med værdien **Elektronisk**.
6. Vælg **Rediger**.
7. Udvid sektionen **Filformater**.
8. Vælg **Ja** i feltet **Generisk elektronisk rapportering**.
9. Skriv eller vælg en værdi i feltet **Eksportér formatkonfiguration**. Vælg konfigurationen **Eksempel på regnearksrapport**.  
10. Vælg **Gem**.
11. Luk siden.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Bruge den oprettede konfiguration til at teste betalingskladdebehandling
1. Gå i navigationsruden til **Moduler > Kreditorer > Betalinger > Betalingskladde**.
2. Vælg **Ny** for at oprette en ny betalingskladde.
3. Skriv **VendPay** i feltet **Navn**.
4. Vælg **Linjer**.
5. I feltet **Konto** skal du angive værdien `GB_SI_000001`.
6. Angiv **Debet** til `1000`.
7. Vælg **Ny**.
8. I feltet **Konto** skal du angive værdien `GB_SI_000005`.
9. Angiv **Debet** til `2000`.
10. Skriv `EUR` i feltet **Valuta**.
11. I feltet **Modkonto** skal du angive værdien `GBSI OPER`.
12. Skriv `Electronic` i feltet **Betalingsmåde**.
13. Vælg **Gem**.
14. Vælg **Opret betalinger**.
15. Skriv `Electronic` i feltet **Betalingsmåde**.
16. Skriv `Payments` i feltet **Filnavn**.
17. Skriv `GBSI OPER` i feltet **Bankkonto**.
18. Vælg **OK**, og vælg derefter **OK** igen. Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
