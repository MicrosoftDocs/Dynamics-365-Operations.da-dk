---
title: Efterspørgselsbaseret planlægning
description: I artiklen beskrives, hvordan der genereres ordreforslag for varer, der angives som nedposteringspunkter.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 4dadd8e258af6e6ffbe8c28fc8f9be511fcdb5bc
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186681"
---
# <a name="demand-driven-planning"></a>Efterspørgselsbaseret planlægning

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

I artiklen beskrives, hvordan der genereres ordreforslag for varer, der angives som nedposteringspunkter.

## <a name="net-flow-and-qualified-demand"></a>Nettoflow og kvalificeret efterspørgsel

Ved varedisponering anvender systemet begrebet *nettoflow* for at fastlægge det faktiske disponible antal på basis af den faktiske disponible lagerbeholdning plus den lagerbeholdning, der er i bestilling (eksisterende forsyningsordrer, der endnu ikke er modtaget), minus det, der kaldes *kvalificeret efterspørgsel* (kvalificeret først salg), som vist i følgende illustration. Når systemet afgør, hvilken bufferzone en vare tilhører, og hvad det bestilte antal skal være, evaluerer systemet nettoflowet og ikke den faktiske disponible lagerbeholdning.

![Eksempel på et diagram med nettoflowberegninger.](media/ddmrp-net-flow-example.png "Eksempel på et diagram med nettoflowberegninger")

Når der udløses et ordreforslag under en planlægningskørsel, vil det bestilte antal være maksimumniveauet minus nettoflowet. Hvis der skal tildeles en ordreprioritet, bruger systemet [prioriteret planlægningsfunktionalitet](priority-based-planning.md) i stedet for behovsdatoer. DDMRP (Demand Driven Material Requirements Planning) tildeler prioriteten for et ordreforslag på basis af det bestilte antal som en procentdel af det maksimale lager. I ovenstående illustration er det bestilte antal 53 procent af maksimumantallet. Ordreprioriteten for genopfyldning er derfor 53. (I forbindelse her er 0 den højeste prioritet, og 100 er den laveste prioritet).

*Kvalificeret* efterspørgsel er det forfaldne behov plus dagens behov plus kvalificeret ordre i fremtiden. I følgende illustration vises et eksempel på efterspørgselsniveauer for i dag (d. 12. juni) og de næste tre dage. DDMRP giver dig mulighed for at angive en ordregrænse for at identificere efterspørgsel, der overstiger de normale forventninger. Hvis grænseværdien er angivet til 25 styk, vil to af de fremtidige datoer, der vises i illustrationen, være ordrerækkefølge. Du skal tildele en ordretærskel for de enkelte produkter individuelt ved hjælp af **varens disponeringsside** som beskrevet i [Opsætning af buffere for en vare, der afgrænser varen.](ddmrp-buffer-profile-and-levels.md#set-up-buffers)

![Eksempel på et diagram med kvalificeret efterspørgselsberegninger.](media/ddmrp-net-qualified-demand-example.png "Eksempel på et diagram med kvalificeret efterspørgselsberegninger")

Hvis der ikke er noget forfaldent behov, kan du nu føje dagens efterspørgsel (18) til mængderne i de to ordresæt (29 og 26) for at få en kvalificeret efterspørgsel på 73. Selv om der er efterspørgsel efter 23. juni, skal du bemærke, at den ikke indgår i nettoflowberegningen, da DDMRP udløser et ordreforslag på en anden måde end de traditionelle planlægningsdisponeringsgrupper.

## <a name="generating-planned-orders-with-ddmrp"></a>Oprette ordreforslag med DDMRP

Under en planlægningskørsel opretter systemet et nyt ordreforslag, hvis nettoflowet for en vare falder under restordrepunktet. Når du bruger DDMRP, vil du normalt udføre en planlægningskørsel hver dag. Derfor kontrollerer du egentlig lagerniveauet en gang om dagen for at bestemme, hvilke varer der skal genopfyldes.

I følgende illustration vises et eksempel på en situation, hvor der bestilles 18 stk. den 20. juni, 29 stk. d. 21. juni, 26 stk. d. 22. juni og 20 stk. d. 23. juni. Da grænseværdien for fastværdi er angivet til 25 styk, markeres to af disse ordrer som ordrer. Der er 220 styk af denne vare i findes.

![Planlægningseksempel 1.](media/ddmrp-planning-example-1.png "Planlægningseksempel 1")

Hvis du kører behovsplanlægning nu, genererer den et ordreforslag, hvis nettoflowet viser sig at falde under bestillingsstedet (219 styk i dette eksempel).

![Planlægningseksempel 2.](media/ddmrp-planning-example-2.png "Planlægningseksempel 2")

I dette eksempel produceres et indkøbsordreforslag for et antal på 130, hvilket er lig med maksimumniveauet minus nettoflowet. Ordreforslaget tildeles en prioritet på 53,07 baseret på dets procentdel af det maksimale antal. Da disse værdier blev fundet d. 20. juni, opretter systemet et ordreforslag, der er dateret 20. juni plus den udskudte leveringstid for varen (fem arbejdsdage i dette eksempel). Da fem arbejdsdage er en uge fra i dag, er ordreforslaget derfor dateret 27. juni.

> [!NOTE]
> Planlægningsoptimering beregner kun varedisponerede varer ved hjælp af DDMRP. Alle andre varer beregnes ved hjælp af MRP (Standard Material Requirements Planning).
