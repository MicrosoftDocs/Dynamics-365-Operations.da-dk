---
title: Rapporter over landingsomkostninger
description: Denne artikel beskriver, hvordan du finder og bruger de forskellige typer rapporter, der er tilgængelige i modulet Landingsomkostninger.
author: Weijiesa
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 836d6b538b32d818ed3b825000d004b005ce95d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905944"
---
# <a name="landed-cost-reports"></a>Rapporter over landingsomkostninger

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Udestående fakturaer

Rapporten over udestående fakturaer indeholder en liste over alle udestående fakturaer for de forskellige omkostningsniveauer, der er knyttet til hver fragt. Den bruges til jævnligt at afstemme fragten og fragtomkostningerne med listen over finanstransaktioner. Når en fast omkostning er faktureret, fjernes den fra rapporten.

Hvis du vil generere en rapport over udestående fakturaer, skal du følge disse trin.

1. Gå til **Landingsomkostninger \> Rapporter \> Sporing \> Udestående fakturaer**.
1. Angiv en dato i feltet **Som på dato** i dialogboksen **Udestående fakturaer**. Alle fakturaer, der var udestående på eller før denne dato, inkluderes i outputtet.
1. Vælg en af nedenstående indstillinger under **Vis**:

    - **Omkostning, der ikke er faktureret** – Medtag omkostninger for fakturerede forsendelser, der har en forkalkuleret kostværdi, men ingen faktiske omkostninger.
    - **Lager, der ikke er faktureret** – Medtag omkostninger, der er faktureret, men indkøbsordren endnu ikke er modtaget for.
    - **Alle ikke fakturerede** – Medtag resultaterne af både indstillingen **Omkostning, der ikke er faktureret** og indstillingen **Lager, der ikke er faktureret**.

1. Angiv indstillingen **Medtag nye omkostninger** til *Ja* for at medtage omkostninger, der endnu ikke har en faktisk omkostning, og som der ikke er modtaget lager for. Hvis du angiver den til *Nej*, indeholder rapporten kun de omkostninger, der er faktureret.
1. Aktivér hver af de detaljer, du vil medtage i rapporten, i afsnittet **Vis**.
1. Ligesom du gør det ved andre typer rapporter i Microsoft Dynamics 365 Supply Chain Management, skal du bruge oversigtspanelet **Destination** til at vælge rapportens outputformat.
1. Ligesom du gør det med andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Poster, der skal indgå** for at begrænse de poster, der vil blive medtaget i rapporten.
1. Vælg **OK** for at generere rapporten.

## <a name="activityprovider-analysis-reports"></a>Rapporter over aktivitets-/udbyderanalyse

Aktivitets-/udbyderanalyserapporterne giver dig mulighed for at gennemgå nøjagtigheden af dine tidsestimater for hver udbyder.

Hvis du vil generere en rapport over aktivitets-/udbyderanalyse, skal du følge disse trin.

1. Afhængigt af den rapporttype, du vil oprette, skal du følge et af disse trin:

    - Gå til **Landingsomkostninger \> Rapporter \> Analyse af aktivitet/udbyder efter aktivitet**. I dette tilfælde grupperes tidsestimerne efter aktivitet.
    - Gå til **Landingsomkostninger \> Rapporter \> Analyse af aktivitet/udbyder efter udbyder**. I dette tilfælde grupperes tidsestimerne efter udbyder.

    Enten vises dialogboksen **Analyse af aktivitet/udbyder efter aktivitet** eller dialogboksen **Analyse af aktivitet/udbyder efter udbyder**. Begge dialogbokse indeholder de samme indstillinger.

1. Ligesom du gør det ved andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Destination** til at vælge rapportens outputformat.
1. Ligesom du gør det med andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Poster, der skal indgå** for at begrænse de poster, der vil blive medtaget i rapporten.
1. Vælg **OK** for at generere rapporten.

## <a name="voyage-costing-reports"></a>Rapporter over efterkalkulation af fragt

Rapporter over efterkalkulation af fragt viser varernes kostpris og importomkostningerne pr. folio, forsendelsescontainer eller fragt afhængigt af, hvilke indstillinger du vælger, når du genererer rapporten. Hver enkelt efterkalkulationsrapport for fragt giver dig mulighed for at se de forkalkulerede omkostninger for en fragt i forhold til de faktiske omkostninger, og den kan opdeles på baggrund af de forskellige identifikationsfaktorer.

Hvis du vil generere en efterkalkulationsrapport for fragt, skal du følge disse trin.

1. Afhængigt af den rapporttype, du vil oprette, skal du følge et af disse trin:

    - Gå til **Landingsomkostninger \> Rapporter \> Efterkalkulation \> Efterkalkulation af fragt efter individuel omkostning**. I dette tilfælde viser den individuelle omkostning importomkostningerne pr. omkostningsområde pr. omkostningstypekode.
    - Gå til **Landingsomkostninger \> Rapporter \> Efterkalkulation \> Efterkalkulation af fragt efter rapporteringskategori**. I dette tilfælde fordeles importomkostningerne på de forskellige rapporteringskategorier. Omkostningstyper grupperes efter rapporteringskategorier.

    Enten vises dialogboksen **Efterkalkulation af fragt efter individuel omkostning** eller dialogboksen **Efterkalkulation af fragt efter rapporteringskategori**. Disse dialogbokse ligner hinanden. Hvis der er forskelle, er de anført i resten af denne procedure.

1. Hvis du har åbnet dialogboksen **Efterkalkulation af fragt efter rapporteringskategori**, skal du vælge en af følgende værdier i feltet **Omkostninger**:

    - **Kostværdi** – Værdien beregnes enten ved hjælp af automatiske omkostninger eller oprettes manuelt i omkostningsområdet.
    - **Estimeret** – Når varerne er modtaget, angives den forkalkulerede omkostning.
    - **Faktisk** – Når ordren er faktureret, angives de faktiske omkostninger til omkostningen på fakturaen.
    - **Bedst** – Systemet anvender den af de foregående tre indstillinger, der er mest nøjagtig. (Det anbefales, at du vælger denne indstilling).

1. Angiv indstillingen **Pr. vare** til *Ja* for at få vist omkostningerne for hver vare. Angiv den til *Nej* for at få vist omkostningerne pr. fragt.
1. Vælg de kategorier, omkostningen skal opdeles efter, i afsnittet **Vis**.
1. Vælg de dimensioner, der skal medtages i rapporten, i sektionen **Dimensioner**.
1. Ligesom du gør det ved andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Destination** til at vælge rapportens outputformat.
1. Ligesom du gør det med andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Poster, der skal indgå** for at begrænse de poster, der vil blive medtaget i rapporten.
1. Vælg **OK** for at generere rapporten.

## <a name="shipping-container-receipts-list"></a>Liste over kvitteringer for forsendelsescontainer

Tilgangslisten for forsendelsescontainere indeholder alle ikke-modtagne antal, der forfalder på eller før en forventet dato. Lagermedarbejderne kan bruge denne rapport til at identificere de forventede varer på en forsendelsescontainer. Den kan også bruges til manuel kontrol af varer, når de modtages på en forsendelsescontainer.

Hvis du vil generere en tilgangsliste for en forsendelsescontainer, skal du følge disse trin.

1. Gå til **Landingsomkostninger \> Rapporter \> Sporing \> Tilgangsliste for forsendelsescontainer**.
1. Angiv en dato i feltet **Forventet dato** i dialogboksen **Tilgangsliste for forsendelsescontainer**. Alle antal, der ikke er modtaget på eller før denne dato, inkluderes i outputtet.
1. Vælg de dimensioner, der skal medtages i rapporten, i sektionen **Dimensioner**.
1. Ligesom du gør det ved andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Destination** til at vælge rapportens outputformat.
1. Ligesom du gør det med andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Poster, der skal indgå** for at begrænse de poster, der vil blive medtaget i rapporten.
1. Vælg **OK** for at generere rapporten.

## <a name="expected-delivery-report"></a>Rapport over forventet levering

Rapporten over forventet levering indeholder grundlæggende oplysninger om fragt, forsendelsescontainer, folio, varer og forventet leveringsdato.

Hvis du vil generere en rapport over forventet levering, skal du følge disse trin.

1. Gå til **Landingsomkostninger \> Rapporter \> Sporing \> Forventet levering**.
1. I dialogboksen **Forventet levering** skal du i feltet **Forventet dato** vælge den dato, hvor varerne forventes leveret til det endelige destinationslagersted. Alle fragtlinjer, der har en forventet dato på eller før denne dato, og som endnu ikke er modtaget, medtages i outputtet.
1. Valgfrit: Vælg en kreditorkonto i feltet **Kreditorkonto**, hvis du kun vil medtage leveringer fra en bestemt leverandør.
1. Vælg de dimensioner, der skal medtages i rapporten, i sektionen **Dimensioner**.
1. Ligesom du gør det ved andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Destination** til at vælge rapportens outputformat.
1. Ligesom du gør det med andre typer rapporter i Supply Chain Management, skal du bruge oversigtspanelet **Poster, der skal indgå** for at begrænse de poster, der vil blive medtaget i rapporten.
1. Vælg **OK** for at generere rapporten.
