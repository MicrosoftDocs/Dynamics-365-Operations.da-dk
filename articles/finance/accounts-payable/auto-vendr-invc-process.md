---
title: Oversigt over automatiske processer for kreditorfakturering
description: Denne artikel beskriver muligheden for at automatisere behandlingen af kreditorfakturaer og fordelene ved at bruge en automatiseret proces.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d2c629ed2d064a3350ec8ffe53940098d12ab0b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883439"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Oversigt over automatiske processer for kreditorfakturering

[!include [banner](../includes/banner.md)]

Denne artikel beskriver muligheden for at automatisere behandlingen af kreditorfakturaer og fordelene ved at bruge en automatiseret proces. Denne egenskab består af funktioner, der aktiveres i funktionsstyring. Disse funktioner gælder kun for kreditorfakturaer, ikke for fakturaer, der behandles ved hjælp af siden **Fakturajournal** eller **Indgangsbogskladde**.

I mange tilfælde samarbejder organisationer med tredjepart om behandlingen af papirfakturaer via en udbyder af optisk tegngenkendelse (OCR). Tjenesteudbyderen returnerer maskinlæsbare fakturametadata. For at hjælpe med automatisering kan du bruge funktionerne til automatisering af kreditorer til at forbruger disse artefakter fra kreditor.

Du kan automatisere nogle kreditorfaktureringsprocesser. Disse processer omfatter afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer. Den automatiserede proces viser statusoplysninger om en kreditorfaktura, når den bevæger sig gennem hver af processerne. Denne mulighed kan hjælpe kreditormedarbejderne og lederne med at behandle kreditorfakturaer mere effektivt. Det hjælper også med at reducere fejl og ineffektivhed, der kan forekomme, når oplysningerne angives og behandles manuelt.

Automatiseringsprocesserne kan bruges til at udføre disse opgaver:

- Anvende forudbetalinger automatisk for kreditorfakturaer
- Automatisk sende importerede fakturaer til arbejdsprocessystemet.
- Afstemme produktkvitteringer med ventende kreditorfakturalinjer.
- Simulere bogføring, før en kreditorfaktura bogføres.
- Få vist arbejdsgang- og automatiseringshistorikken og hurtigt og effektivt.
- Se og analysere resultaterne af at automatisere behandlingen af kreditorfakturaer.
- Genoptag automatisk behandling for flere fakturaer.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Overfør importerede fakturaer til arbejdsprocessystemet

Som del af en berøringsfri kreditorfaktureringsproces kan der automatisk sendes en importeret faktura til arbejdsprocessystemet. Processen kører i baggrunden, med en hyppighed, du angiver (enten hver time eller dagligt). Muligheden for automatisk afsendelse af importerede fakturaer til arbejdsgangssystemet kræver, at processen starter med en importeret faktura. Hvis du vil sikre, at fakturaen kan behandles fra start til slut uden manuel indgriben, skal du medtage en automatisk bogføringsopgave i konfigurationen af arbejdsprocessen.


Fakturaer, der er relateret til indkøbsordrer, og fakturaer, der indeholder en indkøbskategori uden for indkøbsordren og ikke-lagerførte linjer, kan automatisk sendes til arbejdsprocessystemet. De fakturaer, der angives manuelt, og fakturaer, der oprettes ved hjælp af arbejdsområdet **Fakturering af kreditorsamarbejde**, skal sendes manuelt til arbejdsgangssystemet. Behandlingen af programforudbetaling skal udføres manuelt for importerede fakturaer. Du kan anvende forudbetalinger manuelt før eller efter bogføring af den importerede faktura. Du kan anvende forudbetalinger på ikke-bogførte standardfakturaer manuelt ved hjælp af siden **Kreditorfakturaer**. Når den udlignede forudbetaling er bogført, kan den anvendes manuelt på andre fakturaer fra denne kreditor på siden **Kreditorer** (**Kreditor \> Common \> Kreditorer \> Alle kreditorer \> fanen Faktura \> Anvend**).

Automatiseringsfunktionen giver dig en fleksibel ramme med mulighed for at definere firmaspecifikke regler for afsendelse af importerede kreditorfakturaer til arbejdsgangssystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Afstem bogførte produktkvitteringer til fakturalinjer med en trevejs-sammenholdelsespolitik

Bogførte produktkvitteringer kan automatisk afstemmes med fakturalinjer, som en trevejs-sammenholdelsespolitik er defineret for. Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet. I denne proces kan du angive det maksimale antal gange, systemet skal forsøge at afstemme produktkvitteringer med en fakturalinje, før det konkluderer, at processen er mislykket. Processen vil køre i baggrunden, enten hver time eller hver dag. Du kan køre den automatiske sammenholdelsesproces som en del af processen til afsendelse af fakturaer til arbejdsgangssystemet. Du kan også køre den som en enkeltstående proces.

## <a name="pre-validate-vendor-invoice-posting"></a>For-validering af kreditorfakturabogføring

Bogføringssimuleringen fuldfører de valideringstrin, der er udført under bogføringsprocessen for kreditorfakturaer, men der opdateres ikke konti. Hvis du vil køre processen, kan du enten vælge en enkelt faktura eller flere fakturaer på siden **Ventende kreditorfakturaer**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Forbedret erfaring med visning af arbejdsproces og automatisering af historiske oplysninger for kreditorfakturaer

Der leveres en læsevenlig visning af historikken for kreditorfakturaer. Du kan få adgang til arbejdsgangshistorikken for kreditorfakturaer direkte fra kreditorfakturaen. Derfor kræves der færre klik for at finde disse oplysninger. Hvis din organisation har aktiveret muligheden for automatisk at sende importerede kreditorfakturaer til arbejdsgangen, vil automatiseringsoversigten blive medtaget i de importerede fakturaer. Automatiseringshistorikken hjælper dig med at identificere det aktuelle procestrin og de trin, der allerede er fuldført. Når et trin mislykkes, vises detaljerede oplysninger, der kan hjælpe dig med at forstå årsagen til fejlen.

## <a name="analytics-and-metrics"></a>Analyser og målepunkter

Med arbejdsområdet **Kreditorfakturapostering** kan du fokusere på kreditorfakturaer, der ikke har gennemgået den automatiserede proces. Felter på listen i arbejdsområdet viser oplysninger om kreditorfakturaer, der ikke blev sendt korrekt til arbejdsgangssystemet, importeret eller sammenlignet med produktkvitteringer. Microsoft Power BI-målepunkter er også medtaget for at give kreditorchefer indsigt i automatiseringen af kreditorfakturaer.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Genoptag automatisk behandling for flere fakturaer

Når en importeret faktura ikke overføres til en arbejdsgang ved hjælp af den automatiserede proces, fjernes den af yderligere automatisk behandling. En kreditorassistent kan gennemse og redigere fakturaen, før den automatiserede proces sender den til arbejdsgangen igen. Når en fejlårsag kan løses med samme rettelse for flere fakturaer, kan du genstarte den automatiserede proces på siden **Genoptag automatisk fakturabehandling**. 

## <a name="tracking-the-invoice-received-date-value"></a>Sporing af værdien for modtagelsesdato for faktura

Værdien for **Modtagelsesdato for faktura** angiver den dato, hvor virksomheden modtog fakturaen fra kreditoren. Den udgør udgangspunktet for sporing af fakturaens status via automatiseringsprocesserne. Denne værdi kan medtages i de importerede data til en kreditorfaktura. For fakturaer, der er oprettet manuelt, kan du angive datoen. Hvis der ikke angives en værdi, bruges dags dato som standard.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Sporing af værdierne for det importerede fakturabeløb og det importerede momsbeløb

Værdierne for det **importerede fakturabeløb** og de **importerede momsbeløb** for kreditorfakturaer kan leveres i importfilen til kreditorfakturaer. Typisk er disse værdier fra en faktura, der er scannet af en ekstern udbyder og inkluderet i importfilen. Efterhånden som fakturaen behandles i Kreditor, beregnes værdier baseret på fakturadataene. Fakturaen kan kun bogføres, hvis de importerede værdier svarer til de beregnede værdier. Sammenholdelsesværdier sikrer, at fakturaen nøjagtigt afspejler det beløb, kreditoren har tilfaldt. Hvis din organisation tillader, at importerede fakturaer sendes automatisk til arbejdsgangssystemet, kan du vælge at kræve, at de importerede totaler svarer til de beregnede totaler, før fakturaen kan sendes til arbejdsgangssystemet.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automatisering af kreditorfaktura - Genoptag automatisk behandling af flere fakturaer
Når en importeret faktura ikke sendes gennem en arbejdsgang via den automatiserede proces, fjernes den fra yderligere automatisk behandling. En kreditorassistent kan gennemse og redigere fakturaen, før den automatiserede proces sender den til arbejdsgangen igen. Når en fejlårsag kan løses med samme rettelse for flere fakturaer, kan du genstarte den automatiserede proces på siden **Genoptag automatisk fakturabehandling**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
