---
title: Brug af sporing for udfoldning
description: Denne artikel beskriver, hvordan du kan bruge sporing til at undersøge årsagerne bag resultatet af en ordreudfoldning.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 046d4f5270869542d33023b9b9c927e89f5ad40b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209507"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="f33eb-103">Brug af sporing for udfoldning</span><span class="sxs-lookup"><span data-stu-id="f33eb-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f33eb-104">Denne artikel beskriver, hvordan du kan bruge sporing til at undersøge årsagerne bag resultatet af en ordreudfoldning.</span><span class="sxs-lookup"><span data-stu-id="f33eb-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="f33eb-105">Ved at aktivere sporing kan du få vist oplysninger om de faktorer, der bidrog til resultatet af udfoldningen af en bestemt ordre.</span><span class="sxs-lookup"><span data-stu-id="f33eb-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="f33eb-106">Følgende eksempler viser, hvordan du kan bruge sporingsoplysninger:</span><span class="sxs-lookup"><span data-stu-id="f33eb-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="f33eb-107">Få vist forbindelserne mellem handlinger på ordreforslag for at optimere forsyningskæden og lagerreservationer.</span><span class="sxs-lookup"><span data-stu-id="f33eb-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="f33eb-108">Få vist forbindelserne til ordrer, der allerede er godkendt.</span><span class="sxs-lookup"><span data-stu-id="f33eb-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="f33eb-109">Du kan fokusere på automatisk autorisation af afledte behov og derefter prioritere ordrer mere præcist.</span><span class="sxs-lookup"><span data-stu-id="f33eb-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="f33eb-110">Simulere planlægningsresultater for at afgøre, om der er optimale planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="f33eb-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="f33eb-111">Identificere, hvordan produktionsdatoer, mængder og prioriteter for en ordre blev fastlagt.</span><span class="sxs-lookup"><span data-stu-id="f33eb-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="f33eb-112">Du kan få vist detaljer om terminer og handlinger til en valgt ordre.</span><span class="sxs-lookup"><span data-stu-id="f33eb-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="f33eb-113">På siden **Udfoldning** er sporingsoplysninger tilgængelige under fanen **Udfoldning** i den øverste rude.</span><span class="sxs-lookup"><span data-stu-id="f33eb-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="f33eb-114">Sporing forekommer, når du udfolder en ordre.</span><span class="sxs-lookup"><span data-stu-id="f33eb-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="f33eb-115">Start sporing for ordren ved at klikke på **Opdater**, og markér derefter afkrydsningsfeltet **Aktivér spor**.</span><span class="sxs-lookup"><span data-stu-id="f33eb-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="f33eb-116">Du kan bruge feltet **Søg efter tekst** til at søge i logfilen efter specifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f33eb-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="f33eb-117">Søgeresultater fremhæves i træet.</span><span class="sxs-lookup"><span data-stu-id="f33eb-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f33eb-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f33eb-118">Additional resources</span></span>
--------

[<span data-ttu-id="f33eb-119">Oversigt over behovsplaner</span><span class="sxs-lookup"><span data-stu-id="f33eb-119">Master plans overview</span></span>](master-plans.md)



