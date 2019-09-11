---
title: Arbejdsordretyper
description: I dette emne beskrives typer af arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 57120b51c069e49697f8ec4357265974a0d3afb4
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874572"
---
# <a name="work-order-types"></a><span data-ttu-id="e8d98-103">Arbejdsordretyper</span><span class="sxs-lookup"><span data-stu-id="e8d98-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e8d98-104">Arbejdsordretyper bruges til kategorisering af arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="e8d98-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="e8d98-105">Du kan for eksempel have arbejdsordrer, der er relateret til forebyggende vedligeholdelse eller korrigerende vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="e8d98-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="e8d98-106">En arbejdsordretype definerer et tilhørsforhold til en arbejdsordres livscyklusmodel.</span><span class="sxs-lookup"><span data-stu-id="e8d98-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="e8d98-107">En arbejdsordres livscyklusmodel definerer de levetidstilstande for arbejdsordren, som kan angives på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="e8d98-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="e8d98-108">(Eksempler på livscyklustilstande for arbejdsordrer omfatter **Oprettet**, **I gang** og **Afsluttet**).</span><span class="sxs-lookup"><span data-stu-id="e8d98-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="e8d98-109">Du kan finde flere oplysninger om arbejdsordrers livscyklustilstande og projektstadier i [Livscyklustilstande for arbejdsordre](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="e8d98-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="e8d98-110">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Arbejdsordretyper**.</span><span class="sxs-lookup"><span data-stu-id="e8d98-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="e8d98-111">Vælg **Ny** for at oprette en arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="e8d98-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="e8d98-112">Angiv et id for arbejdsordretypen i feltet **Arbejdsordretype**.</span><span class="sxs-lookup"><span data-stu-id="e8d98-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="e8d98-113">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e8d98-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="e8d98-114">Vælg en livscyklusmodel i feltet **Livscyklusmodel for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="e8d98-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="e8d98-115">Vælg **Ja** i indstillingen **Én vedligeholdelsesarbejder**, hvis alle arbejdsordrejob, der er knyttet til en arbejdsordre af denne type, skal planlægges til samme vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="e8d98-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="e8d98-116">I feltet **Omkostningstype** skal du vælge **Korrigerende**, **Forebyggende** eller **Investering** efter behov.</span><span class="sxs-lookup"><span data-stu-id="e8d98-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="e8d98-117">Alle arbejdsordrejob i en arbejdsordre skal have samme omkostningstype.</span><span class="sxs-lookup"><span data-stu-id="e8d98-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="e8d98-118">Vælg **Ja** i de relevante indstillinger i sektionen **Obligatorisk** for at angive, hvilke fejlrelaterede oplysninger eller oplysninger relateret til vedligeholdelsesnedetid, der skal føjes til en arbejdsordre af denne type.</span><span class="sxs-lookup"><span data-stu-id="e8d98-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8d98-119">Indstillingerne i sektionen **Obligatorisk** er relateret til indstillingerne i oversigtspanelet **Valider** på siden **Livscyklustilstande for arbejdsordre** (**Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Livscyklustilstande**).</span><span class="sxs-lookup"><span data-stu-id="e8d98-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="e8d98-120">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e8d98-120">Select **Save**.</span></span>

![Figur 1](media/16-setup-for-work-orders.png)
