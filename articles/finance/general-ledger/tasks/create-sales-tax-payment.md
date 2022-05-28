---
title: Oprette en momsbetaling
description: Jobbet Afregn og bogfør momsprocedurer afregner momssaldi i momskonti og udligner dem til momsafregningskontoen for en given periode.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735930"
---
# <a name="create-a-sales-tax-payment"></a>Oprette en momsbetaling

[!include [banner](../../includes/banner.md)]

Jobbet Afregn og bogfør momsprocedurer afregner momssaldi i momskonti og udligner dem til momsafregningskontoen for en given periode.

1. Gå til **Moms > Opgørelser > Moms > Afregn og bogfør moms**.
2. Vælg rullelisten i feltet **Afregningsperiode** for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
4. Indtast en dato i feltet **Fra dato**. Hvis indstillingen **Medtag korrektioner** ikke er markeret på siden **Finansparametre**, kan afregningen behandles for forskellige versioner. **Oprindelig** er den første afregning for et periodeinterval og kan kun behandles én gang for et periodeinterval. De seneste rettelser udligner momsposteringer, der er bogført efter den oprindelige version er blevet oprettet.
5. Angiv en dato i feltet **Transaktionsdato**.
6. Vælg **OK**. Rapporten **Momsbetalinger** udskrives for at gennemgå de udlignede momsposteringer i perioden.

Fra og med Finance version 10.0.24 kan du udelade den rapport over **Momsbetalinger**, der genereres direkte efter, at den periodiske procedure for **udligning og postering af moms** er implementeret under funktionen **Adskil generering af momsbetalingsrapport fra momsafregning** i arbejdsområdet **Funktionsstyring**.

Når funktionen er aktiveret, udskrives der ingen rapport over momsafregning, når udligningsprocessen er fuldført. Du får i stedet følgende meddelelse: "Momsafregning og bogføring er fuldført. Bilaget 'xxxx, m/d/åååå' er bogført."

Du kan stadig køre momsafregningsrapporten manuelt ved at gå til **Moms** > **Forespørgsler og rapporter** > **Momsforespørgsler** > **Momsafregninger**.

## <a name="performance-consideration"></a>Overvejelser vedrørende ydeevne

Momsbetalingsproceduren kan tage lang tid at fuldføre. De vigtigste faktorer, der har indflydelse på procedurens ydeevne, er antallet af fakturaer i afstemningsperioden og antallet af poster, der skal bogføres i momsafstemningsbilaget. Hvis du vil forbedre ydeevnen, kan du vælge at springe visse funktioner over, som ikke er nødvendige i processen.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Aktivere funktionen til forbedring af ydeevne for momsbetaling

Funktionen **Forbedring af ydeevne for momsbetaling** kan være med til at forbedre ydeevnen for momsbetalingsproceduren ved at samle beløbene i regnskabsvalutaen og rapporteringsvalutaen på én bilagslinjer til momsindbetaling, der har samme hovedkonto, finansdimension og valuta.

1. Gå til **Systemadministration** \> **Arbejdsområder** \> **Funktionsstyring**.
2. Søg efter og vælg **Forbedring af ydeevne for momsbetaling** under fanen **Alle**.
3. Vælg **Aktivér**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Undgå generering af modregning af momsposteringer

Som standard bogfører momsbetalingsbilaget modregning af momsposteringer i forhold til hver momspostering, der udlignes i momsbetalingsproceduren. Disse modposteringer for moms medtages i rapporten **Afstemning moms/finans**. De viser den udestående saldo for momsposteringer, der ikke udlignes i perioden.

Modposteringerne for moms kan dog øge byrden af momsbetalingsproceduren. En flighting med navnet **TaxReportGenOffsetTaxTransPerRecordSetFlighting** kan derfor aktiveres efter behov. Denne flighting kan hjælpe med at forbedre ydeevnen af modposteringsgenerering for lande og områder bortset fra Thailand, Polen, Ungarn, Litauen, Malaysia, Indien, Italien, Rusland, Den Tjekkiske Republik, Estland og Letland.

> [!NOTE]
> Hvis der er brugerdefinerede felter i momsposteringstabellen, kan flighting ikke aktiveres.

Da rapporten **Afstemning moms/finans** generelt kun bruges til intern kontrol og ikke er påkrævet i mange momskategorier, kan du vælge ikke at generere modposteringer af moms på momsafregningsbilaget.

1. Gå til **Moms** \> **Indirekte moms** \> **Moms** \> **Momsafregningsperioder**.
2. Vælg en afregningsperiode.
3. Angiv indstillingen **Undgå at generere modregning af momsposteringer** til **Ja** i oversigtspanelet **Generelt**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
