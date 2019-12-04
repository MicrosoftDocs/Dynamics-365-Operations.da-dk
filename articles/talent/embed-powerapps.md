---
title: Integrere Power Apps-apps i Dynamics 365 - Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830203"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Integrere Power Apps-apps i Dynamics 365 - Core HR

[!include [banner](includes/banner.md)]

**Udsted**

Menupunktet **Power Apps** er forsvundet fra modulet **Systemadministration**.

**Årsag**

Brugergrænsefladens design er blevet ændret, og Microsoft Power Apps er nu inkluderet i standardtilpasningsmodellen.

**Løsning**

Den måde, Power Apps er integreret på, er blevet ændret. Power Apps tilføjes nu via tilpasningsmodellen. Du kan tilføje Power Apps på næsten alle sider i Microsoft Dynamics 365 Talent.

Du kan finde oplysninger om, hvordan du integrerer Power Apps i Talent, under [Integrer Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Enhver Power Apps-kunde, der har integreret apps inden ændringen, bør være blevet opgraderet til den nye model.

Knappen **Power Apps** findes i øverste højre hjørne af næsten alle sider i Talent. Du kan bruge denne knap til at indsætte Power Apps.

Her er et eksempel.

1. Gå til **Personalestyring \> Links \> Arbejdere \> Medarbejdere**.
2. Vælg knappen **Power Apps**, og vælg derefter **Indsæt en PowerApp**.

    ![Power Apps-knap](media/png.png)

3. Udfyld felterne i dialogboksen **Indsæt en PowerApp**.

    ![Dialogboksen Indsæt en PowerApp.](media/insert-powerapp.png)

Du kan også følge disse trin.

1. I handlingsruden på siden skal du under fanen **Indstillinger** i gruppen **Personaliser** vælge **Personaliser denne formular**.

    ![Gruppen Personaliser under fanen Indstillinger](media/options.png)

    Tilpasningsværktøjslinjen vises.

2. Vælg **Indsæt \> PowerApp** på værktøjslinjen.

    ![Tilføje en Power Apps-app ved hjælp af tilpasningsværktøjslinjen](media/powerapp-bar.png)
