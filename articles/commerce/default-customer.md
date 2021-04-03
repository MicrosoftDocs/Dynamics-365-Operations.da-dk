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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477894"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="f6360-103">Oprette en standarddebitor</span><span class="sxs-lookup"><span data-stu-id="f6360-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6360-104">Dette emne beskriver, hvordan du opretter en standarddebitor, der skal bruges, når der oprettes en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6360-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f6360-105">Når du opretter en kanal, skal du angive en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="f6360-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="f6360-106">Der kan nemt oprettes en standarddebitor, når kundegruppen og kundeadressekartoteket først er oprettet.</span><span class="sxs-lookup"><span data-stu-id="f6360-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="f6360-107">Oprette en kundegruppe</span><span class="sxs-lookup"><span data-stu-id="f6360-107">Create a customer group</span></span>

<span data-ttu-id="f6360-108">Hvis der endnu ikke findes nogen kundegrupper, kan du oprette en.</span><span class="sxs-lookup"><span data-stu-id="f6360-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="f6360-109">Eksempler på dette kan være grupper, der repræsenterer forskellige kundegrupper, f.eks. engros, detail, internet, medarbejdere osv.</span><span class="sxs-lookup"><span data-stu-id="f6360-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="f6360-110">Du kan oprette en kundegruppe ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f6360-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="f6360-111">Gå til **Moduler \> Detail og handel \> Kunder \> Kundegrupper** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="f6360-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="f6360-112">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6360-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f6360-113">I feltet **Kundegruppe** skal du indtaste et id for kundegruppen.</span><span class="sxs-lookup"><span data-stu-id="f6360-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="f6360-114">Angiv eventuelt en passende beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f6360-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="f6360-115">Angiv eventuelt en passende beskrivelse i feltet **Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="f6360-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="f6360-116">Angiv en relevant værdi i feltet **Tid mellem fakturaens forfaldsdato og betalingsdato**.</span><span class="sxs-lookup"><span data-stu-id="f6360-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="f6360-117">Angiv en momsgruppe i feltet **Standardmomsgruppe**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="f6360-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="f6360-118">Markér afkrydsningsfeltet **Priserne inkluderer moms**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="f6360-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="f6360-119">I feltet **Standardårsag til afskrivning** skal du angive en passende værdi, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="f6360-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="f6360-120">Følgende billede viser flere konfigurerede kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="f6360-120">The following image shows several configured customer groups.</span></span>

![Debitorgrupper](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="f6360-122">Opret et kundeadressekartotek</span><span class="sxs-lookup"><span data-stu-id="f6360-122">Create a customer address book</span></span>

<span data-ttu-id="f6360-123">En kunde skal være knyttet et adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="f6360-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="f6360-124">Hvis der endnu ikke er oprettet et, skal du oprette det.</span><span class="sxs-lookup"><span data-stu-id="f6360-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="f6360-125">Du kan oprette et kundeadressekartotek ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f6360-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="f6360-126">Gå til **Moduler \> Detail og handel \> Konfiguration af kanal \> Adressekartoteker** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="f6360-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="f6360-127">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6360-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f6360-128">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f6360-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f6360-129">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f6360-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f6360-130">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f6360-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f6360-131">Følgende billede viser et eksempel på et adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="f6360-131">The following image shows an example address book.</span></span>

![Adressebog](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="f6360-133">Oprette en standarddebitor</span><span class="sxs-lookup"><span data-stu-id="f6360-133">Create a default customer</span></span>

<span data-ttu-id="f6360-134">Du kan oprette en standarddebitor ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f6360-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="f6360-135">Gå til **Moduler \> Detail og handel \> Kunder \> Alle kunder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="f6360-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="f6360-136">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f6360-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f6360-137">Vælg "Person" på rullelisten **Type**.</span><span class="sxs-lookup"><span data-stu-id="f6360-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="f6360-138">Vælg eller indtast et kontonummer (f.eks "100001") på rullelisten **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="f6360-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="f6360-139">Vælg eller indtast et navn (f.eks. "Standard") på rullelisten **Fornavn**.</span><span class="sxs-lookup"><span data-stu-id="f6360-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="f6360-140">Vælg eller indtast et navn (f.eks. "Detail") på rullelisten **Mellemnavn**.</span><span class="sxs-lookup"><span data-stu-id="f6360-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="f6360-141">Vælg eller indtast et navn (f.eks. "Kunde") på rullelisten **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="f6360-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="f6360-142">Vælg eller indtast en valuta (f.eks. "USD") på rullelisten **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="f6360-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="f6360-143">Vælg den kundegruppe, du tidligere har oprettet, på rullelisten **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="f6360-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="f6360-144">Vælg et eksisterende kundeadressekartotek på rullelisten **Adressekartoteker**.</span><span class="sxs-lookup"><span data-stu-id="f6360-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="f6360-145">Vælg **Gem** for at gemme og vende tilbage til skærmbilledet med kundedetaljer for den nye kunde.</span><span class="sxs-lookup"><span data-stu-id="f6360-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="f6360-146">Det er ikke nødvendigt at tilføje en adresse for en standardkunde.</span><span class="sxs-lookup"><span data-stu-id="f6360-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="f6360-147">Følgende billede viser et eksempel på kundeoprettelse.</span><span class="sxs-lookup"><span data-stu-id="f6360-147">The following image shows an example of customer creation.</span></span>

![Standardkundeoprettelse](media/default-customer-creation.png)

<span data-ttu-id="f6360-149">Følgende billede viser en standardkonfiguration af kunde.</span><span class="sxs-lookup"><span data-stu-id="f6360-149">The following image shows a default customer configuration.</span></span>

![Eksempelkonfiguration af kunde](media/default-customer-configuration1.png)

<span data-ttu-id="f6360-151">Du kan beholde de fleste af standardværdierne i skærmen kundedetaljer, men to værdier skal ændres.</span><span class="sxs-lookup"><span data-stu-id="f6360-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="f6360-152">Udvid **Salgsordrestandarder** i skærmen med kundedetaljer.</span><span class="sxs-lookup"><span data-stu-id="f6360-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="f6360-153">Vælg eller angiv et forudkonfigureret websted på rullelisten **Angiv**.</span><span class="sxs-lookup"><span data-stu-id="f6360-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="f6360-154">Vælg eller angiv et forudkonfigureret lagersted på rullelisten **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="f6360-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="f6360-155">Følgende billede viser et eksempel på konfiguration af kunde.</span><span class="sxs-lookup"><span data-stu-id="f6360-155">The following image shows an example customer configuration.</span></span>

![Eksempel på konfiguration af kunde](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="f6360-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f6360-157">Additional resources</span></span>

[<span data-ttu-id="f6360-158">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="f6360-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f6360-159">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="f6360-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
