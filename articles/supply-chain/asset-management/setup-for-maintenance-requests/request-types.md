---
title: Typer af vedligeholdelsesanmodninger
description: Dette emne beskriver, hvordan du konfigurerer typer af vedligeholdelsesanmodninger i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e4f622cda62cad13a8146cbc26bc2e5f1a45222
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261183"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="5e2fc-103">Typer af vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="5e2fc-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5e2fc-104">Vedligeholdelsesanmodningstyper bruges til at kategorisere vedligeholdelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="5e2fc-105">Du kan for eksempel have vedligeholdelsesanmodningstyper, der er relateret til forebyggende vedligeholdelse og korrigerende vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="5e2fc-106">Eller du kan have en særlig vedligeholdelsesanmodningstype, der bruges til at administrere reparationer af aktiver (depotreparation).</span><span class="sxs-lookup"><span data-stu-id="5e2fc-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="5e2fc-107">En vedligeholdelsesanmodningstype definerer tilknytningen til en vedligeholdelsesanmodnings livscyklustilstandsgruppe (vedligeholdelseslivscyklusmodel).</span><span class="sxs-lookup"><span data-stu-id="5e2fc-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="5e2fc-108">Livscyklusmodeller for vedligeholdelsesanmodninger definerer de livscyklustilstande, der kan angives for en vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="5e2fc-109">(Eksempler på livscyklustilstande for vedligeholdelsesanmodninger omfatter **Oprettet**, **Aktive** og **Afsluttede**.)</span><span class="sxs-lookup"><span data-stu-id="5e2fc-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="5e2fc-110">Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Vedligeholdelsesanmodningstyper**.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="5e2fc-111">Vælg **Ny** for at oprette en vedligeholdelsesanmodningstype.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="5e2fc-112">I feltet **Vedligeholdelsesanmodningstype** skal du angive et ID for vedligeholdelsesanmodningstypen.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="5e2fc-113">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="5e2fc-114">I oversigtspanelet **Generelt** skal du i feltet **Vedligeholdelsesanmodningens livscyklusmodel** vælge en livscyklusmodel for vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="5e2fc-115">I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="5e2fc-116">Når en vedligeholdelsesanmodning konverteres til en arbejdsordre, får arbejdsordren automatisk den arbejdsordretype, der er relateret til vedligeholdelsesanmodningstypen.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="5e2fc-117">I følgende illustration vises et eksempel på listesiden **Vedligeholdelsesanmodningstype**.</span><span class="sxs-lookup"><span data-stu-id="5e2fc-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Siden Vedligeholdelsesanmodningstyper](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]