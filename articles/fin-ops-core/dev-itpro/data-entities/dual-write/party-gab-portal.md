---
title: Brug af Power Portal sammen med datamodellen for part
description: I dette emne beskrives ændringerne af Power Portal-webrollerne på grund af datamodellen for part i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833084"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="31c04-103">Brug af Power Portal sammen med datamodellen for part</span><span class="sxs-lookup"><span data-stu-id="31c04-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="31c04-104">Dobbeltskrivningsprogrammets orkestreringsløsning version 2.0.999.0 og senere inkluderer datamodelændringer til part- og globalt adressekartotek for tabellerne Konto og Kontakt.</span><span class="sxs-lookup"><span data-stu-id="31c04-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="31c04-105">Ændringerne giver mulighed for mange til mange-relationer, der understøtter avancerede forretningsscenarier.</span><span class="sxs-lookup"><span data-stu-id="31c04-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="31c04-106">Disse ændringer understøttes ikke af portalwebroller, herunder kundeportalen, der medfølger som standard, eller som fandtes i dit miljø, før du installerede dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="31c04-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="31c04-107">Hvis webrollerne skal fungere som forventet, skal du oprette nye webroller ved hjælp af den nye datamodel.</span><span class="sxs-lookup"><span data-stu-id="31c04-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="31c04-108">Kort sagt er den måde, som tabellerne fungerer sammen på, ændret, men tabeltilladelserne i kundeportalen er ikke ændret.</span><span class="sxs-lookup"><span data-stu-id="31c04-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="31c04-109">Dette emne forklarer, hvordan du opretter nye webroller, der kan arbejde med den nye avancerede datamodel.</span><span class="sxs-lookup"><span data-stu-id="31c04-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="31c04-110">Dette diagram viser tabelrelationen **uden** datamodellen for parten og det globale adressekartotek:</span><span class="sxs-lookup"><span data-stu-id="31c04-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![uden partmodel](media/without-party-model.PNG)

<span data-ttu-id="31c04-112">Dette diagram viser tabelrelationen **med** datamodellen for parten og det globale adressekartotek:</span><span class="sxs-lookup"><span data-stu-id="31c04-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![med partmodel](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="31c04-114">Oprette en ny tabeltilladelse</span><span class="sxs-lookup"><span data-stu-id="31c04-114">Create a new table permission</span></span>

<span data-ttu-id="31c04-115">Benyt følgende fremgangsmåde for at oprette disse nye tabeltilladelser:</span><span class="sxs-lookup"><span data-stu-id="31c04-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="31c04-116">Log på [Power Apps](https://make.powerapps.com), og gå til dine apps.</span><span class="sxs-lookup"><span data-stu-id="31c04-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="31c04-117">Vælg din portalstyringsapp.</span><span class="sxs-lookup"><span data-stu-id="31c04-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="31c04-118">Vælg **Sikkerhed > Tabelrettigheder** i sidepanelet.</span><span class="sxs-lookup"><span data-stu-id="31c04-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="31c04-119">Du skal oprette tre nye tilladelser:</span><span class="sxs-lookup"><span data-stu-id="31c04-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="31c04-120">Kontakt til part-forbindelse</span><span class="sxs-lookup"><span data-stu-id="31c04-120">Contact to Party connection</span></span>
    + <span data-ttu-id="31c04-121">Part til konto-forbindelse</span><span class="sxs-lookup"><span data-stu-id="31c04-121">Party to Account connection</span></span>
    + <span data-ttu-id="31c04-122">Konto til ordre-forbindelse</span><span class="sxs-lookup"><span data-stu-id="31c04-122">Account to Order connection</span></span>

4. <span data-ttu-id="31c04-123">Opret og gem en ny tilladelse for forbindelsen Kontakt til part ved at angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="31c04-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="31c04-124">**Navn**: Part til konto-forbindelse (eller dit valg)</span><span class="sxs-lookup"><span data-stu-id="31c04-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="31c04-125">**Tabelnavn**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="31c04-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="31c04-126">**Websted**: Kundeportal</span><span class="sxs-lookup"><span data-stu-id="31c04-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="31c04-127">**Område**: Kontakt</span><span class="sxs-lookup"><span data-stu-id="31c04-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="31c04-128">**Rettigheder**: Vælg alle</span><span class="sxs-lookup"><span data-stu-id="31c04-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="31c04-129">**Webroller**: Godkendte brugere, kunderepræsentant (eller dit valg)</span><span class="sxs-lookup"><span data-stu-id="31c04-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="31c04-130">Opret og gem en ny tilladelse for forbindelsen Part til konto ved at angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="31c04-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="31c04-131">**Navn**: Part til konto-forbindelse (eller dit valg)</span><span class="sxs-lookup"><span data-stu-id="31c04-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="31c04-132">**Tabelnavn**: konto</span><span class="sxs-lookup"><span data-stu-id="31c04-132">**Table Name**: account</span></span>
    + <span data-ttu-id="31c04-133">**Websted**: Kundeportal</span><span class="sxs-lookup"><span data-stu-id="31c04-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="31c04-134">**Område**: Overordnet</span><span class="sxs-lookup"><span data-stu-id="31c04-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="31c04-135">**Rettigheder**: Vælg alle</span><span class="sxs-lookup"><span data-stu-id="31c04-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="31c04-136">**Overordnet tabeltilladelse**: Kontakt til part-forbindelse</span><span class="sxs-lookup"><span data-stu-id="31c04-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="31c04-137">Opret og gem en ny tilladelse for forbindelsen Konto til ordre ved at angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="31c04-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="31c04-138">**Navn**: Konto til ordre-forbindelse (eller dit valg)</span><span class="sxs-lookup"><span data-stu-id="31c04-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="31c04-139">**Tabelnavn**: salgsordre</span><span class="sxs-lookup"><span data-stu-id="31c04-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="31c04-140">**Websted**: Kundeportal</span><span class="sxs-lookup"><span data-stu-id="31c04-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="31c04-141">**Område**: Overordnet</span><span class="sxs-lookup"><span data-stu-id="31c04-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="31c04-142">**Rettigheder**: Vælg alle</span><span class="sxs-lookup"><span data-stu-id="31c04-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="31c04-143">**Overordnet tabeltilladelse**: Part til konto-forbindelse</span><span class="sxs-lookup"><span data-stu-id="31c04-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
