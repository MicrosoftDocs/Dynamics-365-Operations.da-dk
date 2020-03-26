---
title: Brug en relativ sti i databindinger for ER-modeller og -formater
description: ER-værktøjet (Electronic Reporting) giver brugerne mulighed for at definere elektroniske formatstrukturer og derefter beskrive, hvordan disse strukturer skal udfyldes ved hjælp af de data og algoritmer, der findes i programmet.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2940d99243ac52ee0d56a1c4423c4f0250f42f57
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091766"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Brug en relativ sti i databindinger for ER-modeller og -formater

[!include[banner](../includes/banner.md)]

ER-værktøjet (Electronic Reporting) giver brugerne mulighed for at definere elektroniske formatstrukturer og derefter beskrive, hvordan disse strukturer skal udfyldes ved hjælp af de data og algoritmer, der findes i programmet. Du kan finde flere oplysninger under [Oprette ER-konfigurationer (Electronic reporting)](electronic-reporting-configuration.md). Hvis du vil angive dataflowet til hentning af Finance and Operations-data og bruge dem til at generere et elektronisk dokument, skal du gøre følgende:

- Bind konfigurerede datakilder til elementer i den domænespecifikke datamodel, der er designet. Modelstrukturen og de valgte datakilder kan være en del af en kompleks hierarkisk struktur. Derfor kan endelige bindinger være temmelig store og indeholde mange elementer af forskellige typer (f.eks. relationer, tabeller og metoder). Bindingerne kan blive mindre læselige og ret komplekse at gennemgå og forstå, især for ikke-ejere. 
- Bind datamodelelementer med formateringskomponenter for at definere, hvilke data der udfyldes fra datamodellen til det genererede output.

Hvis du vil forbedre anvendeligheden af ER-tilknytningsdesignere, er funktionen relativ sti blevet udgivet. Indstillingen for gengivelsen af den relative sti er som standard slået til for alle nye forekomster af programmet, hvor ER-designoplevelsen er aktiveret (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Vi har implementeret den relative sti, så brugerne kan fortsætte med at bruge den fulde sti, når arbejdet med denne præsentation med ER-bindinger.

[![Brugerparametre](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Når parameteren for brug af den relative sti er slået til, erstatter et enkelt @-tegn stien til det overordnede element i bindingen for det aktuelle modelelement. Hele bindingsstien bliver kortere, hvilket gør hele tilknytningen mere tydelig og nemmere at forstå. I de fleste tilfælde er det ikke nødvendigt at rulle yderligere i ER-designeren for at få vist alle bindingerne i datamodellen.

[![Modeltilknytningsdesigner](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Når du går i gang med at designe et nyt ER-udtryk, skal du kun angive ét tegn for at definere en binding til et felt af i overordnede element.

[![Formeldesigner](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Når du vælger at ændre datakilden for det overordnede modelelement med den absolutte sti, skal du manuelt binde dette modelelement samt alle indlejrede elementer til en ny datakilde. Når en relativ sti er aktiveret, og du vælger en ny datakilde, der skal bindes til et overordnet element, får du mulighed for automatisk at binde alle indlejrede elementer i dette overordnede element sammen med et enkelt klik.

[![Erstat eksisterende stimeddelelse](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Hvis du bekræfter genbinding af af indlejrede elementer, placeres det nye overordnede element på stien for alle de indlejrede elementer, der indeholder det eksisterende overordnede element.
Denne funktion bryder ikke bagud-kompatibiliteten for ER-strukturen. Alle tidligere designede ER-konfigurationer vil fungere med denne nye funktion, og der kræves ingen opgraderinger eller konverteringer.

> [!NOTE]
> Alle de ændringer, der introduceres ved masseændring af bindinger af indlejrede elementer i modeltilknytninger, gemmes korrekt i et konfigurationsdelta (sporing af ændringer). Det giver kunderne mulighed for at basere den afledte version af modeltilknytninger på en hvilken som helst ny basisversion af den, der er ændret, ved hjælp af denne nye funktion.
