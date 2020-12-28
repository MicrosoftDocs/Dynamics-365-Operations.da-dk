---
title: Foretage fejlfinding af varedisponering
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med varedisponering.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645059"
---
# <a name="troubleshoot-master-planning"></a>Foretage fejlfinding af varedisponering

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med varedisponering.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Styklisteudfoldningen opfører sig forskelligt for autoriserede produktionsordrer og forkalkulerede produktionsordrer for manuelt oprettet arbejde.

### <a name="issue-description"></a>Problembeskrivelse

Når en produktionsordre autoriseres, udfoldes varerne ikke, når du udfolder styklisten. Men når du opretter en arbejdsordre manuelt og derefter forkalkulerer produktionsordren, udfoldes varerne.

### <a name="issue-resolution"></a>Problemløsning

Systemet fungerer som forventet. Den udfoldning, der opstår, når produktionsordren autoriseres, peger på ordreforslaget, men det ser ikke ud til, at ordreforslaget er autoriseret i dette tilfælde. Men hvis produktionsordren er forkalkuleret, udløses udfoldningen fra den frigivne produktionsordre, når der ikke findes et ordreforslag.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Forsinkelsesværdien opdateres ikke, når jeg ændrer planlægning af et ordreforslag.

Hvis du vil opdatere forsinkelsen for ordreforslag, skal du åbne dialogboksen **Omplanlægning** for ordreforslaget. I oversigtspanelet **Udfoldning** skal du kontrollere, at indstillingen **Foretag udfoldning efter omplanlægning** er angivet til *Ja*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>I produktionsplanlægning tages der ikke hensyn til de sikkerhedsmargener, der er angivet på varedisponeringen for sporede forsyninger.

### <a name="issue-description"></a>Problembeskrivelse

Varedisponering tager højde for sikkerhedsmargener. Sikkerhedsmargenerne ignoreres dog, når produktionsordreforslag planlægges.

### <a name="issue-resolution"></a>Problemløsning

Margener betragtes kun for varedisponering, ikke under manuel planlægning. Margener er designet til at fungere som en buffer i planlægningsfasen, så der gives nogen "margen" for den faktiske proces.

Du kan få det ønskede resultat ved at fjerne margen. Ruten skal derefter opdateres, så den omfatter den ønskede tid (f.eks. køtid). Både varedisponering og manuel planlægning bør derefter give samme resultat.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Ordreforslag genereres, selvom der allerede findes varer på lager og produktionsordrer for dem.

Du kan muligvis løse dette problem ved at øge værdien af **Positive dage** for de relevante grupper på siden **Disponeringsgruppe**. Denne ændring bevirker, at systemet afgør, om disponibel lagerbeholdning kan bruges til efterspørgslen. Derefter vil der ikke blive genereret et nyt ordreforslag for de varer, der er på lager.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Varedisponering overholder tilsyneladende ikke kapacitetsbegrænsninger og planlægger mere end den tilgængelige kapacitet.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruger grovplanlægning, hvor der er kapacitetsbegrænsning, og hvor ruten angiver en blanding af behov for både en ressourcegruppe og de enkelte ressourcer, er der en lille risiko for at overbooke på grund af den måde, som algoritmen validerer for kapacitetskonflikter. Denne overbooking kan forekomme, når du bruger hjælpefunktioner til at køre varedisponering. Det sker oftest, hvis der er mange job med forholdsvis kort kørselstid.

### <a name="issue-resolution"></a>Problemløsning

Hvis det er vigtigt, at der ikke opstår nogen overbooking til grovplanlægning, kan du gøre planlægningsdelen af varedisponering enkelttrådet ved at aktivere indstillingen **Præcis kapacitetsbegrænsning for grovplanlægning** på siden **Parametre for varedisponering**. Denne indstilling er som standard ikke tilgængelig. Du skal manuelt føje den til siden ved hjælp af tilpasningsfunktioner. Når du bruger denne indstilling, kører planlægningen langsommere på grund af manglende parallel behandling.

## <a name="planned-orders-take-a-long-time-to-update"></a>Det tager lang tid at opdatere ordreforslag.

### <a name="issue-description"></a>Problembeskrivelse

Når behovsantallet og/eller leveringsdatoen opdateres på et ordreforslag, tager det normalt mindst 30 sekunder pr. ordre at gemme opdateringen.

### <a name="issue-resolution"></a>Problemløsning

Dette er et kendt problem med det indbyggede varedisponeringsprogram. Det skyldes den underliggende automatiske udfoldning via styklistestrukturen under redigeringer. Dette problem håndteres i Planlægningsoptimering, hvor en planlægger kan opdatere og godkende de relevante ordrer og, hvor det er relevant, udløse en planlægningskørsel for at opdatere ordreforslag for den underliggende styklistestruktur.

En måde at forbedre ydeevnen med det indbyggede varedisponeringsprogram på er at gøre følgende:

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en plan.
1. Udvid oversigtspanelet **Tidshorisont i dage**.
1. Angiv **Udfoldning** til *Ja*, og angiv feltet under denne indstilling til 0 (nul).

> [!NOTE]
> Dette vil begrænse den periode for udfoldning, der udføres for denne behovsplan, til en enkelt dag.
