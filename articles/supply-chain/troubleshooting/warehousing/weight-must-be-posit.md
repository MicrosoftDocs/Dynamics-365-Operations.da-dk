---
title: Vægt skal være positiv
description: Vægt skal være positiv
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924297"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="29a0e-103">Vægt skal være positiv</span><span class="sxs-lookup"><span data-stu-id="29a0e-103">Weight must be positive</span></span>

<span data-ttu-id="29a0e-104">Fejlkode: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="29a0e-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="29a0e-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="29a0e-105">Symptoms</span></span>

<span data-ttu-id="29a0e-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="29a0e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="29a0e-107">Vægt skal være positiv.</span><span class="sxs-lookup"><span data-stu-id="29a0e-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="29a0e-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="29a0e-108">Cause</span></span>

<span data-ttu-id="29a0e-109">Feltet **Bruttovægt** er angivet til *0* (nul) eller en negativ værdi.</span><span class="sxs-lookup"><span data-stu-id="29a0e-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="29a0e-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="29a0e-110">Resolution</span></span>

<span data-ttu-id="29a0e-111">Hvis du vil angive en vægt, skal du benytte en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="29a0e-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="29a0e-112">Angiv en værdii feltet **Bruttovægt**.</span><span class="sxs-lookup"><span data-stu-id="29a0e-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="29a0e-113">Vælg derefter en enhed på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="29a0e-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="29a0e-114">Vælg **Hent systemvægt** til beregning af værdien for **Bruttovægt**.</span><span class="sxs-lookup"><span data-stu-id="29a0e-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
