---
title: "Løbende gennemsnitskostpris"
description: "Lagerlukningsprocessen afgangsposteringer til tilgangsposteringer, der er baseret på den metode til lagerværdi, der er valgt i varens varemodelgruppe. Før lagerlukningen køres, beregner systemet dog en løbende gennemsnitskostpris, der typisk bruges bogføring af afgangsposteringer."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Løbende gennemsnitskostpris

Lagerlukningsprocessen afgangsposteringer til tilgangsposteringer, der er baseret på den metode til lagerværdi, der er valgt i varens varemodelgruppe. Før lagerlukningen køres, beregner systemet dog en løbende gennemsnitskostpris, der typisk bruges bogføring af afgangsposteringer.

Systemet estimerer denne løbende gennemsnitskostpris for en vare ved hjælp af følgende formel: Estimeret pris = (fysisk beløb + økonomisk beløb) ÷ (fysisk antal + økonomisk antal)

## <a name="using-the-running-average-cost-price"></a>Brug af den løbende gennemsnitskostpris
Tabellen nedenfor viser, hvornår systemet bogfører lagerposteringer ved hjælp af den løbende gennemsnitskostpris, og hvornår den kostpris, der er defineret på den overordnede post i stedet bruges.

| Betingelse                                               | Systemet bruger den beregnede løbende gennemsnitskostpris | Systemet bruger den kostpris, der er defineret i varens stamdata |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Både tælleren\* og nævner\*\* er positive.  | Ja                                                      | Nr.                                                                |
| Tælleren\*, nævner\*\*, eller begge er negative. | Nr.                                                       | Ja                                                               |
| Nævner\*\* er 0 (nul).                        | Nr.                                                       | Ja                                                               |

\*Tæller = (fysisk beløb + økonomisk beløb) \*\*nævner = (fysisk antal + økonomisk antal) **Bemærk:** Hvis den **Medtag fysisk værdi** indstilling ikke er markeret for en vare, bruger systemet 0 (nul) for både fysisk beløb og det fysiske antal. Oplysninger om denne indstilling finder du under [Medtag fysisk værdi](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Undgå overestimering af priser
I sjældne tilfælde priser systemet flere problemer, før det er tilgange nok til at basere prisen på. Dette scenario kan forårsage, at estimater af den løbende gennemsnitskostpris bliver alt for oppustede. Du kan dog undgå overestimering af priser eller reducere de negative virkninger, når det opstår. **Scenarie** Følgende posteringer forekommer for en vare, du har valgt indstillingen **Medtag fysisk værdi** for:

1.  Økonomisk modtager du et antal på 100 til kr. 100,00.
2.  Du udsteder økonomisk et antal på 200.
3.  Du modtager fysisk et antal på 101 til kr. 202,00.

Når du undersøger den estimerede løbende gennemsnitskostpris for en vare, forventer du en kostpris på kr. 1,51. I stedet skal du finde en anslået løbende gennemsnit af USD 102.00, der er baseret på følgende formel: Estimeret pris = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 denne prissætning forstærkning opstår, fordi når 200 styk økonomisk i trin 2, skal systemet pris 100 elementer, før programmet har nogen tilsvarende tilgange. Denne situation medfører negativ lagerbeholdning. Systemet beregner derefter en enhedspris på USD 1.00, som vi kan forvente. Når de tilsvarende 100 tilgange ankommer, bliver de dog er til en enhedspris på kr. 2,00. **Bemærk!** Selvom afgangene medfører negativt lager, er lageret positivt, når afgangsprisen beregnes. Derfor bruges den løbende gennemsnitskostpris og ikke prisen fra varens stamdata. På dette tidspunkt har systemet en lager værdien forskydning af USD 100.00. Mens modværdien blev bygget på 100 styk, hvor der var en enhedsmodværdi på kr. 1,00 pr. styk, er der nu kun ét styk på lageret. Denne modværdi på kr. 100,00 fordeles derfor til dette ene styk. Resultatet er, at den forkalkulerede kostpris fejlvurderes. **Bemærk!** Til sammenligning kan du bemærke, at hvis trin 2 og 3 tilbageføres i ovenstående scenarie, vil der blive udlagret 200 styk til en enhedspris på kr. 1,51, og prisen for 1 styk vil fortsat være kr. 1,51. Da denne overestimering kan forekomme, når der forekommer negativt lager, er det svært at undgå i følgende situationer:

-   Du skal estimere afgangspriserne for værdien og antallet for det disponible antal.
-   Du skal justere den værdien og antallet for den disponible lagerbeholdning på afgange og tilgange.
-   Forretningsmodellen tillader, at du udsender eller prissætter flere styk, end der er på lager.
-   Du skal acceptere alle tilgangsværdier og tilgangsantal, der sendes til dig.

Hvis din forretningsmodel tillader det, kan følgende fremgangsmåder dog hjælpe dig med at undgå, at negative antal muliggør denne overestimering af priser:

-   Hvis du vælger indstillingen **Medtag fysisk værdi** for en vare, skal du fjerne markeringen i **Fysisk negativt lager** afkrydsningsfeltet på siden **Varemodelgrupper**.
-   Hvis du *ikke* vælger indstillingen **Medtag fysisk værdi** for en vare, skal du fjerne markeringen i **Økonomisk negativt lager** afkrydsningsfeltet på siden **Varemodelgrupper**.

Husk også, at den maksimale modpostering i den fysiske lagerværdi er begrænset til antallet af fysiske posteringer og forskellen mellem fysiske og økonomiske priser. Forudsat at alle fysiske posteringer opdateres økonomisk i den sidste ende, kan den fysiske værdi ikke stige til ekstremt høje niveauer. Husk til slut, at risikoen for overestimerings aftager også væsentligt, hvis den akkumulerede modpostering fordeles over flere disponible stykvarer og ikke bare én.


