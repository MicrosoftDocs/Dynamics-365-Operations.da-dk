---
title: Beregn kapacitetsbelastning
description: Dette emne beskriver, hvordan du beregner kapacitetsbelastning i Styring af aktiver.
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
ms.openlocfilehash: da737cedfcd678a835e85a2b82a05394d771f8cc
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652258"
---
# <a name="calculate-capacity-load"></a>Beregne kapacitetsbelastning

[!include [banner](../../includes/banner.md)]


I Styring af aktiver kan du beregne kapacitetsbelastning på:

- vedligeholdelsestidsplanslinjer  
- arbejdsordrer, der endnu ikke er planlagt  
- planlagte arbejdsordrer

Dette er nyttigt, hvis du vil have en oversigt over forventet kapacitetsbelastning i en bestemt periode. Beregning af kapacitetsbelastning kan foretages på alle aktiver eller udvalgte aktiver. Du kan også foretage en beregning af aktiviteter med vedligeholdelsesnedetid eller arbejdsordrepuljer.

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Kapacitetsbelastning** eller **Styring af aktiver** > **Generelt** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** / **Aktive arbejdsordrepuljer** > vælg arbejdsordrepulje på listen > knappen **Kapacitetsbelastning** eller **Styring af aktiver** > **Generelt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle aktiviteter med vedligeholdelsesnedetid** / **Aktive aktiviteter med vedligeholdelsesnedetid** > vælg vedligeholdelsesaktivitet på listen > knappen **Kapacitetsbelastning**.

2. Vælg en periode til beregningen i felterne **Startdato/-klokkeslæt** og **Slutdato/-klokkeslæt** i dialogboksen **Beregn kapacitetsbelastning**.

3. Vælg "Ja" på knappen **Medtag vedligeholdelsestidsplan**, hvis du vil medtage vedligeholdelsestidsplanlinjer i beregningen.

4. Vælg "Ja" på knappen **Medtag arbejdsordre**, hvis du vil medtage arbejdsordrejob i beregningen.

5. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede kapacitetsbelastningslinjerne skal være i forbindelse med arbejdssteder. 

    Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer og arbejdsordrer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. 
    
    Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanlinjer og alle arbejdsordrer på alle de arbejdsstedsniveauer, de er relateret til.

6. Klik på **OK** for at starte beregningen.

7. I **Sammenlæg pr.**-grupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen. I skærmbilledet nedenfor fremhæves de valgte **Sammenlæg pr.**-knapper med blå farve. Klik på en knap for at aktivere eller deaktivere den.

    ![Figur 1](media/01-capacity-planning.png)

>[!NOTE]
>Hvis du kun vil fokusere på kapacitetsplanlægning i forbindelse med planlagte arbejdsordrer, skal du se [Beregne kapacitetsbelastning på planlagte arbejdsordrer](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).
