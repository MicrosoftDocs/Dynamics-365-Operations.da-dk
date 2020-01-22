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
ms.openlocfilehash: a44d2e43752960d3026fa7ac92c7b261aee05448
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897021"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="cf562-103">Talent vises ikke sammen med Microsoft Dynamics 365-apps (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="cf562-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

<span data-ttu-id="cf562-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="cf562-104">**Issue**</span></span>

<span data-ttu-id="cf562-105">Kunden ikke kan finde Microsoft Dynamics 365 Talent-appen mellem Microsoft Dynamics 365-appsene.</span><span class="sxs-lookup"><span data-stu-id="cf562-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="cf562-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="cf562-106">**Resolution**</span></span>

<span data-ttu-id="cf562-107">Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="cf562-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="cf562-108">Den administratorbruger, der har licens til Power Apps Plan 2, skal åbne [Power Apps Administration-portalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="cf562-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="cf562-109">Vælg **Miljøer**, og vælg det korrekte miljø til Talent.</span><span class="sxs-lookup"><span data-stu-id="cf562-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="cf562-110">Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.</span><span class="sxs-lookup"><span data-stu-id="cf562-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="cf562-112">Under fanen **Brugere** skal du tilføje brugeren eller din organisation.</span><span class="sxs-lookup"><span data-stu-id="cf562-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brugere](media/environment-maker.png)

5. <span data-ttu-id="cf562-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cf562-114">Select **Save**.</span></span>
6. <span data-ttu-id="cf562-115">Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="cf562-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="cf562-116">Vælg **Synkroniser** for at opdatere brugerappsene.</span><span class="sxs-lookup"><span data-stu-id="cf562-116">Select **Sync** to update the user apps.</span></span>

    ![Knappen Synkroniser](media/get-more.png)

    <span data-ttu-id="cf562-118">Når synkroniseringen er fuldført, vises Talent på startsiden.</span><span class="sxs-lookup"><span data-stu-id="cf562-118">After synchronization is completed, Talent will appear on the home page.</span></span>
