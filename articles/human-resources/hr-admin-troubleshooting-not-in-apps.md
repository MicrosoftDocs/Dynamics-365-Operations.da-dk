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
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="7ab14-103">Personale vises ikke i Microsoft Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="7ab14-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="7ab14-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="7ab14-104">**Issue**</span></span>

<span data-ttu-id="7ab14-105">Kunden ser ikke Dynamics 365 Human Resources blandt Microsoft Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="7ab14-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="7ab14-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="7ab14-106">**Resolution**</span></span>

<span data-ttu-id="7ab14-107">Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7ab14-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="7ab14-108">Den administratorbruger, der har licens til Power Apps Plan 2, skal åbne [Power Apps Administration-portalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="7ab14-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="7ab14-109">Vælg **Miljøer**, og vælg det korrekte miljø til Personale.</span><span class="sxs-lookup"><span data-stu-id="7ab14-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="7ab14-110">Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.</span><span class="sxs-lookup"><span data-stu-id="7ab14-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="7ab14-112">Under fanen **Brugere** skal du tilføje brugeren eller din organisation.</span><span class="sxs-lookup"><span data-stu-id="7ab14-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brugere](media/environment-maker.png)

5. <span data-ttu-id="7ab14-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7ab14-114">Select **Save**.</span></span>

6. <span data-ttu-id="7ab14-115">Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="7ab14-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="7ab14-116">Vælg **Synkroniser** for at opdatere brugerappsene.</span><span class="sxs-lookup"><span data-stu-id="7ab14-116">Select **Sync** to update the user apps.</span></span>

    ![Knappen Synkroniser](media/get-more.png)

    <span data-ttu-id="7ab14-118">Når synkroniseringen er fuldført, vises Personale på startsiden.</span><span class="sxs-lookup"><span data-stu-id="7ab14-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
