---
title: Oprette og anvende betingelser for tilbageholdelse af kreditorbetaling
description: Dette afsnit indeholder oplysninger om konfiguration og vedligeholdelse af betingelserne for tilbageholdelse af kreditorbetalinger.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410205"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Oprette og anvende betingelser for tilbageholdelse af kreditorbetaling

[!include [banner](../includes/banner.md)] 

Opsætning af betingelser for tilbageholdelse af kreditorbetalinger for et projekt er nyttig, når organisationen vil tilbageholde en del af de betalinger, der foretages til en kreditor. Når du f.eks. ønsker at tilbageholde betalingen til en leverandør, indtil de leverede produkter opfylder dine forventninger. Betingelserne for tilbageholdelse af kreditorbetalinger kan specificeres, når du forhandler en kreditorkontrakt.

## <a name="create-vendor-payment-retention-terms"></a>Oprette tilbageholdelsesbetingelser for kreditorbetaling

Du kan angive en procentdel af en kreditorbetaling, som du vil tilbageholde, og den procentdel af tidligere tilbageholdte beløb, som du vil frigive. Der tilbageholdes automatisk beløb for kreditorfakturaer, indtil kontrakten har nået det angivne færdiggørelsesniveau. Når du har konfigureret tilbageholdelsesbetingelserne, kan du anvende dem på ethvert af projekterne for den pågældende kreditor.

Brug følgende trin til at konfigurere og vedligeholde tilbageholdelsesbetingelser for kreditorbetalinger. 

1. Gå til **Projektstyring og regnskab** > **Tilbageholdelse** > **Tilbageholdelsesbetingelser for kreditorbetaling**.
2. Vælg **Ny** for at tilføje en ny kreditortilbageholdelsesbetingelse. Værdien for **Regel-id** for den nye betingelse angives automatisk. 
3. Angiv en kort beskrivelse i feltet **Beskrivelse**, og vælg **Betingelser** i oversigtspanelet. Vælg **Tilføj linje** for at angive betingelsesværdier for følgende:

   - **Procentdel af leverede enheder**: Angiv en færdiggørelsesprocent for betingelsen. Beløb tilbageholdes automatisk for kreditorfakturaer, indtil projektstadiet for færdiggørelse er lig med den specificerede procentdel. Hvis du f.eks. skriver 50,00, tilbageholdes beløb, indtil 50 % af projektet er fuldført.
   - **Procentdel, der skal tilbageholdes**: Angiv den procentdel af beløbet på en kreditorfaktura, der skal tilbageholdes. Hvis du f.eks. skriver 10,00, tilbageholdes 10 procent af beløbet på en kreditorfaktura, indtil projektet når den færdiggørelsesgrad, der er indstillet i feltet **Procentdel af leverede enheder**.
   - **Procentdel, der skal frigives**: Vælg **Tilføj linje** for at angive en procentdel af eventuelle tidligere tilbageholdte beløb, der skal frigives på det valgte færdiggørelsesniveau for projektet.

> [!NOTE]
> Hvis du har mere end én milepæl for forskellige niveauer af projektfærdiggørelse, skal du angive en særskilt kreditortilbagholdelsesbetingelseslinje for hver tilbageholdelsesregel. Hver linje kan angive en særskilt tilbageholdelsesprocentdel og en særskilt frigivelsesprocentdel for hvert angivet niveau af projektfærdiggørelse.

Når du har oprettet tilbageholdelsesbetingelser for en kreditor, kan du anvende betingelserne på et projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Anvende kreditortilbageholdelsesbetingelser på et projekt

1. Gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**, og åbn et projekt på siden projektliste.
2. I oversigtpanelet **Kreditoraftaler** skal du vælge **Tilføj linje**.
3. Vælg én af følgende indstillinger i feltet **Kontokode**: 

   - **Tabel**: Kreditortilbageholdelsesbetingelserne gælder for en enkelt kreditor.
   - **Gruppe**: Kreditortilbageholdelsesbetingelserne gælder for alle kreditorer i en kreditorgruppe.
   - **Alle**; Kreditortilbageholdelsesbetingelserne gælder for alle kreditorer.

4. I feltet **Kreditor/Kreditorgruppe** skal du vælge den kreditor eller kreditorgruppe, som kreditortilbageholdelsesbetingelserne gælder for. Hvis du har valgt **Alle** i det foregående trin, er dette felt ikke tilgængeligt.
5. I feltet **Kreditortilbageholdelsesbetingelser** skal du vælge den tilbageholdelsesbetingelse, som du oprettede under den forrige procedure.
6. Hvis projektet også har betingelser for betal ved betaling konfigureret for kreditoren, skal du angive grænseprocenten for projektet i feltet **Grænseværdi for Betal ved betaling i procent**.

Betingelser for tilbageholdelse af kreditorbetaling vises også på indkøbsordrer, som du opretter for kreditoren.
