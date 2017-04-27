---
title: Forsinkelser
description: "Denne artikel indeholder oplysninger om forsinkede datoer i varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9113c7728c5d23b70e3809bab31136aff63c6acf
ms.lasthandoff: 03/31/2017


---

# <a name="delays"></a>Forsinkelser

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om forsinkede datoer i varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.

Varedisponering kan beregne den tidligste dato for udførelse af en transaktion, der er baseret på leveringstider, tilgængelighed af materiale, disponibel kapacitet og forskellige planlægningsparametre. 

Hvis Varedisponering beregner en ordredato, der ligger før dags dato, kan ordren ikke opfyldes til tiden. Derfor er ordren forsinket. I så fald planlægger Varedisponering ordren fremad fra dags dato og medtager leveringstider. Disse leveringstider starter med alle komponentvarer på lavere niveau. Ordren tildeles derefter en forsinket dato. En forsinket dato er en realistisk forfaldsdato, der er baseret på de aktuelle data. Varedisponering beregner også forsinkelsen i antal dage. 

I nogle situationer kan du vælge ikke at beregne forsinkelser, som når brugerne ved, at de kan fremskynde leveringstider ved at vælge alternative leveringsmåder. 

Du kan konfigurere, hvordan forsinkelser beregnes for en disponeringsgruppe. Du kan så senere knytte disponeringsgruppen til en vare. 

På siden **Varedisponeringsparametre** kan du angive starttidspunktet for beregningen af forsinkelser. Hvis en ordre opfyldes efter dette tidspunkt, lægges der en forsinkelse på én dag til ordrens forsinkede dato. 

**Bemærk!** I tidligere versioner blev beregnede forsinkelser kaldt *terminssætninger*, den forsinkede dato blev kaldt *terminsdato*, og en forsinket transaktion blev kaldt *en transaktion angivet i fremtiden*.

<a name="see-also"></a>Se også
--------

[Disponeringsindstillinger](coverage-settings.md)




