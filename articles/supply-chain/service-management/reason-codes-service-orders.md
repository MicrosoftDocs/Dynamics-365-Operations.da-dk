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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b059ad5b2ea9cd577624355cf17925cfb9b4867b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258512"
---
# <a name="reason-codes-for-service-orders"></a><span data-ttu-id="74a27-103">Årsagskoder for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="74a27-103">Reason codes for service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="74a27-104">Du kan bruge årsagskoder til at forklare statussen for en serviceordre, når fasen for en serviceordre opdateres.</span><span class="sxs-lookup"><span data-stu-id="74a27-104">You can use reason codes to help explain the status of a service order when the stage of a service order is updated.</span></span> <span data-ttu-id="74a27-105">Hvis du eksempelvis annullerer en serviceordre, kan du vælge en årsagskode for annulleringen.</span><span class="sxs-lookup"><span data-stu-id="74a27-105">For example, if you cancel a service order, you can select a reason code for the cancellation.</span></span>

<span data-ttu-id="74a27-106">Hvis du vil have vist oplysninger om årsagskoder, der bruges til at spore statussen for serviceordrer, skal du køre rapporten Status for serviceordre.</span><span class="sxs-lookup"><span data-stu-id="74a27-106">To view information about reason codes that are used to track the progress of service orders, run the Service order progress report.</span></span> <span data-ttu-id="74a27-107">I denne rapport kan du se alle serviceordrer, uanset hvor i processen de befinder sig, og de årsagskoder, der er angivet i forbindelse med opdateringen af et serviceordrestadie.</span><span class="sxs-lookup"><span data-stu-id="74a27-107">This report lists all service orders, regardless of their stage, and the reason codes that are specified when a service order stage is updated.</span></span>

## <a name="turn-reason-codes-on-or-off"></a><span data-ttu-id="74a27-108">Aktivere og deaktivere årsagskoder</span><span class="sxs-lookup"><span data-stu-id="74a27-108">Turn reason codes on or off</span></span>

<span data-ttu-id="74a27-109">Det er valgfrit, om du vil bruge årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="74a27-109">Reason codes are optional.</span></span> <span data-ttu-id="74a27-110">Du kan bestemme, om du vil kræve en årsagskode, når du opdaterer en serviceordre til et bestemt servicestadie.</span><span class="sxs-lookup"><span data-stu-id="74a27-110">You can decide whether to require a reason code when you update a service order to a specific service stage.</span></span>

1.  <span data-ttu-id="74a27-111">Klik på **Servicestyring** \> **Opsætning** \> **Serviceordrer** \> **Servicestadier**.</span><span class="sxs-lookup"><span data-stu-id="74a27-111">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="74a27-112">I formularen **Servicestadier** skal du vælge et servicestadie, og marker derefter afkrydsningsfeltet **Årsag** for servicestadiet.</span><span class="sxs-lookup"><span data-stu-id="74a27-112">In the **Service stages** form, select a service stage, and then select the **Reason** check box for the service stage.</span></span>

3.  <span data-ttu-id="74a27-113">Luk formen for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="74a27-113">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="74a27-114">Se også</span><span class="sxs-lookup"><span data-stu-id="74a27-114">See also</span></span>

[<span data-ttu-id="74a27-115">Konfigurer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="74a27-115">Set up service order stages</span></span>](set-up-service-order-stages.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]