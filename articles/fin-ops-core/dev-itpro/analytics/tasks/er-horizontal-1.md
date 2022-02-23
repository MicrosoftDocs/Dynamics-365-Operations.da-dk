---
title: 'ER Bruge vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk (del 1: Designformat)'
description: Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e36a2238ab4c67a2384d6da2a1e2c767414c21a1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684493"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Bruge vandrette områder, der kan udvides, til at tilføje kolonner i Excel-rapporter dynamisk (del 1: Designformat)

[!include [banner](../../includes/banner.md)]

Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret. Disse trin kan udføres i en hvilken som helst virksomhed.

Du skal først udføre disse tre opgaveguider for at fuldføre disse trin: 

"ER Oprette en konfigurationsudbyder og markere den som aktiv"

"ER Bruge økonomiske dimensioner som en datakilde (Del 1: Design datamodel)"

"ER Bruge økonomiske dimensioner som en datakilde (Del 2: Modeltilknytning)"

Du skal også hente og gemme en lokal kopi af skabelonen med et rapporteksempel, du finder her: [Eksempel på økonomisk dimensions webtjenesterapport](https://go.microsoft.com/fwlink/?linkid=862266).

Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-a-new-report-configuration"></a>Opret en ny rapportkonfiguration
1. Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.
2. Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.
3. Klik på Opret konfiguration for at åbne dialogboksen.
4. Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.
    * Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.  
5. Skriv 'Eksempel på rapport med vandret områder, der kan udvides' i feltet Navn.
    * Eksempel på rapport med vandret områder, der kan udvides  
6. Skriv 'Sådan opretter du Excel-output med dynamisk tilføjelse af kolonner' i feltet Beskrivelse.
    * Sådan opretter du Excel-output med dynamisk tilføjelse af kolonner  
7. Vælg Post i feltet Definition.
8. Klik på Opret konfiguration.

## <a name="design-the-report-format"></a>Design rapportformatet
1. Klik på Designer.
2. Slå til/fra-knappen 'Vis detaljer' til.
3. Klik på Importér i handlingsruden.
4. Klik på Importér fra Excel.
5. Klik på Vedhæftede filer.
    * Importer rapportskabelonen. Brug den Excel-fil, du har downloadet til det.  
6. Klik på Ny.
7. Klik på Filer.
8. Luk siden.
9. Indtast eller vælg en værdi i feltet Skabelon.
    * Vælg den downloadede skabelon.  
10. Klik på OK.
    * Tilføj et nyt område for at oprette Excel-output dynamisk med så mange kolonner, som du har valgt (i formen for brugerdialogboksen) for økonomiske dimensioner. Hver celle for hver kolonne repræsenterer navnet på en enkelt økonomisk dimension.  
11. Klik på Tilføj for at åbne dialogboksen.
12. Vælg "Excel\Range" i træet.
13. Skriv 'DimNames' i feltet Excel-interval.
    * DimNames  
14. Vælg 'Vandret' i feltet Replikeringsretning.
15. Klik på OK.
16. Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.
17. Klik på Flyt op.
18. Vælg 'Excel = "SampleFinDimWsReport"\Cell<DimNames>' i træet.
19. Klik på Klip.
20. Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.
21. Klik på Sæt ind.
22. Udvid 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.
23. Udvid 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical' i træet.
24. Udvid 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical' i træet.
25. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical' i træet.
    * Tilføj et nyt område for at oprette Excel-output dynamisk med så mange kolonner, som du har valgt (i formen for brugerdialogboksen) for økonomiske dimensioner. Hver celle for hver kolonne repræsenterer en enkelt økonomisk dimensions værdi for de enkelte rapporteringstransaktioner.  
26. Klik på Tilføj et interval.
27. Skriv 'DimValues' i feltet Excel-interval.
    * DimValues  
28. Vælg 'Vandret' i feltet Replikeringsretning.
29. Klik på OK.
30. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>' i træet.
31. Klik på Klip.
32. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' i træet.
33. Klik på Sæt ind.
34. Udvid 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' i træet.

## <a name="map-format-elements-to-data-sources"></a>Knyt formatelementer til datakilder
1. Klik på fanen Tilknytning.
2. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.
3. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.
4. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.
5. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.
6. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>' i træet.
7. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.
8. Klik på Bind.
9. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' i træet.
10. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.
11. Klik på Bind.
12. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>' i træet.
13. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.
14. Klik på Bind.
15. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>' i træet.
16. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.
17. Klik på Bind.
18. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>' i træet.
19. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.
20. Klik på Bind.
21. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>' i træet.
22. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.
23. Klik på Bind.
24. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>' i træet.
25. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.
26. Klik på Bind.
27. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>' i træet.
28. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.
29. Klik på Bind.
30. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical' i træet.
31. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.
32. Klik på Bind.
33. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>' i træet.
34. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.
35. Klik på Bind.
36. Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical' i træet.
37. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.
38. Klik på Bind.
39. Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Dimensionsindstilling: Postliste' i træet.
40. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Dimensionsindstilling: Postliste\Kode: Streng' i træet.
41. Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>' i træet.
42. Klik på Bind.
43. Vælg 'model: Data Eksempelmodel for datamodellen Økonomiske dimensioner\Dimensionsindstilling: Postliste' i træet.
44. Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.
45. Klik på Bind.
46. Vælg 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>' i træet.
47. Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.
48. Klik på Bind.
49. Klik på Gem.
50. Luk siden.

