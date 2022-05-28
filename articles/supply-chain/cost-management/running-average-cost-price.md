---
title: Løbende gennemsnitskostpris
description: Under processen til lagerlukning udlignes afgangsposteringer i forhold til tilgangsposteringer på baggrund af den metode til lagerværdi, der er valgt i varens varemodelgruppe. Men inden lagerlukningen køres, beregner systemet en løbende gennemsnitskostpris, der typisk bruges, når afgangsposteringer bogføres.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672172"
---
# <a name="running-average-cost-price"></a>Løbende gennemsnitskostpris

[!include [banner](../includes/banner.md)]

Under processen til lagerlukning udlignes afgangsposteringer i forhold til tilgangsposteringer på baggrund af den metode til lagerværdi, der er valgt i varens varemodelgruppe. Men inden lagerlukningen køres, beregner systemet en løbende gennemsnitskostpris, der typisk bruges, når afgangsposteringer bogføres.

Systemet estimerer denne løbende gennemsnitskostpris for en vare ved hjælp af følgende formel:

Estimeret pris = (fysisk beløb + økonomisk beløb) ÷ (fysisk antal + økonomisk antal)

## <a name="default-item-cost"></a>Standardvareomkostning

Standardvareomkostningerne for et frigivet produkt kan konfigureres på en af to måder på siden **Frigivne produktdetaljer**:

- Opret en standardomkostning ved at vælge **Varepris** i gruppen **Konfigurer** under fanen **Administrer omkostninger** i handlingsruden. Hvis du bruger denne metode, skal du bruge en standardomkostnings efterkalkulationsversion, og omkostningen skal være aktiveret.
- Definer en standardvarekostpris for et frigivet produkt ved at angive en værdi i feltet **Pris** i oversigtspanelet **Administrer omkostninger**.

Ud over at angive eller oprette en pris kan du markere afkrydsningsfeltet **Anvend seneste kostpris** i oversigtspanelet **Administrer omkostninger** på siden **Frigivne produktdetaljer**. I dette tilfælde opdaterer systemet automatisk feltet **Pris**, når du bogfører en økonomisk opdatering. Hvis du f.eks. bogfører en indkøbsordrefaktura, angives feltet til købsprisen fra denne faktura.

Hvis du har en kostpris i en aktiv efterkalkulationsversion, og du angiver en pris i oversigtspanelet **Administrer omkostninger**, bruger systemet prisen fra den aktive efterkalkulationsversion, før det bruger den pris, der er defineret i oversigtspanelet **Administrer omkostninger**.

## <a name="using-the-running-average-cost-price"></a>Brug af den løbende gennemsnitskostpris

I nedenstående tabel vises det, hvornår systemet bogfører lagerposteringer ved hjælp af den løbende gennemsnitskostpris, og hvornår programmet i stedet bruger den kostpris, der er angivet på stamdataposten for varen.

| Betingelse | Systemet bruger den beregnede løbende gennemsnitskostpris | Systemet bruger standardvarekostprisen |
| --- | --- | --- |
| Tælleren\* og nævneren\*\* er begge positive. | Ja | Nej |
| Tælleren\*, nævneren\*\* eller begge er negative. | Nej | Ja |
| Nævneren\*\* er 0 (nul). | Nej | Ja |

\* Tæller = (Fysisk beløb + Økonomisk beløb)  
\*\* Nævner = (Fysisk antal + Økonomisk antal)

> [!NOTE]
> Hvis indstillingen **Medtag fysisk værdi** ikke er valgt for en vare, bruger systemet 0 (nul) til både det fysiske beløb og det fysiske antal. Oplysninger om denne indstilling finder du under [Medtag fysisk værdi](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Undgå overestimering af priser

Det kan evt. forekomme, at systemet beregner priser for flere afgange, før der et tilstrækkeligt antal tilgange at basere prisen på. Dette scenario kan forårsage, at estimater af den løbende gennemsnitskostpris bliver alt for oppustede. Du kan dog undgå overestimering af priser eller reducere de negative virkninger, når det opstår.

**Scenarie:** Følgende posteringer forekommer for en vare, du har valgt indstillingen **Medtag fysisk værdi** for:

1. Økonomisk modtager du et antal på 100 til kr. 100,00.
2. Du udsteder økonomisk et antal på 200.
3. Du modtager fysisk et antal på 101 til kr. 202,00.

Når du undersøger den estimerede løbende gennemsnitskostpris for en vare, forventer du en kostpris på kr. 1,51. Du får i stedet en estimeret løbende gennemsnitskostpris på kr. 102,00 ved hjælp af følgende formel:

Estimeret pris = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Denne overestimering af priser sker, da der udstedes 200 varer økonomisk i trin 2, så systemet er tvunget til at prissætte 100 af varerne, før der er tilsvarende tilgange. Denne situation medfører negativ lagerbeholdning. Systemet estimerer derefter en enhedspris på kr. 1,00, som vi kunne forvente det. Når de tilsvarende 100 tilgange ankommer, bliver de dog er til en enhedspris på kr. 2,00.

> [!NOTE]
> Selvom afgangene medfører negativt lager, er lageret positivt, når afgangsprisen beregnes. Derfor bruges den løbende gennemsnitskostpris og ikke prisen fra varens stamdata. På dette tidspunkt findes der i systemet en lagermodværdi på kr. 100,00. Mens modværdien blev bygget på 100 styk, hvor der var en enhedsmodværdi på kr. 1,00 pr. styk, er der nu kun ét styk på lageret. Denne modværdi på kr. 100,00 fordeles derfor til dette ene styk. Resultatet er, at den forkalkulerede kostpris fejlvurderes.
>
> Til sammenligning kan du bemærke, at hvis trin 2 og 3 tilbageføres i ovenstående scenarie, vil der blive udlagret 200 styk til en enhedspris på kr. 1,51, og prisen for 1 styk vil fortsat være kr. 1,51. Da denne overestimering kan forekomme, når der forekommer negativt lager, er det svært at undgå i følgende situationer:
>
> - Du skal estimere afgangspriserne for værdien og antallet for det disponible antal.
> - Du skal justere den værdien og antallet for den disponible lagerbeholdning på afgange og tilgange.
> - Forretningsmodellen tillader, at du udsender eller prissætter flere styk, end der er på lager.
> - Du skal acceptere alle tilgangsværdier og tilgangsantal, der sendes til dig.

Hvis din forretningsmodel tillader det, kan følgende fremgangsmåder dog hjælpe dig med at undgå, at negative antal muliggør denne overestimering af priser:

- Hvis du vælger indstillingen **Medtag fysisk værdi** for en vare, skal du fjerne markeringen i afkrydsningsfeltet **Fysisk negativt lager** på siden **Varemodelgrupper**.
- Hvis du **ikke** vælger indstillingen **Medtag fysisk værdi** for en vare, skal du fjerne markeringen i **Økonomisk negativt lager** afkrydsningsfeltet på siden **Varemodelgrupper**.

Husk også, at den maksimale modpostering i den fysiske lagerværdi er begrænset til antallet af fysiske posteringer og forskellen mellem fysiske og økonomiske priser. Forudsat at alle fysiske posteringer opdateres økonomisk i den sidste ende, kan den fysiske værdi ikke stige til ekstremt høje niveauer. Husk til slut, at risikoen for overestimerings aftager også væsentligt, hvis den akkumulerede modpostering fordeles over flere disponible stykvarer og ikke bare én.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Undgå en kostpris på nul på afgange

Når indstillingen **Medtag fysisk værdi** ikke markeres på siden **Varemodelgruppe**, kan en lagerafgang have en kostpris på nul, hvis der ikke er nogen økonomisk opdaterede tilgange på lageret. Overvej følgende muligheder for at undgå dette scenarie:

- Markér feltet **Medtag fysisk værdi** på siden **Varemodelgruppe**. Denne indstilling vil forhindre en kostpris på nul for en afgang, forudsat at tilgangen opdateres fysisk. Hvis du ikke tillader negativt fysisk lager, beregner afgange det løbende gennemsnit fra de fysisk opdaterede transaktioner.
- Opret en standardvarekostpris ved at aktivere en efterkalkulationsversion, der har en standardkostpris, eller angiv prisen i oversigtspanelet **Administrer omkostninger** på siden **Frigivne produktdetaljer**. Denne indstilling er bedst, når indstillingen **Medtag fysisk værdi** ikke er valgt på siden **Varemodelgruppe**, da systemet altid vil have en reservepris at bruge.
- Vælg indstillingen **Anvend seneste kostpris** i oversigtspanelet **Administrer omkostninger** på siden **Frigivne produktdetaljer**. Denne indstilling holder feltet **Pris** opdateret, hver gang du opdaterer en tilgang økonomisk. Hvis du vælger denne indstilling, men ikke angiver en standardpris eller aktiverer en omkostning i en standardefterkalkulationsversionen, kan du stadig have en kostpris på nul for en afgang.

Hvis du har afgangsposteringer, der har nul omkostninger, vil processen *Lagerlukning og -regulering* rette kostprisen ved at oprette en regulering, efter at tilgangene er økonomisk opdateret. Husk på, at den økonomiske periode, hvor denne opdatering finder sted, kan være forskellig fra den økonomiske periode, hvor varerne fysisk er modtaget eller afsendt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
