---
title: Personale vises ikke i Microsoft Dynamics 365-apps
description: I denne artikel emne beskrives det, hvad du skal gøre, hvis kunden ikke kan se Microsoft Dynamics 365 Human Resources-appen mellem Microsoft Dynamics 365-apps.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008560"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Personale vises ikke i Microsoft Dynamics 365-apps

**Udsted**

Kunden ser ikke Dynamics 365 Human Resources blandt Microsoft Dynamics 365-apps.

**Løsning**

Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft Power Apps.

1. Den administratorbruger, der har licens til Power Apps Plan 2, skal åbne [Power Apps Administration-portalen](https://preview.admin.powerapps.com/).

2. Vælg **Miljøer**, og vælg det korrekte miljø til Personale.

3. Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.

    ![Fanen Miljøroller](media/environment-roles.png)

4. Under fanen **Brugere** skal du tilføje brugeren eller din organisation.

    ![Fanen Brugere](media/environment-maker.png)

5. Vælg **Gem**.

6. Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Vælg **Synkroniser** for at opdatere brugerappsene.

    ![Knappen Synkroniser](media/get-more.png)

    Når synkroniseringen er fuldført, vises Personale på startsiden.
