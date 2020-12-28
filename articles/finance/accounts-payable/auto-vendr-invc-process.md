---
title: Oversigt over automatiske processer for kreditorfakturering
description: I dette emne beskrives muligheden for at automatisere behandlingen af kreditorfakturaer og fordelene ved at bruge en automatiseret proces.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec3598ebd158cc23ac7c02d7e33557141d5901bc
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022490"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Oversigt over automatiske processer for kreditorfakturering

[!include [banner](../includes/banner.md)]

I dette emne beskrives muligheden for at automatisere behandlingen af kreditorfakturaer og fordelene ved at bruge en automatiseret proces. Denne egenskab består af funktioner, der aktiveres i funktionsstyring. Disse funktioner gælder kun for kreditorfakturaer, ikke for fakturaer, der behandles via siden **Fakturajournal** eller **Indgangsbogskladde**.

I mange tilfælde samarbejder organisationer med tredjepart om behandlingen af papirfakturaer via en udbyder af optisk tegngenkendelse (OCR). Tjenesteudbyderen returnerer maskinlæsbare fakturametadata. For at hjælpe med automatisering kan du bruge funktionerne til automatisering af kreditorer til at forbruger disse artefakter fra kreditor.

Du kan automatisere nogle kreditorfaktureringsprocesser. Disse processer omfatter afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer. Den automatiserede proces viser statusoplysninger om en kreditorfaktura, når den bevæger sig gennem hver af processerne. Denne mulighed kan hjælpe kreditormedarbejderne og lederne med at behandle kreditorfakturaer mere effektivt. Det hjælper også med at reducere fejl og ineffektivhed, der kan forekomme, når oplysningerne angives og behandles manuelt.

Automatiseringsprocesserne kan bruges til at udføre disse opgaver:

- Automatisk sende importerede fakturaer til arbejdsprocessystemet.
- Afstemme produktkvitteringer med ventende kreditorfakturalinjer.
- Simulere bogføring, før en kreditorfaktura bogføres.
- Få vist arbejdsgangshistorikken hurtigt og effektivt.
- Se og analysere resultaterne af at automatisere behandlingen af kreditorfakturaer.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Automatisering af kreditorfaktura – Send importerede kreditorfakturaer til arbejdsgangssystemet

Som del af en berøringsfri kreditorfaktureringsproces kan du få systemet til automatisk at sende en importeret faktura til arbejdsgangssystemet. Processen kører i baggrunden, med en hyppighed, du angiver (enten hver time eller dagligt). Muligheden for automatisk afsendelse af importerede fakturaer til arbejdsgangssystemet kræver, at processen starter med en importeret faktura. Hvis du vil sikre, at fakturaen kan behandles fra start til slut uden manuel indgriben, skal du medtage en automatisk bogføringsopgave i konfigurationen af arbejdsprocessen.

'Fakturaer, der er relateret til indkøbsordrer, og fakturaer, der indeholder en indkøbskategori uden for indkøbsordren og ikke-lagerførte linjer, kan automatisk sendes til arbejdsprocessystemet. De fakturaer, der angives manuelt, og fakturaer, der oprettes via arbejdsområdet **Fakturering af kreditorsamarbejde** , skal sendes manuelt til arbejdsgangssystemet.

Automatiseringsfunktionen giver dig en fleksibel ramme med mulighed for at definere firmaspecifikke regler for afsendelse af importerede kreditorfakturaer til arbejdsgangssystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Automatisering af kreditorfaktura – Afstemme produktkvitteringer med fakturalinjer med en trevejs-sammenholdelsespolitik

Systemet kan automatisk afstemme bogførte produktkvitteringer med fakturalinjer, som en trevejs-sammenholdelsespolitik er defineret for. Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet. I denne proces kan du angive det maksimale antal gange, systemet skal forsøge at afstemme produktkvitteringer med en fakturalinje, før det konkluderer, at processen er mislykket. Processen vil køre i baggrunden, enten hver time eller hver dag. Du kan køre den automatiske sammenholdelsesproces som en del af processen til afsendelse af fakturaer til arbejdsgangssystemet. Du kan også køre den som en enkeltstående proces.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Automatisering af kreditorfaktura – Validere bogføring af kreditorfaktura på forhånd

Bogføringssimuleringen fuldfører de valideringstrin, der er udført under bogføringsprocessen for kreditorfakturaer, men der opdateres ikke konti. Hvis du vil køre processen, kan du enten vælge en enkelt faktura eller flere fakturaer på siden **Ventende kreditorfakturaer**.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Automatisering af kreditorfakturaer – Forbedret erfaring med visning af historiske oplysninger om en arbejdsproces for kreditorfakturaer

Der leveres en læsevenlig visning af historikken for kreditorfakturaer. Du kan få adgang til arbejdsgangshistorikken for kreditorfakturaer direkte fra kreditorfakturaen. Derfor kræves der færre klik for at finde disse oplysninger.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Automatisering af kreditorfaktura – Analyser og målepunkter

Med arbejdsområdet **Kreditorfakturapostering** kan du fokusere på kreditorfakturaer, der ikke har gennemgået den automatiserede proces. Felter på listen i arbejdsområdet viser oplysninger om kreditorfakturaer, der ikke blev sendt korrekt til arbejdsgangssystemet, importeret eller sammenlignet med produktkvitteringer. Microsoft Power BI-målepunkter er også medtaget for at give kreditorchefer indsigt i automatiseringen af kreditorfakturaer.