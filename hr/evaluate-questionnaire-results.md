---
title: "Få vist og evaluere resultaterne af et spørgeskema"
description: "I dette emne forklares det, hvordan du kan få vist og evaluere resultaterne af de spørgeskemaer, som svarpersonerne har udfyldt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b7c4a612d54f3ae8967be930c0b98e4783fd8200
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# Få vist og evaluere resultaterne af et spørgeskema
<a id="view-and-evaluate-the-results-of-a-questionnaire" class="xliff"></a>

[!include[banner](includes/banner.md)]


I dette emne forklares det, hvordan du kan få vist og evaluere resultaterne af de spørgeskemaer, som svarpersonerne har udfyldt. 

Når svarpersonerne har udfyldt et spørgeskema, kan du få vist og evaluere spørgeskemaresultaterne på følgende måder:

-   **Fuldførte besvarelser** – Få vist oplysninger om de spørgeskemaer, som svarpersonernes har udfyldte, og generér rapporter for at opsummere svar og eventuelle point, der blev opnået.
-   **Resultatgrupper** – Få vist oplysninger om resultatgrupper og statistikker for spørgeskemaer. Statistikker for resultatgrupper kan genereres enten for en enkelt besvarelse af et spørgeskema eller for alle besvarelser.
-   **Spørgeskemastatistik** – Angiv kriterier for at beregne statistik for en bestemt gruppe svarpersoner.

Du kan også generere forskellige rapporter til visning af resultater, der sorteres efter person, besvarelse eller resultatgruppe. Der er følgende tilgængelige rapporter vedrørende udfyldte spørgeskemaer:

-   Besvarelser
-   Besvarelser pr. spørgeskema.
-   Besvarelser pr. person.
-   Feedbackanalyse

## Resultater af besvarelser
<a id="answer-session-results" class="xliff"></a>
Når svarpersoner udfylder et spørgeskema, kan du se resultaterne af de fuldførte besvarelser. En svarsession er en brugers svar på et spørgeskema. Du kan få vist detaljer om fuldførte besvarelser på siden **Svar**. Besvarelser, der findes på siden **Svar**, er filtreret på forskellige måder, afhængigt af hvordan du åbner siden:

-   Alle spørgeskemaer
-   Et bestemt spørgeskema
-   En bestemt person

Fra siden **Svar** kan du se oplysninger om svar, opnåede point, svarpersonens svar i hver resultatgruppe og det spørgsmålshierarki, der blev brugt til det valgte spørgeskema, hvis der blev brugt spørgsmålshierarki. Du kan også generere og udskrive følgende rapporter:

-   **Resultatrapport** – denne rapport viser en grafisk repræsentation af de point, der blev opnået pr. resultatgruppe for den valgte besvarelse.
-   **Svarrapport** – denne rapport viser de svar, som svarpersonen valgte for hver enkelt spørgsmål i spørgeskemaet.
-   **Forkerte svar** – denne rapport indeholder oplysninger, der er relateret til de forkerte svar, som svarpersonen valgte.

> **Bemærk**
>   Rapporten **Resultater** er kun tilgængelig, hvis du bruger resultatgrupper på spørgeskemaet, og hvis du har valgt **Resultatside** på siden **Spørgeskemaer**. Rapporten **Smart** og rapporten **Forkerte svar** er kun tilgængelige, hvis du har valgt **Svarrapport** på siden **Spørgeskemaer**.

## Spørgeskemastatistik
<a id="questionnaire-statistics" class="xliff"></a>
Du kan bruge spørgeskemastatistik til at analysere resultaterne af et udfyldt spørgeskema baseret på beregninger, som du definerer. Når du skal definere beregninger, skal du udføre følgende opgaver:

-   Vælg kriterier til at beregne og få vist statistikken.
    -   Du kan få vist statistik efter spørgeskema, spørgsmål, spørgsmålsrækker eller grupper af resultater.
    -   Vælg den type diagram, der skal bruges, når du får vist resultaterne.
    -   Vælg persontyper fra netværket, f.eks. medarbejder, kontakter eller ansøger, som du vil medtage svar fra. Du kan også medtage svar fra spørgeskemaer, der blev fuldført anonymt.
    -   Definer intervaller, der er baseret på alder eller anciennitet for at analysere resultaterne.
-   Vælg eller kontrollér indstillinger, der afgrænser emnet i statistikken. Ved at vælge et postnummer kan du f.eks. analysere resultater fra alle svarpersoner i et specifikt geografisk område.
-   Vælg eller bekræft kriterier til at analysere resultaterne efter svarperson eller spørgeskemakarakteristika. Hvis du vælger **Postnummer**, kan du f.eks. analysere korrelationen mellem en svarpersons placering og korrekte svar.

De indstillinger, du definerer, gemmes og kan bruges til at genberegne resultater med jævne mellemrum.

Se også
<a id="see-also" class="xliff"></a>
--------

[Udforme spørgeskemaer](design-questionnaires.md)

[Brug af spørgeskemaer](questionnaires.md)

[Distribution og udfyldning af et spørgeskema](distribute-questionnaires.md)



