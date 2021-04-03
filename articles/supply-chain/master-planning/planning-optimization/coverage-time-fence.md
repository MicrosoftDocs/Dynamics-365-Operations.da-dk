---
title: Disponeringstidshorisonter
description: Dette emne beskriver, hvordan disponeringstidshorisonter defineres, når du bruger Planlægningsoptimering. En disponeringstidshorisont angiver planlægningshorisonten og -grænsen.
author: ChristianRytt
manager: tfehr
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2b52a49109274c9be9ed8aa069517b175ea6281c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501312"
---
# <a name="coverage-time-fences"></a>Disponeringstidshorisonter

Dette emne beskriver, hvordan *disponeringstidshorisonter* defineres, når du bruger Planlægningsoptimering. Planlæggere kan definere planlægningshorisonten (disponeringstidshorisonten i dage) og udelukke udbud og efterspørgsel, der ligger uden for denne tidshorisont. Derfor medvirker disponeringstidshorisonter til at forhindre "støj", der forårsages af forsyningsforslag, som du ikke behøver at reagere på i flere måneder. Dette kan f.eks. omfatte prognose- og kundeordrer for næste år, som ligger langt ud over den normale gennemløbstid.

En disponeringstidshorisont er det antal dage efter dags dato (eller mere præcist den dato, hvor planlægningen køres), hvor udbud og efterspørgsel udelukkes. Hvis du vil undgå forsinkelser, skal du sikre dig, at disponeringstidshorisonten er længere end den samlede leveringstid. Systemets standardværdi er 100 dage.

Du kan angive en disponeringstidshorisont på hvert af følgende niveauer:

- **Disponeringsgruppe** – Du kan angive en standarddisponeringstidshorisont for hver disponeringsgruppe.
- **Varedisponering** – Du kan tilsidesætte den disponeringstidshorisont, der nedarves fra den disponeringsgruppe, der er knyttet til en vare.
- **Behovsplan** – Du kan tilsidesætte de disponeringstidshorisonter, der nedarves fra disponeringsgruppen og indstillingerne for varedisponering.

I følgende afsnit forklares, hvordan du kan angive en disponeringsgruppe på hvert niveau.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Angive en disponeringstidshorisont for en disponeringsgruppe

Når du angiver en disponeringstidshorisont for en disponeringsgruppe, gælder indstillingen for alle varer (produkter), der tilhører den pågældende gruppe. Du kan dog tilsidesætte indstillingen for bestemte varer eller specifikke behovsplaner.

Hvis du vil angive en disponeringstidshorisont for en disponeringsgruppe, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Dækningsgrupper**.
1. Vælg en eksisterende disponeringsgruppe på listen, eller opret en ny disponeringsgruppe.
1. I oversigtspanelet **Generelt** skal du angive feltet **Disponeringstidshorisont (dage)** til det antal dage, du vil bruge som disponeringstidshorisont for disponeringsgruppen.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Angive en disponeringstidshorisont for en bestemt vare

Hver vare (produkt) tilhører en disponeringsgruppe. Hvis der ikke udtrykkeligt er tildelt en disponeringsgruppe til en vare, anvendes en standarddisponeringsgruppe. Hver vare nedarver en disponeringstidshorisont fra disponeringsgruppen. Du kan dog tilsidesætte denne tidshorisont for bestemte varer efter behov.

Hvis du vil angive en disponeringstidshorisont for en bestemt vare, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg et produkt i gitteret.
1. Vælg **Varedisponering** i gruppen **Disponering** under fanen **Planlæg** i handlingsruden.
1. På siden **Varedisponering** under fanen **Oversigt** skal du markere eller oprette en række til det sted, hvor du vil angive en disponeringstidshorisont.
1. Vælg fanen **Generelt** for at åbne indstillingerne for det valgte sted.
1. Markér afkrydsningsfeltet **Tilsidesæt indstillinger for disponeringsgruppe**.
1. Angiv feltet **Disponeringstidshorisont (dage)** til det antal dage, du vil bruge som disponeringstidshorisont for varen.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Angive en disponeringstidshorisont for en bestemt behovsplan

Du kan angive en disponeringstidshorisont på hvert behovsplanniveau. På denne måde kan du definere det antal dage, som beregningerne i behovsplanlægningen dækker for en behovsplan. Denne indstilling tilsidesætter eventuelle indstillinger for disponeringstid, der er defineret for hver relevant vare og disponeringsgruppe.

Hvis du vil angive en disponeringstidshorisont for en behovsplan, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en eksisterende behovsplan på listen, eller opret en ny behovsplan.
1. Angiv indstillingen **Disponering** til **Ja** i oversigtspanelet *Tidshorisonter i dage*. Angiv i feltet under indstillingen det antal dage, du vil bruge som disponeringstidshorisont for behovsplanen.

## <a name="considerations-for-coverage-time-fences"></a>Overvejelser omkring disponeringstidshorisonter

Når du konfigurerer disponeringstidshorisonter, skal du overveje følgende:

- Disponeringstidshorisonter påvirker kun inputdata til varedisponering. Hvis der indtræffer forsinkelser, kan ordreforslag som resultat have en dato, der ligger efter dags dato plus disponeringstidshorisonten.
- Disponeringstidshorisonter angives i kalenderdage. Kalendere, der bruger arbejdsdage, påvirker ikke beregningen af tidshorisonten. En uge betragtes f.eks. altid som syv dage, også selvom weekenderne er konfigureret som lukkede dage i arbejdstidskalenderen.
- Behovstransaktioner genereres ikke for noget behov og efterspørgsel, der ligger uden for disponeringstidshorisonten.
- Hvis godkendt behov og efterspørgsel falder uden for disponeringstidshorisonten, indlæses den ikke i programmet. Derfor udløser den ikke genopfyldninger, og der beregnes ikke forsinkelser. Dette udbud og efterspørgsel bør dog ikke fjernes fra systemet.
- Variationer i sikkerhedslagermængder (fra minimumnøgler) ignoreres, hvis de falder uden for disponeringstidshorisonten.
- Internt behov ignoreres, hvis den ønskede afsendelsesdato, der beregnes, ikke er inden for disponeringstidshorisonten. Bemærk, at den interne efterspørgsel i forbindelse med indbygget varedisponering ikke er begrænset til disponeringstidshorisonten.
- Behovsprognoser ignoreres, hvis budgetdatoen ikke ligger inden for disponeringstidshorisonten. Bemærk, at behovsprognoser for indbygget varedisponering ikke er begrænset til disponeringstidshorisonten.
- Planlægningsoptimering er tidszonebaseret. Den tager højde for tidszonen på udbuds- og efterspørgselsstederne samt tidspunktet for planlægningskørslen. Varedisponering udløses f.eks. den 15. oktober kl. 11 fra et sted i Danmark (GMT+1 tidszone), og der bruges en disponeringstidshorisont på ti dage. I dette tilfælde medtages behov og efterspørgsel fra et sted i Seattle (GMT-8 tidszone) indtil 25. oktober kl 2 (= ti 24-timers dage efter, at varedisponering blev udløst, minus tidszonedifferencen på ni timer). Bemærk, at det indbyggede varedisponeringsprogram kun tager højde for datoen i tidshorisonten. Resultatet kan derfor variere.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]