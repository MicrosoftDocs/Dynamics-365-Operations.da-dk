---
title: Beregn varebudget
description: Dette emne beskriver, hvordan du beregner varebudget i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886764"
---
# <a name="calculate-item-forecast"></a>Beregn varebudget

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ligesom du kan foretage kapacitetsbelastningsberegninger, som er beskrevet i forrige afsnit, kan du også foretage beregninger af varebudgettet på

- Vedligeholdelsestidsplanslinjer  
- Arbejdsordrer, der endnu ikke er planlagt  
- Planlagte arbejdsordrer

Dette er nyttigt, hvis du vil have en oversigt over forventet vareforbrug (reservedele og andre varer, der kræves for at udføre arbejdsordrer) i en bestemt periode. Beregning af varebudget kan foretages på alle aktiver eller udvalgte aktiver. Du kan også foretage en beregning på en aktivitet for vedligeholdelsesnedetid (**Alle aktiviteter for vedligeholdelsesnedetid** eller **Aktive aktiviteter for vedligeholdelsesnedetid**) eller på en arbejdsordrepulje (**Alle arbejdsordrepuljer** eller **Aktive arbejdsordre puljer**).

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Varebudget** eller **Styring af aktiver** > **Generelt** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** / **Aktive arbejdsordrepuljer** > vælg arbejdsordrepulje på listen > knappen **Varebudget** eller **Styring af aktiver** > **Generelt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle aktiviteter med vedligeholdelsesnedetid** / **Aktive aktiviteter med vedligeholdelsesnedetid** > vælg aktivitet for vedligeholdelsesnedetid på listen > knappen **Varebudget**.

2. Vælg en periode til beregningen i felterne **Startdato/-klokkeslæt** og **Slutdato/-klokkeslæt** i dialogboksen **Beregn varebudget**.

3. Vælg "Ja" på knappen **Medtag vedligeholdelsestidsplan**, hvis du vil medtage vedligeholdelsestidsplanlinjer i budgetberegningen.

4. Vælg "Ja" på knappen **Medtag arbejdsordre**, hvis du vil medtage arbejdsordrejob i budgetberegningen.

5. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede varebudgetlinjerne skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer og arbejdsordrer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanlinjer og alle arbejdsordrer på alle de arbejdsstedsniveauer, de er relateret til.

6. Klik på **OK** for at starte beregningen.

7. I **Sammenlæg pr.**-handlingsrudegrupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen. De valgte handlingsrudegrupper er fremhævet med blåt. Klik på en knap for at aktivere eller deaktivere den.

8. Klik på knappen **Vis dimensioner**, hvis du vil se de produkt-, lagrings- eller sporingsdimensioner, der er relateret til varerne. Markér relevante afkrydsningsfelter, og klik på **OK**.

I figuren herunder vises et skærmbillede af grænsefladen.

![Figur 1](media/02-capacity-planning.png)
