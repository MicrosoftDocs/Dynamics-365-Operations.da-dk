---
title: Arbejde kan ikke annulleres på grund af dets status
description: Arbejde kan ikke annulleres på grund af dets status
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924249"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="0b54a-103">Arbejde kan ikke annulleres på grund af dets status</span><span class="sxs-lookup"><span data-stu-id="0b54a-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="0b54a-104">Fejlkode: WAX2190</span><span class="sxs-lookup"><span data-stu-id="0b54a-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="0b54a-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="0b54a-105">Symptoms</span></span>

<span data-ttu-id="0b54a-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="0b54a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0b54a-107">Du kan ikke annullere arbejdet %1, fordi det har statussen %2.</span><span class="sxs-lookup"><span data-stu-id="0b54a-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="0b54a-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="0b54a-108">Cause</span></span>

<span data-ttu-id="0b54a-109">Arbejdet kan ikke annulleres i dets aktuelle tilstand.</span><span class="sxs-lookup"><span data-stu-id="0b54a-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="0b54a-110">Arbejdshovedet eller arbejdslinjerne har ikke den forventede værdi for **Arbejdsstatus**.</span><span class="sxs-lookup"><span data-stu-id="0b54a-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="0b54a-111">Feltet **Arbejdsstatus** i arbejdshovedet er ikke angivet til *Åben* eller *I gang*.</span><span class="sxs-lookup"><span data-stu-id="0b54a-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="0b54a-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="0b54a-112">Resolution</span></span>

<span data-ttu-id="0b54a-113">Hvis du vil annullere arbejdet, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="0b54a-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="0b54a-114">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="0b54a-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="0b54a-115">Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.</span><span class="sxs-lookup"><span data-stu-id="0b54a-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="0b54a-116">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b54a-116">Select **OK**.</span></span>
1. <span data-ttu-id="0b54a-117">Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="0b54a-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="0b54a-118">Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="0b54a-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
