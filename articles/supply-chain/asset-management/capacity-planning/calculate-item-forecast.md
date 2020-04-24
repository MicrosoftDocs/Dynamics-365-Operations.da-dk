---
title: Beregn varebudget
description: Dette emne beskriver, hvordan du beregner varebudget i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
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
ms.openlocfilehash: 20f969b68e4e9a9936f377000191ba9db202447f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216453"
---
# <a name="calculate-item-forecast"></a>Beregn varebudget

[!include [banner](../../includes/banner.md)]

 

Ligesom du kan foretage kapacitetsbelastningsberegninger, som er beskrevet i forrige afsnit, kan du også foretage beregninger af varebudgettet på:

- vedligeholdelsestidsplanslinjer  
- arbejdsordrer, der endnu ikke er planlagt  
- planlagte arbejdsordrer

Dette er nyttigt, hvis du vil have en oversigt over forventet vareforbrug (reservedele og andre varer, der kræves for at udføre arbejdsordrer) i en bestemt periode. Beregning af varebudget kan foretages på alle aktiver eller udvalgte aktiver. Du kan også foretage en beregning på en aktivitet for vedligeholdelsesnedetid (**Alle aktiviteter for vedligeholdelsesnedetid** eller **Aktive aktiviteter for vedligeholdelsesnedetid**) eller på en arbejdsordrepulje (**Alle arbejdsordrepuljer** eller **Aktive arbejdsordre puljer**).

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Varebudget** eller **Styring af aktiver** > **Generelt** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** / **Aktive arbejdsordrepuljer** > vælg arbejdsordrepulje på listen > knappen **Varebudget** eller **Styring af aktiver** > **Generelt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle aktiviteter med vedligeholdelsesnedetid** / **Aktive aktiviteter med vedligeholdelsesnedetid** > vælg aktivitet for vedligeholdelsesnedetid på listen > knappen **Varebudget**.

2. Vælg en periode til beregningen i felterne **Startdato/-klokkeslæt** og **Slutdato/-klokkeslæt** i dialogboksen **Beregn varebudget**.

3. Vælg "Ja" på knappen **Medtag vedligeholdelsestidsplan**, hvis du vil medtage vedligeholdelsestidsplanlinjer i budgetberegningen.

4. Vælg "Ja" på knappen **Medtag arbejdsordre**, hvis du vil medtage arbejdsordrejob i budgetberegningen.

5. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede varebudgetlinjerne skal være i forbindelse med arbejdssteder. 

      Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer og arbejdsordrer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
  
      Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanlinjer og alle arbejdsordrer på alle de arbejdsstedsniveauer, de er relateret til.

6. Klik på **OK** for at starte beregningen.

7. I **Sammenlæg pr.**-grupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen. I skærmbilledet nedenfor fremhæves de valgte **Sammenlæg pr.**-knapper med blå farve. Klik på en knap for at aktivere eller deaktivere den.

8. Klik på knappen **Vis dimensioner**, hvis du vil se de produkt-, lagrings- eller sporingsdimensioner, der er relateret til varerne. Markér relevante afkrydsningsfelter, og klik på **OK**.

![Figur 1](media/02-capacity-planning.png)
