---
title: Integrere PowerApps-apps i Dynamics 365 - Core HR
description: I dette emne beskrives, hvordan du kan løse problemet, når PowerApps-menupunktet er forsvundet fra modulet Systemadministration.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008424"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>Integrer PowerApps-apps i Core HR

[!include [banner](includes/banner.md)]

**Udsted**

Menupunktet **PowerApps** er forsvundet fra modulet **Systemadministration**.

**Årsag**

Brugergrænsefladens design er blevet ændret, og Microsoft PowerApps er nu inkluderet i standardtilpasningsmodellen.

**Løsning**

Den måde, PowerApps-apps er integreret på, er blevet ændret. PowerApps-apps tilføjes nu via tilpasningsmodellen. Du kan tilføje PowerApps-apps på næsten alle sider i Microsoft Dynamics 365 Talent.

Du kan finde oplysninger om, hvordan du integrerer PowerApps-apps i Talent, under [Integrer PowerApps-apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Enhver PowerApps-kunde, der har integreret apps inden ændringen, bør være blevet opgraderet til den nye model.

Knappen **PowerApps** findes i øverste højre hjørne af næsten alle sider i Talent. Du kan bruge denne knap til at indsætte en PowerApps-app.

Her er et eksempel.

1. Gå til **Personalestyring \> Links \> Arbejdere \> Medarbejdere**.
2. Vælg knappen **PowerApps**, og vælg derefter **Indsæt en PowerApp**.

    ![PowerApps-knap](media/png.png)

3. Udfyld felterne i dialogboksen **Indsæt en PowerApp**.

    ![Dialogboksen Indsæt en PowerApp.](media/insert-powerapp.png)

Du kan også følge disse trin.

1. I handlingsruden på siden skal du under fanen **Indstillinger** i gruppen **Personaliser** vælge **Personaliser denne formular**.

    ![Gruppen Personaliser under fanen Indstillinger](media/options.png)

    Tilpasningsværktøjslinjen vises.

2. Vælg **Indsæt \> PowerApp** på værktøjslinjen.

    ![Tilføje en PowerApps-app ved hjælp af tilpasningsværktøjslinjen](media/powerapp-bar.png)
