---
title: Bruge stadieårsagskoder
description: Ved at bruge en årsagskode kan du angive, hvorfor en serviceniveauaftale er annulleret, eller hvorfor en serviceniveauaftale har overskredet den tidsgrænse, der er angivet i serviceniveauaftalen.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74594871e9eeed86ae2914d1e5a08c0af28ab643
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424782"
---
# <a name="use-stage-reason-codes"></a>Bruge stadieårsagskoder 

[!include [banner](../includes/banner.md)]


Ved at bruge en årsagskode kan du angive, hvorfor en serviceniveauaftale er annulleret, eller hvorfor en serviceniveauaftale har overskredet den tidsgrænse, der er angivet i serviceniveauaftalen.

Du kan også angive, at en årsagskode er påkrævet, når en serviceniveauaftale annulleres, eller når tidsgrænsen overskrider den tid, der er angivet i serviceniveauaftalen for serviceordren.

Hvis du har angivet, at der kræves en årsagskode, skal du angive en årsagskode i følgende situationer:

  - Når en serviceordre overgår til et stadie, hvor tidsregistreringen i forhold til serviceniveauaftalen stoppes for serviceordren.

  - Når serviceordren lukkes.

  - Når tidsregistreringen stoppes manuelt.

## <a name="set-up-reason-codes"></a>Definer årsagskoder

1.  Klik på **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Stadieårsagskoder**.

2.  Klik på **Ny** i formularen **Stadieårsagskoder** for at oprette en ny årsagskode.

3.  Indtast en entydig stadieårsagskode i feltet **Stadieårsagskode**.

4.  Indtast en beskrivelse af stadieårsagskoden i feltet **Beskrivelse**.

5.  Luk formen for at gemme ændringerne.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Kræve årsagskoder, når en serviceniveauaftale annulleres

1.  Klik på **Servicestyring** \> **Opsætning** \> **Parametre for servicestyring**.

2.  I formularen **Parametre for servicestyring** skal du klikke på linket **Generelt** og derefter markere afkrydsningsfeltet **Årsagskode ved annullering**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Kræve årsagskoder, når en serviceordre overskrider den tidsgrænse, der er fastsat i serviceniveauaftalen

1.  Klik på **Servicestyring** \> **Opsætning** \> **Parametre for servicestyring**.

2.  I formularen **Parametre for servicestyring** skal du klikke på linket **Generelt** og derefter markere afkrydsningsfeltet **Årsagskode ved overskridelse af tid**.

## <a name="see-also"></a>Se også

[Starte og stoppe tidsregistrering på en serviceordre](start-and-stop-time-recording-on-a-service-order.md)

  


