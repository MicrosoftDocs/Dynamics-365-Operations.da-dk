---
title: "Overtrædelser af overvågningspolitik og sager"
description: "I artiklen beskrives det, hvordan revisionssager genereres ud fra overtrædelser af overvågningspolitikregler. Den indeholder også oplysninger om de forskellige metoder for overvågningspolitikkernes brug af datointerval for dokumentvalg."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 882f99beff256f96b6879c4af4c4ca8a6c4dbec3
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="audit-policy-violations-and-cases"></a>Overtrædelser af overvågningspolitik og sager

[!include[banner](../includes/banner.md)]


I artiklen beskrives det, hvordan revisionssager genereres ud fra overtrædelser af overvågningspolitikregler. Den indeholder også oplysninger om de forskellige metoder for overvågningspolitikkernes brug af datointerval for dokumentvalg.

<a name="how-audit-cases-are-generated"></a>Sådan genereres revisionssager
-----------------------------

Overvågningspolitikker bruges til at identificere udgiftsrapporter, indkøbsordrer og kreditorfakturaer, der ikke overholder de forretningsregler, som du definerer og konfigurerer som regler for overvågningspolitik. 

Overvågningspolitikker køres i batchtilstand. Når du kører en overvågningspolitik, køres alle de politikregler, der er del af den pågældende politik, på samme tidspunkt.

Hver politikregel evaluerer et sæt dokumenter. Politikreglen vælger dokumenter, der ligger i datointervallet for dokumentvalg, og som svarer til de angivne kriterier. En politikregel kan f.eks. vælge udgiftsrapporter, hvor der figurerer måltider, som overstiger 50,00. En anden politikregel kan måske vælge kreditorfakturaer, der skal betales til en bestemt kreditor. For hvert dokument, der er valgt i sættet, genereres der en overtrædelse. Denne overtrædelse registrerer, at et bestemt dokument, f.eks. faktura 12345, ikke overholder politikreglen. 

Flere poster for overtrædelse af overvågning grupperes sammen og knyttes til overvågningssager. Sager til hver overvågningspolitik grupperes som standard efter overvågningspolitikregel. Hvis du foretrækker det, kan du vælge andre kriterier for gruppering ved brug af siden **Kriterier for sagsgruppering**. Du kan f.eks. gruppere udgiftshoveder efter projekt-id og kreditorfakturaer efter kreditorkonto. I dette tilfælde bliver alle overtrædelser af udgiftshoveder, der har samme projekt-id, grupperet under samme sag, og alle kreditorfakturaer, der har samme kreditorkonto, bliver grupperet under samme sag. 

> [!NOTE]
> Ved regler for overvågningspolitikker, der er baseret på forespørgselstypen **Dublet**, grupperes overtrædelser ikke efter politikregel eller efter de kriterier, der er angivet på siden **Kriterier for sagsgruppering**. De grupperes i stedet efter de kriterier, der er indbygget i overvågningspolitikreglen. Hvis en politikregel f.eks. evaluerer udgiftsrapporter for dubletudgifter med samme beløb, forhandler-id og dato, vil alle udgifter, der har samme værdier i disse felter, være én sag. Eventuelle udgifter, der har andre værdier, vil udgøre en særskilt sag.

Når revisionssagerne er genereret, håndteres de med brug af typiske processer til sagsstyring.

## <a name="document-selection-date-ranges"></a>Datointervaller for dokumentvalg
Når en overvågningspolitik er kørt, vælger hver politikregel dokumenter af den angivne type, som har en dato, der ligger i datointervallet for dokumentvalg. Datointervallet for dokumentvalg angives på siden **Yderligere indstillinger**. Mange dokumenter har mere end én tilknyttet dato. Det datofelt, der bruges af overvågningspolitikreglen, er angivet på siden **Regeltype**.

Her er nogle andre måder, en overvågningspolitik bruger datointervallet for dokumentvalg på:

-   Politikken bruger den version af hver politikregel, der var gældende på den sidste dag i datointervallet for dokumentvalg. Du kan få vist gyldighedsdatoerne for hver politikregel på listesiden **Overvågningspolitikker**.
-   Politikken bruger de organisationsnoder, der er knyttet til politikken på den sidste dag i datointervallet for dokumentvalg. Det er kun de organisationsnoder, der aktuelt er knyttet til politikken, der vises på listesiden **Overvågningspolitikker**.
-   I forbindelse med politikregler, der er baseret på forespørgselstypen **Listesøgning**, evaluerer politikken dokumenter til overvågede enheder, som er gyldige på den sidste dag i datointervallet for dokumentvalg.


Du kan finde flere oplysninger i [Overvåge politikregler](audit-policy-rules.md)




