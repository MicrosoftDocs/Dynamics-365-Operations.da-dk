---
title: Detailprisrapporter
description: Dette emne indeholder en oversigt over prisrapportfunktionen, der kan bruges til at få vist kommende prisændringer for udvalgte produkter.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: e14b029a1420eda6af6e83392f295a071a29842a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972424"
---
# <a name="retail-price-reports"></a>Detailprisrapporter

[!include [banner](includes/banner.md)]


Når forhandlere vil give deres kunder konkurrencedygtige priser, ændrer de ofte priserne på produkter. Butikschefer vil gerne have nem adgang til de seneste eller kommende prisændringer, så de kan planlægge, hvilke ressourcer de skal bruge til at opdatere de prisetiketter, der vises på hylderne. Med version 10.0 af Retail kan en butikschef åbne **Pris**-rapporten ved at gå til **Alle butikker \> \> Prisrapport** og se de opdaterede priser for de produkter, der er knyttet til butikken. 

Når du vil aktivere prisrapporten, skal parameteren **Aktivér prisrapport for butik** være aktiveret. Denne parameter findes under fanen **Commerce-parametre \> Rabatter \> Diverse**. Når du åbner siden **Prisrapport** , vises en dialogboks med forskellige konfigurationer. De tilgængelige konfigurationer er angivet nedenfor.

| Variantkonfiguration | Betegnelse |
|---|---|
| Fra dato/Til dato| Det datointerval, som prisrapporten skal genereres for. Varigheden er i øjeblikket begrænset til syv dage. |
| Kanal| Den butik, som prisrapporten skal genereres for. |
| Vis produkter med tilgængeligt lager.| Når du indstiller dette til **Ja**, er det kun priserne for de produkter, som har en tilgængelig fysiske lagerbeholdning i butikken, der vises. |
| Vis priser for varianter | Når du vælger **Ja**, vises priser for varianterne sammen med produktmasterne. Du skal kun slå denne indstilling **Til**, hvis du har variantspecifikke priser, fordi antallet af rækker bliver meget stort. I fremtidige versioner anvender vi priser, der er baseret på dimensioner, så butikschefen kan vælge de dimensioner, som priserne skal vises for. |
| Vis produkter med prisændringer | Hvis du vælger **Ja** i denne indstilling, viser kun priserne for de datoer, hvor prisen er blevet ændret. Prisen for *én dag før* den valgte **Fra dato** vises altid, så butikschefen kan nemt identificere de produkter, der ikke har ændret pris i den samlede valgte varighed, og de kan også få vist den aktuelle pris. |

Når rapporten er oprettes, kan Excel-filen hentes ved eventuelle yderligere behov for filtrering. Prisrapporten kan også bruges til at kontrollere historiske priser på varer for datoer i fortiden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]