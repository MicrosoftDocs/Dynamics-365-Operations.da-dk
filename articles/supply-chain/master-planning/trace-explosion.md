---
title: Brug af sporing for udfoldning
description: Denne artikel beskriver, hvordan du kan bruge sporing til at undersøge årsagerne bag resultatet af en ordreudfoldning.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f2821eb6a17d2caaacf399f8d519e4caf3ecd04
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813655"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="12bac-103">Brug af sporing for udfoldning</span><span class="sxs-lookup"><span data-stu-id="12bac-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12bac-104">Denne artikel beskriver, hvordan du kan bruge sporing til at undersøge årsagerne bag resultatet af en ordreudfoldning.</span><span class="sxs-lookup"><span data-stu-id="12bac-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="12bac-105">Ved at aktivere sporing kan du få vist oplysninger om de faktorer, der bidrog til resultatet af udfoldningen af en bestemt ordre.</span><span class="sxs-lookup"><span data-stu-id="12bac-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="12bac-106">Følgende eksempler viser, hvordan du kan bruge sporingsoplysninger:</span><span class="sxs-lookup"><span data-stu-id="12bac-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="12bac-107">Få vist forbindelserne mellem handlinger på ordreforslag for at optimere forsyningskæden og lagerreservationer.</span><span class="sxs-lookup"><span data-stu-id="12bac-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="12bac-108">Få vist forbindelserne til ordrer, der allerede er godkendt.</span><span class="sxs-lookup"><span data-stu-id="12bac-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="12bac-109">Du kan fokusere på automatisk autorisation af afledte behov og derefter prioritere ordrer mere præcist.</span><span class="sxs-lookup"><span data-stu-id="12bac-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="12bac-110">Simulere planlægningsresultater for at afgøre, om der er optimale planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="12bac-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="12bac-111">Identificere, hvordan produktionsdatoer, mængder og prioriteter for en ordre blev fastlagt.</span><span class="sxs-lookup"><span data-stu-id="12bac-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="12bac-112">Du kan få vist detaljer om terminer og handlinger til en valgt ordre.</span><span class="sxs-lookup"><span data-stu-id="12bac-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="12bac-113">På siden **Udfoldning** er sporingsoplysninger tilgængelige under fanen **Udfoldning** i den øverste rude.</span><span class="sxs-lookup"><span data-stu-id="12bac-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="12bac-114">Sporing forekommer, når du udfolder en ordre.</span><span class="sxs-lookup"><span data-stu-id="12bac-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="12bac-115">Start sporing for ordren ved at klikke på **Opdater**, og markér derefter afkrydsningsfeltet **Aktivér spor**.</span><span class="sxs-lookup"><span data-stu-id="12bac-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="12bac-116">Du kan bruge feltet **Søg efter tekst** til at søge i logfilen efter specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="12bac-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="12bac-117">Søgeresultater fremhæves i træet.</span><span class="sxs-lookup"><span data-stu-id="12bac-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="12bac-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="12bac-118">Additional resources</span></span>
--------

[<span data-ttu-id="12bac-119">Oversigt over behovsplaner</span><span class="sxs-lookup"><span data-stu-id="12bac-119">Master plans overview</span></span>](master-plans.md)



