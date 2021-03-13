---
title: Human Resources vises ikke i Microsoft Dynamics 365-apps
description: I denne artikel emne beskrives det, hvad du skal gøre, hvis kunden ikke kan se Microsoft Dynamics 365 Human Resources-appen mellem Microsoft Dynamics 365-apps.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: d78199cf0e76ffd0676a26961a8e646938dc7333
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111973"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="99c3d-103">Human Resources vises ikke i Microsoft Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="99c3d-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="99c3d-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="99c3d-104">**Issue**</span></span>

<span data-ttu-id="99c3d-105">Kunden ser ikke Dynamics 365 Human Resources blandt Microsoft Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="99c3d-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="99c3d-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="99c3d-106">**Resolution**</span></span>

<span data-ttu-id="99c3d-107">Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="99c3d-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="99c3d-108">Den administratorbruger, der har licens til Power Apps Plan 2, skal åbne [Power Apps Administration-portalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="99c3d-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="99c3d-109">Vælg **Miljøer**, og vælg det korrekte miljø til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="99c3d-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="99c3d-110">Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.</span><span class="sxs-lookup"><span data-stu-id="99c3d-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="99c3d-112">Under fanen **Brugere** skal du tilføje brugeren eller din organisation.</span><span class="sxs-lookup"><span data-stu-id="99c3d-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brugere](media/environment-maker.png)

5. <span data-ttu-id="99c3d-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="99c3d-114">Select **Save**.</span></span>

6. <span data-ttu-id="99c3d-115">Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="99c3d-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="99c3d-116">Vælg **Synkroniser** for at opdatere brugerappsene.</span><span class="sxs-lookup"><span data-stu-id="99c3d-116">Select **Sync** to update the user apps.</span></span>

    ![Knappen Synkroniser](media/get-more.png)

    <span data-ttu-id="99c3d-118">Når synkroniseringen er fuldført, vises Human Resources på startsiden.</span><span class="sxs-lookup"><span data-stu-id="99c3d-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
