---
title: Konfigurere indstillinger for automatisering af kreditorfaktura (prøveversion)
description: I dette emne beskrives de indstillinger, der er tilgængelige for opsætning og konfiguration af automatisering af kreditorfakturaer.
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
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40de7c378bff602fa3629bb190a7a89fe584d2a6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993188"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Opsætningsindstillinger for automatisering af kreditorfaktura

[!include [banner](../includes/banner.md)]

I dette emne beskrives de indstillinger, der er tilgængelige for opsætning og konfiguration af automatisering af kreditorfakturaer. Funktioner til fakturaautomatisering bruger følgende typer opsætningsparametre:

- Parametre for afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer.
- Parametre til behandling af automatiserede baggrundsopgaver. Strukturen for procesautomatisering bruges til at sende importerede kreditorfakturaer til arbejdsprocessystemet. Den bruges også til automatisk at matche bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer og til at udføre fakturasammenholdelse for manuelle fakturaer, der automatisk er afstemt med produktkvitteringslinjer. Forskellige forretningsprocesser bruger denne struktur til at definere, hvor ofte den valgte proces skal køres. De tilgængelige frekvenser for baggrundsprocesserne **Afstem produktkvittering med fakturalinjer** og **Send kreditorfakturaer til arbejdsproces** omfatter **Time** og **Daglig**.

Hvis du vil konfigurere eller se oplysninger om en baggrundsopgave, skal du gå til **Systemadministration \> Konfiguration \> Procesautomatiseringer** og vælge fanen **Baggrundsopgave**.

Du skal konfigurere en arbejdsgang for kreditorfakturaer for at opnå en berøringsfri automatisering fra importprocessen via bogføring af kreditorfakturaer. Gå til **Kreditor > Opsætning > Kreditorarbejdsgange** for at konfigurere en arbejdsproces. Hvis du vil sikre, at fakturaen kan behandles fra start til slut uden manuel indgriben, skal du medtage en opgave til automatisk bogføring i konfigurationen af arbejdsprocessen.

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parametre for afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet

Der bruges bestemte parametre for afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet. Der bruges også parametre til at matche bogførte produktkvitteringslinjer med afventende kreditorfakturalinjer. De parametre, du skal angive, er fordelt mellem følgende afsnit under fanen **Automatisering af kreditorfaktura** på siden **Kreditorparametre**:

- Arbejdsgang for kreditorfaktura
- Afstem produktkvitteringer automatisk

Følgende parametre er tilgængelige:

- **Send automatisk importerede fakturaer til arbejdsgang** – Hvis du angiver denne indstilling til **Ja**, sendes importerede fakturaer automatisk til arbejdsprocessystemet. Hvis denne indstilling er angivet til **Nej**, skal fakturaer sendes manuelt. Hvis du angiver denne indstilling til **Ja**, aktiverer du en berøringsfri proces fra resultaterne af importen via bogføring.

    Du kan kun angive denne indstilling til **Ja**, hvis der er konfigureret en aktiv arbejdsgang for kreditorfakturaer for din juridiske enhed. Gå til **Kreditor \> Opsætning \> Kreditorarbejdsgange** for at konfigurere en arbejdsproces.

- **Afstem produktkvitteringer med fakturalinjer, før de sendes automatisk** – Hvis du angiver denne indstilling til **Ja**, kan den importerede faktura ikke automatisk sendes til arbejdsprocessystemet, før det afstemte produktkvitteringsantal er lig med fakturaantallet. Hvis du angiver denne indstilling til **Ja**, aktiverer du automatisk afstemning af bogførte produktkvitteringer med fakturalinjer, som en trevejs-sammenholdelsespolitik er defineret for. Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet. På dette tidspunkt sendes fakturaen automatisk til arbejdsprocessystemet.

    Indstillingen 'Afstem produktkvitteringer med fakturalinjer, før de sendes automatisk' er kun tilgængelig, hvis indstillingen **Aktivér validering af fakturasammenholdelse** er valgt. Når denne indstilling er valgt, vælges automatisk indstillingen **Afstem automatisk produktkvitteringer med fakturalinjer**.

- **Kræv, at de beregnede totaler er lig med de importerede totaler for automatisk afsendelse af arbejdsgang** – Hvis du angiver denne indstilling til **Ja**, kan fakturaen ikke automatisk sendes til arbejdsprocessystemet, før de totaler, der er beregnet for fakturaen, er lig med de importerede totaler. Hvis denne indstilling er angivet til **Nej**, kan fakturaen automatisk sendes til arbejdsprocessystemet, men den kan ikke bogføres, før de beregnede totaler er rettet, så de stemmer overens med de importerede totaler. Hvis du ikke importerer fakturabeløbet eller momsbeløbet, skal denne indstilling angives til **Nej**.
- **Afstem automatisk produktkvitteringer med fakturalinjer** – Hvis du angiver denne indstilling til **Ja**, kan baggrundsbehandling bruges til at foretage automatisk sammenholdelse af bogførte produktkvitteringer for at fakturere linjer, som en trevejs-sammenholdelsespolitik er defineret for. Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet, eller indtil værdien af feltet **Antal gange, der skal forsøges automatisk afstemning** er nået. Processen kan køres, indtil fakturaen er sendt til arbejdsprocessystemet.

    Denne indstilling er kun tilgængelig, hvis indstillingen **Aktivér validering af fakturasammenholdelse** er valgt.

    Hvis du indstiller **Afstem produktkvitteringer med fakturalinjer, før de afstemmes automatisk** til **Ja**, kan denne indstilling ikke angives til **Nej**. Hvis du vil angive denne indstilling til **Nej**, skal du først angive **Afstem produktkvitteringer med fakturalinjer, før de afstemmes automatisk** til **Nej**.

- **Antal gange, der skal forsøges automatisk afstemning** – Vælg det antal gange, systemet skal forsøge at afstemme produktkvitteringer med en fakturalinje, før det konkluderer, at processen er mislykket. Når det angivne antal forsøg er nået, fjernes fakturaen fra automatisk behandling.

