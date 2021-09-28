---
title: Omplacering af indtægtsføring
description: Dette emne indeholder oplysninger om omplacering, der giver organisationer mulighed for at genberegne omsætningspriser, når betingelserne for kontraktmæssige salg ændres. Den indeholder links til andre emner, der beskriver, hvordan du kan genkende indtægter i flere scenarier.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 53304842bdbe7dadb435ab3a0381f3835c2c443a
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487012"
---
# <a name="revenue-recognition-reallocation"></a>Omplacering af indtægtsføring

[!include [banner](../includes/banner.md)]

Omplacering giver organisationer mulighed for at genberegne omsætningspriser, når betingelserne for kontraktmæssige salg ændres. Med henblik på indtægtsføring betragtes salgsordredokumenterne som kontrakten.

Organisationen skal selv afgøre, om der kræves genplacering. Tilføjelse af en ny linje til en salgsordre eller tilføjelse af en ny salgsordre for en kunde udgør muligvis ikke en ændring af kontrakten. Følgende scenarier kan kræve genplacering:

- En kunde har føjet varer til en salgsordre eller fjernet varer fra salgsordren, efter at ordren er fuldt eller delvist faktureret.
- Flere salgsordrer, enten i bekræftet tilstand eller faktureret tilstand, blev angivet for samme forhandlede kontrakt.
- En kunde, der har returneret eller modtaget en kreditering for en vare, efter at den oprindelige salgsordre er fuldt eller delvist faktureret.

Der er nogle få vigtige begrænsninger på omplaceringsprocessen:

- Processen kan kun køres én gang. Det er derfor vigtigt, at du først kører den, når alle ændringer er afsluttet.

    - Denne begrænsning fjernes i udgivelse 10.0.17 og senere.

- Processen kan ikke køres på projektsalgsordrer.

    - Denne begrænsning fjernes i udgivelse 10.0.17 og senere.

- Hvis der er flere salgsordrer involveret, skal de være for samme debitorkonto.
- Alle salgsordrer, der er genallokeret, skal være i samme posteringsvaluta.
- Processen kan ikke tilbageføres eller fortrydes, efter at den er kørt.

    - Denne begrænsning fjernes i udgivelse 10.0.17 og senere.

- Der kan kun foretages genallokering for salgsordrer eller projektsalgsordrer. Den kan ikke foretages i en kombination af salgsordrer og projektsalgsordrer.

    - Denne begrænsning fjernes i udgivelse 10.0.17 og senere.

## <a name="set-up-reallocation"></a>Konfigurere genallokering

En parameter har indflydelse på genallokeringsprocessen.

Da der kan foretages omplacering på en salgsordre, som er delvist eller fuldt faktureret, skal eventuelle tidligere regnskabsposter for fakturaen rettes ved hjælp af de nye, omfordelte omsætningspriser. Denne rettelse kan du gøre ved at tilbagefør den oprindelige fakturas regnskabspost og bogføre en ny regnskabspost, der er baseret på de omfordelte omsætningspriser.

Alle organisationer skal beslutte, om rettelsen kun skal opdatere Finans, eller om den også skal opdatere Debitor. Den beslutning, der nås, bestemmer den relevante indstilling i **Bogfør fakturakorrektioner til debitor**-indstillingen under fanen **Indtægtsføring** på siden **Finansparametre** (**Indtægtsføring \> Opsætning \> Finansparametre**). Den relevante indstilling afhænger af det specifikke scenario. Du kan få flere oplysninger om mulige scenarier ved at bruge linkene i afsnittet [Scenarier til genplacering](#scenarios-for-reallocation) i dette emne.

[![Fanen Indtægtsføring på siden Finansparametre.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Hvis indstillingen **Bogfør fakturakorrektioner i Debitor** er angivet til **Ja**, giver genplaceringsprocessen følgende resultat:

- Der oprettes et kreditdokument i Debitor for at tilbageføre den faktura, der kræver rettelse.

    - Kreditdokumentet genbruger det oprindelige fakturanummer, men "-1" tilføjes.
    - Kreditdokumentet udlignes automatisk mod den oprindelige faktura. Hvis den oprindelige faktura allerede er udlignet med et andet kreditdokument eller en anden betaling, tilbageføres den pågældende udligning automatisk.
    - Kreditdokumentet bogføres i Finans for at tilbageføre den regnskabspost, der blev bogført på den oprindelige faktura. Posterne for lager og vareforbrug (COGS) tilbageføres dog ikke.

- Der oprettes en ny faktura, som er baseret på de nye, omallokerede prisbeløb i Debitor.

    - Den nye faktura genbruger det oprindelige fakturanummer, men "-2" tilføjes.
    - Den nye faktura udlignes automatisk mod alle kreditdokumenter eller betalinger, der tidligere er udlignet med den oprindelige faktura.
    - Den nye faktura bogføres i Finans ved hjælp af de nye omallokerede omsætningsprisbeløb. Det bogføres ikke på lager- og vareforbrugskontiene igen, da disse poster vedligeholdes for den oprindelige fakturas regnskabspost.

Hvis indstillingen **Bogfør fakturakorrektioner i Debitor** er angivet til **Nej**, giver genplaceringsprocessen følgende resultat:

- En post for tilbageførselsregnskabet bogføres kun i Finans. Alle regnskaber fra den oprindelige faktura tilbageføres, undtagen kontoposterne for lager og vareforbrug.
- En ny regnskabspost bogføres kun i Finans på baggrund af de nye omfordelte omsætningspriser. Det bogføres ikke på lager- og vareforbrugskontiene igen, da disse poster vedligeholdes for den oprindelige fakturas regnskabspost.
- Fakturaen på siden **Debitorposteringer** påvirkes eller ændres ikke, men den afspejler stadig den oprindelige regnskabspost. Der er ingen reference til tilbageførslen eller nye regnskabsposter.

Som det er blevet nævnt, kan du kun opdatere Finans, eller du kan opdatere både Finans og Debitor. Begge tilgange har fordele og ulemper. Det anbefales, at du evaluerer organisationens krav for at bestemme, hvilken indstilling du skal bruge. Hvis du opdaterer både Finans og Debitor, vises de korrekte regnskabsposter på den nye faktura og kan ses fra dokumentet på siden **Debitorposteringer**. Udligningsprocessen bruger desuden de opdaterede regnskabsposter til at bogføre evt. kasserabatter og gevinster eller tab. På den anden side vises kreditdokumentet og den nye faktura på kundekontoudtog og aldersfordelingsrapporter på samme måde som andre kreditdokumenter og debitorfakturaer. Beskrivelsen af disse dokumenter angiver, at de er oprettet via en regnskabsrettelse.

## <a name="run-the-reallocation-process"></a>Kør omfordelingsprocessen

Hvis du vil starte omfordelingsprocessen, skal du vælge **Omfordel pris med nye ordrelinjer** i en salgsordre, du skal allokere. Du kan også gå til **Indtægtsføring \> Periodiske opgaver \> omfordel pris med nye ordrelinjer** og derefter angive de relevante filtre, f.eks. debitorkontoen.

[![Genalloker pris med siden med nye ordrelinjer.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Det øverste gitter på siden **Alloker pris med nye ordrelinjer** kaldes **Salg**. Den viser en oversigt over salgsordrerne for kunden. Vælg de salgsordrer, der skal genallokeres. Hvis en salgsordre har et genallokerings-id, er den allerede blevet markeret til genallokering af en anden bruger. Hvis en eller flere salgsordrer tidligere er blevet genallokeret og skal medtages i en anden genallokering, skal tildelingen af disse salgsordrer først fortrydes. Den kan derefter medtages i en ny genallokering. Du kan finde mere detaljerede oplysninger i afsnittene [Fortryd en genallokering](#undo-a-reallocation) og [Genalloker flere gange](#reallocate-multiple-times) senere i dette emne.

Det nederste gitter på siden kaldes **Linjer**. Når du har valgt en eller flere salgsordrer i gitteret **Salg**, viser gitteret **Linjer** salgsordrelinjerne. Vælg de salgsordrelinjer, der skal ændres. Hvis du kun har valgt én salgsordre, skal linjerne i den samme salgsordre genallokeres. Denne situation kan forekomme, når en af salgsordrelinjerne tidligere er faktureret, og derefter er tilføjet en ny linje, eller en eksisterende linje er fjernet eller annulleret. Hvis en linje er blevet fjernet, vises den ikke i gitteret. Det kan derfor ikke vælges. Det tages dog stadig i betragtning, når der køres en omplaceringsproces.

Når du er færdig med at vælge de nødvendige salgsordrelinjer, kan du bruge knapperne i handlingsruden som beskrevet her:

- **Opdater genplacering** - Beregn de nye omsætningsprisbeløb for de valgte salgsordrelinjer. Hvis en linje er blevet fjernet eller annulleret, udføres genplaceringen kun for de eksisterende linjer, du har valgt. I følgende illustration vises et eksempel på salgsordrelinjer, inden genplaceringen opdateres.

    [![Salgsordrelinjer, før genplaceringen opdateres.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    De nye omsætningsprisbeløb vises i kolonnen **Omallokeret beløb** i **Linjer**-gitteret. På dette tidspunkt er omplaceringen behandlet, men den er endnu ikke beregnet. I følgende illustration vises et eksempel på salgsordrelinjer, når genplaceringen er opdateret.

    [![Salgsordrelinjer efter genplaceringen opdateres.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Proces** – Bearbejd eller bogfør de genallokerede omsætningspriser. Når du har valgt denne knap, kan du ikke tilbageføre omplaceringen. Hvis du ikke har valgt **Opdater genplacering**, før du vælger **Proces**, køres omplaceringen automatisk.

    - Hvis der ikke er faktureret en salgsordrelinje, opdateres omsætningsprisbeløbene på eventuelle salgsordrer, der er valgt til genplacering.
    - Hvis en eller flere salgsordrelinjer er faktureret, vil regnskabsposterne blive rettet, og eventuelle detaljer i omsætningsplanen, der er oprettet for den fakturerede salgsordrelinje, bliver rettet.

- **Forventet bilag** - Se en prøveversoin af de regnskabsposter, der er oprettet for eventuelle salgsordrelinjer, der er faktureret. Hvis der ikke er faktureret linjer, vises intet. Hvis du ikke har valgt **Opdater genplacering**, før du vælger **Forventet bilag**, køres omplaceringen automatisk.
- **Omplacering af omsætning** - Åbn en side, der viser fordeling af omsætningspris for alle de valgte linjer. Du kan ikke ændre oplysningerne på siden. Den viser de linjebeløb, der blev brugt til omplaceringen.

    [![Linjebeløb, der blev brugt til omplacering.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Nulstil data for den valgte debitor** – Hvis omplaceringsprocessen er startet, men ikke er fuldført, skal du kun rydde dataene i tabellen med genplaceringer for den valgte debitor. Du kan f.eks. markere flere salgsordrelinjer til omplacering, lade siden være åben uden at vælge **Proces**, og derefter får siden timeout. I dette tilfælde forbliver salgsordrelinjerne markeret og vil ikke være tilgængelige for en anden bruger til at fuldføre genplaceringsprocessen. Siden kan også være tom, når den åbnes. I denne situation kan knappen **Nulstil data for den valgte debitor** bruges til at rydde ubehandlede salgsordrer, så en anden bruger kan fuldføre genallokeringsprocessen.

## <a name="undo-a-reallocation"></a>Fortryde en genallokering

En genallokering fortrydes ved at køre en anden genallokering. Genallokeringen udføres igen, og brugeren vælger forskellige salgsordrelinjer, der skal medtages i den anden genallokeringsproces.

Hvis der er foretaget en genallokering på tværs af to eller flere separate salgsordrer, kan du fortryde den ved at vælge **Genalloker pris med nye ordrelinjer** fra en salgsordre, der er inkluderet i genallokeringen. Du kan ikke gå til **Indtægtsføring \> Periodiske opgaver \> Genalloker pris med siden med nye ordrelinjer** for at ændre genallokeringen med nye ordrelinjer, da den side, der åbnes på denne måde, kun viser salgsordrer, der ikke har et genallokerings-id. Genallokerings-id'et tildeles, når dokumentet er blevet genallokeret.

På siden **Genalloker pris med nye ordrelinjer** skal du fjerne markeringen af eventuelle salgsordrer, der skal udelades fra den kontraktmæssige aftale. Brug de relevante knapper i handlingsruden, f.eks. **Opdater genallokering** og **Proces**, til at behandle genallokeringen. Hvis alle salgsordrer bortset fra den aktive salgsordre ikke er markeret, fjernes genallokerings-id'et, når ændringen er behandlet.

Hvis der er foretaget en genallokering ved at føje en ny linje til en komplet eller delvist faktureret salgsordre, kan den egentlige genallokering kun fortrydes ved at fjerne linjen fra salgsordren og derefter køre genallokeringen igen. Salgsordrelinjen skal fjernes, da alle linjer i en salgsordre antages at være en del af samme kontrakt. Du kan ikke fjerne markeringen af en salgsordrelinje, mens du arbejder på siden **Genalloker pris med nye ordrelinjer**.

## <a name="reallocate-multiple-times"></a>Genallokere flere gange

Der kan foretages flere genallokeringer i forhold til samme salgsordre, hvis der er foretaget flere ændringer i kontrakten. Hver genallokering udløser tildelingen af et genallokerings-id til salgsordren eller salgsordregruppen for at gruppere ændringerne sammen. Hvis der udføres flere genallokeringer, bruger hver ekstra genallokering det samme genallokerings-id som den første genallokering.

Salgsordre 00045 angives f.eks. og har flere linjer. Når salgsordren er fuldt faktureret, føjes der en ny salgsordrelinje til den. Genallokeringen køres derefter ved at åbne siden **Genalloker pris med nye ordrelinjer** fra salgsordre 00045 eller ved at gå til **Indtægtsføring \> Periodiske opgaver \> Genalloker pris med nye ordrelinjer**. Genallokerings-id'et **Reall000001** tildeles salgsordren.

Der oprettes endnu en salgsordre, 00052, for den samme kontrakt. Genallokeringen kan køres igen ved at åbne siden **Genalloker pris med nye ordrelinjer** fra salgsordre 00045, men ikke fra salgsordre 00052. Hvis du åbner siden **Genalloker pris med nye ordrelinjer** fra salgsordre 00052, vises salgsordre 00045 ikke, da der er tildelt et genallokerings-id til den. På siden vises kun salgsordrer, der ikke har et genallokerings-id.

Den anden genallokering kan foretages på to måder. Du kan fortryde genallokeringen af salgsordre 00045. I dette tilfælde fjernes genallokerings-id'et, og du kan derefter udføre genallokeringen fra salgsordre 00045 eller salgsordre 00052. Du kan også åbne siden **Genalloker pris med nye ordrelinjer** fra salgsordre 00045 og tilføje den anden salgsordre. Når genallokeringen er behandlet, tildeles genallokerings-id **Reall000001** til salgsordre 00045 og salgsordre 00052.

## <a name="scenarios-for-reallocation"></a>Scenarier for genallokering

Følgende emner gennemgår forskellige scenarier for indtægtsføring:

- [Omplacering af indtægtsføring – Eksempel 1](rev-rec-reallocation-scenario-1.md) - Der angives to salgsordrer, men de er kun bekræftet. Det samme scenario giver lignende resultater, hvis mere end to salgsordrer er i bekræftet tilstand.
- [Omplacering af indtægtsføring – Eksempel 2](rev-rec-reallocation-scenario-2.md) - Der angives to salgsordrer, og kunden føjer en vare til kontrakten, efter at den første salgsordre er faktureret.
- [Omplacering af indtægtsføring – Eksempel 3](rev-rec-reallocation-scenario-3.md) - Der føjes en ny linje til en eksisterende faktureret salgsordre.
- [Omplacering af indtægtsføring - Eksempel 4](rev-rec-reallocation-scenario-4.md) - Der fjernes en linje fra en eksisterende delvist faktureret salgsordre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
