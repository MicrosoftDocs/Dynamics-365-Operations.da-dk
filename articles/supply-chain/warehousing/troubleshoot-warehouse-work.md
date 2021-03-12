---
title: Foretage fejlfinding af lagerstedsarbejde
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsarbejde i Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970225"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="7286f-103">Foretage fejlfinding af lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="7286f-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7286f-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsarbejde i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7286f-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="7286f-105">Jeg kan ikke flytte id'er, der har serienummervarer, når blank afgang og blank tilgang er tilladt i sporingsdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="7286f-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7286f-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="7286f-106">Issue description</span></span>

<span data-ttu-id="7286f-107">Du kan ikke flytte et id ved at bruge menupunktet **Bevægelse**, hvis serienummeret har indstillingen *Blank afgang tilladt* og *Blank tilgang tilladt* i sporingsdimensionsgruppen, og hvis der er flere id'er på samme lokation, hvoraf nogle har serienumre og nogle ikke har dem.</span><span class="sxs-lookup"><span data-stu-id="7286f-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7286f-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="7286f-108">Issue resolution</span></span>

<span data-ttu-id="7286f-109">Dette problem løses af de ændringer, der implementeres i [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="7286f-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="7286f-110">Disse ændringer gør feltet **Serienummer** valgfrit, når blank tilgang og blank afgang er tilladt.</span><span class="sxs-lookup"><span data-stu-id="7286f-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="7286f-111">Jeg modtager følgende fejlmeddelelse i lagerstedsappen, når jeg behandler bevægelser: "Lagerejeren %1 er ikke tilladt i denne proces".</span><span class="sxs-lookup"><span data-stu-id="7286f-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7286f-112">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="7286f-112">Issue description</span></span>

<span data-ttu-id="7286f-113">Sporingsdimensionen **Ejer** mangler, når lagerstedsappen bruges til at foretage bevægelser.</span><span class="sxs-lookup"><span data-stu-id="7286f-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="7286f-114">En almindelig lageroverførselskladde fra Supply Chain Management-klienten ser ud til at fungere efter hensigten og kan kun bogføres, hvis dimensionen **Ejer** er udfyldt.</span><span class="sxs-lookup"><span data-stu-id="7286f-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7286f-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="7286f-115">Issue resolution</span></span>

<span data-ttu-id="7286f-116">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="7286f-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="7286f-117">I øjeblikket understøtter lagerstyringsprocesser kun det lager, der ejes af den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="7286f-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
