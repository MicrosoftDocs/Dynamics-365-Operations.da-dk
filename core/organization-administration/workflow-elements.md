---
title: Arbejdsgangselementer
description: "I denne artikel beskrives de forskellige elementer, der indgår i en arbejdsgang."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee20b567b402bf638a54f6394159f7f8a9f02da6
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-elements"></a>Arbejdsgangselementer

I denne artikel beskrives de forskellige elementer, der indgår i en arbejdsgang.

En arbejdsgang består af elementer. Følgende afsnit indeholder beskrivelser af hver type element.

## <a name="tasks"></a>Opgaver
En *opgave* er en arbejdsenhed, der skal udføres. To typer af opgaver kan føjes til en arbejdsgang: manuelle opgaver eller automatiserede opgaver.

### <a name="manual-task"></a>Manuel opgave

En *manuel opgave* er en arbejdsenhed, der skal udføres af en bruger. En arbejdsgang for en udgiftsrapport kan f.eks. have manuelle opgaver, der kræver, at de brugere, der har fået tildelt opgaven, skal udføre følgende handlinger:

-   Gennemgå de kvitteringer, der er indsendt sammen med en udgiftsrapport.
-   Kontakte en medarbejders chef.

### <a name="automated-task"></a>Automatiseret opgave

En *automatiseret opgave* er en arbejdsenhed, der skal udføres af systemet. Der kræves ingen brugerindgriben. En arbejdsgang for en salgsordre kan f.eks. have automatiserede opgaver, der kræver, at systemet skal udføre følgende handlinger:

-   Udføre kreditkontrol.
-   Oprette en kundepost for kunden, hvis der ikke allerede findes en post.

## <a name="approval-processes"></a>Godkendelsesprocesser
En *godkendelsesproces* er en proces, der består af separate trin. På hvert enkelt godkendelsestrin kan brugeren udføre følgende handlinger:

-   Godkend dokumentet.
-   Afvis dokumentet.
-   Anmode om en ændring af dokumentet.
-   Tildele dokumentet til en anden bruger til godkendelse.

## <a name="lineitem-workflow-elements"></a>Lineitem elementer i arbejdsgang
En arbejdsgang kan oprettes for at behandle enten dokumenter eller linjeelementerne i et dokument. Du har f.eks. oprettet en godkendelsesarbejdsgang for timesedler. (Vi vil henvise til denne arbejdsproces som de *dokumentarbejdsgang*.) Du kan tilføje en *linjeelement arbejdsprocessen* element til denne dokumentarbejdsgang. Når elementet i linjeelementet køres, sendes hvert linjeelement i dokumentet til behandling. Det kan være, at du vil have alle linjeelementer behandlet af samme arbejdsgang for linjeelement, eller at du vil måske have hvert enkelt linjeelement behandlet af en særskilt arbejdsgang for linjeelement. Antag, at en medarbejder har sendt en timeseddel, der ligner nedenstående figur. ![Arbejdsgang med linjeelementer](./media/workflow_lineitemworkflow.gif) I dette scenario kan du muligvis oprette følgende arbejdsgange for linjeelementer:

-   **Arbejdsgang for linjeelement 1** – denne arbejdsgang bruges til at behandle linjeelementer, hvor projekt-id er 1111.
-   **Arbejdsgang for linjeelement 2** – denne arbejdsgang bruges til at behandle linjeelementer, hvor projekt-id er 2222.
-   **Arbejdsgang for linjeelement 3** – denne arbejdsgang bruges til at behandle linjeelementer, hvor projekt-id er 3333.

## <a name="flowcontrol-elements"></a>Flowcontrol elementer
Følgende elementer sætter dig i stand til at designe arbejdsgange, der har alternative forgreninger eller grene, der kører samtidigt.

### <a name="manual-decision"></a>Manuel beslutning

En *manuel beslutning* er et punkt, hvor en arbejdsgang deles i to grene. En bruger skal træffe en beslutning, og med denne beslutning bestemmes det, hvilken gren der bliver brugt til behandling af det sendte dokument.

### <a name="conditional-decision"></a>Betinget beslutning

En *betinget beslutning* er også et punkt, hvor en arbejdsgang deles i to grene. Men systemet bestemmer, hvilken forgrening der bruges til at behandle det sendte dokument. For at træffe denne beslutning evaluerer systemet dokumentet for at afgøre, om det opfylder de angivne betingelser.

### <a name="parallel-activity"></a>Parallel aktivitet

En *parallel aktivitet* er et arbejdsgangselement, der omfatter to eller flere arbejdsgangsgrene, som kører samtidigt.

### <a name="subworkflow"></a>Underarbejdsgang

En *underarbejdsgang* er en arbejdsgang, der køres inden for rammerne af en anden arbejdsgang.

