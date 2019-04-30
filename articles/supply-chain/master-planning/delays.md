---
title: Forsinkelser
description: Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/20/2019
ms.locfileid: "878304"
---
# <a name="delays"></a>Forsinkelser

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.

Varedisponering kan beregne den tidligste dato for udførelse af en transaktion, der er baseret på leveringstider, tilgængelighed af materiale, disponibel kapacitet og forskellige planlægningsparametre. 

Hvis Varedisponering beregner en ordredato, der ligger før dags dato, kan ordren ikke opfyldes til tiden. Derfor er ordren forsinket. I så fald planlægger Varedisponering ordren fremad fra dags dato og medtager leveringstider. Disse leveringstider starter med alle komponentvarer på lavere niveau. Ordren tildeles derefter en forsinket dato. En forsinket dato er en realistisk forfaldsdato, der er baseret på de aktuelle data. Varedisponering beregner også forsinkelsen i antal dage. 

I nogle situationer kan du vælge ikke at beregne forsinkelser, som når brugerne ved, at de kan fremskynde leveringstider ved at vælge alternative leveringsmåder. 

Du kan konfigurere, hvordan forsinkelser beregnes for en disponeringsgruppe. Du kan så senere knytte disponeringsgruppen til en vare. 

På siden **Varedisponeringsparametre** kan du angive starttidspunktet for beregningen af forsinkelser. Hvis en ordre opfyldes efter dette tidspunkt, lægges der en forsinkelse på én dag til ordrens forsinkede dato. 

> [!Bemærk} I tidligere versioner blev beregnede forsinkelser kaldt *terminssætninger*, den forsinkede dato blev kaldt *terminsdato*, og en forsinket transaktion blev kaldt *en fremtidig angivet transaktion*.

## <a name="desired-date"></a>Ønsket dato

På siden **Planlagt ordre** under fanen **Forsinkelser** forefindes den **Ønskede dato** for den planlagte ordre. Den ønskede dato for en planlagt ordre er basisdatoen for forsinkelser, hvilket er en beregnet dato, der svarer til **Anmodet dato**, som beregnes på grundlag af **Nettobehov**. Såfremt den planlagte ordre er en styklistelinje, en produktionslinje eller en kanbanlinje, baseres den ønskede dato på **Behovsdatoen**, og den ønskede dato vil ikke fremgå af siden med **Planlagt ordre**.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Disponeringsindstillinger](coverage-settings.md)
