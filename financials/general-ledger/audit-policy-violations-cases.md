---
title: "Overtrædelser af overvågningspolitik og sager"
description: "I artiklen beskrives det, hvordan revisionssager genereres ud fra overtrædelser af overvågningspolitikregler. Den indeholder også oplysninger om de forskellige metoder for overvågningspolitikkernes brug af datointerval for dokumentvalg."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 77f72c9414f1fad720055e58e3f704b9c713072f
ms.lasthandoff: 03/31/2017


---

# <a name="audit-policy-violations-and-cases"></a>Overtrædelser af overvågningspolitik og sager

I artiklen beskrives det, hvordan revisionssager genereres ud fra overtrædelser af overvågningspolitikregler. Den indeholder også oplysninger om de forskellige metoder for overvågningspolitikkernes brug af datointerval for dokumentvalg.

<a name="how-audit-cases-are-generated"></a>Sådan genereres revisionssager
-----------------------------

Overvågningspolitikker bruges til at identificere udgiftsrapporter, indkøbsordrer og kreditorfakturaer, der ikke overholder de forretningsregler, som du definerer og konfigurerer som regler for overvågningspolitik. 

Overvågningspolitikker køres i batchtilstand. Når du kører en overvågningspolitik, køres alle de politikregler, der er del af den pågældende politik, på samme tidspunkt.

Hver politikregel evaluerer et sæt dokumenter. Politikreglen vælger dokumenter, der ligger i datointervallet for dokumentvalg, og som svarer til de angivne kriterier. En politikregel kan f.eks. vælge udgiftsrapporter, hvor der figurerer måltider, som overstiger 50,00. En anden politikregel kan måske vælge kreditorfakturaer, der skal betales til en bestemt kreditor. For hvert dokument, der er valgt i sættet, genereres der en overtrædelse. Denne overtrædelse registrerer, at et bestemt dokument, f.eks. faktura 12345, ikke overholder politikreglen. 

Flere poster for overtrædelse af overvågning grupperes sammen og knyttes til overvågningssager. Sager til hver overvågningspolitik grupperes som standard efter overvågningspolitikregel. Hvis du foretrækker det, kan du vælge andre kriterier for gruppering ved brug af siden **Kriterier for sagsgruppering**. Du kan eksempelvis gruppere udgift sidehoveder af projekt-ID og leverandør fakturaer efter kreditorkonto. I dette tilfælde alle udgiftshoveder med samme projekt-ID vil blive grupperet under samme sag, og alle kreditorfakturaer med samme kreditorkonto grupperes under samme sag. 

> [!NOTE]
> Regler for overvågningspolitikker, der er baseret på en **Dupliker** forespørgselstype, grupperes i overtrædelser ikke efter politikreglen eller efter de kriterier, der er angivet på den **sag grupperingskriterierne** side. De grupperes i stedet efter de kriterier, der er indbygget i overvågningspolitikreglen. Hvis en politikregel f.eks. evaluerer udgiftsrapporter for dubletudgifter med samme beløb, forhandler-id og dato, vil alle udgifter, der har samme værdier i disse felter, være én sag. Eventuelle udgifter, der har andre værdier, vil udgøre en særskilt sag.

Når revisionssagerne er genereret, håndteres de med brug af typiske processer til sagsstyring.

## <a name="document-selection-date-ranges"></a>Datointervaller for dokumentvalg
Når en overvågningspolitik er kørt, vælger hver politikregel dokumenter af den angivne type, som har en dato, der ligger i datointervallet for dokumentvalg. Datointervallet for dokumentvalg angives på siden **Yderligere indstillinger**. Mange dokumenter har mere end én tilknyttet dato. Det datofelt, der bruges af overvågningspolitikreglen, er angivet på siden **Regeltype**.

Her er nogle andre måder, en overvågningspolitik bruger datointervallet for dokumentvalg på:

-   Politikken bruger den version af hver politikregel, der var gældende på den sidste dag i datointervallet for dokumentvalg. Du kan få vist gyldighedsdatoerne for hver politikregel på listesiden **Overvågningspolitikker**.
-   Politikken bruger de organisationsnoder, der er knyttet til politikken på den sidste dag i datointervallet for dokumentvalg. Det er kun de organisationsnoder, der aktuelt er knyttet til politikken, der vises på listesiden **Overvågningspolitikker**.
-   I forbindelse med politikregler, der er baseret på forespørgselstypen **Listesøgning**, evaluerer politikken dokumenter til overvågede enheder, som er gyldige på den sidste dag i datointervallet for dokumentvalg.


Yderligere oplysninger finder du [regler for overvågningspolitik](audit-policy-rules.md)


