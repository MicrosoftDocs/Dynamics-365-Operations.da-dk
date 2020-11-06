---
title: Oprette en kreditorkonto
description: Denne fremgangsmåde viser, hvordan du opretter en kreditorkonto og tilføjer en adresse og kontaktoplysninger.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017201"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="52d76-103">Oprette en kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="52d76-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52d76-104">Denne fremgangsmåde viser, hvordan du opretter en kreditorkonto og tilføjer en adresse og kontaktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="52d76-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="52d76-105">Fremgangsmåden viser ikke, hvordan du udfylder alle felter med henblik på købsformål og økonomiske formål.</span><span class="sxs-lookup"><span data-stu-id="52d76-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="52d76-106">Hvis du vil vide mere om disse felter, skal du læse i feltbeskrivelserne.</span><span class="sxs-lookup"><span data-stu-id="52d76-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="52d76-107">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="52d76-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="52d76-108">Der oprettes typisk kreditorkonti af en indkøber eller debitorpersonale.</span><span class="sxs-lookup"><span data-stu-id="52d76-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="52d76-109">Oprette en kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="52d76-109">Create a vendor account</span></span>
1. <span data-ttu-id="52d76-110">Gå til **navigationsruden > Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="52d76-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="52d76-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="52d76-111">Click **New**.</span></span>
3. <span data-ttu-id="52d76-112">Skriv en værdi i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="52d76-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="52d76-113">Værdien udfyldes eventuelt automatisk.</span><span class="sxs-lookup"><span data-stu-id="52d76-113">The value may be populated automatically.</span></span> <span data-ttu-id="52d76-114">Hvis det er tilfældet, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="52d76-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="52d76-115">Du kan oprette kreditorkonti for en person eller organisation.</span><span class="sxs-lookup"><span data-stu-id="52d76-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="52d76-116">Dette påvirker, hvilke felter der er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="52d76-116">This will affect which fields are available.</span></span> <span data-ttu-id="52d76-117">I dette eksempel opretter vi en kreditorkonto for en organisation.</span><span class="sxs-lookup"><span data-stu-id="52d76-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="52d76-118">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="52d76-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="52d76-119">Hvis din kreditor allerede er en registreret part i dit system, kan du bruge rullelisten og vælge den i dette felt. Den nye kreditorkonto arver adresse og kontaktoplysninger, der allerede er registreret.</span><span class="sxs-lookup"><span data-stu-id="52d76-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="52d76-120">Indtast eller vælg en værdi i feltet **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="52d76-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="52d76-121">Kreditorgruppen bruges til at gruppere kreditorer, der har en eller flere af følgende parametre til fælles: betalingsbetingelse, afregningsperiode, finanskonti til lagerbogføring – inklusive momsgruppen, standardfinanskonti, produktfilterkoder eller konfiguration af forsyningsprognose.</span><span class="sxs-lookup"><span data-stu-id="52d76-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="52d76-122">Indtast et tal i feltet **Antal medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="52d76-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="52d76-123">Indtast en værdi i feltet **Organisationsnummer**.</span><span class="sxs-lookup"><span data-stu-id="52d76-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="52d76-124">Tilføj en adresse</span><span class="sxs-lookup"><span data-stu-id="52d76-124">Add an address</span></span>
1. <span data-ttu-id="52d76-125">Udvid sektionen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="52d76-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="52d76-126">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="52d76-126">Click **Add**.</span></span>
3. <span data-ttu-id="52d76-127">Indtast eller vælg en værdi i feltet **Formål**.</span><span class="sxs-lookup"><span data-stu-id="52d76-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="52d76-128">Du kan vælge ét eller flere formål.</span><span class="sxs-lookup"><span data-stu-id="52d76-128">You can select one or more purposes.</span></span> <span data-ttu-id="52d76-129">Disse bruges til at vælge den korrekte adresse til et bestemt formål.</span><span class="sxs-lookup"><span data-stu-id="52d76-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="52d76-130">Hvis formålet f.eks. er "Faktura", vil denne adresse blive brugt, når du sender fakturaer.</span><span class="sxs-lookup"><span data-stu-id="52d76-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="52d76-131">Skriv en værdi i feltet **Navn eller beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="52d76-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="52d76-132">Indtast eller vælg en værdi i feltet **Land/område**.</span><span class="sxs-lookup"><span data-stu-id="52d76-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="52d76-133">Indtast adresseoplysninger.</span><span class="sxs-lookup"><span data-stu-id="52d76-133">Enter the address details.</span></span> <span data-ttu-id="52d76-134">Det land/område, du har valgt, bestemmer de felter, der vises, og de svarer til adresseformatet for landet/området.</span><span class="sxs-lookup"><span data-stu-id="52d76-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="52d76-135">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d76-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="52d76-136">Tilføj kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="52d76-136">Add contact information</span></span>
1. <span data-ttu-id="52d76-137">Udvid sektionen **Kontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="52d76-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="52d76-138">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="52d76-138">Click **Add**.</span></span>
3. <span data-ttu-id="52d76-139">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="52d76-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="52d76-140">Vælg en indstilling i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="52d76-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="52d76-141">Skriv en værdi i feltet **Kontaktpersons nummer/adresse**.</span><span class="sxs-lookup"><span data-stu-id="52d76-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="52d76-142">Du kan markere afkrydsningsfeltet Primær, hvis dette er den primære kontakt.</span><span class="sxs-lookup"><span data-stu-id="52d76-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="52d76-143">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="52d76-143">Click **Save**.</span></span>
7. <span data-ttu-id="52d76-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="52d76-144">Close the page.</span></span>
8. <span data-ttu-id="52d76-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="52d76-145">Close the page.</span></span>

