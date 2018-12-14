---
title: Talent vises ikke sammen med Microsoft Dynamics 365-apps (CDS1.0)
description: "I dette emne beskrives, hvad du skal gøre, hvis kunden ikke kan se Microsoft Dynamics 365 for Talent-appen mellem Microsoft Dynamics 365-apps."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent vises ikke sammen med Microsoft Dynamics 365-apps (CDS1.0)

[!include [banner](includes/banner.md)]

**Afgang**

Kunden kan ikke se Microsoft Dynamics 365 for Talent-appen mellem Microsoft Dynamics 365-apps.

**Løsning**

Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft PowerApps.

1. Den administratorbruger, der har licens til PowerApps Plan 2, skal åbne [PowerApps Administration-portalen](https://preview.admin.powerapps.com/).
2. Vælg **Miljøer**, og vælg det korrekte miljø til Talent.
3. Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.

    ![Fanen Miljøroller](media/environment-roles.png)

4. Under fanen **Brugere** skal du tilføje brugeren eller din organisation.

    ![Fanen Brugere](media/environment-maker.png)

5. Vælg **Gem**.
6. Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Vælg **Synkroniser** for at opdatere brugerappsene.

    ![Knappen Synkroniser](media/get-more.png)

    Når synkroniseringen er fuldført, vises Talent på startsiden.

