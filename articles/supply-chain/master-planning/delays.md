---
title: Forsinkelser
description: Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dcb11b3665c5d2f296f1ba2ce4708c4eff241b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977982"
---
# <a name="delays"></a>Forsinkelser

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.

Varedisponering kan beregne den tidligste dato for udførelse af en transaktion, der er baseret på leveringstider, tilgængelighed af materiale, disponibel kapacitet og forskellige planlægningsparametre. 

Hvis Varedisponering beregner en ordredato, der ligger før dags dato, kan ordren ikke opfyldes til tiden. Derfor er ordren forsinket. I så fald planlægger Varedisponering ordren fremad fra dags dato og medtager leveringstider. Disse leveringstider starter med alle komponentvarer på lavere niveau. Ordren tildeles derefter en forsinket dato. En forsinket dato er en realistisk forfaldsdato, der er baseret på de aktuelle data. Varedisponering beregner også forsinkelsen i antal dage. 

I nogle situationer kan du vælge ikke at beregne forsinkelser, som når brugerne ved, at de kan fremskynde leveringstider ved at vælge alternative leveringsmåder. 

Du kan konfigurere, hvordan forsinkelser beregnes for en disponeringsgruppe. Du kan så senere knytte disponeringsgruppen til en vare. 

På siden **Varedisponeringsparametre** kan du angive starttidspunktet for beregningen af forsinkelser. Hvis en ordre opfyldes efter dette tidspunkt, lægges der en forsinkelse på én dag til ordrens forsinkede dato. 

> [!NOTE]
> I tidligere versioner blev beregnede forsinkelser kaldt *terminssætninger*, den forsinkede dato blev kaldt *terminsdato*, og en forsinket transaktion blev kaldt *en fremtidig angivet transaktion*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Begrænsede forsinkelser i produktionsopsætningen med flere styklisteniveauer
Når du arbejder med forsinkelser i en produktionsopsætning, der har flere styklisteniveauer, er det vigtigt at bemærke, at det kun er varer direkte over varen (i styklistestrukturen), som forårsager forsinkelsen, der opdateres med en forsinkelse som del af varedisponeringskørslen. Andre varer i styklistestrukturen vil ikke få den anvendte forsinkelse, før den første varedisponering køres, når den planlagte ordre på øverste niveau er godkendt eller autoriseret. 

Produktionsordrerne øverst i styklistestrukturen med forsinkelser kan godkendes (eller autoriseres), før næste varedisponering køres, for at løse denne kendte begrænsning. På denne måde bevares forsinkelsen fra den godkendte planlagte produktionsordre, og alle underliggende komponenter opdateres tilsvarende.
Handlingsmeddelelser kan også bruges til at identificere planlagte ordrer, der kan flyttes til en senere dato på grund af andre forsinkelser i styklistestrukturen.

## <a name="desired-date"></a>Ønsket dato

På siden **Planlagt ordre** under fanen **Forsinkelser** forefindes den **Ønskede dato** for den planlagte ordre. Den ønskede dato for en planlagt ordre er basisdatoen for forsinkelser, hvilket er en beregnet dato, der svarer til **Anmodet dato**, som beregnes på grundlag af **Nettobehov**. Såfremt den planlagte ordre er en styklistelinje, en produktionslinje eller en kanbanlinje, baseres den ønskede dato på **Behovsdatoen**, og den ønskede dato vil ikke fremgå af siden med **Planlagt ordre**.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Disponeringsindstillinger](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]