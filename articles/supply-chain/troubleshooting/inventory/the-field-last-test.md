---
title: Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer
description: Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026382"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="3a095-103">Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="3a095-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="3a095-104">KB-nummer: 4612803</span><span class="sxs-lookup"><span data-stu-id="3a095-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="3a095-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="3a095-105">Symptoms</span></span>

<span data-ttu-id="3a095-106">Feltet **Sidste testdato** opdateres ikke, når der oprettes flere kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3a095-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="3a095-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="3a095-107">Resolution</span></span>

<span data-ttu-id="3a095-108">Systemet fungerer som designet.</span><span class="sxs-lookup"><span data-stu-id="3a095-108">The system is behaving as designed.</span></span> <span data-ttu-id="3a095-109">Den sidste testdato er ikke relateret til kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="3a095-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="3a095-110">Den gemmer den dato, hvor de færdige varer blev købt eller produceret første gang.</span><span class="sxs-lookup"><span data-stu-id="3a095-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="3a095-111">Denne dato bruges til at beregne hyldelevetidsvejledningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="3a095-111">This date is used to calculate the shelf life advice date.</span></span>
