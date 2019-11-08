---
title: Guiden installation af varedisponering
description: I dette emne beskrives forskellige vigtige strategier og parametre, der bruges til definition af varedisponering.
author: t-benebo
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 8fbccce6e23c9bc965f66f761f4c1cab32224ef1
ms.sourcegitcommit: fbd6d027ef3b50c056260e30e78066839efa3ddb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2019
ms.locfileid: "2635120"
---
# <a name="master-planning-setup-wizard"></a>Guiden installation af varedisponering

[!include [banner](../includes/banner.md)]

Dette emne indeholder en vejledning til **Guiden installation af varedisponering**. Den forklarer, hvordan parameterforslag beregnes, og indeholder også eksempler, som viser, hvordan forskellige firmaer konfigurerer varedisponering på grundlag af deres forretningsbehov.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3YnSB]

Videoen [Guiden Opsætning af varedisponering i Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.


## <a name="specific-requirements-of-your-company"></a>Specifikke krav til din virksomhed

Den første side i guiden spørger ind til de specifikke krav i din virksomhed. Dine svar på disse spørgsmål behøver ikke at være nøjagtige, men du bør være i stand til at give en grov tilnærmelse af, hvad antallet af varer og planlagte ordrer vil være for den juridiske enhed. Dine svar bruges til at konfigurere de parametre, der finder anvendelse for din juridiske enhed, og ikke kun for den behovsplan, du har valgt. De følgende afsnit beskriver de parametre, der beregnes, og de formler, der bruges.

### <a name="number-of-threads"></a>Antal tråde

- **Hvis du fremstiller nogle af disse varer:** Antal tråde = Antal ordreforslag ÷ 1.000
- **Hvis du ikke fremstiller nogle af disse varer:** Antal tråde = Antal varer ÷ 1.000

Hvis antallet af tråde, der beregnes, overstiger 75 procent af det tilgængelige antal tråde, er det begrænset til 75 procent af det antal tråde, der er tilgængelige for hver kunde. (Antallet af tilgængelige tråde vil blive fastlagt for hver kunde.)

Du kan finde flere oplysning er i [Antal af tråde](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Bundtstørrelse

Bundtstørrelsen vil blive angivet til **1**. Denne værdi er ofte den bedste værdi, fordi den hjælper med at forbedre ydeevnen i forbindelse med varedisponering.

Du finder flere oplysninger under [Antal opgaver i hjælpeopgavebundter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Autorisation af bundtstørrelse

- **Hvis du fremstiller varerne:** Autorisationen af bundtstørrelsen vil blive angivet til den største af disse to værdier: **10** og bundtberegningen
- **Hvis du ikke fremstiller varerne:** Autorisationen af bundtstørrelsen vil blive angivet til den største af disse to værdier: **50** og bundtberegningen

Bundtberegning = (antal ordreforslag × (autorisation af tidshorisont ÷ tidshorisontdato) ÷ antal tråde) ÷ 10

### <a name="cache-size"></a>Cachestørrelse

Cachestørrelsen vil blive angivet til **Maksimum**. Denne værdi er ofte den bedste værdi, fordi den hjælper med at forbedre ydeevnen i forbindelse med varedisponering.

Du finder flere oplysninger under [Alloker tid til jobs i et jobbundt](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Opsætning af produktion

Hvis du fremstiller varer, bliver der senere i guiden vist en side for **Opsætning af produktion**.

## <a name="scope-of-the-current-plan"></a>Omfang af den aktuelle plan

På siden **Omfang af den aktuelle plan** i guiden besvarer du spørgsmål, der er relateret til, hvor langt ude i fremtiden de forskellige behov skal tages i betragtning og beregnes i varedisponering. Hvert spørgsmål spørger, om du vil bruge en funktion, og hvordan du vil konfigurere den.

I forbindelse med funktionen hovedplan, spørger guiden eksempelvis om følgende: "Vil du bruge en hovedplan i varedisponering, således at ordreforslag vil blive foreslået for at opfylde den anslåede efterspørgsel?"

Følgende indstillinger er tilgængelige:

- **Nej** – varedisponering foreslår ikke, at planlagte ordrer skal opfylde en prognose. Under fanen **Tidshorisonter** på siden **Behovsplaner** (**Varedisponering \> Opsætning \> Planer \> Behovsplaner**) angiver guiden indstillingen for **Hovedplan (tidshorisont)** til **Ja** samt angiver antallet af dage til **0** (nul). Denne opsætning tilsidesætter den tidshorisont, der er angivet i disponeringsgruppen. Da antallet af dage er angivet til **0** (nul), bruges funktionen ikke.
- **Ja, som defineret i denne behovsplan** – et felt bliver tilgængeligt, hvor du kan angive det antal dage, som varedisponeringen foreslår, at de planlagte ordrer opfylder den anslåede efterspørgsel i. Guiden angiver indstillingen for **Hovedplan (tidshorisont)** til **Ja** samt angiver antallet af dage til det antal dage, der er indtastet i feltet **Hovedplan** under fanen **Tidshorisont** på siden **Behovsplaner**. Denne opsætning tilsidesætter de værdier, der er angivet i disponeringsgrupperne.
- **Ja, som defineret i dækningen** – guiden indstiller **Hovedplanen (tidshorisont)** til **Nej**. De tidshorisonter, der er angivet i disponeringsgruppen, bruges til at angive, hvor lang tid, du ønsker at planlægge for prognosen.

De resterende spørgsmål på denne side og deres svar følger det samme skema:

- **Nej** – indstillingen for **Hovedplan (tidshorisont)** angives til **ja**, og antallet af dage angives som **0** (nul).
- **Ja, som defineret i denne behovsplan** – indstillingen **Hovedplan (tidshorisont)** angives til **Ja**. Det antal dage, du indtaster, vil blive brugt og vil tilsidesætte de værdier, der er angivet i disponeringsgrupperne.
- **Ja, som defineret i dækningsgruppen** – indstillingen **Hovedplan (tidshorisont)** angives til **Nej**.

Du kan finde flere oplysninger i [Jobplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Planlægningsindstillinger

Siden **Planlægningsindstillinger** vises kun, hvis du har svaret **Ja** til spørgsmålet "Fremstiller du de planlagte varer?" på første side i guiden.

Dit svar på det første spørgsmål på denne side ("Har du brug for at planlægge operationer, der er inddelt i individuelle job?") bestemmer planlægningsmetoden under fanen **Generelt** på siden **Behovsplaner**.

- **Ja** – jobplanlægning bliver brugt.
- **Nej** – planlægning af operation bliver brugt.

Du kan finde flere oplysninger under [Planlægning af operationer](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) og [Jobplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Opdateringer af udbud og efterspørgsel

Spørgsmålene på siden **Opdateringer af udbud og efterspørgsel** er relateret til autorisation, aktionsmeddelelser og forsinkelser.

Opsætningen af varedisponering opdateres ud fra dine svar i henhold til det samme skema, som er beskrevet i forrige afsnit:

- **Nej** – indstillingen **Tidshorisont** på siden **Behovsplaner** angives til **Ja**, og antallet af dage angives til **0** (nul).
- **Ja, som defineret i denne behovsplan** – indstillingen **Tidshorisont** angives til **Ja**. Det antal dage, du indtaster, vil blive brugt og vil tilsidesætte de værdier, der er angivet i disponeringsgrupperne.
- **Ja, som defineret i dækningsgruppen** – indstillingen **Tidshorisont** angives til **Nej**.

Ved beregnede forsinkelser vil dine svar på spørgsmålene i guiden opdatere de tilsvarende parametre under fanen **Beregnede forsinkelser** på siden **Behovsplaner**.

## <a name="summary-of-your-changes"></a>Sammendrag af dine ændringer

Den sidste side i guiden viser de ændringer, der anbefales på baggrund af dine svar. Den viser både værdien i din opsætning (**Aktuel opsætning**), og den værdi, som guiden anbefaler (**Ny konfiguration**).

Du kan også tilpasse parametrene i den nye konfiguration. Parametrene er opdelt i parametre, der gælder for din juridiske enhed, og de parametre, der alene gælder for den behovsplan, du har valgt. Hvis du vil have vist alle de opsætningsparametre, der kan ændres ved hjælp af guiden, skal du vælge **Vis alle parametre** nederst på siden. Du kan derefter ændre parametrene.

Slutteligt, når du vælger **Udfør**, anvendes den nye konfiguration. Hvis du vælger **Annuller**, anvendes ingen af ændringerne.

## <a name="examples"></a>Eksempler

I dette afsnit beskrives opsætningen af to fiktive virksomheder for at vise, hvordan opsætningen kan ændre sig i henhold til behovene i hver enkelt virksomhed.

### <a name="example-1-contoso-manufacturer"></a>Eksempel 1: Contoso Manufacturer

Contoso Manufacturer er en produktionsvirksomhed, der producerer højttalere. Den køber de forskellige råmaterialer og komponenter, der anvendes til de endelige højtalere fra forskellige leverandører. Her er nogle af de særlige kendetegn ved virksomhedens forsyninger og produktion:

- De endelige varer, som virksomheden fremstiller, har en styklistestruktur (BOM).
- Alle endelige varer og komponenter planlægges ved hjælp af varedisponering. Manuel planlægning er ikke færdig.
- Der defineres en operationsrute for produktionen af den enkelte færdige vare.
- Produktionsanlægget producerer de endelige varer. Det har et defineret antal fræsnings- og boremaskiner, som anvendes til at behandle komponenterne. De forskellige komponenter skal behandles af disse maskiner.
- Der er mange leverandører. Den gennemsnitlige leveringstid for varerne er en uge. En gruppe varer fra samme leverandør vil have en leveringstid på syv uger.

I guiden angives følgende værdier for Contoso Manufacturer:

- **Disponering:**

    - **Spørgsmål:** "Vil du angive antallet af dage i planlægningshorisonten?"
    - **Svar:** "Ja, som defineret i disponeringsgrupperne."

    Da leveringstiden for varer er meget forskellig, behøver Contoso ikke at planlægge alle varerne til den samme periode i fremtiden. Disponeringsgrupper for varerne oprettes. Varer med en lignende leveringstid tildeles den samme disponeringsgruppe. Planlægningshorisonten for hver disponeringsgruppe (dvs. dækningstidshorisonten) svarer ca. til leveringstiden plus en margin på en uge. Varedisponering sikrer derefter, at varerne planlægges på forhånd på grundlag af deres leveringstid.

    Der vil derfor blive oprettet to disponeringsgrupper til dette eksempel. Den ene disponeringsgruppe vil have en disponeringstidshorisont på to uger, og den anden vil have en disponeringstidshorisont på otte uger.

    Hvis **Ja, som defineret i denne behovsplan** er valgt som svar, skal antallet af dage, der indtastes, overskride den længste leveringstid for alle varerne. Men da mange varer ikke skal planlægges så langt på forhånd, vil mange planlagte ordrer blive beregnet, men aldrig brugt. Varedisponeringens løbetid vil derfor stige.

- **Planlægning:**

    - **Spørgsmål:** "Har du brug for at planlægge operationer inddelt i individuelle job?"
    - **Svar:** Jja."

    Contoso Manufacturing skal lave en plan for og planlægge de individuelle job, der skal udføres på produktionsgulvet. Den vil derfor bruge jobplanlægning.

- **Kapacitet:**

    - **Spørgsmål:** "Vil du planlægge ved hjælp af ressourcernes kapacitet?"
    - **Svar:** "Ja, som defineret i denne behovsplan." **10 dage** indtastes.

    Antallet af fræsnings-og boremaskiner er begrænset. Produktionsplanlægningen skal tage hensyn til denne begrænsning og tilrettelægge jobsne i behørig tid i forhold til ressourcernes kapacitet. Med andre ord vil de job, der er planlagt, blive planlagt på ny på grundlag af de begrænsede ressourcer. I tillæg til den definerede perioden anvender planlægningen leveringstiden. (Produktionsordreforslag kan overlappe.) Da produktionsleveringstiden for varerne er syv dage, vil ressourcernes kapacitet til varedisponering blive taget i betragtning i løbet af 10 dage.

- **Rækkefølge:**

    - **Spørgsmål:** "Vil du opdele ordreforslag i sekvenser ved hjælp af produktets sekvensværdier?"
    - **Svar:** "Ja, som defineret i disponeringsgrupperne."

    Der defineres en rute for produktionen af den enkelte færdige vare. Varedisponering vil derfor planlægge ordrerne i behørig tid i henhold til de definerede ruter.

- **Udfoldning:**

    - **Spørgsmål:** "Vil du planlægge ordrer for alle elementerne i en stykliste (plan for forælderen og alle underordnede elementer)?"
    - **Svar:** "Ja, som defineret i disponeringsgrupperne."

    Alle de varer, der bruges til produktionen, skal planlægges. Da varerne har meget forskellige leveringstide, vil varedisponering få en bedre ydeevne, når den bruger disponeringsgrupperne. Det skal gentages, at der kan angives en margin på en uge, og udfoldning kan udføres for den samme periode som disponeringen.

### <a name="example-2-contoso-retailer"></a>Eksempel 2: Contoso Retailer

Contoso Retailer er et distributionsselskab i modebranchen. Det bruger varedisponering til at beregne, hvornår indkøbsordrer skal placeres på grundlag af det estimerede salg. Her er nogle af virksomhedens karakteristika:

- Contoso Retailer bruger en behovsprognose til at forudsige salg. Indkøbsordrer planlægges i henhold til prognosen.
- Detailbutikker bruger rekvisitioner til genopfyldning.
- Leveringstiden fra hovedlageret til hver butik er ca. to uger for alle varer.

I guiden angives følgende værdier for Contoso Retailer:

- **Estimeret efterspørgsel:**

    - **Spørgsmål:** "Vil du bruge en hovedplan i varedisponering, således at det foreslås, at ordreforslag anvendes til at opfylde den estimerede efterspørgsel?"
    - **Svar:** "Ja, som defineret i denne behovsplan."

    Contoso har medtaget en behovsprognose for at forudsige salget. Derfor skal varedisponering anbefale ordreforslag for at opfylde prognosen.

- **Autorisation:**

    - **Spørgsmål:** "Vil du have varedisponering til automatisk at autorisere ordreforslag i bestillingsdokumenter, f.eks. produktions- eller indkøbsordrer?"
    - **Svar:** "Ja, som defineret i denne behovsplan." **1 dag** indtastes.

    Da Contoso Retailer opretter indkøbsordrer direkte fra indkøbsordreforslag, er det nyttigt, hvis indkøbsordreforslag autoriseres automatisk. Da virksomheden kører varedisponering hver dag, vil en tidshorisont for autorisering på én dag automatisk autorisere alle de ordrer, der er behov for til den kommende dag.

- **Godkendte rekvisitioner:**

    - **Spørgsmål:** "Vil du medtage efterspørgsel fra godkendte rekvisitioner for at genopfylde detailbutikker?"
    - **Svar:** "Ja, som defineret i denne behovsplan." **1 dag** indtastes.

    Contoso bruger de godkendte rekvisitioner fra sine detailbutikker til at oprette indkøbsordreforslag for at genopfylde disse butikker. Da varedisponering køres hver dag, medtages rekvisitionerne fra den sidste dag i planlægningen.
