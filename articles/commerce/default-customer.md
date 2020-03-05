---
title: Oprette en standarddebitor
description: Dette emne beskriver, hvordan du opretter en standarddebitor, der skal bruges, når der oprettes en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e1087821b357c578993cdd5742399c5ec0ecc95
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001800"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="887e3-103">Oprette en standarddebitor</span><span class="sxs-lookup"><span data-stu-id="887e3-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="887e3-104">Dette emne beskriver, hvordan du opretter en standarddebitor, der skal bruges, når der oprettes en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="887e3-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="887e3-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="887e3-105">Overview</span></span>

<span data-ttu-id="887e3-106">Når du opretter en detail- eller onlinekanal, skal du angive en standarddebitor.</span><span class="sxs-lookup"><span data-stu-id="887e3-106">When creating a retail or online channel, you will need to provide a default customer.</span></span> <span data-ttu-id="887e3-107">Der kan nemt oprettes en standarddebitor, når kundegruppen og kundeadressekartoteket først er oprettet.</span><span class="sxs-lookup"><span data-stu-id="887e3-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="887e3-108">Oprette en kundegruppe</span><span class="sxs-lookup"><span data-stu-id="887e3-108">Create a customer group</span></span>

<span data-ttu-id="887e3-109">Hvis der endnu ikke findes nogen kundegrupper, kan du oprette en.</span><span class="sxs-lookup"><span data-stu-id="887e3-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="887e3-110">Eksempler på dette kan være grupper, der repræsenterer forskellige kundegrupper, f.eks. engros, detail, internet, medarbejdere osv.</span><span class="sxs-lookup"><span data-stu-id="887e3-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="887e3-111">Du kan oprette en kundegruppe ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="887e3-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="887e3-112">Gå til **Moduler \> Detail og handel \> Kunder \> Kundegrupper** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="887e3-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="887e3-113">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="887e3-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="887e3-114">I feltet **Kundegruppe** skal du indtaste et id for kundegruppen.</span><span class="sxs-lookup"><span data-stu-id="887e3-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="887e3-115">Angiv eventuelt en passende beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="887e3-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="887e3-116">Angiv eventuelt en passende beskrivelse i feltet **Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="887e3-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="887e3-117">Angiv en relevant værdi i feltet **Tid mellem fakturaens forfaldsdato og betalingsdato**.</span><span class="sxs-lookup"><span data-stu-id="887e3-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="887e3-118">Angiv en momsgruppe i feltet **Standardmomsgruppe**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="887e3-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="887e3-119">Markér afkrydsningsfeltet **Priserne inkluderer moms**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="887e3-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="887e3-120">I feltet **Standardårsag til afskrivning** skal du angive en passende værdi, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="887e3-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="887e3-121">Følgende billede viser flere konfigurerede kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="887e3-121">The following image shows several configured customer groups.</span></span>

![Debitorgrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="887e3-123">Opret et kundeadressekartotek</span><span class="sxs-lookup"><span data-stu-id="887e3-123">Create a customer address book</span></span>

<span data-ttu-id="887e3-124">En kunde skal være knyttet et adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="887e3-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="887e3-125">Hvis der endnu ikke er oprettet et, skal du oprette det.</span><span class="sxs-lookup"><span data-stu-id="887e3-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="887e3-126">Du kan oprette et kundeadressekartotek ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="887e3-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="887e3-127">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Adressekartoteker** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="887e3-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="887e3-128">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="887e3-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="887e3-129">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="887e3-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="887e3-130">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="887e3-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="887e3-131">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="887e3-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="887e3-132">Følgende billede viser et eksempel på et adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="887e3-132">The following image shows an example address book.</span></span>

![Adressebog](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="887e3-134">Oprette en standarddebitor</span><span class="sxs-lookup"><span data-stu-id="887e3-134">Create a default customer</span></span>

<span data-ttu-id="887e3-135">Du kan oprette en standarddebitor ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="887e3-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="887e3-136">Gå til **Moduler \> Detail og handel \> Kunder \> Alle kunder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="887e3-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="887e3-137">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="887e3-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="887e3-138">Vælg "Person" på rullelisten **Type**.</span><span class="sxs-lookup"><span data-stu-id="887e3-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="887e3-139">Vælg eller indtast et kontonummer (f.eks "100001") på rullelisten **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="887e3-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="887e3-140">Vælg eller indtast et navn (f.eks. "Standard") på rullelisten **Fornavn**.</span><span class="sxs-lookup"><span data-stu-id="887e3-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="887e3-141">Vælg eller indtast et navn (f.eks. "Detail") på rullelisten **Mellemnavn**.</span><span class="sxs-lookup"><span data-stu-id="887e3-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="887e3-142">Vælg eller indtast et navn (f.eks. "Kunde") på rullelisten **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="887e3-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="887e3-143">Vælg eller indtast en valuta (f.eks. "USD") på rullelisten **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="887e3-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="887e3-144">Vælg den kundegruppe, du tidligere har oprettet, på rullelisten **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="887e3-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="887e3-145">Vælg et eksisterende kundeadressekartotek på rullelisten **Adressekartoteker**.</span><span class="sxs-lookup"><span data-stu-id="887e3-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="887e3-146">Vælg **Gem** for at gemme og vende tilbage til skærmbilledet med kundedetaljer for den nye kunde.</span><span class="sxs-lookup"><span data-stu-id="887e3-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="887e3-147">Det er ikke nødvendigt at tilføje en adresse for en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="887e3-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="887e3-148">Følgende billede viser et eksempel på kundeoprettelse.</span><span class="sxs-lookup"><span data-stu-id="887e3-148">The following image shows an example of customer creation.</span></span>

![Standardkundeoprettelse](media/default-customer-creation.png)

<span data-ttu-id="887e3-150">Følgende billede viser en standardkonfiguration af kunde.</span><span class="sxs-lookup"><span data-stu-id="887e3-150">The following image shows a default customer configuration.</span></span>

![Eksempelkonfiguration af kunde](media/default-customer-configuration1.png)

<span data-ttu-id="887e3-152">Du kan beholde de fleste af standardværdierne i skærmen kundedetaljer, men to værdier skal ændres.</span><span class="sxs-lookup"><span data-stu-id="887e3-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="887e3-153">Udvid **Salgsordrestandarder** i skærmen med kundedetaljer.</span><span class="sxs-lookup"><span data-stu-id="887e3-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="887e3-154">Vælg eller angiv et forudkonfigureret websted på rullelisten **Angiv**.</span><span class="sxs-lookup"><span data-stu-id="887e3-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="887e3-155">Vælg eller angiv et forudkonfigureret lagersted på rullelisten **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="887e3-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="887e3-156">Følgende billede viser et eksempel på konfiguration af kunde.</span><span class="sxs-lookup"><span data-stu-id="887e3-156">The following image shows an example customer configuration.</span></span>

![Eksempel på konfiguration af kunde](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="887e3-158">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="887e3-158">Additional resources</span></span>

[<span data-ttu-id="887e3-159">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="887e3-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="887e3-160">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="887e3-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)