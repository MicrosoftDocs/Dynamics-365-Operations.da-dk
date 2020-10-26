---
title: Sende fakturaer til arbejdsgangssystemet og afstemme produktkvitteringslinjer (prøveversion)
description: Dette emne forklarer, hvordan kreditorfakturaer sendes til arbejdsgangssystemet, og bogførte produktkvitteringslinjer automatisk afstemmes med kreditorfakturaer.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
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
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 3387595e41fb03e98bb437588f6de78794ae383f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930913"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a>Sende fakturaer til arbejdsgangssystemet og afstemme produktkvitteringslinjer (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan kreditorfakturaer sendes til arbejdsgangssystemet, og bogførte produktkvitteringslinjer automatisk afstemmes med kreditorfakturaer.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer

Som del af en berøringsfri kreditorfaktureringsproces kan du få systemet til automatisk at sende en importeret faktura til arbejdsgangssystemet. Du kan konfigurere processen for afsendelse af importerede fakturaer til arbejdsprocessystemet under fanen **Automatisering af kreditorfaktura** på siden **Kreditorparametre** (**Kreditor \> Konfiguration \> Kreditorparametre**). Processen for send til-arbejdsgang køres i baggrunden, med en hyppighed, du angiver (enten hver time eller dagligt).

Når du automatisk sender fakturaer til arbejdsprocessystemet, skal du starte med en importeret faktura. Hvis du vil sikre, at fakturaen kan behandles fra start til slut uden manuel indgriben, skal du medtage en opgave til automatisk bogføringsopgave i konfigurationen af arbejdsprocessen. Fakturaer, der er relateret til indkøbsordrer, og fakturaer, der indeholder en indkøbskategori uden for indkøbsordren og ikke-lagerførte linjer, kan automatisk sendes til arbejdsprocessystemet. Fakturaer, der angives manuelt, skal sendes manuelt til arbejdsprocessystemet.

Værdien **Sendt af** i arbejdsgangen er det bruger-id, der blev angivet for baggrundsopgaven **Send kreditorfakturaer til arbejdsproces** på siden **Procesautomatisering**. Den bruger, der har det pågældende bruger-id, kan tilbagekalde fakturaen fra arbejdsprocessystemet efter behov.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Afstemme bogførte produktkvitteringer til fakturalinjer med en trevejs-sammenholdelsespolitik

Som et led i en berøringsfri kreditorfaktureringsproces, kan systemet automatisk sammenholde bogførte produktkvitteringer med fakturalinjer. Der skal defineres en trevejs-sammenholdelsespolitik for denne opgave. Denne funktion er tilgængelig, hvis funktionen **Automatisering af kreditorfakturaer** er blevet aktiveret på siden **Funktionsstyring**.

Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet. I denne proces kan du angive det maksimale antal gange, systemet skal forsøge at afstemme produktkvitteringer med en fakturalinje, før det konkluderer, at processen er mislykket. Processen vil køre i baggrunden, enten hver time eller hver dag. Du kan køre den automatiske sammenholdelsesproces som en del af processen til afsendelse af fakturaer til arbejdsgangssystemet. Du kan også køre den som en enkeltstående proces. Du kan konfigurere processen for afstemning af produktkvitteringer med fakturalinjer under fanen **Automatisering af kreditorfaktura** på siden **Kreditorparametre** (**Kreditor \> Konfiguration \> Kreditorparametre**).

Fakturalinjer med en trevejs-sammenholdelsespolitik, hvor det tilsvarende kvitteringsantal er mindre end fakturaantallet, medtages i den automatiske afstem-med-produktkvittering-proces.

Hvis du vil have vist den **Seneste match**-status for fakturaer, der ikke er en del af den automatiske afsendelse til arbejdsproces, skal du åbne fakturaen fra siden **Kreditorfakturaer**. Når du får vist fakturaen, opdateres de tilsvarende oplysninger om validering.

En fakturalinje vil blive udelukket fra den automatiske behandling, hvis en eller flere af følgende betingelser er opfyldt:

- Værdien for **Status for automatisk kvitteringsafstemning** på fakturalinjen er **Mislykket**.
- Fakturaen er i brug.
- Fakturaen er i arbejdsprocessystemet.
