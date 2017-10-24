---
title: Forsinkelser
description: "Denne artikel indeholder oplysninger om forsinkede datoer i varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

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




