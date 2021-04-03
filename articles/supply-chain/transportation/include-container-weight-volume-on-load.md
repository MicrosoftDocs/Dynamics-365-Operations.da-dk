---
title: Omfatte containers vægt og volumen ved indlæsning
description: Dette emne beskriver, hvordan du kan konfigurere og anvende en funktion til at medtage containervægt og -rumfang på laster.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a58510f46b1390296f46039e2ba741b1248b4a64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265977"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="14c66-103">Omfatte containers vægt og volumen ved indlæsning</span><span class="sxs-lookup"><span data-stu-id="14c66-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14c66-104">Funktionen til at medtage containervægten og -rumfanget på en last giver en klar oversigt over den samlede vægt og volumen af containere og varer, der indgår i en last.</span><span class="sxs-lookup"><span data-stu-id="14c66-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="14c66-105">En last indeholder en enkelt forsendelse eller flere forsendelser, og disse forsendelser indeholder forskellige varer, der tilhører en enkelt salgsordre eller flere salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="14c66-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="14c66-106">Varerne er lagret i en container, og containere læsses på en last.</span><span class="sxs-lookup"><span data-stu-id="14c66-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="14c66-107">Varer, der er uden for en container, kan også være en del af en belastning.</span><span class="sxs-lookup"><span data-stu-id="14c66-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="14c66-108">Baseret på disse betingelser, beregner systemet værdier for vægt og volumen af lasten ved at tage højde for vægt og volumen af både containere og varer.</span><span class="sxs-lookup"><span data-stu-id="14c66-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="14c66-109">Hvis de beregnede værdier ikke er præcise, kan du justere dem ved at angive de faktiske værdier for vægt og rumfang på lasten.</span><span class="sxs-lookup"><span data-stu-id="14c66-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="14c66-110">Værdierne for vægt og rumfang bruges i processer for styring af transporten.</span><span class="sxs-lookup"><span data-stu-id="14c66-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="14c66-111">For eksempel bruges værdierne i rutesatspanelet, hvor de hjælper med at definere satsen og ruten for laster, og de bruges også til transporttilbud og chaufførens check-in.</span><span class="sxs-lookup"><span data-stu-id="14c66-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="14c66-112">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="14c66-112">Where it applies</span></span>

<span data-ttu-id="14c66-113">Funktionen til at medtage containervægt og -rumfang på en last anvendes i transportstyringsprocesser, f.eks. rutesatspanelet, transporttilbud og chaufførens check-in.</span><span class="sxs-lookup"><span data-stu-id="14c66-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="14c66-114">Sådan konfigureres den</span><span class="sxs-lookup"><span data-stu-id="14c66-114">How it is set up</span></span>

<span data-ttu-id="14c66-115">Antallet af containere, som skal bruges til en last beregnes på basis af vægten og volumen af containeren og af den procentdel af containeren, der bruges.</span><span class="sxs-lookup"><span data-stu-id="14c66-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="14c66-116">For at angive vægt og rumfang for en container skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containertyper**.</span><span class="sxs-lookup"><span data-stu-id="14c66-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="14c66-117">For at angive containerudnyttelsen i procent skal du klikke på **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containergrupper** og derefter angive en værdi i feltet **Containerudnyttelse i procent**.</span><span class="sxs-lookup"><span data-stu-id="14c66-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]