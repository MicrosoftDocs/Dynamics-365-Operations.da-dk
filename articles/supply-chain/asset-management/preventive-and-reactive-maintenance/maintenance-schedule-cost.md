---
title: Omkostning til vedligeholdelsestidsplan
description: I dette emne beskrives omkostning til vedligeholdelsestidsplaner i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: 91c5b2e70ee083bf2741e245f1ca840ab939ad3f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424661"
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

![Figur 1](media/17-preventive-maintenance.png)

