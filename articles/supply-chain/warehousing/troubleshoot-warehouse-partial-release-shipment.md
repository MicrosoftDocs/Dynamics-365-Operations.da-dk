---
title: Foretage fejlfinding af delvise frigivelser og delvise forsendelser
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med delvise frigivelser og delvise forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645942"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="89694-103">Foretage fejlfinding af delvise frigivelser og delvise forsendelser</span><span class="sxs-lookup"><span data-stu-id="89694-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89694-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med delvise frigivelser og delvise forsendelser i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="89694-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="89694-105">En salgsordres frigivelsesstatus forbliver Delvist frigivet, selv efter at salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="89694-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="89694-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="89694-106">Issue description</span></span>

<span data-ttu-id="89694-107">En salgsordre er en leveringsordre, men en eller flere varer på den har en anden leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="89694-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="89694-108">Når ordren er faktureret, har den stadig frigivelsesstatussen *Delvist frigivet*.</span><span class="sxs-lookup"><span data-stu-id="89694-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="89694-109">En salgsordre har f.eks. to varer: én til levering og én til afhentning.</span><span class="sxs-lookup"><span data-stu-id="89694-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="89694-110">Både levering og afhentning er udført.</span><span class="sxs-lookup"><span data-stu-id="89694-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="89694-111">Derfor er begge linjer faktureret.</span><span class="sxs-lookup"><span data-stu-id="89694-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="89694-112">Frigivelsesstatussen vises dog stadig som *Delvist frigivet*, hvilket er misvisende.</span><span class="sxs-lookup"><span data-stu-id="89694-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="89694-113">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="89694-113">Issue resolution</span></span>

<span data-ttu-id="89694-114">Frigivelsesstatussen gælder kun for de ordrelinjer, hvor varerne er aktiveret til lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="89694-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="89694-115">Derfor forbliver frigivelsesstatus *Delvist frigivet* i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="89694-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="89694-116">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="89694-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="89694-117">En udvidelse kan tilføjes som en del af følgesedlen og faktureringsprocessen for at opdatere frigivelsesstatussen.</span><span class="sxs-lookup"><span data-stu-id="89694-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
