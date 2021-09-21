---
title: Produktionsplanlægningen tager ikke sikkerhedsmargenerne i betragtning
description: I produktionsplanlægning tages der ikke hensyn til de sikkerhedsmargener, der er angivet på varedisponeringen for sporede forsyninger
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
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475883"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Produktionsplanlægningen tager ikke sikkerhedsmargenerne i betragtning

## <a name="symptoms"></a>Symptomer

Varedisponering tager højde for sikkerhedsmargener. Sikkerhedsmargenerne ignoreres dog, når produktionsordreforslag planlægges.

## <a name="resolution"></a>Løsning

Margener betragtes kun for varedisponering, ikke under manuel planlægning. Margener er designet til at fungere som en buffer i planlægningsfasen, så der gives nogen "margen" for den faktiske proces.

Du kan få det ønskede resultat ved at fjerne margen. Ruten skal derefter opdateres, så den omfatter den ønskede tid (f.eks. køtid). Både varedisponering og manuel planlægning bør derefter give samme resultat.
