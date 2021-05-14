---
title: Du kan ikke annullere arbejde, der er angivet for en bruger
description: Du kan ikke annullere arbejde, der er angivet for en bruger
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924395"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="6e42f-103">Du kan ikke annullere arbejde, der er angivet for en bruger</span><span class="sxs-lookup"><span data-stu-id="6e42f-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="6e42f-104">Fejlkode: WAX708</span><span class="sxs-lookup"><span data-stu-id="6e42f-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="6e42f-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="6e42f-105">Symptoms</span></span>

<span data-ttu-id="6e42f-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="6e42f-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6e42f-107">Du kan ikke annullere arbejde, der er for en bruger.</span><span class="sxs-lookup"><span data-stu-id="6e42f-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="6e42f-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="6e42f-108">Cause</span></span>

<span data-ttu-id="6e42f-109">Arbejdet låses af en bruger og kan ikke annulleres.</span><span class="sxs-lookup"><span data-stu-id="6e42f-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="6e42f-110">Hvis du vil bekræfte dette, skal du åbne arbejds-id'et og derefter åbne fanen **Generelt**. Hvis arbejdet er låst, er feltet **Arbejdsstatus** angivet til *Igangværende*, og feltet **Låst efter** vil være angivet til et bruger-id.</span><span class="sxs-lookup"><span data-stu-id="6e42f-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="6e42f-111">Løsning</span><span class="sxs-lookup"><span data-stu-id="6e42f-111">Resolution</span></span>

<span data-ttu-id="6e42f-112">Hvis du vil annullere arbejdet, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="6e42f-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6e42f-113">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="6e42f-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6e42f-114">Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.</span><span class="sxs-lookup"><span data-stu-id="6e42f-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6e42f-115">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e42f-115">Select **OK**.</span></span>
1. <span data-ttu-id="6e42f-116">Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="6e42f-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6e42f-117">Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6e42f-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
