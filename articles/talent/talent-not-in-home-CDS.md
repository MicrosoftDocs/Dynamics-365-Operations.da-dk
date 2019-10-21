---
title: Talent vises ikke sammen med Microsoft Dynamics 365-apps (Common Data Service 1.0)
description: I dette emne beskrives, hvad du skal gøre, hvis kunden ikke kan se Microsoft Dynamics 365 Talent-appen mellem Microsoft Dynamics 365-apps.
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
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009370"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent vises ikke sammen med Microsoft Dynamics 365-apps (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Udsted**

Kunden ikke kan finde Microsoft Dynamics 365 Talent-appen mellem Microsoft Dynamics 365-appsene.

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
