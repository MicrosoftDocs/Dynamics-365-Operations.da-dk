---
title: "Initialisere lagerbeholdninger på lagerstedet"
description: "Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 953125ae6e9d669bd13a3344c9f679747af6ff93
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# Initialisere lagerbeholdninger på lagerstedet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden. (Det er også muligt at opdatere den disponible lagerbeholdning ved at importere posteringer i dataenheder). Du kan køre denne guide i demodatafirmaet USMF, hvor alle de nødvendige komponenter som kladdenavn, vareopsætning, posteringsprofiler og konti er tilgængelige. Guiden foreslår specifikke værdier for varen og dimensionerne, der bruges. Hvis du vælger et andet element, skal du indtaste værdier for forskellige dimensioner.

1. Gå til Lagerstyring > Kladdeposteringer > Elementer > Bevægelser.
2. Klik på Ny.
3. Klik på rullelisten i feltet Navn for at åbne opslaget.
4. Vælg IMov.
    * Det er en god ide at bruge forskellige journalnavnskabeloner for de forskellige forretningsmæssige formål.  
5. Klik op linket i den valgte række på listen.
6. I feltet Modkonto skal du angive værdien "140200".
    * Dette er den modkonto, der skal være standardkontoen på kladdelinjerne. Det er muligt at tilsidesætte standardindstillingerne for at tildele forskellige modkonti pr. linje.  
7. Klik på OK.
8. Klik på Ny.
9. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
10. Vælg vare A0001.
11. Klik op linket i den valgte række på listen.
12. Klik på fanen Lagerdimensioner.
13. Klik på rullelisten i feltet Sted for at åbne opslaget.
14. Vælg sted 1.
15. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
16. Vælg lagersted 13.
17. Klik op linket i den valgte række på listen.
18. Klik på rullelisten i feltet Lokation for at åbne opslaget.
19. Vælg lokalitet 13.
20. Angiv et tal i feltet Antal.
21. Klik på Gem.
22. Klik på Bogfør.
23. Markér eller fjern markeringen af afkrydsningsfeltet Overfør alle posteringsfejl til en ny kladde.
    * Hvis du aktiverer denne indstilling, kopieres alle linjer, der ikke kan bogføres, til en ny journal. Du kan bruge oplysningerne i logfilen til at løse problemerne og derefter bogføre linjerne igen.  
24. Klik på OK.
25. Luk siden.
26. Luk siden.

