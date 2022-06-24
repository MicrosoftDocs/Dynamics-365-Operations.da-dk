---
title: Human Resources vises ikke i Microsoft Dynamics 365-apps
description: Denne artikel forklarer, hvad du skal gøre, hvis Microsoft Dynamics 365 Human Resources ikke er anført blandt Microsoft Dynamics 365-apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872233"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources-appen vises ikke i Microsoft Dynamics 365-apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Emne**

Kunden ser ikke Dynamics 365 Human Resources blandt Microsoft Dynamics 365-apps.

**Løsning**

Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft Power Apps.

1. Den administratorbruger, der har licens til Power Apps Plan 2, skal åbne [Power Apps Administration-portalen](https://preview.admin.powerapps.com/).

2. Vælg **Miljøer**, og vælg det korrekte miljø til Human Resources.

3. Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.

    ![Fanen Miljøroller.](media/environment-roles.png)

4. Under fanen **Brugere** skal du tilføje brugeren eller din organisation.

    ![Fanen Brugere.](media/environment-maker.png)

5. Vælg **Gem**.

6. Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Vælg **Synkroniser** for at opdatere brugerappsene.

    ![Knappen Synkroniser.](media/get-more.png)

    Når synkroniseringen er fuldført, vises Human Resources på startsiden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
