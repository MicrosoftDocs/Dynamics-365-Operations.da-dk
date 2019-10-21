---
title: Aktiver forsinket momsberegning på kladde
description: I dette emne forklares det, hvordan du kan bruge funktionen **Aktiver forsinket momsberegning på kladde** til at forbedre ydeevnen for momsberegningen, når antallet af kladdelinjer er stort.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176936"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Aktiver forsinket momsberegning på kladde
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne forklares det, hvordan du kan bruge funktionen **Aktiver forsinket momsberegning på kladde** til at forbedre ydeevnen for momsberegningen, når antallet af kladdelinjer er stort.

Den aktuelle beregningsmåde for moms i kladden udløses i realtid, når brugeren opdaterer momsrelaterede felter, f.eks. momsgruppe/varemomsgruppe. Hvis der opdateres på kladdelinjeniveau, beregnes momsbeløbet igen på alle kladdelinjer. Det hjælper brugeren med at få vist beregnet momsbeløb i realtid, men det kan også give problemer med ydeevnen, hvis antallet af kladdelinjer er stort.

Denne funktion giver mulighed for at udsætte momsberegningen for at løse problemer med ydeevnen. Hvis denne funktion er slået til, vil momsbeløbet kun blive beregnet, når brugeren klikker på "Moms" eller bogfører kladden.

Brugeren kan slå parameteren til og fra på tre niveauer:
- af juridisk enhed
- efter kladdenavn
- efter kladdehoved

Systemet vil tage parameterværdien i kladdehovedet som endelig. Parameterværdien til kladdeoverskriften bruges som standard fra kladdenavn. Parameterværdien på kladdenavnet angives som standard fra finanskladdeparameteren, når kladdenavnet oprettes.

Felterne "Faktisk momsbeløb" og "Beregnet momsbeløb" i kladden vil blive skjult, hvis denne parameter er slået til. Formålet er ikke at forvirre brugeren, fordi værdien af disse to felter altid vil vise 0, før brugeren udløser momsberegningen.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Aktivér udsat beregning af moms efter juridisk enhed

1. Gå til **Finans > Opsætning Finans > Finansparametre**.
2. Klik på fanen **Moms**
3. Under fanen **Generelt** kan du finde parameteren **Forsinket momsberegning**, slå den til/fra

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Aktiver forsinket momsberegning efter kladdenavn

1. Gå til **Finans > Kladdeopsætning > Kladdenavne**.
2. Under fanen **Generelt** kan du finde parameteren **Forsinket momsberegning**, slå den til/fra

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Aktiver forsinket momsberegning efter kladde

1. Gå til **Finans > Kladdeposteringer > Finanskladder**.
2. Klik på **Ny**
3. Vælg et kladdenavn
4. Klik på **Opsætning**.
5. Find parameteren **Forsinket momsberegning**, slå den til/fra

![](media/delayed-tax-calculation-journal-header.png)
