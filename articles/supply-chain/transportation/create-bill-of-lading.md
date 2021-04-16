---
title: Opret en fragtseddel
description: I dette emne beskrives det, hvordan du opretter en fragtseddel, når du bruger lagerstyringsprocesser.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a14d971475c71e6a02957acfa0c6e6494c4638fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807626"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="380de-103">Opret en fragtseddel</span><span class="sxs-lookup"><span data-stu-id="380de-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="380de-104">I dette emne beskrives det, hvordan du opretter en fragtseddel, når du bruger lagerstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="380de-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="380de-105">En fragtseddel er et juridisk dokument mellem den virksomhed, der leverer varerne, og transportvirksomheden.</span><span class="sxs-lookup"><span data-stu-id="380de-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="380de-106">Dokumentet ledsager de leverede varer, og den fungerer som en kvittering for levering, når varerne leveres til destinationen.</span><span class="sxs-lookup"><span data-stu-id="380de-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="380de-107">Hvis du bruger lagerstyring, er der to metoder til at generere en fragtseddel:</span><span class="sxs-lookup"><span data-stu-id="380de-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="380de-108">Opret rapporten manuelt ved hjælp af siden **Fragtseddel**.</span><span class="sxs-lookup"><span data-stu-id="380de-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="380de-109">Generér rapporten fra **Panelet lastplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="380de-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="380de-110">Hvis du genererer fragtsedlen fra **Panelet lastplanlægning**, skal laststatus være **Leveret.**</span><span class="sxs-lookup"><span data-stu-id="380de-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="380de-111">Hvis der er mere end én leverance i belastningen, oprettes en fragtseddel for hver leverance.</span><span class="sxs-lookup"><span data-stu-id="380de-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="380de-112">Når en fragtseddel er blevet oprettet, du kan foretage ændringer af den på siden **Fragtseddel**.</span><span class="sxs-lookup"><span data-stu-id="380de-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="380de-113">Hovedfragtseddel</span><span class="sxs-lookup"><span data-stu-id="380de-113">Master bill of lading</span></span>
<span data-ttu-id="380de-114">Hvis der er mere end en levering i lasten, kan du generere en hovedfragtseddel.</span><span class="sxs-lookup"><span data-stu-id="380de-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="380de-115">Den har samme layout og oplysninger som en fragtseddel, men indeholder det opsummerede indhold for alle leverancer.</span><span class="sxs-lookup"><span data-stu-id="380de-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="380de-116">Hvis indstillingen **Opret en hovedfragtseddel, når der er mere end én leverance i en last** er angivet til **Ja** på siden **Transportstyringsparametre**, genereres der automatisk en hovedfragtseddel, hvis du opretter en fragtseddel fra **Panelet lastplanlægning**, og der er mere end én leverance.</span><span class="sxs-lookup"><span data-stu-id="380de-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="380de-117">Du kan også få en oversigt over fragtsedlerne ved at klikke på **Relaterede oplysninger** &gt; **Fragtseddel**.</span><span class="sxs-lookup"><span data-stu-id="380de-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="380de-118">Hvis du vil oprette fragtsedler manuelt, kan du oprette en hovedfragtseddel på siden **Fragtseddel**.</span><span class="sxs-lookup"><span data-stu-id="380de-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]