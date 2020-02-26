---
title: Integrere Power Apps-apps i Dynamics 365 Human Resources
description: I dette emne beskrives, hvordan du kan løse problemet, når Microsoft Power Apps-menupunktet er forsvundet fra modulet Systemadministration.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017867"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Integrere Power Apps-apps i Dynamics 365 Human Resources

**Udsted**

Menupunktet **Power Apps** er forsvundet fra modulet **Systemadministration**.

**Årsag**

Brugergrænsefladens design er blevet ændret, og Microsoft Power Apps er nu inkluderet i standardtilpasningsmodellen.

**Løsning**

Den måde, Power Apps er integreret på, er blevet ændret. Power Apps tilføjes nu via tilpasningsmodellen. Du kan tilføje Power Apps på næsten alle sider i Microsoft Dynamics 365 Talent.

Du kan finde oplysninger om, hvordan du integrerer Power Apps i Talent, under [Integrer Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Enhver Power Apps-kunde, der har integreret apps inden ændringen, bør være blevet opgraderet til den nye model.

Knappen **Power Apps** findes i øverste højre hjørne af næsten alle sider i Talent. Du kan bruge denne knap til at indsætte apps.

Her er et eksempel.

1. Gå til **Personalestyring \> Links \> Arbejdere \> Medarbejdere**.
2. Vælg knappen **Power Apps**, og vælg derefter **Tilføj en app fra Power Apps**.

    ![Power Apps-knap](media/png.png)

3. Udfyld felterne i dialogboksen **Tilføj en app fra Power Apps**.

    ![Dialogboksen Tilføj en app fra Power Apps](media/insert-powerapp.png)

Du kan også følge disse trin.

1. I handlingsruden på siden skal du under fanen **Indstillinger** i gruppen **Personaliser** vælge **Tilpas denne side**.

    ![Gruppen Personaliser under fanen Indstillinger](media/options.png)

    Tilpasningsværktøjslinjen vises.

2. Vælg **Tilføj en app fra Power Apps** på værktøjslinjen.

    ![Tilføje en app fra Power Apps ved hjælp af tilpasningsværktøjslinjen](media/powerapp-bar.png)
