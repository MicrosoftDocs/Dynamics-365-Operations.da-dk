---
title: Startside for varedisponering
description: Med Varedisponering kan virksomheder bestemme og afbalancere deres fremtidige behov for råmaterialer og evne til at opfylde virksomhedens mål.
author: ChristianRytt
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15fbab7d0260ed714edfbbb5ef54caddb69cae3c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359999"
---
# <a name="master-planning-home-page"></a>Startside for varedisponering

[!include [banner](../includes/banner.md)]

Kernefunktionen i Varedisponering gør det muligt for virksomheder at bestemme og afbalancere deres fremtidige behov for råmaterialer og evne til at opfylde virksomhedens mål. Varedisponering vurderer følgende:

- Hvilke råvarer og hvilken kapacitet er tilgængelig i øjeblikket?
- Hvilke råvarer og hvilken kapacitet kræves, for at produktionen kan gennemføres? F.eks. hvad skal fremstilles, købes, overføres eller sættes på sikkerhedslager, før du kan fuldføre produktionen.

Varedisponering bruger oplysningerne til at beregne behovene og oprette ordreforslag.

De tre vigtigste planlægningsprocesser er:

- **Varedisponering** - Behovsplanen beregner nettobehovene. Den er baseret på faktiske aktuelle ordrer og gør det muligt for virksomheder at styre genopfyldning af lageret på en kortsigtet daglig basis. Et andet udtryk, der kræver nærmere beskrivelse, er *Plan for nettobehov*. Du kan finde flere oplysninger under [Oversigt over Behovsplaner](master-plans.md).

- **Hovedplanlægning** - Hovedplanen beregner bruttobehov. Den er baseret på fremtidige projektioner (eller budgetter) og giver firmaer mulighed for udføre langsigtet planlægning for materialer og kapacitet. Du kan finde flere oplysninger under [Oversigt over Behovsprognose](introduction-demand-forecasting.md).

- **Intern varedisponering** - Den interne behovsplan beregner nettobehov på tværs af juridiske enheder. Den forbinder behov og forsyning mellem firmaer, ikke kun kortsigtet, fast behov og forsyning, men også langsigtet, planlagt (der endnu ikke er autoriseret) behov og forsyning. Du kan finde flere oplysninger under [Intern planlægning](planning-optimization/Intercompany-planning.md).

Firmaer kan ændre resultatet af planen. De kan køre total, nettoændring eller begge dele. Totalplaner opdaterer alle behov, mens nettoplaner kun opdaterer planen for varer med nye behov, der er kommet efter den seneste behovsplanlægning.

Planer for behovsplanlægning er normalt kortsigtede og kan være alt fra en uge til seks måneder. Varedisponeringsmodulet bestemmer forsynings- (materiale) og kapacitetsbehov (ressourcer), som opfylder aktuelle behov (nettobehov). I de fleste firmaer omfatter dette også den længste akkumulerede leveringstid for de produkter, der skal modtages.

## <a name="learning-map"></a>Køreplan

Følgende køreplan viser de vigtigste begreber og opgaver, der udgør strukturen i varedisponeringsmodulet. Klik på linksene i sektionen [Hurtige links](#quick-links) for at få mere at vide, hvordan du bruger modulet.

[![Køreplan for varedisponering.](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Hurtige links

- [Oversigt over behovsplaner](master-plans.md)  
- [Generere en begrænset plan](./tasks/constrained-plan.md)
- [Oprette en materialeplan for samprodukter](./tasks/create-material-plan-co-products.md)
- [Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)
- [Oprette en intern plan](./tasks/create-intercompany-plan.md)
- [Oversigt over behovsprognoser](introduction-demand-forecasting.md)
- [Prognosereduktionsnøgler](reduction-keys.md)

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="roadmaps"></a>Strategier

Gå til [Microsoft Dynamics 365-oversigten](https://roadmap.dynamics.com/) for at se, hvilke nye funktioner der er blevet frigivet, og hvilke nye funktioner der er under udvikling.

### <a name="blogs"></a>Blogs

Du kan finde meninger, nyheder og andre oplysninger om Varedisponering og andre løsninger på [Dynamics AX Manufacturing R&D-teamets blog](/archive/blogs/axmfg/) og [Supply Chain Management i Dynamics AX R&D-teamets blog](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Opgaveguider

Du kan finde yderligere hjælp i form af opgaveguider. Du kan få adgang til opgaveguider ved at klikke på knappen **Hjælp** på en vilkårlig side.

### <a name="webinars"></a>Webinarer

[Bruge Azure Machine Learning til behovsprognose](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Optagelser af tekniske konferencer

- [Udvide behovsprognosefunktionen](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [Varedisponering - tips og tricks til forbedring af ydeevnen](https://youtu.be/7v8BPmEs9Dg)
- [Hjælp! MPS er langsom!](https://youtu.be/RLXybx20B5o)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]