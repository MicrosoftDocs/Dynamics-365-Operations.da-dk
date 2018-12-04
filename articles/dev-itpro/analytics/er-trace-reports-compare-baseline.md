---
title: "Spore genererede rapportresultater og sammenligne dem med basisværdier"
description: "Dette emne indeholder oplysninger om, hvordan du kan sammenligne resultaterne af oprettede ER-rapporter med basisrapportværdier."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Spore genererede rapportresultater og sammenligne dem med basisværdier

[!include[banner](../includes/banner.md)]

Du kan spore resultaterne af ER-formater, der genererer udgående elektroniske dokumenter. Når sporingsgenerering er aktiveret (ER-brugerparameteren **Kør i fejlfindingstilstand**), genereres en ny sporingspost i ER-formatudførelsesloggen, hver gang denne ER-rapport køres. Følgende oplysninger gemmes i de enkelte spor, der genereres:

- Alle advarsler, der er oprettet af valideringsregler
- Alle fejl, der er oprettet af valideringsregler
- Alle genererede filer, der er gemt som vedhæftede filer, af sporingsposten

Du kan gemme individuelle basisprogramfiler til ethvert ER-format. Filer betragtes som basisfiler, når de beskriver de forventede resultater af rapporter, der køres. Hvis en basisfil er tilgængelig for et ER-format, som blev kørt, mens sporingsgenereringen var aktiveret, gemmer sporingen ud over de oplysninger, der blev nævnt tidligere, resultatet af sammenligningen af det genererede elektroniske dokument i basisfilen. Med et enkelt klik kan du også få det genererede elektroniske dokument og dets basisfil i en enkelt zip-fil. Derefter kan du foretage detaljeret sammenligning ved hjælp af et eksternt værktøj, f.eks. Windiff.

Du kan evaluere sporingen for at analysere, om de elektroniske dokumenter, der genereres, medtager det forventede indhold. Du kan foretage denne evaluering i et UAT-testmiljø til brugeraccept, når kodebasen er blevet ændret (f.eks. når du har overflyttet til en ny forekomst af programmet, installeret hotfix-pakker eller implementeret ændringer af koden). På denne måde kan du sikre dig, at vurderingen ikke påvirker udførelsen af ER-rapporter, der er i brug. For mange ER-rapporter kan evalueringen foretages i uovervåget tilstand.

Du kan finde flere oplysninger om denne funktion ved at afspille opgaveguiderne **ER Generere rapporter og sammenligne resultater (del 1)** og **ER Generere rapporter og sammenligne resultater (del 2)**, der er en del af forretningsprocessen **7.5.4.3 Test it-ydelser og -løsninger ( 10679)** og kan hentes fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Disse opgaveguider gennemgår, hvordan ER-strukturen konfigureres til at bruge basisfiler for at evaluere genererede elektroniske dokumenter.

