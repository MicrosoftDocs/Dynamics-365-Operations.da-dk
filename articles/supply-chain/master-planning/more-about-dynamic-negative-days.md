---
title: Negative dage og dynamiske negative dage
description: Dette emne giver oplysninger om negative dage og dynamiske negative dage, og hvordan du kan bruge dem til at hjælpe din virksomhed.
author: t-benebo
manager: tfehr
ms.date: 06/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea21134fd45cfd284297e778a96789f329f379c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264036"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negative dage og dynamiske negative dage

[!include [banner](../includes/banner.md)]

Dette emne giver oplysninger om negative dage og dynamiske negative dage, og hvordan du kan bruge dem til at hjælpe din virksomhed. *Tidshorisont for negative dage* repræsenterer det antal dage, du er villig til at vente, før du bestiller en ny genopfyldning, når du har negativ lagerbeholdning.

I dette emne får du følgende oplysninger:

- Hvordan ordreforslag oprettes
- Korrelationen mellem tidshorisonten for negative dage og varens leveringstid
- Hvordan tidshorisonent for dynamiske negative dage beregnes, og hvordan varens leveringstid indregnes i beregningen
- Hvordan du fortolker [forslagene til forbedring af kørselstiden for materialebehovsplanlægning (MRP) (varedisponering)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx), der er relateret til negative dage

I dette emne anvendes tre hypotetiske scenarier, der kan hjælpe dig med at forstå disse oplysninger. Forskellen mellem scenarierne er det tidspunkt, hvor du får behov: før, under eller efter varens leveringsperiode.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Scenarie 1: Du får behov før varens leveringsperiode

Du kan få behov enten relativt tidligt i leveringstiden for varen, eller umiddelbart før leveringstiden begynder. Her er et eksempel på dette scenarie:

- DemoProduct-varen har en indkøbsleveringstid på seks.
- På dag nul (1. januar) er lagerbeholdningsniveauet for DemoProduct-varen 0 (nul).
- På dag nul (1. januar) får du en salgsordre på 10 stk. af DemoProduct-varen.
- På dag syv (7. januar) findes der en eksisterende indkøbsordre på 10 stk. af DemoProduct-varen.

I følgende illustration vises en grafisk visning af dette scenarie.

![Grafisk visning af scenarie 1](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Eksempel A: Negative dage er mindre end varens leveringstid

Hvis du angiver de negative dage som et tal, der er mindre end varens leveringstid, søger MRP efter tilgange for DemoProduct-varen inden for tidshorisonten for negative dage. Da der ikke findes nogen tilgange, opretter MRP et nyt indkøbsordreforslag. Dette ordreforslag forsinkes straks med seks dage (leveringstiden). Den vil derfor blive modtaget d. 7. januar. Den eksisterende indkøbsordre får handlingsmeddelsen **Annuller**, fordi oprettelsen af det nye indkøbsordreforslag er blevet overflødigt.

I følgende illustration vises et skærmbillede af dette eksempel.

![Skærmbillede for eksempel A til scenarie 1](./media/negative-days-2.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel A til scenarie 1](./media/negative-days-3.png)

Hvis du betragter MPS-performance og planlægger nervøsitet, fungerer dette eksempel ikke godt. MRP skal oprette et nyt ordreforslag og skal beregne forsinkelser og handlinger. Disse opgaver tager lang tid. I dette eksempel føjes der også to yderligere transaktioner til planen. Salgsordren bliver på den anden side kun forsinket med seks dage, ikke syv dage.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Eksempel B: Negative dage er mere end varens leveringstid

For at forbedre MPS-performance kan du angive negative dage til et tal, der er større end varens leveringstid. Da du ikke kan få forsyningen inden for leveringstiden i dette scenarie, kan du søge efter tilgange, så længe denne søgning giver mening. Selvom kørselstiden for MRP vil være kortere, bør du holde øje med yderligere forsinkelser for ordrerne.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Eksempel C: Korreler automatisk varens leveringstid med tidshorisonten for negative dage

Hvis du automatisk vil korrelere varens leveringstid med tidshorisonten for negative dage, skal du bruge dynamiske negative dage. Hvis du vil bruge dynamiske negative dage, skal du til  **Varedisponering \> Opsætning \> Varedisponeringsparametre** og derefter gå til fanen **Generelt** i sektionen **DisponeringBrug** og angive indstillingen **Brug dynamiske negative dage** til **Ja**. MRP søger derefter efter tilgange inden for tidshorisonten for de dynamiske negative dage. Denne tidshorison beregnes ved hjælp af følgende formel:

Tidshorison for dynamiske negative dage = Leveringstid for indkøb + Tidshorison for negative dage + (aktuel dato – behovsdato)

(Hvis standardordretypen for DemoProduct-varen er **Produktion** eller **Overførsel**, er leveringstiden den samme som leveringstiden for **lagerbeholdning**).

Når der bruges dynamiske negative dage, er den tidshorisont, som MRP leder efter for tilgange, nu 6 + 2 + 0 = 8 dage. MRP finder den eksisterende indkøbsordre og fastfryser salgsordren mod den. Ingen nye ordreforslag oprettes. Derfor er kørselstiden for MRP kortere. I den følgende illustration vises nettobehovet for DemoProduct-varen.

![Nettokrav til eksempel C i scenarie 1](./media/negative-days-4.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel C til scenarie 1](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Eksempel D: Brug kun dynamiske negative dage

Hvis du angiver de negative dage til **0** (nul) og kun bruger tidshorisonten for dynamiske negative dage, er tidshorisonten for dynamiske negative dage 6 + 0 + 0 = 6 dage. I dette tilfælde er resultatet det samme som resultatet eksempel A for dette scenario. MRP skal oprette et nyt ordreforslag og skal beregne forsinkelser og handlinger. Disse opgaver er tidskrævende og kan også være frustrerende. Der er også to flere transaktioner, der skal behandles. Da efterspørgslen ikke kan udføres til tiden, for den vare, der skal ankomme, giver dette eksempel unødvendige komplikationer i forhold til din plan.

I følgende illustration vises et skærmbillede af dette eksempel.

![Skærmbillede for eksempel D til scenarie 1](./media/negative-days-6.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel D til scenarie 1](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Eksempel E: Brug både negative dage, som er større end varens leveringstid og tidshorisonten for de dynamiske negative dage

Hvis du angiver de negative dage et tal, der er større end varens leveringstid, og hvis du også bruger tidshorisonten for dynamiske negative dage, er tidshorisonten for dynamiske negative dage 6 + 6 + 0 = 12 dage. Denne fremgangsmåde kan resultere i en meget lang tidshorisont, som MRP skal søge efter resultater i. Du kan få oplysninger om, hvordan eksempel E er relateret til en situation, hvor du angiver de negative dage til en lang tidshorisont, under afsnittet [Konklusion](#conclusion) i dette emne.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Scenarie 2: Du får behov under varens leveringsperiode

Der kan opstå et behov på et tidspunkt i løbet af varens leveringstid. Her er et eksempel på dette scenarie:

- DemoProduct-varen har en indkøbsleveringstid på seks. 
- På dag nul (1. januar) er lagerbeholdningsniveauet for DemoProduct-varen 0 (nul).
- På dag fire (5. januar), der ligger inden for varens leveringstid, får du en salgsordre på 10 stk. af DemoProduct-varen.
- På dag syv (8. januar) findes der en indkøbsordre på 10 stk. af DemoProduct-varen.

I følgende illustration vises en grafisk visning af dette scenarie.

![Grafisk visning af scenarie 1](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Eksempel A: Negative dage er mindre end varens leveringstid

Hvis du angiver de negative dage som et tal, der er mindre end varens leveringstid, søger MRP efter tilgange for DemoProduct-varen inden for tidshorisonten for negative dage. Da der ikke findes tilgage, opretter MRP et nyt indkøbsordreforslag, der bruger dags dato som ordredatoen. Dette ordreforslag forsinkes straks med seks dage (leveringstiden). Den vil derfor blive modtaget d. 7. januar. Den eksisterende indkøbsordre får handlingsmeddelsen **Annuller**, fordi oprettelsen af det nye indkøbsordreforslag er blevet overflødigt.

I følgende illustration vises et skærmbillede af dette eksempel.

![Skærmbillede for eksempel A til scenarie 2](./media/negative-days-9.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel A til scenarie 2](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Eksempel B: Negative dage er mere end varens leveringstid

Denne situation ligner eksempel B til scenarie 1. Hvis du angiver de negative dage til et tal, der er større end varens leveringstid, får du ikke et nyt ordreforslag. Salgsordren er tilknyttet den eksisterende indkøbsordre.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Eksempel C: Korreler automatisk varens leveringstid med tidshorisonten for negative dage

Denne situation ligner eksempel C i scenarie 1, fordi dynamiske negative dage fungerer lige så vel, som de gør i dette eksempel. Tidshorisonten for dynamiske negative dage er nu 6 + 2 – 4 = 4 dage. Hvis du bruger denne fremgangsmåde, finder MPS den eksisterende indkøbsordre og knytter salgsordren til den. Da der ikke er oprettet nye ordreforslag, er kørselstiden for MRP kortere.

I følgende illustration vises et skærmbillede af dette eksempel.

![Skærmbillede for eksempel C til scenarie 2](./media/negative-days-11.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel C til scenarie 2](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Eksempel D: Brug kun dynamiske negative dage

Hvis du angiver de negative dage til **0** (nul) og kun bruger tidshorisonten for dynamiske negative dage, er tidshorisonten for dynamiske negative dage nu 6 + 0 – 4 = 2 dage. I dette tilfælde er resultatet det samme som resultatet eksempel A for dette scenario. Hvis du vil have vist en grafisk fremstilling af, hvad der sker, henvises til eksempel A til dette scenarie.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Eksempel E: Brug både negative dage, som er større end varens leveringstid og tidshorisonten for de dynamiske negative dage

Hvis du angiver de negative dage et tal, der er større end varens leveringstid, og hvis du også bruger tidshorisonten for dynamiske negative dage, er tidshorisonten for dynamiske negative dage 6 + 6 – 4 = 8 dage. Denne fremgangsmåde kan resultere i en meget lang tidshorisont, som MRP skal søge efter resultater i. Du kan få oplysninger om, hvordan eksempel E er relateret til en situation, hvor du angiver de negative dage til en lang tidshorisont, under afsnittet [Konklusion](#conclusion) i dette emne.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Scenarie 3: Du får behov efter varens leveringsperiode

Du får måske behov efter varens leveringstid. Her er et eksempel på dette scenarie:

- DemoProduct-varen har en indkøbsleveringstid på seks.
- På dag nul (1. januar) er lagerbeholdningen for DemoProduct-varen 0 (nul).
- På dag syv (8. januar), der ligger uden for varens leveringstid, får du en salgsordre på 10 stk. af DemoProduct-varen.
- På dag 10 (11. januar) findes der en indkøbsordre på 10 stk. af DemoProduct-varen.

I følgende illustration vises en grafisk visning af dette scenarie.

![Grafisk visning af scenarie 3](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Eksempel A: Negative dage er mindre end varens leveringstid

Hvis du angiver de negative dage som et tal, der er mindre end varens leveringstid, vil MRP kigge to dage forud for salgsordrens behovsdato. Da der ikke findes noget, opretter MRP et indkøbsordreforslag den 2. januar. Dette indkøbsordreforslag leveres kun i lige tide til at opfylde salgsordrebehovet. Den eksisterende indkøbsordre får handlingsmeddelelsen **Annuller**, fordi den ikke er behov for den.

I følgende illustration vises et skærmbillede af dette eksempel.

![Skærmbillede for eksempel A til scenarie 3](./media/negative-days-14.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel A til scenarie 3](./media/negative-days-15.png)

> [!NOTE]
> På det foregående skærmbillede er behovsdatoen for indkøbsordren 12. januar. Da det pågældende skærmbillede blev taget i 2015, hvor 11. januar var en søndag, flytter MRP behovsdatoen til næste arbejdsdag, som var mandag d. 12. januar. Indkøbsordren har dog leveringsdato den 11. januar.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Eksempel B: Negative dage er mere end varens leveringstid

Hvis du angiver de negative dage til et tal, der er større end varens leveringstid, får du ikke et nyt ordreforslag. Salgsordren fastfryses mod den eksisterende indkøbsordre. Derfor er salgsordren forsinket. Hvis du opretter et ordreforslag, kan du afsende salgsordren til tiden.

I følgende illustration vises et skærmbillede af dette eksempel.

![Skærmbillede for eksempel B til scenarie 3](./media/negative-days-16.png)

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel B til scenarie 3](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Eksempel C: Korreler automatisk varens leveringstid med tidshorisonten for negative dage

Denne situation ligner eksempel C i scenarie 1, fordi dynamiske negative dage fungerer lige så vel, om ikke bedre, end de fungerer i eksempel B til dette scenarie.

Tidshorisonten for dynamiske negative dage er 6 + 2 – 7 = 1 dag. I dette tilfælde tager systemet dog stadig højde for de negative dages leveringstid (2), fordi MPS betragter maksimumværdien mellem de negative dages leveringstid og de dynamiske negative dages leveringstid. Derfor vil resultatet i dette eksempel være det samme som resultatet i eksempel A for dette scenario.

I følgende illustration vises en grafisk visning af, hvad der sker i dette eksempel.

![Grafisk visning af eksempel C til scenarie 3](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Eksempel D: Brug kun dynamiske negative dage

Hvis du angiver de negative dage til **0** (nul) og kun bruger tidshorisonten for dynamiske negative dage, er tidshorisonten for dynamiske negative dage nu 6 + 0 – 7 = -1 dag. I dette tilfælde tager systemet stadig højde for de negative dages leveringstid (2). Derfor vil resultatet i dette eksempel være det samme som resultatet i eksempel A og have alle de samme ulemper. Hvis du vil have vist en grafisk fremstilling af, hvad der sker, henvises til scenarie 2.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Eksempel E: Brug både negative dage, som er større end varens leveringstid og tidshorisonten for de dynamiske negative dage

Denne eksempel er det samme som eksempel E til scenarie 1 og 2. Det har grundlæggende samme fordele og ulemper.

## <a name="conclusion"></a>Konklusion

Som de tre scenarier i dette emne viser, er det en god ide at angive de negative dage som et tal, der er større end leveringstiden for varerne i disponeringsgruppen. Det er også en god ide kun at bruge dynamiske negative dage og til at angive de negative dage som det antal dage, du vil vente, før du bestiller en ny genopfyldning, når du har en negativ lagerbeholdning (med andre ord det antal dage, du er villig til yderligere at forsinke behov). Desuden bør varer i samme disponeringsgruppe have tilsvarende leveringstider.

Hvis du angiver de negative dage til **0** (nul) og ikke bruger dynamiske negative dage, opretter MPS altid et nyt ordreforslag for at opfylde behovet. I denne situation er det vigtigt, at du arbejder med handlingsmeddelelserne for at sikre, at du ikke får fyldt for meget op på lageret.

Du kan angive de negative dage som en lang tidshorisont og derefter arbejde med handlingsmeddelelser. Denne fremgangsmåde giver gode planlægningsresultater, men det er også en smule langsommere. Det kan også være sværere at analysere, fordi du skal analysere og anvende handlingsmeddelelserne. Her er et eksempel:

- DemoProduct-varen har en indkøbsleveringstid på seks.
- På dag nul (1. januar) er lagerbeholdningen for DemoProduct-varen 0 (nul).
- På dag nul (1. januar) får du en salgsordre på 10 stk. af DemoProduct-varen.
- På dag 10 (10. januar) får du en salgsordre på 10 stk. af DemoProduct-varen.
- På dag 12 (12. januar) findes der en indkøbsordre på 10 stk. af DemoProduct-varen.
- Negative dage angives til **20**, hvilket er langt mere end varens leveringstid.

I følgende illustration vises en grafisk visning af, hvad der sker.

![Grafisk gennemgang af eksemplet](./media/negative-days-19.png)

MRP producerer følgende resultater.

![Resultater](./media/negative-days-20.png)

På det foregående skærmbillede er behovsdatoen for salgsordren den 9. januar i stedet for den 10. januar. Da det pågældende skærmbillede blev taget i 2015, hvor 10. januar var en søndag, flytter skal behovsdatoen for ordren være den forudgående arbejdsdag, som var fredag d. 9. januar.

MPS opretter en planlagt indkøbsordre for at opfylde det behov, der kræves af den første salgsordre, men det anbefales også, at du annullerer ordreforslaget, da du kan rykke den eksisterende indkøbsordre frem og øge antallet i den.

Resultaterne er ikke forkerte, men kørselstiden for MRP kan være længere, da MRP skal oprette alle forsinkelser og forslag. Derudover er planlæggeren måske nødt til at bruge mere tid på at forstå MRP-resultaterne. Det vigtigste i dette tilfælde er, at det er afgørende, at planlæggeren forstår og bruger handlingsmeddelelserne.

Hvis du reducerer de negative dage til et tal, der ligger tættere på varens leveringstid, og du bruger dynamiske negative dage, producerer MRP følgende resultater.

![Resultater](./media/negative-days-21.png)

MRP opretter et ordreforslag, der er knyttet til den første salgsordre. Det forventes, at den anden salgsordre udlignes derefter mod den eksisterende indkøbsordre, baseret på indstillingen for negative dage. Dette planlægningsresultat er også korrekt, og kørselstiden for MRP kan være kortere. I dette tilfælde er det ikke vigtigt, at du forstår og ved, hvordan du skal arbejde med handlingsmeddelelser.

Som en hjælp til at sikre, at der er angivet de korrekte værdier for din virksomhed, skal du tænke både på funktionalitet og MRP-kørselstid. Derfor kan det kræve, at du skal prøve dig frem, for at fastsætte de optimale værdier.

## <a name="see-also"></a>Se også

Få mere diskussion ved at se det oprindelige blogindlæg [Mere om (dynamiske) negative dage](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]