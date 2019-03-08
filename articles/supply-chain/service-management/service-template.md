---
title: Serviceskabeloner
description: Du kan definere en serviceaftale som en skabelon og senere kopiere linjerne i skabelonen til en anden serviceaftale eller til en serviceordre.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c4bde1869b2be6e4cbbf979dae1b84c2a4974a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "327314"
---
# <a name="service-templates"></a><span data-ttu-id="68d4d-103">Serviceskabeloner</span><span class="sxs-lookup"><span data-stu-id="68d4d-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68d4d-104">Du kan definere en serviceaftale som en skabelon og senere kopiere linjerne i skabelonen til en anden serviceaftale eller til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="68d4d-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="68d4d-105">Eksempel</span><span class="sxs-lookup"><span data-stu-id="68d4d-105">Example</span></span>

<span data-ttu-id="68d4d-106">En kunde, som du yder service til, har identiske serviceelevatorer på fem forskellige lokationer.</span><span class="sxs-lookup"><span data-stu-id="68d4d-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="68d4d-107">Du vil definere fem serviceaftaler for kunden, én for hvert sted.</span><span class="sxs-lookup"><span data-stu-id="68d4d-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="68d4d-108">For at begrænse gentagelser i opsætningen og for at sikre, at opsætningsoplysninger i serviceaftalerne er identiske, opretter du en serviceaftale og specificerer den som en skabelon til servicearbejdet med elevatorerne.</span><span class="sxs-lookup"><span data-stu-id="68d4d-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="68d4d-109">Du kan nu kopiere skabelonlinjerne til de fem nye serviceaftaler, så hver serviceaftale udfyldes med linjerne fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="68d4d-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="68d4d-110">Opret en skabelon</span><span class="sxs-lookup"><span data-stu-id="68d4d-110">Create a template</span></span>

<span data-ttu-id="68d4d-111">Når du opretter en serviceskabelon, opretter du en serviceaftale, samtidig med at du opretter de nødvendige linjer i den, og derefter knytter du serviceaftalen til serviceskabelongruppen.</span><span class="sxs-lookup"><span data-stu-id="68d4d-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="68d4d-112">En serviceaftale kan kun defineres som en skabelon, hvis den ikke har tilknyttede serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="68d4d-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="68d4d-113">Der kan desuden ikke oprettes serviceordrer ud fra en serviceaftale, der er defineret som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="68d4d-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="68d4d-114">Kopiér skabelonlinjer</span><span class="sxs-lookup"><span data-stu-id="68d4d-114">Copy template lines</span></span>

<span data-ttu-id="68d4d-115">Du kan kopiere skabelonlinjer fra en serviceskabelon til en anden serviceaftale eller til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="68d4d-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="68d4d-116">Når du kopierer skabelonlinjer til dine serviceordrer eller -aftaler, vises skabelongrupperne i en trævisning, hvor hver gruppe kan udvides.</span><span class="sxs-lookup"><span data-stu-id="68d4d-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="68d4d-117">I denne visning kan du få vist hver skabelon og skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="68d4d-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="68d4d-118">Det er lettere at fastlægge, hvilke serviceskabelonlinjer du vil kopiere, hvis du har grupperet skabelonerne under navne, der afspejler brugen af skabelonerne.</span><span class="sxs-lookup"><span data-stu-id="68d4d-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68d4d-119">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="68d4d-119">Related topics</span></span>

[<span data-ttu-id="68d4d-120">Kopiere serviceskabelonlinjer</span><span class="sxs-lookup"><span data-stu-id="68d4d-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
