---
title: Vise økonomirapporter
description: I dette emne beskrives, hvordan du kan se og undersøge økonomirapporter i Microsoft Dynamics 365 Finance. Artiklen indeholder oplysninger om de forskellige indstillinger, du kan anvende på økonomirapporter for at ændre deres udseende og de data, de indeholder.
author: kweekley
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 485d8f0aee791aa577432947d74b08caf484da0a3056d8119579e9d659ca3d57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730500"
---
# <a name="view-financial-reports"></a>Vise økonomirapporter

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du kan se og undersøge økonomirapporter. Artiklen indeholder oplysninger om de forskellige indstillinger, du kan anvende på økonomirapporter for at ændre deres udseende og de data, de indeholder.

## <a name="financial-reporting-overview"></a>Oversigt over økonomirapportering

## <a name="open-a-financial-report"></a>Åbne en økonomisk rapport
Hvis du vil åbne en rapport, skal du vælge rapportnavnet. Første gang en rapport åbnes, genereres den automatisk for den foregående måned. For eksempel, hvis du åbner en rapport for første gang i august 2015, oprettes rapporten for 31. juli 2015. Når en rapport er åben, kan du begynde at udforske den ved at foretage detailudledning for bestemte data og ændre rapportindstillinger.

## <a name="drill-down-on-a-financial-report"></a>Foretage detailudledning for en økonomisk rapport
Økonomiske rapporter kan indeholde flere niveauer med detaljer. Det økonomiske niveau er det første niveau, du ser, når du åbner en økonomisk rapport. For at gå til kontoniveau skal du vælge de data, der skal foretages detaljeopløftning af. Hvis du for eksempel vil have vist kontooplysninger for salg, skal du vælge de salgsdata, du vil undersøge. Fra kontoniveau kan du foretage detailudledning for at få vist de posteringer, der indgår i kontosaldoen. Der er to måder at få vist posteringer på: rapporttransaktioner og bilagsposteringer.

-   **Rapporttransaktioner** – Transaktioner vises i en formateret visning, der indgår i den økonomiske rapport. For at få vist transaktionerne i den formaterede visning, skal du vælge dataene, der skal detaljeopløftes, og derefter klikke på **Vis detaljer på rapportposteringsniveau**.
-   **Bilagsposteringer** – En forespørgsel på bilagspostering åbnes, hvor du kan få vist posteringer. For at få vist transaktionerne i forespørgslen på bilagspostering skal du vælge dataene, der skal detaljeopløftes, og derefter klikke på **Åbne kontotransaktioner**.

Hvis dataene er budgetdata, kan du vælge at åbne budgetkontoposter. For at lukke et af niveauerne i rapporten og vende tilbage til det sted, hvor du startede, kan du enten trykke på Esc-tasten eller klikke på knappen **Luk** (**X**) i øverste højre hjørne.

## <a name="change-report-options"></a>Ændre rapportindstillinger
Du kan anvende attribut- og dimensionsfiltre eller ændre budgetscenariet for en rapport af typen **Faktisk vs. budget**. Klik i handlingsruden på **Rapportindstillinger**, og følg derefter et eller flere af disse trin:

-   Du kan anvende attributfiltre til en rapport ved at vælge **Tilføj et attributfilter**. Vælg attributten, skriv attributværdien, og klik derefter på **OK**. Hvis du f.eks. vælger attributten **Kontokategori**, skal du angive **SALG** som attributværdi. Hvis du vil fjerne et attributfilter, skal du klikke på **Ryd**.
-   Du kan anvende dimensionsfiltre på en rapport ved at vælge **Tilføj et attributfilter**. Vælg dimensionen, og derefter enten skriv dimension-ID'et, eller vælg dimensionen på listen. Hvis du vil fjerne et dimensionsfilter, skal du klikke på **Ryd**.
-   Hvis du vil ændre scenariet i en rapport af typen **Faktisk vs. budget**, Vælg et nyt scenario, og klik derefter på **OK**. Hvis det valgte scenarie er for et andet regnskabsår, fremkommer der ingen resultater. Hvis eksempelvis en rapport genereres for regnskabsåret 2015, og det aktuelle scenarie ligeledes er for regnskabsåret 2015, men det nye scenarie der vælges, er for regnskabsåret 2016, fremkommer der ingen resultater. Hvis der er behov for et nyt scenarie for et andet regnskabsår, skal du generere en ny version af rapporten for det regnskabsår, der er relateret til det pågældende scenarie.

Når du klikker på **OK**, anvendes alle de indstillinger, du har valgt til rapporten. Hvis du beslutter, at du ikke vil anvende de valgte indstillinger, skal du klikke på **Annuller**.

## <a name="update-a-financial-report"></a>Opdatere en økonomisk rapport
Du kan opdatere en økonomisk rapport, så den viser de nyeste data for den periode og år, som rapporten blev oprettet for. Hvis du eksempelvis opdaterer en økonomisk rapport, der blev genereret for oktober 2015, afspejler rapporten eventuelle nye transaktioner, der er bogført for oktober 2015. Hvis du vil opdatere en økonomisk rapport i handlingsruden, skal du klikke på **Opdater**. En opdateret rapport er kun tilgængelig for den person, der har opdateret den. Hvis andre skal kunne se samme data, skal rapporten publiceres.

## <a name="publish-a-financial-report"></a>Publicere en økonomisk rapport
Når du opdaterer en økonomisk rapport, kan du publicere den. Andre personer i organisationen vil derefter kunne se den. Hvis du vil publicere en rapport i handlingsruden, skal du klikke på **Publicer**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Få vist en økonomisk rapport i en anden valuta
En økonomisk rapport kan vises når som helst vises i enhver valuta. For at få vist en rapport i en anden valuta i handlingsruden skal du klikke på **Valuta** og derefter vælge en valuta. Rapporten er oversat til denne valuta, og resultaterne vises. Alle valutakoder eller -symboler, der er inkluderet som en del af rapportdesignet, opdateres for at afspejle den nye valuta. De valutaer, der vises på listen, er rapporteringsvalutaer, der er konfigureret i Finance.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Få vist en opsummeret oversigt over den økonomiske rapport
En økonomisk rapport kan indeholde detaljelinjerne og oversigtslinjer. Detaljelinjer er linjer, der indeholder hovedkontiene eller dimensionerne. Oversigts linjer er linjer til beskrivelse, total og beregning. For at få vist oversigtslinjerne i en rapport skal du klikke på **Vis** og derefter klikke på **Kun oversigtslinjer**. Rapporten er skjult og viser kun oversigtslinjerne. Klik for at se detaljelinjerne sammen med oversigtslinjerne, Klik på **Vis**, og klik derefter på **Kun oversigtslinjer** igen.

## <a name="print-a-financial-report"></a>Udskrive en økonomisk rapport
Ved udskrivning af en økonomisk rapport oprettes en PDF-fil, som du kan derefter udskrive manuelt. Hvis du vil oprette en økonomisk rapport, der kan udskrives, i handlingsruden, skal du klikke på **Udskriv**, og derefter følge en eller flere af disse trin for at angive udskriftsindstillingerne:

-   Når du vil medtage forskellige detaljeniveauer i den udskrevne rapport, skal du indstille skyderen til **Ja** eller **Nej**. Hvis en rapport bruger et rapporteringstræ, kan du vælge at medtage alle rapporteringsenheder eller blot den aktuelle rapporteringsenhed.
-   Vælg en sidestørrelse på listen for at angive sidestørrelsen.
-   Hvis du vil ændre sidelayout, skal du vælge et layout på listen. Hvis du vil have rapportens indhold til at passe til den bredde, du har valgt, kan du indstille skyderen til **Ja**.
-   Vil du indstille sidemargener, skal du skrive størrelsen på top, bund, venstre og højre margener i tommer.

Når du er færdig med at angive udskriftsindstillingerne, skal du klikke på **Udskriv** for at fortsætte. Du bliver spurgt, om du vil hente filen eller gemme filen til OneDrive eller SharePoint. Hvis du beslutter, at du ikke vil fortsætte, skal du i stedet klikke på **Annuller**. Når du fortsætter, begynder gengivelse af rapporten på serveren, og du bliver bedt om at hente rapporten i PDF-format. Du kan nu få vist rapporten i PDF-fremviseren, og herfra kan du vælge printeren, som rapporten skal sendes til, og foretage eventuelle yderligere reguleringer af udskriftsindstillingerne.

## <a name="export-a-financial-report"></a>Eksportere en økonomisk rapport
Hvis du vil eksportere en økonomisk rapport i handlingsruden, skal du klikke på **Publicer**. Rapporten eksporteres til Microsoft Excel, og browseren beder dig om at åbne eller gemme den eksporterede fil. De eksportindstillinger, der er defineret i rapportdesignet, anvendes til den eksporterede rapport.    

## <a name="additional-resources"></a>Yderligere ressourcer

[Økonomirapportering](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]