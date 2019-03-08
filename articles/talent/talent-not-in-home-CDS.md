---
title: Talent vises ikke sammen med Microsoft Dynamics 365-apps (CDS1.0)
description: I dette emne beskrives, hvad du skal gøre, hvis kunden ikke kan se Microsoft Dynamics 365 for Talent-appen mellem Microsoft Dynamics 365-apps.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303769"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="6bf72-103">Talent vises ikke sammen med Microsoft Dynamics 365-apps (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="6bf72-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6bf72-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="6bf72-104">**Issue**</span></span>

<span data-ttu-id="6bf72-105">Kunden ikke kan finde Microsoft Dynamics 365 for Talent-appen mellem Microsoft Dynamics 365-appsene.</span><span class="sxs-lookup"><span data-stu-id="6bf72-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="6bf72-106">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="6bf72-106">**Resolution**</span></span>

<span data-ttu-id="6bf72-107">Brugeren skal føjes til rollen Miljøopretter for miljøet i Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="6bf72-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="6bf72-108">Den administratorbruger, der har licens til PowerApps Plan 2, skal åbne [PowerApps Administration-portalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="6bf72-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="6bf72-109">Vælg **Miljøer**, og vælg det korrekte miljø til Talent.</span><span class="sxs-lookup"><span data-stu-id="6bf72-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="6bf72-110">Under fanen **Miljøroller** under fanen **Sikkerhed** skal du vælge **Miljøopretter**.</span><span class="sxs-lookup"><span data-stu-id="6bf72-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="6bf72-112">Under fanen **Brugere** skal du tilføje brugeren eller din organisation.</span><span class="sxs-lookup"><span data-stu-id="6bf72-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brugere](media/environment-maker.png)

5. <span data-ttu-id="6bf72-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6bf72-114">Select **Save**.</span></span>
6. <span data-ttu-id="6bf72-115">Brugeren skal nu logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="6bf72-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="6bf72-116">Vælg **Synkroniser** for at opdatere brugerappsene.</span><span class="sxs-lookup"><span data-stu-id="6bf72-116">Select **Sync** to update the user apps.</span></span>

    ![Knappen Synkroniser](media/get-more.png)

    <span data-ttu-id="6bf72-118">Når synkroniseringen er fuldført, vises Talent på startsiden.</span><span class="sxs-lookup"><span data-stu-id="6bf72-118">After synchronization is completed, Talent will appear on the home page.</span></span>
