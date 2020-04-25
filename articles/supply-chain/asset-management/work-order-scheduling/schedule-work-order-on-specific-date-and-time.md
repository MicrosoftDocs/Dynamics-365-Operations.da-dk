---
title: Planlægge arbejdsordre på bestemt dato og klokkeslæt
description: I dette emne beskrives, hvordan du planlægger en arbejdsordrer på en bestemt dato og klokkeslæt i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215257"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Planlægge arbejdsordre på bestemt dato og klokkeslæt

[!include [banner](../../includes/banner.md)]

 

Hvis en arbejdsordre skal planlægges på en bestemt dato *og* et bestemt klokkeslæt, kan du tilsidesætte standardplanlægningsprocessen i Styring af aktiver og oprette en specifik tidsplan for arbejdsordren.

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Klik på arbejdsordre-id'et i kolonnen **Arbejdsordre** på listen over arbejdsordrer.

3. Klik på **Rediger**.

4. I oversigtspanelet **Arbejdsordrehoved** skal du indsætte start- og slutdatoer og -klokkeslæt i felterne **Forventet startdato** og **Forventet slutdato**.

    ![Figur 1](media/05-work-order-scheduling.png)

5. Under fanen **Generelt** skal du klikke på **Planlæg** for at bruge standardplanlægningsprocessen eller klikke på **Udsend**, hvis du vil tildele en bestemt arbejder arbejdsordren.

6. Hvis du vil tilsidesætte eksisterende kapacitetsreservationer for at sikre, at arbejdsordren planlægges i den forventede periode, skal du vælge de indstillinger, der er angivet i figuren nedenfor, i dialogboksen **Planlæg arbejdsordre** > sektionen **Kapacitetsbegrænsning**. Det betyder, at den planlægningsprocessen ignorerer eksisterende kapacitetsreservationer, fordi arbejdsordren skal starte på det forventede starttidspunkt.

    ![Figur 2](media/06-work-order-scheduling.png)

7. Klik på **OK** for at starte planlægningen.

8. Hvis planlægningsprocessen resulterer i dobbeltreservationer, vises der en meddelelse på skærmen, og du kan justere de relaterede arbejdsordrer.

>[!NOTE]
>Hvis du vil planlægge en vedligeholdelsesarbejder til arbejdsordren, skal denne arbejder være tilgængelig på den forventede startdato og -klokkeslæt. Arbejderes tilgængelighed konfigureres i [Arbejderens kalender](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 

