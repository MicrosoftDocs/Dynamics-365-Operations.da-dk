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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263222"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="65096-103">Foretage fejlfinding af delvise frigivelser og delvise forsendelser</span><span class="sxs-lookup"><span data-stu-id="65096-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65096-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med delvise frigivelser og delvise forsendelser i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="65096-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="65096-105">En salgsordres frigivelsesstatus forbliver Delvist frigivet, selv efter at salgsordren er faktureret.</span><span class="sxs-lookup"><span data-stu-id="65096-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="65096-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="65096-106">Issue description</span></span>

<span data-ttu-id="65096-107">En salgsordre er en leveringsordre, men en eller flere varer på den har en anden leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="65096-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="65096-108">Når ordren er faktureret, har den stadig frigivelsesstatussen *Delvist frigivet*.</span><span class="sxs-lookup"><span data-stu-id="65096-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="65096-109">En salgsordre har f.eks. to varer: én til levering og én til afhentning.</span><span class="sxs-lookup"><span data-stu-id="65096-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="65096-110">Både levering og afhentning er udført.</span><span class="sxs-lookup"><span data-stu-id="65096-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="65096-111">Derfor er begge linjer faktureret.</span><span class="sxs-lookup"><span data-stu-id="65096-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="65096-112">Frigivelsesstatussen vises dog stadig som *Delvist frigivet*, hvilket er misvisende.</span><span class="sxs-lookup"><span data-stu-id="65096-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="65096-113">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="65096-113">Issue resolution</span></span>

<span data-ttu-id="65096-114">Frigivelsesstatussen gælder kun for de ordrelinjer, hvor varerne er aktiveret til lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="65096-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="65096-115">Derfor forbliver frigivelsesstatus *Delvist frigivet* i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="65096-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="65096-116">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="65096-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="65096-117">En udvidelse kan tilføjes som en del af følgesedlen og faktureringsprocessen for at opdatere frigivelsesstatussen.</span><span class="sxs-lookup"><span data-stu-id="65096-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]