---
title: Konfigurere indstillinger for automatisering af kreditorfaktura (prøveversion)
description: Denne artikel beskriver de indstillinger, der er tilgængelige for opsætning og konfiguration af automatisering af kreditorfakturaer.
author: sunfzam
ms.date: 02/14/2022
ms.topic: article
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
ms.openlocfilehash: 86ad68b3dc08bf2c57ab5f9bc6c65bc37c0901e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874835"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Opsætningsindstillinger for automatisering af kreditorfaktura

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de indstillinger, der er tilgængelige for opsætning og konfiguration af automatisering af kreditorfakturaer. Funktioner til fakturaautomatisering bruger følgende typer opsætningsparametre:

- Parametre til automatisk anvendelse af forudbetalinger i importerede fakturaer.
- Parametre for afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet og tilsvarende bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer.
- Parametre til behandling af automatiserede baggrundsopgaver. Strukturen for procesautomatisering bruges til at sende importerede kreditorfakturaer til arbejdsprocessystemet. Den bruges også til automatisk at matche bogførte produktkvitteringslinjer til ventende kreditorfakturalinjer og til at udføre fakturasammenholdelse for manuelle fakturaer, der automatisk er afstemt med produktkvitteringslinjer. Forskellige forretningsprocesser bruger denne struktur til at definere, hvor ofte den valgte proces skal køres. De tilgængelige frekvenser for baggrundsprocesserne **Afstem produktkvittering med fakturalinjer** og **Send kreditorfakturaer til arbejdsproces** omfatter **Time** og **Daglig**.

Hvis du vil konfigurere eller se oplysninger om en baggrundsopgave, skal du gå til **Systemadministration \> Konfiguration \> Procesautomatiseringer** og vælge fanen **Baggrundsopgave**.

Du skal konfigurere en arbejdsgang for kreditorfakturaer for at opnå en berøringsfri automatisering fra importprocessen via bogføring af kreditorfakturaer. Gå til **Kreditor > Opsætning > Kreditorarbejdsgange** for at konfigurere en arbejdsproces. Hvis du vil sikre, at fakturaen kan behandles fra start til slut uden manuel indgriben, skal du medtage en opgave til automatisk bogføring i konfigurationen af arbejdsprocessen.

## <a name="parameters-for-automatically-applying-prepayments-in-imported-invoices"></a>Parametre til automatisk anvendelse af forudbetalinger i importerede fakturaer

- **Anvend automatisk forudbetaling for importerede fakturaer** – Når denne indstilling er angivet til **Ja**, søges der automatisk i eksisterende forudbetalinger efter en tilsvarende indkøbsordre, når kreditorfakturaer importeres. Hvis der findes forudbetalinger, der kan anvendes, tilføjes der én ekstra linje for at anvende forudbetalingerne på de kreditorfakturaer, der importeres.
- **Bloker den opfølgende automatiseringsproces i tilfælde af applikationsfejl ved forudbetaling** – Når denne indstilling er angivet til **Ja**, spærres fakturaer, hvis der ikke kan anvendes en forudbetaling. Som andre automatiske processer, for eksempel processen til sammenligning af kvitteringer og processen til afsendelse til en arbejdsproces, henter automatiseringsprocessen for fakturaer ikke blokerede fakturaer, før forudbetalingen er anvendt manuelt. 

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parametre for afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet

Der bruges bestemte parametre for afsendelse af importerede kreditorfakturaer til arbejdsprocessystemet. Der bruges også parametre til at matche bogførte produktkvitteringslinjer med afventende kreditorfakturalinjer. De parametre, du skal angive, er fordelt mellem følgende afsnit under fanen **Automatisering af kreditorfaktura** på siden **Kreditorparametre**:

- Arbejdsgang for kreditorfaktura
- Afstem produktkvitteringer automatisk

Følgende parametre er tilgængelige:

- **Send automatisk importerede fakturaer til arbejdsgang** – Hvis du angiver denne indstilling til **Ja**, sendes importerede fakturaer automatisk til arbejdsprocessystemet. Hvis denne indstilling er angivet til **Nej**, skal fakturaer sendes manuelt. Hvis du angiver denne indstilling til **Ja**, aktiverer du en berøringsfri proces fra resultaterne af importen via bogføring.

    Du kan kun angive denne indstilling til **Ja**, hvis der er konfigureret en aktiv arbejdsgang for kreditorfakturaer for din juridiske enhed. Gå til **Kreditor \> Opsætning \> Kreditorarbejdsgange** for at konfigurere en arbejdsproces.

- **Afstem produktkvitteringer med fakturalinjer, før de sendes automatisk** – Hvis du angiver denne indstilling til **Ja**, kan den importerede faktura ikke automatisk sendes til arbejdsprocessystemet, før det afstemte produktkvitteringsantal er lig med fakturaantallet. Hvis du angiver denne indstilling til **Ja**, aktiverer du automatisk afstemning af bogførte produktkvitteringer med fakturalinjer, som en trevejs-sammenholdelsespolitik er defineret for. Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet. På dette tidspunkt sendes fakturaen automatisk til arbejdsprocessystemet.

    Indstillingen **Afstem produktkvitteringer med fakturalinjer, før de sendes automatisk** er kun tilgængelig, hvis indstillingen **Aktivér validering af fakturasammenholdelse** er valgt. Når denne indstilling er valgt, vælges automatisk indstillingen **Afstem automatisk produktkvitteringer med fakturalinjer**.

- **Kræv, at de beregnede totaler er lig med de importerede totaler for automatisk afsendelse af arbejdsgang** – Hvis du angiver denne indstilling til **Ja**, kan fakturaen ikke automatisk sendes til arbejdsprocessystemet, før de totaler, der er beregnet for fakturaen, er lig med de importerede totaler. Hvis denne indstilling er angivet til **Nej**, kan fakturaen automatisk sendes til arbejdsprocessystemet, men den kan ikke bogføres, før de beregnede totaler er rettet, så de stemmer overens med de importerede totaler. Hvis du ikke importerer fakturabeløbet eller momsbeløbet, skal denne indstilling angives til **Nej**.
- **Afstem automatisk produktkvitteringer med fakturalinjer** – Hvis du angiver denne indstilling til **Ja**, kan baggrundsbehandling bruges til at foretage automatisk sammenholdelse af bogførte produktkvitteringer for at fakturere linjer, som en trevejs-sammenholdelsespolitik er defineret for. Denne proces vil køre, indtil det afstemte produktkvitteringsantal er lig med fakturaantallet, eller indtil værdien af feltet **Antal gange, der skal forsøges automatisk afstemning** er nået. Processen kan køres, indtil fakturaen er sendt til arbejdsprocessystemet.

    Denne indstilling er kun tilgængelig, hvis indstillingen **Aktivér validering af fakturasammenholdelse** er valgt.

    Hvis du indstiller **Afstem produktkvitteringer med fakturalinjer, før de afstemmes automatisk** til **Ja**, kan denne indstilling ikke angives til **Nej**. Hvis du vil angive denne indstilling til **Nej**, skal du først angive **Afstem produktkvitteringer med fakturalinjer, før de afstemmes automatisk** til **Nej**.

- **Antal gange, der skal forsøges automatisk afstemning** – Vælg det antal gange, systemet skal forsøge at afstemme produktkvitteringer med en fakturalinje, før det konkluderer, at processen er mislykket. Når det angivne antal forsøg er nået, fjernes fakturaen fra automatisk behandling.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
