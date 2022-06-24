---
title: Omkostning til vedligeholdelsestidsplan
description: Denne artikel beskriver omkostning til vedligeholdelsestidsplaner i Styring af aktiver.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 91481f9bcb778796255fad006c6187916d8e6bb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908737"
---
# <a name="maintenance-schedule-cost"></a>Omkostning til vedligeholdelsestidsplan

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du beregne budgetomkostninger på vedligeholdelsestidsplanslinjer. Dette er nyttigt, hvis du vil have en oversigt over forventede omkostninger, f.eks. omkostninger i forbindelse med planlagte forebyggende vedligeholdelsesjob for det næste år. Beregningerne er baseret på eksisterende vedligeholdelsestidsplanslinjer af typen "Vedligeholdelsesplaner", "Vedligeholdelsesrunder" og "Vedligeholdelsesanmodninger".

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Omkostning til vedligeholdelsestidsplan**.

2. I dialogboksen **Omkostning til vedligeholdelsestidsplan** kan du vælge en **Økonomisk dimensionsopsætning**, hvis du vil have vist omkostninger, der er grupperet i økonomiske dimensioner.

>[!NOTE]
>Økonomiske dimensionsopsætninger oprettes i **Finans** > **Kontoplan** > **Dimensioner** > **Økonomiske dimensionsopsætninger**.

3. Du kan bruge feltet **Niveau** til at angive, hvor detaljerede vedligeholdelsestidsplanslinjerne skal være i forbindelse med arbejdssteder. Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau. Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanslinjer på alle de arbejdsstedsniveauer, de er relateret til.

4. Hvis du vil foretage en beregning for bestemte aktiver, skal du klikke på **Filter** i oversigtspanelet **Poster, der skal indgå** og vælge de relevante aktiver. Hvis det er nødvendigt, kan du også angive en **Forventet startdato** for omkostningsberegningen eller vælge en anden **Status** for omkostningsberegningen

5. Klik på **OK** for at starte omkostningsberegningen.

6. Under fanen **Omkostning til vedligeholdelsestidsplan** i **Gruppér efter...**-handlingsrudegrupper skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i omkostningsberegningen. De valgte gruppeknapper i handlingsruden er fremhævet. Klik på en knap for at aktivere eller deaktivere den.

7. Klik på knappen **Beregn omkostninger**, hvis du vil foretage en ny omkostningsberegning.

I illustrationen herunder vises resultaterne af en omkostningsberegning for en vedligeholdelsestidsplan.

![Figur 1.](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]