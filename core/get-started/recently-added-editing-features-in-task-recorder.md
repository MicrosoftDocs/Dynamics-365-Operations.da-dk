---
title: "Redigeringsfunktioner tilføjet for nylig i Arbejdsrutineoptager"
description: Hvis du bruger Arbejdsrutineoptager til at oprette opgaveguider, kan du redigere dine filer mere effektivt med de funktioner, der er beskrevet i denne wiki.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Redigeringsfunktioner tilføjet for nylig i Arbejdsrutineoptager

Hvis du bruger Arbejdsrutineoptager til at oprette opgaveguider, kan du redigere dine filer mere effektivt med de funktioner, der er beskrevet i denne wiki.

Disse funktioner er tilgængelige i menuen **indstillinger &gt; Arbejdsrutineoptager &gt; Rediger optagelse**.

-   Indsæt trin uden at optage hele filen igen.
-   Flyt trin under en underordnet opgave uden optage hele filen igen.
-   Skjul felterne med registreringens navn og beskrivelse.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Indsæt trin uden at optage hele filen igen.
Du kan nu tilføje et trin overalt i en opgaveguide uden at afspille eller optage hele filen igen.

1.  Vælg det trin, hvor du ønsker, at det nye trin skal indsættes efter. Kontrollér, at trinnet er fremhævet.

For at Arbejdsrutineoptager kan indsætte et trin, skal du have den rigtige side åben. Den rigtige side er den side, hvor det nye trin forekommer på. Arbejdsrutineoptager har en mekanisme, der bestemmer, hvad den aktive side er, og den vil deaktivere funktionen, hvis den korrekte side ikke er åbent. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Når du er på den rigtige side bliver **Indsæt trin** tilgængelig.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klik på **Indsæt trin**.

Når du klikker på **Indsæt trin**, skifter Arbejdsrutineoptager til registreringstilstand. Alle handlinger, der foretages i brugergrænsefladen, registreres nu og tilføjes på stedet som trin.

3. Klik på **Stop**.

Du kan gentage processen og tilføje så mange trin eller flytte så mange underordnede opgaver som nødvendigt (se nedenfor om underopgaver).

4. Når du er færdig med at redigere opgaveguiden, skal du klikke på **Redigeringen blev afsluttet** og derefter vælge en af indstillingerne for at gemme eller udgive opgaveguiden.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Flyt trin under en underordnet opgave uden at registrere hele filen igen
Du kan flytte trin under en underordnet opgave uden at registrere hele filen igen. Du kan også flytte underopgavetrinnet eller afslutte underopgavetrinnet, hvis du vil gruppere en eksisterende blok af trin.

1.  Vælg det trin eller det underopgavetrin, du vil flytte. Kontrollér, at trinnet er fremhævet.
2.  Klik på ellipsen, og klik derefter på **Flyt trin efter**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Vælg det trin eller underopgavetrin, du vil flytte trinnet eller underopgavetrinnet efter. Arbejdsrutineoptager flytter trinnet.

4. Hvis du vil flytte det sidste underopgavetrin, skal du markere det, klikke på ellipsen, klikke på **Flyt trin efter** og derefter vælge det trin, hvorefter du ønsker, at det sidste underopgavetrin skal være.

Hvis du ønsker, at det første trin i opgaveguiden skal ligge inden for en underopgave, skal du oprette et underopgavetrin som andet trin, og derefter flytte det første trin ind i det. Du kan tilføje eller flytte så mange trin eller underopgaver, som det er nødvendigt.

5. Når du er færdig med at redigere opgaveguiden, skal du klikke på **Redigeringen blev afsluttet** og derefter vælge en af indstillingerne for at gemme eller udgive opgaveguiden.

## <a name="collapse-recording-name-and-description"></a>Skjul registreringens navn og beskrivelse.
Du kan udvide og skjule felterne **Registreringsnavn** og **Beskrivelse af registrering**. Når disse felter er skjult, vil flere trin være synlige i redigeringsruden i Arbejdsrutineoptager. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Se også
--------

[Oprette dokumentation eller undervisning ved hjælp af opgaveregistreringer](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Hurtig reference til Arbejdsrutineoptager](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


