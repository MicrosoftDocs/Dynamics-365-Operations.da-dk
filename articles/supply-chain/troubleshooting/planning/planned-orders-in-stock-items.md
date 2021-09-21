---
title: Der oprettes ordreforslag for lager med produktionsordrer
description: Ordreforslag genereres, selvom der allerede findes varer på lager og produktionsordrer for dem
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475953"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Der oprettes ordreforslag for lager med produktionsordrer

## <a name="symptoms"></a>Symptomer

Ordreforslag genereres, selvom der allerede findes varer på lager og produktionsordrer for dem.

## <a name="resolution"></a>Løsning

Du kan muligvis løse dette problem ved at øge værdien af **Positive dage** for de relevante grupper på siden **Disponeringsgruppe**. Denne ændring bevirker, at systemet afgør, om disponibel lagerbeholdning kan bruges til efterspørgslen. Derefter vil der ikke blive genereret et nyt ordreforslag for de varer, der er på lager.
