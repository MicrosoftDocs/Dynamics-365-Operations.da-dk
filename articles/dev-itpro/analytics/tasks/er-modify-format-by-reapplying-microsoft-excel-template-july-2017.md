---
title: Ændre formater ved at genanvende Excel-skabeloner
description: For at fuldføre trinene i denne procedure skal du først fuldføre proceduren Designe en ER-konfiguration til generering af rapporter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551155"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Ændre formater ved at genanvende Excel-skabeloner

[!include [task guide banner](../../includes/task-guide-banner.md)]

For at fuldføre trinene i denne procedure skal du først fuldføre proceduren Designe en ER-konfiguration til generering af rapporter i OPENXML-format.

Denne procedure beskriver, hvordan du ændrer en konfiguration af et elektronisk rapporteringsformat (ER) ved at anvende en Microsoft Excel-skabelon, der er blevet ændret, igen. I denne procedure skal du importere en ændret Excel-skabelon til ER-formatkonfigurationer, der er oprettet til eksempelfirmaet Litware, Inc., og derefter generere elektroniske dokumenter. Denne procedure er beregnet til brugere, der har rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af GBSI-datasættet. Før du begynder, skal du hente og gemme filen SampleVendPaymWsReport2.xlsx, som er anført i Hjælp-emnet Rediger et elektronisk rapporteringsformat ved at genanvende en Microsoft Excel-skabelon (modify-electronic-reporting-format-reapply-excel-template/).

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren Opret en konfigurationsudbyder, og markér den som aktiv.  

## <a name="select-the-er-format"></a>Vælg ER-formatet
1. Klik på Rapporteringskonfigurationer.
2. Udvid "Betalingsmodel" i træet.
3. Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.
4. Klik på Vedhæftede filer.
    * Bemærk, at Excel-filen SampleVendPaymWsReport.xlsx i øjeblikket bruges som skabelon ved behandling af betalingskladden.   
5. Klik på Åbn.
    * Klik på Åbn for at udforske layoutet for Excel-skabelonen.  
    * Gennemse af skabelonen. Bemærk, at den aktuelt indeholder følgende oplysninger for hver betalingslinje: kreditorkontonummer, kreditornavnet, bank, registreringsnummer, kontonummer, debet, kredit og valuta. I dette eksempel skal vil vi udvide denne liste ved at tilføje detaljer om betalingsdatoen.   
6. Luk siden.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Genanvend en ny Excel-skabelon på ER-format
1. Klik på Designer.
    * Åbn kladdeversionen af det valgte ER-format til redigering.  
2. Klik på Importér i handlingsruden.
3. Klik på Opdater fra Excel.
    * Klik på 'Opdater skabelon', og vælg derefter filen SampleVendPaymWsReport2.xlsx.  
    * Klik på Opdater skabelon, og gennemse for at finde den SampleVendPaymWsReport2.xlsx-fil, du hentede tidligere.  
4. Klik på OK.
    * Skabelonen SampleVendPaymWsReport2.xlsx anvendes. Strukturen af ER-formatet synkroniseres med indholdet af skabelonen, hvis elementer føjes til ER-formatet. Eventuelle eksisterende elementer i ER-formatet, der ikke findes i skabelonen, fjernes fra formatdefinitionen.  
5. Vælg Excel i træet.
    * Bemærk, at feltet Skabelon nu indeholder en reference til den nye skabelon.   
6. Klik på Vedhæftede filer.
7. Klik på Åbn.
    * Klik på Åbn for at udforske layoutet for den ændrede Excel-skabelon.  
    * Gennemse af skabelonen. Bemærk, at det nu indeholder en linje til betalingsdatoen.   
8. Luk siden.
9. Udvid Excel i træet.
10. Udvid "Excel\PaymLines" i træet.
11. Vælg 'Excel\PaymLines\PaymDate' i træet.
    * Bemærk, at ER-formatet nu indeholder et element yderligere. En celle, PaymDate, er blevet føjet til Excel-skabelonen.  
12. Klik på fanen Tilknytning.
13. Udvid 'model' i træet.
14. Udvid 'model\Betalinger' i træet.
15. Vælg "model\Betalinger\Transaktionsdato(TransactionDate)" i træet.
16. Klik på Bind.
    * Angiv, hvilke data der skal føjes til den nye celle under kørslen.  
17. Klik på Gem.
18. Luk siden.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Aktivere den ændrede kladdeversion af ER-formatet til brug i behandling af betalingskladde
1. Klik på Konfigurationer i handlingsruden.
2. Klik på Brugerparametre.
3. Vælg Ja i feltet Indstillinger for kørsel.
4. Klik på OK.
5. Klik på Rediger.
6. Vælg Ja i feltet Udkast til kørsel.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Bruge den ændrede kladdeversion af ER-formatet i behandling af betalingskladde
    * Gennemse det oprettede regneark, inklusive nye betalingslinjeoplysninger – betalingsdato.  

