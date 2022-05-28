---
title: Bruge stadieårsagskoder
description: Ved at bruge en årsagskode kan du angive, hvorfor en serviceniveauaftale er annulleret, eller hvorfor en serviceniveauaftale har overskredet den tidsgrænse, der er angivet i serviceniveauaftalen.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06c2b6a2b338dbfdbecdeb75e12fa1c20af8e56d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669510"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]