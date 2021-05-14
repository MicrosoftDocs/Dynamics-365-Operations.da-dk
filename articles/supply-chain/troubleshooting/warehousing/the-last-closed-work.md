---
title: Den seneste lukkede arbejdslinje skal være Læg på lager
description: Den seneste lukkede arbejdslinje skal være Læg på lager
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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924369"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="c4fe9-103">Den seneste lukkede arbejdslinje skal være Læg på lager</span><span class="sxs-lookup"><span data-stu-id="c4fe9-103">The last closed work line must be a put</span></span>

<span data-ttu-id="c4fe9-104">Fejlkode: WAX1285</span><span class="sxs-lookup"><span data-stu-id="c4fe9-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="c4fe9-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="c4fe9-105">Symptoms</span></span>

<span data-ttu-id="c4fe9-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="c4fe9-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c4fe9-107">Den seneste lukkede arbejdslinje skal være Læg på lager.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="c4fe9-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="c4fe9-108">Cause</span></span>

<span data-ttu-id="c4fe9-109">Arbejdet kan ikke annulleres i dets aktuelle tilstand.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="c4fe9-110">På den sidste arbejdslinje er feltet **Arbejdsstatus** angivet til *Lukket*, men feltet **Arbejdstype** er ikke angivet til *Læg på lager*.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c4fe9-111">Løsning</span><span class="sxs-lookup"><span data-stu-id="c4fe9-111">Resolution</span></span>

<span data-ttu-id="c4fe9-112">Hvis du vil annullere arbejdet, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="c4fe9-113">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="c4fe9-114">Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="c4fe9-115">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-115">Select **OK**.</span></span>
1. <span data-ttu-id="c4fe9-116">Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="c4fe9-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="c4fe9-117">Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="c4fe9-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
