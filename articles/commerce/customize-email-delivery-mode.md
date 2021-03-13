---
title: Tilpasse transaktionsmails efter leveringsmåde
description: Dette emne beskriver, hvordan du konfigurerer brugerdefinerede mailskabeloner for specifikke beskedtyper og leveringsmåder i Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031842"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="12cac-103">Tilpasse transaktionsmails efter leveringsmåde</span><span class="sxs-lookup"><span data-stu-id="12cac-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12cac-104">Dette emne beskriver, hvordan du konfigurerer brugerdefinerede mailskabeloner for specifikke beskedtyper og leveringsmåder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12cac-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="12cac-105">Transaktionsmails kan nu tilpasses til en kombination af en beskedtype (f.eks. **Ordre oprettet**, **Ordre pakket** eller **Ordre faktureret**) og en leveringsmåde (f.eks. i løbet af natten, in-afhentning i butikken eller ved fortovskanten).</span><span class="sxs-lookup"><span data-stu-id="12cac-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="12cac-106">Brugerdefinerede transaktionsmails gør det muligt for detailhandlerne at give deres kunder ordrer med opfyldningsoplevelser, der er skræddersyet til ordrens leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="12cac-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="12cac-107">Hændelsen "ordre pakket" kan f.eks. tilpasses, så den giver afhentningsinstruktioner til kunder, der vælger afhentning ved fortovskanten.</span><span class="sxs-lookup"><span data-stu-id="12cac-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="12cac-108">Alternativt kan den give oplysninger om fragtmand og levering til kunder, der vælger, at deres ordre skal afsendes.</span><span class="sxs-lookup"><span data-stu-id="12cac-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="12cac-109">Hvis du vil bruge funktionaliteten til tilpassede transaktionsmails, skal du først aktivere funktionen **Tilpasse transaktionsmails efter leveringsmåde** ved at gå til **Arbejdsområder \> Funktionsstyring** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="12cac-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="12cac-110">E-mails kan tilpasses efter leveringsmåde for følgende beskedtyper:</span><span class="sxs-lookup"><span data-stu-id="12cac-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="12cac-111">**Ordreannullering** – Denne mailbeskedtype er ny.</span><span class="sxs-lookup"><span data-stu-id="12cac-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="12cac-112">**Der er oprettet en ordre**</span><span class="sxs-lookup"><span data-stu-id="12cac-112">**Order created**</span></span>
- <span data-ttu-id="12cac-113">**Bekræftet ordre**</span><span class="sxs-lookup"><span data-stu-id="12cac-113">**Order confirmed**</span></span>
- <span data-ttu-id="12cac-114">**Ordre faktureret** – Denne mailbeskedtype er ny.</span><span class="sxs-lookup"><span data-stu-id="12cac-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="12cac-115">Den kan bruges i stedet for beskedtypen **Ordre leveret**, der sender en besked om enhver fakturahændelse, der har en afsendelsesmåden levering (ikke afhentning eller elektronisk leveringsmåde).</span><span class="sxs-lookup"><span data-stu-id="12cac-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="12cac-116">**Ordre afhentet**</span><span class="sxs-lookup"><span data-stu-id="12cac-116">**Order picked**</span></span>
- <span data-ttu-id="12cac-117">**Ordre pakket**</span><span class="sxs-lookup"><span data-stu-id="12cac-117">**Order packed**</span></span>
- <span data-ttu-id="12cac-118">**Ordre klar til afhentning** – Denne beskedtype kan kun tilpasses efter leveringsmåde, hvis funktionen **Understøttelse af flere leveringsmåder for afhentning** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="12cac-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="12cac-119">I dette tilfælde har denne beskedtype samme funktion om beskedtypen **Ordre pakket**.</span><span class="sxs-lookup"><span data-stu-id="12cac-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="12cac-120">**Betalingen blev ikke udført**</span><span class="sxs-lookup"><span data-stu-id="12cac-120">**Payment failed**</span></span>
- <span data-ttu-id="12cac-121">**Erstatningsordre oprettet**</span><span class="sxs-lookup"><span data-stu-id="12cac-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="12cac-122">Konfigurere mailskabeloner til bestemte leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="12cac-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="12cac-123">I denne procedure antages det, at du allerede har oprettet de nye brugerdefinerede mailskabeloner og føjet dem til siden **Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="12cac-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="12cac-124">Du kan finde oplysninger om, hvordan du opretter og overfører mailskabeloner, i [Oprette e-mailskabeloner til transaktionshændelser](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="12cac-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="12cac-125">Hvis du vil konfigurere mailskabeloner for bestemte leveringsmåder i Commerce Headquarters, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="12cac-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="12cac-126">Gå til **Commerce-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="12cac-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="12cac-127">Vælg en eksisterende beskedtype under **Indstillinger for besked om detailhændelse**.</span><span class="sxs-lookup"><span data-stu-id="12cac-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="12cac-128">Mens beskedtypen stadig er valgt, skal du vælge **Konfigurere leveringsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="12cac-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="12cac-129">I dialogboksen **Leveringsmåder** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="12cac-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="12cac-130">I feltet **Leveringsmåde** i den nye række skal du vælge en leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="12cac-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="12cac-131">Vælg den mailskabelon, der skal knyttes til leveringsmåden, i feltet **E-mail-id**.</span><span class="sxs-lookup"><span data-stu-id="12cac-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="12cac-132">Marker afkrydsningsfeltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="12cac-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="12cac-133">Gentag trin 4 til 7 for at tilføje flere leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="12cac-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="12cac-134">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="12cac-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="12cac-135">Når der findes mere end én leveringsmåde på tværs af linjer i en salgsordre, bruges standardskabelonen.</span><span class="sxs-lookup"><span data-stu-id="12cac-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="12cac-136">Standardskabelonen er den skabelon, der er knyttet til beskedtypen på siden **Commerce-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="12cac-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="12cac-137">Hvis en salgsordre har en leveringsmåde, der ikke er konfigureret til en brugerdefineret mailskabelon, bruges e-mailstandardskabelonen.</span><span class="sxs-lookup"><span data-stu-id="12cac-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12cac-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="12cac-138">Additional resources</span></span>

[<span data-ttu-id="12cac-139">Oprette callcenter-ordrer</span><span class="sxs-lookup"><span data-stu-id="12cac-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="12cac-140">Skifte leveringsmåde til i POS</span><span class="sxs-lookup"><span data-stu-id="12cac-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)
