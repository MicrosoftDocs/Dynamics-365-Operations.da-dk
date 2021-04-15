---
title: Opret juridiske enheder
description: Dette emne beskriver, hvordan du opretter juridiske enheder i Microsoft Dynamics 365 Commerce, som skal være oprettet og konfigureret, før du opretter kanaler.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800608"
---
# <a name="create-legal-entities"></a><span data-ttu-id="76de1-103">Opret juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="76de1-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76de1-104">Dette emne beskriver, hvordan du opretter juridiske enheder i Microsoft Dynamics 365 Commerce, som skal være oprettet og konfigureret, før du opretter kanaler.</span><span class="sxs-lookup"><span data-stu-id="76de1-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="76de1-105">En juridisk enhed er en organisation, der består af en registreret eller lovgivningsbaseret juridisk struktur.</span><span class="sxs-lookup"><span data-stu-id="76de1-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="76de1-106">Juridiske enheder kan indgå juridisk bindende kontrakter og skal udarbejde opgørelser med afrapportering af deres præstation.</span><span class="sxs-lookup"><span data-stu-id="76de1-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="76de1-107">Et firma er en type juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="76de1-107">A company is a type of legal entity.</span></span> <span data-ttu-id="76de1-108">I øjeblikket er firmaer den eneste slags juridiske enhed, som du kan oprette, og hver juridiske enhed får tilknyttet et firma-id.</span><span class="sxs-lookup"><span data-stu-id="76de1-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="76de1-109">Denne tilknytning findes, da nogle funktionsområder i programmet bruger et firma-id, eller *DataAreaId* i deres datamodeller.</span><span class="sxs-lookup"><span data-stu-id="76de1-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="76de1-110">Firmaer bruges som en afgrænsning for datasikkerhed i disse funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="76de1-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="76de1-111">Brugere har kun adgang til data for det firma, som de er logget på.</span><span class="sxs-lookup"><span data-stu-id="76de1-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="76de1-112">Når du opretter en kanal, skal du angive den juridiske enhed, som kanalen tilhører.</span><span class="sxs-lookup"><span data-stu-id="76de1-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="76de1-113">Opret en ny juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="76de1-113">Create a new legal entity</span></span>

<span data-ttu-id="76de1-114">Gør følgende for at oprette en ny juridisk enhed i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="76de1-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="76de1-115">Gå til **Moduler \> Konfiguration af hovedkontor \> Juridiske enheder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="76de1-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="76de1-116">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="76de1-116">On the action pane, select **New**.</span></span> <span data-ttu-id="76de1-117">Ruden **Ny juridisk enhed** vises til højre.</span><span class="sxs-lookup"><span data-stu-id="76de1-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="76de1-118">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="76de1-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="76de1-119">Angiv en værdi i feltet **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="76de1-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="76de1-120">Indtast eller vælg en værdi i feltet **Land/område**.</span><span class="sxs-lookup"><span data-stu-id="76de1-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="76de1-121">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="76de1-121">Select **OK**.</span></span> 

   ![Oprettelse af en juridisk enhed](media/legal-entities.png)

1. <span data-ttu-id="76de1-123">Angiv følgende generelle oplysninger om den juridiske enhed i sektionen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="76de1-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="76de1-124">Angiv et søgenavn, hvis et søgenavn er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="76de1-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="76de1-125">Et søgenavn er et alternativt navn, der kan bruges til at søge efter den pågældende juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="76de1-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="76de1-126">Angiv, om den pågældende juridiske enhed skal bruges til et konsolideret regnskab.</span><span class="sxs-lookup"><span data-stu-id="76de1-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="76de1-127">Angiv, om den pågældende juridiske enhed skal bruges til et elimineringsregnskab.</span><span class="sxs-lookup"><span data-stu-id="76de1-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="76de1-128">Vælg **standardsproget** for enheden.</span><span class="sxs-lookup"><span data-stu-id="76de1-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="76de1-129">Vælg **tidszonen** for enheden.</span><span class="sxs-lookup"><span data-stu-id="76de1-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="76de1-130">Vælg **Rediger** for at angive adresseoplysninger, som f.eks. gadenavn, husnummer, postnummer og by, i sektionen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="76de1-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="76de1-131">Angiv oplysninger om kommunikationsmåder som f.eks. mailadresser, URL-adresser og telefonnumre, i sektionen **Kontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="76de1-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="76de1-132">Angiv de registreringsnumre, der bruges til lovpligtig rapportering, i sektionen **Lovpligtig rapportering**.</span><span class="sxs-lookup"><span data-stu-id="76de1-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="76de1-133">Angiv de oplysninger, der kræves af den juridiske enhed, i sektionen **Registreringsnumre**.</span><span class="sxs-lookup"><span data-stu-id="76de1-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="76de1-134">Angiv bankkonti og registreringsnumre for den juridiske enhed, i sektionen **Bankkontooplysninger**.</span><span class="sxs-lookup"><span data-stu-id="76de1-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="76de1-135">Angiv forsendelsesoplysninger for den juridiske enhed, i sektionen **Udenrigshandel og logistik**.</span><span class="sxs-lookup"><span data-stu-id="76de1-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="76de1-136">Du kan se de nummerserier, der er tilknyttet den juridiske enhed, i sektionen **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="76de1-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="76de1-137">Dette er tomt fra starten.</span><span class="sxs-lookup"><span data-stu-id="76de1-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="76de1-138">Vis eller skift det logo og/eller dashboardbillede, der er tilknyttet den juridiske enhed, i sektionen **Dashboardbillede**.</span><span class="sxs-lookup"><span data-stu-id="76de1-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="76de1-139">Angiv de registreringsnumre, der bruges til rapportering til skattemyndigheder, i sektionen **Momsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="76de1-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="76de1-140">Angiv 1099-oplysninger for den juridiske enhed i sektionen **1099-skat**.</span><span class="sxs-lookup"><span data-stu-id="76de1-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="76de1-141">Angiv momosoplysningerne for den juridisk enhed i sektionen **Momsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="76de1-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="76de1-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="76de1-142">Select **Save**.</span></span>

<span data-ttu-id="76de1-143">Følgende billede viser et eksempel på en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="76de1-143">The following image shows details of an example legal entity.</span></span>

![Sektion for generel juridisk enhed](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="76de1-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="76de1-145">Additional resources</span></span>

[<span data-ttu-id="76de1-146">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="76de1-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76de1-147">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="76de1-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76de1-148">Organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="76de1-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="76de1-149">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="76de1-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="76de1-150">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="76de1-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
