---
title: Arbejde kan ikke annulleres, fordi det er blokeret
description: Arbejde kan ikke annulleres, fordi det er blokeret
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924273"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="47c5b-103">Arbejde kan ikke annulleres, fordi det er blokeret</span><span class="sxs-lookup"><span data-stu-id="47c5b-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="47c5b-104">Fejlkode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="47c5b-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="47c5b-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="47c5b-105">Symptoms</span></span>

<span data-ttu-id="47c5b-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="47c5b-106">The system shows the following error message:</span></span>

> <span data-ttu-id="47c5b-107">Arbejde %1 kan ikke annulleres, fordi det er blokeret af årsagstype %2.</span><span class="sxs-lookup"><span data-stu-id="47c5b-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="47c5b-108">Arbejdets blokering skal fjernes, før det kan annulleres.</span><span class="sxs-lookup"><span data-stu-id="47c5b-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="47c5b-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="47c5b-109">Cause</span></span>

<span data-ttu-id="47c5b-110">Arbejdet er blokeret og kan ikke annulleres.</span><span class="sxs-lookup"><span data-stu-id="47c5b-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="47c5b-111">På siden **Arbejde** under fanen **Generelt** er indstillingen **Blokeret** angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="47c5b-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="47c5b-112">Denne indstilling angiver, at arbejdet er blokeret.</span><span class="sxs-lookup"><span data-stu-id="47c5b-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="47c5b-113">Fanen **Blokeringsårsager** viser, hvorfor arbejdet er blokeret.</span><span class="sxs-lookup"><span data-stu-id="47c5b-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="47c5b-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="47c5b-114">Resolution</span></span>

<span data-ttu-id="47c5b-115">Hvis du vil fjerne blokeringen af arbejdet, skal du vælge fanen **Blokeringsårsager** og derefter følge et af disse trin:</span><span class="sxs-lookup"><span data-stu-id="47c5b-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="47c5b-116">Hvis feltet **Årsag til blokering af arbejde** er angivet til *Ikke-defineret årsag*: Vælg **Fjern blokering af arbejde** i gruppen **Arbejde** under fanen **Arbejde** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="47c5b-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="47c5b-117">Hvis feltet **Årsag til blokering af arbejde** er angivet til *Behandler bølge*: Vælg **Bølge** i gruppen **Relaterede oplysninger** under fanen **Relaterede oplysninger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="47c5b-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="47c5b-118">Vælg **Ryd op i bølgedata** i gruppen **Bølge** under fanen **Bølge** på siden **Bølger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="47c5b-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="47c5b-119">Løsning</span><span class="sxs-lookup"><span data-stu-id="47c5b-119">Workaround</span></span>

<span data-ttu-id="47c5b-120">Hvis de foregående trin ikke løser problemet, kan du annullere arbejdet med følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="47c5b-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="47c5b-121">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="47c5b-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="47c5b-122">I feltet **Arbejds-id** skal du angive id'et for det arbejde, du vil annullere, og som i øjeblikket har en værdien for **Arbejdsstatus** *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="47c5b-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="47c5b-123">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="47c5b-123">Select **OK**.</span></span>
1. <span data-ttu-id="47c5b-124">Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="47c5b-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="47c5b-125">Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="47c5b-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
