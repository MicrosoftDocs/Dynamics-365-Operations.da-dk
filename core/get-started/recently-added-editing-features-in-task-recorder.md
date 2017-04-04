---
title: "Tilføjet for nylig redigeringsfunktioner i Arbejdsrutineoptager"
description: "Hvis du bruge Arbejdsrutineoptager til at oprette hjælpelinjer til opgaven, kan du redigere dine filer mere effektivt med de funktioner, der er beskrevet i denne wiki."
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

# <a name="recently-added-editing-features-in-task-recorder"></a>Tilføjet for nylig redigeringsfunktioner i Arbejdsrutineoptager

Hvis du bruge Arbejdsrutineoptager til at oprette hjælpelinjer til opgaven, kan du redigere dine filer mere effektivt med de funktioner, der er beskrevet i denne wiki.

Disse funktioner er tilgængelige på den **indstillinger &gt;Arbejdsrutineoptager &gt;Rediger optagelse** i menuen.

-   Indsæt trin uden indtalingen hele filen.
-   Flyt trin under en underordnet opgave uden indtalingen hele filen.
-   Skjul registrering navn og beskrivelse.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Indsæt trin uden rerecording hele filen
Du kan nu tilføje et trin overalt i en opgave-guide uden afspiller eller optager hele filen igen.

1.  Vælg det trin, hvor du ønsker nye trinnet skal indsættes. Kontroller, at trinnet er fremhævet.

Arbejdsrutineoptager indsætte et trin skal, du have den rigtige side, der er åbne. Den rigtige side er siden, hvor det nye trin forekommer. Arbejdsrutineoptager har en mekanisme, der bestemmer, hvad den aktive side er, og vil deaktivere funktionen, hvis den korrekte side ikke er åbent. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Når du er på den rigtige side **Indsæt trin** bliver tilgængelige.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klik på **Indsæt trin**.

Når du klikker på **Indsæt trin**, Arbejdsrutineoptager skifter til post-tilstand. Eventuelle foranstaltninger truffet i Brugergrænsefladen, nu registreres og tilføjes i stedet som trin.

3. Klik på **holder**.

Du kan gentage processen, at tilføje så mange trin eller flytte så mange underordnede opgaver efter behov (se nedenfor for at underopgaver).

4. Når du er færdig redigering opgave programguiden, skal du klikke på **færdig med at redigere**, og vælg derefter en af indstillingerne for at gemme eller udgive opgave-vejledning.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Flyt trin under en underopgave uden rerecording hele filen
Du kan flytte trin under en underordnet opgave uden afspiller eller optager hele filen igen. Du kan også flytte trinnet underopgave eller slutningen underopgavens trin, hvis du vil gruppere en eksisterende blok af trin.

1.  Vælg det trin eller underopgave trin, du vil flytte. Sørg for, at trinnet er fremhævet.
2.  Klik på ellipsen, og klik derefter på **Flyt trin efter**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Vælg det trin eller underopgave trin, du vil flytte eller underopgave trin trin efter. Arbejdsrutineoptager, flyttes trinnet.

4. Flyt trin end underopgave, markere den, klik på ellipsen, klikke på **Flyt trin efter**, og vælg derefter det trin, hvorefter du vil ende underopgavens trin til at være.

Det første trin i guiden opgave skal ligge inden for en underordnet opgave skal du oprette en underordnet opgave trin som andet trin, og derefter flytte det første trin i den. Du kan tilføje eller flytte så mange trin eller underordnede opgaver efter behov.

5. Når du er færdig redigering opgave programguiden, skal du klikke på **færdig med at redigere**, og vælg derefter en af indstillingerne for at gemme eller udgive opgave-vejledning.

## <a name="collapse-recording-name-and-description"></a>Skjul optagelse navn og beskrivelse
Du kan udvide og skjule de **optagelse navn** og **optagelse beskrivelse** felter. Når disse felter er skjult, er yderligere trin være synlig i Arbejdsrutineoptager redigere rude. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Se også
--------

[Oprette dokumentation eller undervisning ved hjælp af opgaveregistreringer](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Hurtig reference til opgave-optager](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


