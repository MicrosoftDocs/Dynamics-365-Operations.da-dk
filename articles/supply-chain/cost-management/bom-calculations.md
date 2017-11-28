---
title: Styklistekalkulationer
description: Beregningerne af den opsummerede kostpris og salgsprisen kaldes styklistekalkulationer, og du starter dem fra siden Beregninger. Dette emne indeholder oplysninger om styklistekalkulationer.
author: AndersGirke
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, SalesQuotationTable, SalesTable, SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad00a3b5e41892aaa705fd8eafa52cc199e1d806
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="bom-calculations"></a>Styklistekalkulationer

[!include[banner](../includes/banner.md)]


Beregningerne af den opsummerede kostpris og salgsprisen kaldes styklistekalkulationer, og du starter dem fra siden Beregninger. Dette emne indeholder oplysninger om styklistekalkulationer.

Beregningerne af den opsummerede kostpris og salgsprisen kaldes styklisteberegninger, og du starter dem fra siden **Beregninger**. Du skal bruge siden **Beregninger** til at udføre følgende opgaver:

-   Beregne en produceret vares kostpris og oprette en tilknyttet kostprispost for en vare i en efterkalkulationsversion.
-   Beregne salgsprisen for produceret vare og oprette en tilknyttet salgsprispost i en efterkalkulationsversion.

Siden **Beregninger** bruges på forskellige måder, afhængigt af hvordan du starter styklisteberegningerne. Din brug af siden **Beregninger** afhænger også af, om styklisteberegningerne omfatter en efterkalkulationsversion for standardomkostninger eller planlagte omkostninger, og af flere regler, der er defineret i den efterkalkulationsversion, som bruges i styklisteberegningerne. **Bemærk!** En variant af siden **Beregninger** bruges sammen med en linjevare i en salgsordre, et salgstilbud eller en serviceordre. Disse beregninger kaldes ordrespecifikke styklistekalkulationer. En ordrespecifik styklistekalkulation genererer ikke en vareomkostningspost i en efterkalkulationsversion. I stedet genereres en kalkulationspost, som vises på siden **Oplysninger om styklisteberegning**. Beregningsposten omfatter en beregnet kostpris og en beregnet salgspris. Siden **Beregninger** kan åbnes for en enkelt produceret vare eller for en efterkalkulationsversion.

-   Hvis du vil beregne omkostninger for en enkelt produceret vare, skal du starte styklistekalkulationer fra siden **Varepris**. Siden **Beregninger** arver vareidentifikatoren. Efterkalkulationversionen, styklisteversionen, ruteversionen, kalkulationsantallet, beregningsdatoen og det sted, der skal angives.
    -   Som standard er styklisteversionen og ruteversionen indstillet til de aktive versioner for vare, lokation, dato og kalkulationsantal. Du kan dog tilsidesætte standardværdierne med godkendte versioner.
    -   Som standard er kalkulationsantallet indstillet til varens standardordreantal. Du kan dog tilsidesætte standardværdien.
    -   Beregningsdatoen eller lokationen kan vælges af efterkalkulationsversionen, eller der kan angives brugerspecifikke værdier, når datoen eller lokationen ikke er valgt i efterkalkulationsversionen. En fremtidig beregningsdato bestemmer, hvordan ventende kostprisposter bruges. Styklistekalkulationer bruger en ventende kostprispost, der har den nærmeste fra-dato, som er på eller før beregningsdatoen.
-   For at beregne kostpriser for alle producerede varer eller for bestemte varer eller for at opdatere varer, efterhånden som de bruges, skal du starte styklistekalkulationerne fra siden **Opsætning af efterkalkulationsversion** eller siden **Vedligeholdelse af efterkalkulationsversion**. Siden **Beregninger** arver efterkalkulationsversionen.
    -   I beregningerne antages det, at den aktive styklisteversion og ruteversionen bruges for en produceret vare (og for den tilknyttede lokation, dato og antal), medmindre der er angivet en understykliste eller underrute for en produceret komponent.
    -   For beregningerne antages det, at standardordreantallet bruges til producerede varer. Standardordreantallet danner grundlag for beregning af komponentantal og definerer de relevante styklisteversioner og ruteversioner (når du bruger antalsfølsomme styklister og ruter) og afskriver konstante omkostninger. Når en produceret komponent har en styklistelinje af typen **Produktion** eller **Kreditor**, eller når du bruger en fremstil til ordre-udfoldningstilstand for styklistekalkulationerne, anvendes denne antagelse ikke, da antal afspejler det angivne beregningsantal.
    -   Beregningsdatoen eller lokationen kan vælges af efterkalkulationsversionen, eller der kan angives brugerspecifikke værdier, når datoen eller lokationen ikke er valgt i efterkalkulationsversionen.

Andre variationer i styklistekalkulationer afspejler efterkalkulationstypen og begrænsninger i efterkalkulationsversionen:

-   Styklistekalkulationer, som bruger standardomkostninger, skal begrænses af regler for efterkalkulationsversionen, da begrænsningerne er med til at sikre, at der anvendes standardprincipper for efterkalkulation. Standardprincipper for efterkalkulation kræver, at begrænsninger gennemtvinges, hvad angår brugen af standardomkostninger for købte varer, en udfoldningstilstand med ét niveau og medtagelsen af tillæg i enhedskostpriser.
-   Styklistekalkulationer, som bruger planlagte omkostninger, behøver ikke at følge standardprincipperne for efterkalkulation. Disse styklisteberegninger kan bruge forskellige udfoldningstilstande, alternative kilder til kostprisdata for købte varer og valgfri gennemtvingelse af begrænsninger i efterkalkulationsversionen.

### <a name="bom-calculations-that-use-standard-costs"></a>Styklistekalkulationer, som bruger standardomkostninger

Regler i efterkalkulationsversionen (for standardomkostninger) kan medføre, at fem regler for styklisteberegning gennemtvinges. Indstillingen **Begrænsning i registrering** i efterkalkulationsversionen medfører brugen af disse regler, mens tillæg skal medtages i enhedsprisen. Tillæg for købte varer kan angives manuelt, mens tillæg for producerede varer afspejler den beregnede afskrivning af konstante omkostninger. Indstillingen **Begrænsning i registrering** i efterkalkulationsversionen medfører brugen af fire andre regler for styklistekalkulation.

-   Kilden til kostbidragene for købte varer skal baseres på standardomkostninger. Styklistekalkulationer skal med andre ord bruge kostprisposten for varen i den angivne efterkalkulationsversion eller i det beredskab, der indeholder standardomkostningerne.
-   Udfoldningstilstanden skal være et enkelt niveau som hjælp til at sikre en præcis og ensartet beregning af standardomkostninger.
-   Avanceindstillingen skal vælges som en hjælp til at opnå ensartede resultater, når varens salgspris beregnes. Avanceindstillingen kan kun anvendes, og salgsprisposterne for varen kan kun oprettes, hvis efterkalkulationsversionen kan indeholde salgspriser.
-   Reservestatussen skal vælges og kan indstilles til **Ingen**, **Aktiv** (for aktive kostprisposter) eller **Efterkalkulationsversion** (for en angivet efterkalkulationsversion).

### <a name="bom-calculations-that-use-planned-costs"></a>Styklistekalkulationer, som bruger planlagte omkostninger

Regler i efterkalkulationsversionen (for planlagte omkostninger) kan indstilles til at medføre, at fem regler for styklisteberegning gennemtvinges. Politikkerne kan også bare angive standardværdier. Indstillingen **Begrænsning i registrering** i efterkalkulationsversionen bestemmer, om regler for styklistekalkulation i forbindelse med tillæg vælges eller fungerer som en standardværdi. Det er valgfrit, om tillæg skal medtages i enhedsprisen. Indstillingen **Begrænsning i registrering** i efterkalkulationsversionen bestemmer, om de andre fire regler for styklistekalkulation vælges eller fungerer som standardværdier.

-   Kilden til kostbidraget for en indkøbt vare kan være kostprisposten for varen i en efterkalkulationsversion. Kilden kan også defineres af den styklistekalkulationsgruppe, der er tildelt til varen. Styklistekalkulationsgruppen kan f.eks. definere samhandelsaftaler om indkøbspriser som kilden til kostbidragsdataene.
-   Udfoldningstilstanden kan være med et enkelt niveau, flere niveauer eller fremstilling til ordre, eller den kan baseres på linjevaren på styklisten. Udfoldningstilstanden for linjevaren på styklisten replikerer omkostningsberegningslogikken for forkalkulerede produktionsordrer.
-   Avanceindstillingen kan vælges, eller den kan være en standardværdi. Avanceindstillingen kan kun anvendes, og salgsprisposterne for varen kan kun oprettes, hvis efterkalkulationsversionen kan indeholde salgspriser.
-   Reserveprincippet kan vælges, eller det kan være en standardværdi. Reservestatussen kan indstilles til **Ingen**, **Aktiv** (for aktive kostprisposter) eller **Efterkalkulationsversion** (for en angivet efterkalkulationsversion).

Under styklisteberegninger oprettes advarsler og andre typer meddelelser. Flere regler om styklistekalkulation bestemmer typerne af meddelelser. Advarselssituationerne er defineret i den styklistekalkulationsgruppe, som er tildelt varerne. Du kan dog tilsidesætte disse advarselssituationer, når du starter en styklistekalkulation. Når der bruges reservestatus, er det ofte en god ide, at reserveoplysningerne vises som en meddelelse med oplysninger. Når du forsøger at opdatere beregnede kostpriser for varer, der har manglende kostprisposter, er det også en god ide, hvis meddelelsen med oplysninger identificerer elementer, der ikke er opdateret.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Styklistekalkulationer ud fra reserveprincippet
Følgende situationer er eksempler på to forskellige anvendelser af beredskabsprincippet:

-   **Metode med to versioner for opdaterede standardomkostninger** − En efterkalkulationsversion kan indeholde trinvise ændringer til standardomkostninger, f.eks. ventende omkostningsposter, der afspejler de nye ændringer til vare eller omkostning. I denne situation, kan det være en fordel at anvende beredskabsprincippet til at identificere de aktive standardomkostninger, der er indeholdt i andre efterkalkulationsversioner.
-   **Simulering af effekten af omkostningsændringer ved hjælp af planlagte omkostninger** - En efterkalkulationsversion for planlagte omkostninger kan indeholde trinvise ændringer til brug ved simulering. Denne omkostningsversion indeholder ventende omkostningsposter, der afspejler de simulerede omkostningsændringer til varer, omkostningsarter og beregningsformler til indirekte omkostninger. I denne situation, kan det være en fordel at anvende beredskabsprincippet til at identificere de aktive standardomkostninger, der er indeholdt i andre efterkalkulationsversioner.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Styklistekalkulation af en foreslået salgspris
Når du bruger en beregning af omkostninger plus avance afspejler den beregnede salgspris for en vare de procentdele for avancesæt, der er angivet for styklistekalkulationen, og de omkostninger, der er knyttet til varens komponentvarer, ruteoperationer og de gældende indirekte produktionsomkostninger. Avancen afspejler de procentdele for avancesæt, der tildeles til kostprisgrupper og de kostprisgrupper, der er tildelt til varer, omkostningskategorier for ruteoperationer og formler til beregning af indirekte omkostninger for indirekte produktionsomkostninger. Procentdelene for avancesæt kaldes **Standard**, **Avance 1**, **Avance 2** og **Avance 3**. I sættet Avance 1 kan der f.eks. defineres en procentdel for avancesæt på 50 procent for en kostprisgruppe, der er tildelt til købt materiale, og der kan defineres en procentdel for avancesæt på 80 procent for en kostprisgruppe, der er tildelt til omkostningskategorier for ruteoperationer. Styklistekalkulationens kontekst bestemmer, hvordan resultaterne af en beregnet salgspris håndteres:

-   **Styklistekalkulation for en vare og en angivet efterkalkulationsversion** − Under styklistekalkulationen oprettes der en ventende salgsprispost i efterkalkulationsversionen. Denne salgsprispost udgør startpunktet for visning af kalkulationsdetaljer (f.eks. på siden **Beregn varens kostpris**). Salgsprisposten fungerer primært som referenceoplysninger og bruges ikke som udgangspunkt for en salgspris på salgsordrer.
-   **Ordrespecifik styklistekalkulation** − En varians af siden **Styklistekalkulation** bruges sammen med en vare på en linje i en salgsordre, et salgstilbud eller en serviceordre. Med en ordrespecifik styklistekalkulation genereres der ikke en omkostningspost i en efterkalkulationsversion. I stedet genereres en kalkulationspost, som vises på siden **Resultater af styklistekalkulation**. Denne kalkulationspost udgør startpunktet for visning af kalkulationsdetaljer (f.eks. på siden **Beregn varens kostpris**). Oplysninger om en valgt kalkulationspost kan overføres til det oprindelige linjeelement. Den beregnede salgspris kan for eksempel overføres til et salgsordrelinjeelement.

## <a name="order-specific-bom-calculations"></a>Ordrespecifikke styklistekalkulationer
En ordrespecifik styklistekalkulation repræsenterer en variant af en styklistekalkulation for en fremstillet vare. Den ordrespecifikke styklistekalkulation udføres til en linjevare i en salgsordre, et salgstilbud eller en serviceordre. En ordrespecifik styklistekalkulation genererer en kalkulationspost, der vises på siden **Resultater af styklistekalkulation**. Kalkulationsposten indeholder en beregnet vægt, en beregnet omkostning, der er baseret på omkostninger til aktive poster, og en beregnet salgspris. Kalkulationsposten, som hver ordrespecifikke styklistekalkulation for en vare genererer på siden **Resultater af styklistekalkulation** identificeres entydigt med et kalkulationsnummer. Resultaterne af en kalkulationspost kan også overføres til den oprindelige varelinje. En ordrespecifik styklistekalkulation adskiller sig fra en styklistekalkulation for en produceret vare på to måder:

-   En ordrespecifik styklistekalkulation genererer ikke en vareomkostningspost i en efterkalkulationsversion. Derfor anvendes reglerne for styklistekalkulation ikke, når der oprettes en vareomkostningspost, eller når en omkostningspost overskrives.
-   En ordrespecifik styklistekalkulation bruger altid aktive omkostningsposter for komponenter, omkostningskategorier og beregningsformler for indirekte omkostninger.






