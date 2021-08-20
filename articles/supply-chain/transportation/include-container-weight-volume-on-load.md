---
title: Omfatte containers vægt og volumen ved indlæsning
description: Dette emne beskriver, hvordan du kan konfigurere og anvende en funktion til at medtage containervægt og -rumfang på laster.
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b42bd0b97564a493a50331d1424ca8084b389b29518f012f443d9cf722efe7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763909"
---
# <a name="include-container-weight-and-volume-on-load"></a>Omfatte containers vægt og volumen ved indlæsning

[!include [banner](../includes/banner.md)]

Funktionen til at medtage containervægten og -rumfanget på en last giver en klar oversigt over den samlede vægt og volumen af containere og varer, der indgår i en last.

En last indeholder en enkelt forsendelse eller flere forsendelser, og disse forsendelser indeholder forskellige varer, der tilhører en enkelt salgsordre eller flere salgsordrer. Varerne er lagret i en container, og containere læsses på en last. Varer, der er uden for en container, kan også være en del af en belastning. Baseret på disse betingelser, beregner systemet værdier for vægt og volumen af lasten ved at tage højde for vægt og volumen af både containere og varer.

Hvis de beregnede værdier ikke er præcise, kan du justere dem ved at angive de faktiske værdier for vægt og rumfang på lasten. Værdierne for vægt og rumfang bruges i processer for styring af transporten. For eksempel bruges værdierne i rutesatspanelet, hvor de hjælper med at definere satsen og ruten for laster, og de bruges også til transporttilbud og chaufførens check-in.

## <a name="where-it-applies"></a>Hvor det er relevant

Funktionen til at medtage containervægt og -rumfang på en last anvendes i transportstyringsprocesser, f.eks. rutesatspanelet, transporttilbud og chaufførens check-in.

## <a name="how-it-is-set-up"></a>Sådan konfigureres den

Antallet af containere, som skal bruges til en last beregnes på basis af vægten og volumen af containeren og af den procentdel af containeren, der bruges.

-   For at angive vægt og rumfang for en container skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containertyper**.

-   For at angive containerudnyttelsen i procent skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containergrupper** og derefter angive en værdi i feltet **Containerudnyttelse i procent**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]