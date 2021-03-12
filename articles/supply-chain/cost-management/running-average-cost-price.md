---
title: Løbende gennemsnitskostpris
description: Under processen til lagerlukning udlignes afgangsposteringer i forhold til tilgangsposteringer på baggrund af den metode til lagerværdi, der er valgt i varens varemodelgruppe. Men inden lagerlukningen køres, beregner systemet en løbende gennemsnitskostpris, der typisk bruges, når afgangsposteringer bogføres.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 776f886fc0dfccf1b2675c9d54d44c16c6df4f09
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963757"
---
# <a name="running-average-cost-price"></a>Løbende gennemsnitskostpris

[!include [banner](../includes/banner.md)]

Under processen til lagerlukning udlignes afgangsposteringer i forhold til tilgangsposteringer på baggrund af den metode til lagerværdi, der er valgt i varens varemodelgruppe. Men inden lagerlukningen køres, beregner systemet en løbende gennemsnitskostpris, der typisk bruges, når afgangsposteringer bogføres.

Systemet estimerer denne løbende gennemsnitskostpris for en vare ved hjælp af følgende formel: 

Estimeret pris = (fysisk beløb + økonomisk beløb) ÷ (fysisk antal + økonomisk antal)

## <a name="using-the-running-average-cost-price"></a>Brug af den løbende gennemsnitskostpris
I nedenstående tabel vises det, hvornår systemet bogfører lagerposteringer ved hjælp af den løbende gennemsnitskostpris, og hvornår programmet i stedet bruger den kostpris, der er angivet på stamdataposten for varen.

| Betingelse                                               | Systemet bruger den beregnede løbende gennemsnitskostpris | Systemet bruger den kostpris, der er defineret i varens stamdata |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Tælleren\* og nævneren\*\* er begge positive.  | Ja                                                      | Nr.                                                                |
| Tælleren\*, nævneren\*\* eller begge er negative. | Nr.                                                       | Ja                                                               |
| Nævneren\*\* er 0 (nul).                        | Nr.                                                       | Ja                                                               |

\* Tæller = (fysisk beløb + økonomisk beløb) \*\* Nævner = (fysisk antal + økonomisk antal) 

**Bemærk!** Hvis indstillingen **Medtag fysisk værdi** ikke er markeret for en vare, bruger systemet 0 (nul) til både det fysiske beløb og det fysiske antal. Oplysninger om denne indstilling finder du under [Medtag fysisk værdi](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Undgå overestimering af priser
Det kan evt. forekomme, at systemet beregner priser for flere afgange, før der et tilstrækkeligt antal tilgange at basere prisen på. Dette scenario kan forårsage, at estimater af den løbende gennemsnitskostpris bliver alt for oppustede. Du kan dog undgå overestimering af priser eller reducere de negative virkninger, når det opstår. **Scenarie** Følgende posteringer forekommer for en vare, du har valgt indstillingen **Medtag fysisk værdi** for:

1.  Økonomisk modtager du et antal på 100 til kr. 100,00.
2.  Du udsteder økonomisk et antal på 200.
3.  Du modtager fysisk et antal på 101 til kr. 202,00.

Når du undersøger den estimerede løbende gennemsnitskostpris for en vare, forventer du en kostpris på kr. 1,51. I stedet skal du finde et estimeret løbende gennemsnit af 102,00 kr., som er baseret på følgende formel: Estimeret pris = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102. Denne overestimering forekommer, fordi når der udstedes 200 varer økonomisk i trin 2, skal systemet prissætte 100 stk. af varerne, før programmet har nogen tilsvarende tilgange. Denne situation medfører negativ lagerbeholdning. Systemet estimerer derefter en enhedspris på kr. 1,00, sådan som vi kunne forvente. Når de tilsvarende 100 tilgange ankommer, bliver de dog er til en enhedspris på kr. 2,00. 

**Bemærk!** Selvom afgangene medfører negativt lager, er lageret positivt, når afgangsprisen beregnes. Derfor bruges den løbende gennemsnitskostpris og ikke prisen fra varens stamdata. På dette tidspunkt findes der i systemet en lagermodværdi på kr. 100,00. Mens modværdien blev bygget på 100 styk, hvor der var en enhedsmodværdi på kr. 1,00 pr. styk, er der nu kun ét styk på lageret. Denne modværdi på kr. 100,00 fordeles derfor til dette ene styk. Resultatet er, at den forkalkulerede kostpris fejlvurderes. 

**Bemærk!** Til sammenligning kan du bemærke, at hvis trin 2 og 3 tilbageføres i ovenstående scenarie, vil der blive udlagret 200 styk til en enhedspris på kr. 1,51, og prisen for 1 styk vil fortsat være kr. 1,51. Da denne overestimering kan forekomme, når der forekommer negativt lager, er det svært at undgå i følgende situationer:

-   Du skal estimere afgangspriserne for værdien og antallet for det disponible antal.
-   Du skal justere den værdien og antallet for den disponible lagerbeholdning på afgange og tilgange.
-   Forretningsmodellen tillader, at du udsender eller prissætter flere styk, end der er på lager.
-   Du skal acceptere alle tilgangsværdier og tilgangsantal, der sendes til dig.

Hvis din forretningsmodel tillader det, kan følgende fremgangsmåder dog hjælpe dig med at undgå, at negative antal muliggør denne overestimering af priser:

-   Hvis du vælger indstillingen **Medtag fysisk værdi** for en vare, skal du fjerne markeringen i **Fysisk negativt lager** afkrydsningsfeltet på siden **Varemodelgrupper**.
-   Hvis du *ikke* vælger indstillingen **Medtag fysisk værdi** for en vare, skal du fjerne markeringen i **Økonomisk negativt lager** afkrydsningsfeltet på siden **Varemodelgrupper**.

Husk også, at den maksimale modpostering i den fysiske lagerværdi er begrænset til antallet af fysiske posteringer og forskellen mellem fysiske og økonomiske priser. Forudsat at alle fysiske posteringer opdateres økonomisk i den sidste ende, kan den fysiske værdi ikke stige til ekstremt høje niveauer. Husk til slut, at risikoen for overestimerings aftager også væsentligt, hvis den akkumulerede modpostering fordeles over flere disponible stykvarer og ikke bare én.



