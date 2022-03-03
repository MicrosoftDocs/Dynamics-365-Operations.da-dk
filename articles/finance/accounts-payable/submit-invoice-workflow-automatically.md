---
title: Sende fakturaer til arbejdsgangsystemet og sammenholde produktkvitteringslinjer
description: Dette emne forklarer, hvordan kreditorfakturaer sendes til arbejdsgangssystemet, og bogførte produktkvitteringslinjer automatisk afstemmes med kreditorfakturaer.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0962ea2bfa28deb3e86620c364feffd209cfc38e
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109937"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Sende fakturaer til arbejdsgangsystemet og sammenholde produktkvitteringslinjer

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan kreditorfakturaer sendes til arbejdsgangssystemet, og bogførte produktkvitteringslinjer automatisk afstemmes med kreditorfakturaer.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer

Som del af en berøringsfri kreditorfaktureringsproces kan du få systemet til automatisk at sende en importeret faktura til arbejdsprocessystemet. Du kan konfigurere processen for afsendelse af importerede fakturaer til arbejdsprocessystemet under fanen **Automatisering af kreditorfaktura** på siden **Kreditorparametre** (**Kreditor \> Konfiguration \> Kreditorparametre**). Processen for send til-arbejdsgang køres i baggrunden, med en hyppighed, du angiver (enten hver time eller dagligt).

Når du automatisk sender fakturaer til arbejdsprocessystemet, skal du starte med en importeret faktura. Hvis du vil sikre, at fakturaen kan behandles fra start til slut uden manuel indgriben, skal du medtage en opgave til automatisk bogføringsopgave i konfigurationen af arbejdsprocessen. Fakturaer, der er relateret til indkøbsordrer, og fakturaer, der indeholder en indkøbskategori uden for indkøbsordren og ikke-lagerførte linjer, kan automatisk sendes til arbejdsprocessystemet. Fakturaer, der angives manuelt, skal sendes manuelt til arbejdsprocessystemet.

Værdien **Sendt af** i arbejdsgangen er det bruger-id, der blev angivet for baggrundsopgaven **Send kreditorfakturaer til arbejdsproces** på siden **Procesautomatisering**. Den bruger, der har det pågældende bruger-id, kan tilbagekalde fakturaen fra arbejdsprocessystemet efter behov.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Afstemme bogførte produktkvitteringer til fakturalinjer med en trevejs-sammenholdelsespolitik

Som et led i en berøringsfri kreditorfaktureringsproces, kan bogførte produktkvitteringer automatisk sammenholdes med fakturalinjer. Der skal defineres en trevejs-sammenholdelsespolitik for denne opgave. Denne funktion er tilgængelig, hvis funktionen **Automatisering af kreditorfakturaer** er blevet aktiveret på siden **Funktionsstyring**.

Denne matchningsproces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet. Men hvis der er flere produktkvitteringer for en enkelt fakturalinje, skal du køre processen flere gange for at opnå det fulde antalsmatch. Du kan angive det maksimale antal gange, systemet skal forsøge at afstemme produktkvitteringer med en fakturalinje, før det konkluderer, at processen er mislykket. Processen vil køre i baggrunden, enten hver time eller hver dag. 

Du kan køre den automatiske sammenholdelsesproces som en del af processen til afsendelse af fakturaer til arbejdsgangssystemet. Du kan også køre den som en enkeltstående proces. Du kan konfigurere processen for afstemning af produktkvitteringer med fakturalinjer under fanen **Automatisering af kreditorfaktura** på siden **Kreditorparametre** (**Kreditor \> Konfiguration \> Kreditorparametre**).

Fakturalinjer med en trevejs-sammenholdelsespolitik, hvor det tilsvarende kvitteringsantal er mindre end fakturaantallet, medtages i den automatiske afstem-med-produktkvittering-proces.

Hvis du vil have vist den **Seneste match**-status for fakturaer, der ikke er en del af den automatiske afsendelse til arbejdsproces, skal du åbne fakturaen fra siden **Kreditorfakturaer**. Når du får vist fakturaen, opdateres de tilsvarende oplysninger om validering. Status for **Sidste match** kan opdateres automatisk ved hjælp af baggrundsopgaven **Valider sammenholdelse af fakturaer**. Du kan konfigurere processen til automatisk opdatering af status for **Sidste match** på fanen **Baggrundsprocesser** på siden **Procesautomatisering** (**Systemadminstration\> Opsætning\> Procesautomatiseringer**).

En fakturalinje vil blive udelukket fra den automatiske behandling, hvis en eller flere af følgende betingelser er opfyldt:

- Værdien for **Status for automatisk kvitteringsafstemning** på fakturalinjen er **Mislykket**.
- Fakturaen er i brug.
- Fakturaen er i arbejdsprocessystemet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
