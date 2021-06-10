---
title: Human Resources vises ikke i Microsoft Dynamics 365-apps
description: I denne artikel emne beskrives det, hvad du skal gøre, hvis kunden ikke kan se Microsoft Dynamics 365 Human Resources-appen mellem Microsoft Dynamics 365-apps.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17a454cd32a08db105a13577c32368ad819bed1c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053365"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources vises ikke i Microsoft Dynamics 365-apps

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Udsted**

Kunden ser ikke Dynamics 365 Human Resources blandt Microsoft Dynamics 365-apps.

**Løsning**

Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft Power Apps.

1. Den administratorbruger, der har licens til Power Apps Plan 2, skal åbne [Power Apps Administration-portalen](https://preview.admin.powerapps.com/).

2. Vælg **Miljøer**, og vælg det korrekte miljø til Human Resources.

3. Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.

    ![Fanen Miljøroller](media/environment-roles.png)

4. Under fanen **Brugere** skal du tilføje brugeren eller din organisation.

    ![Fanen Brugere](media/environment-maker.png)

5. Vælg **Gem**.

6. Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Vælg **Synkroniser** for at opdatere brugerappsene.

    ![Knappen Synkroniser](media/get-more.png)

    Når synkroniseringen er fuldført, vises Human Resources på startsiden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]