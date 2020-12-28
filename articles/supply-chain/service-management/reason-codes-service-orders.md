---
title: Årsagskoder for serviceordrer
description: Brug årsagskoder til at forklare statussen for en serviceordre, når fasen for en serviceordre opdateres.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec8a318561663f4a1b2cfd7735b5c1a5d18e8c0f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424378"
---
# <a name="reason-codes-for-service-orders"></a><span data-ttu-id="d4920-103">Årsagskoder for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="d4920-103">Reason codes for service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d4920-104">Du kan bruge årsagskoder til at forklare statussen for en serviceordre, når fasen for en serviceordre opdateres.</span><span class="sxs-lookup"><span data-stu-id="d4920-104">You can use reason codes to help explain the status of a service order when the stage of a service order is updated.</span></span> <span data-ttu-id="d4920-105">Hvis du eksempelvis annullerer en serviceordre, kan du vælge en årsagskode for annulleringen.</span><span class="sxs-lookup"><span data-stu-id="d4920-105">For example, if you cancel a service order, you can select a reason code for the cancellation.</span></span>

<span data-ttu-id="d4920-106">Hvis du vil have vist oplysninger om årsagskoder, der bruges til at spore statussen for serviceordrer, skal du køre rapporten Status for serviceordre.</span><span class="sxs-lookup"><span data-stu-id="d4920-106">To view information about reason codes that are used to track the progress of service orders, run the Service order progress report.</span></span> <span data-ttu-id="d4920-107">I denne rapport kan du se alle serviceordrer, uanset hvor i processen de befinder sig, og de årsagskoder, der er angivet i forbindelse med opdateringen af et serviceordrestadie.</span><span class="sxs-lookup"><span data-stu-id="d4920-107">This report lists all service orders, regardless of their stage, and the reason codes that are specified when a service order stage is updated.</span></span>

## <a name="turn-reason-codes-on-or-off"></a><span data-ttu-id="d4920-108">Aktivere og deaktivere årsagskoder</span><span class="sxs-lookup"><span data-stu-id="d4920-108">Turn reason codes on or off</span></span>

<span data-ttu-id="d4920-109">Det er valgfrit, om du vil bruge årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="d4920-109">Reason codes are optional.</span></span> <span data-ttu-id="d4920-110">Du kan bestemme, om du vil kræve en årsagskode, når du opdaterer en serviceordre til et bestemt servicestadie.</span><span class="sxs-lookup"><span data-stu-id="d4920-110">You can decide whether to require a reason code when you update a service order to a specific service stage.</span></span>

1.  <span data-ttu-id="d4920-111">Klik på **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Servicestadier**.</span><span class="sxs-lookup"><span data-stu-id="d4920-111">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="d4920-112">I formularen **Servicestadier** skal du vælge et servicestadie, og marker derefter afkrydsningsfeltet **Årsag** for servicestadiet.</span><span class="sxs-lookup"><span data-stu-id="d4920-112">In the **Service stages** form, select a service stage, and then select the **Reason** check box for the service stage.</span></span>

3.  <span data-ttu-id="d4920-113">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="d4920-113">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4920-114">Se også</span><span class="sxs-lookup"><span data-stu-id="d4920-114">See also</span></span>

[<span data-ttu-id="d4920-115">Konfigurer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="d4920-115">Set up service order stages</span></span>](set-up-service-order-stages.md)



