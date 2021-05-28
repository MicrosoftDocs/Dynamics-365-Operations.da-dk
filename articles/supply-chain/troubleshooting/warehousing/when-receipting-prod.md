---
title: Der udskrives kun én label for flere arbejdshoveder på en enkelt kvittering
description: Der udskrives kun én label for flere arbejdshoveder på en enkelt kvittering.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026370"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="53d3b-103">Der udskrives kun én label for flere arbejdshoveder på en enkelt kvittering</span><span class="sxs-lookup"><span data-stu-id="53d3b-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="53d3b-104">KB-nummer: 4614667</span><span class="sxs-lookup"><span data-stu-id="53d3b-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="53d3b-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="53d3b-105">Symptoms</span></span>

<span data-ttu-id="53d3b-106">Der oprettes flere arbejdshoveder for samme mål-id som del af en enkelt lagerstedsapp, der modtager hændelsen.</span><span class="sxs-lookup"><span data-stu-id="53d3b-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="53d3b-107">Der udskrives dog kun én id-label, når produktet modtages.</span><span class="sxs-lookup"><span data-stu-id="53d3b-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="53d3b-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="53d3b-108">Resolution</span></span>

<span data-ttu-id="53d3b-109">Systemet fungerer som designet.</span><span class="sxs-lookup"><span data-stu-id="53d3b-109">The system is behaving as designed.</span></span>

<span data-ttu-id="53d3b-110">I det aktuelle design oprettes der altid en enkelt id-label, uanset hvor mange arbejdshoved- og arbejdslinjekombinationer der findes.</span><span class="sxs-lookup"><span data-stu-id="53d3b-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="53d3b-111">Den genererede label indeholder oplysninger om kun én kombination.</span><span class="sxs-lookup"><span data-stu-id="53d3b-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="53d3b-112">Du kan løse dette problem ved at sikre, at oprettelsen af arbejdshovedet altid kun er knyttet til ét mål-id.</span><span class="sxs-lookup"><span data-stu-id="53d3b-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
