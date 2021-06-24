---
title: Brugersikkerhed på leverandørportal
description: Denne artikel beskriver, hvordan du konfigurerer sikkerhed for eksterne leverandører, der bruger leverandørportalen. Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2b95d386dd12bb1cb3577c3820b0be82d28df8e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188482"
---
# <a name="vendor-portal-user-security"></a><span data-ttu-id="edd88-104">Brugersikkerhed på leverandørportal</span><span class="sxs-lookup"><span data-stu-id="edd88-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edd88-105">Denne artikel beskriver, hvordan du konfigurerer sikkerhed for eksterne leverandører, der bruger leverandørportalen.</span><span class="sxs-lookup"><span data-stu-id="edd88-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="edd88-106">Oplysningerne i dette emne gælder kun for versioner af Dynamics AX fra februar 2016 og maj 2016.</span><span class="sxs-lookup"><span data-stu-id="edd88-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="edd88-107">Kreditorportal-funktionaliteten er blevet erstattet af udvidede kreditorsamarbejdsfunktioner i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="edd88-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="edd88-108">Du kan finde flere oplysninger om opsætning af sikkerhed for leverandørsamarbejde under [Konfigurere og vedligeholde kreditorsamarbejde](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="edd88-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="edd88-109">Kreditorportalen viser et begrænset sæt oplysninger om indkøbsordrer (PO'er) til eksterne kreditorer.</span><span class="sxs-lookup"><span data-stu-id="edd88-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="edd88-110">Det er vigtigt, at du har konfigureret brugertilladelserne for kreditorportalen i Microsoft Dynamics AX korrekt, så kreditorerne ikke utilsigtet har adgang til yderligere oplysninger i din Dynamics AX-installation.</span><span class="sxs-lookup"><span data-stu-id="edd88-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="edd88-111">**Vigtigt!** I modsætning til andre brugere bør eksterne kreditorer ikke have rollen **Systembruger**.</span><span class="sxs-lookup"><span data-stu-id="edd88-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="edd88-112">Rollen **Systembruger** giver adgang til et sæt rettigheder, der ikke er egnet til eksterne brugere.</span><span class="sxs-lookup"><span data-stu-id="edd88-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="edd88-113">Konfigurere en bruger til kreditorportalen</span><span class="sxs-lookup"><span data-stu-id="edd88-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="edd88-114">Før du opretter en brugerkonto til en person, der bruger kreditorportalen, skal du konfigurere kreditoren til at tillade samarbejde på kreditorportalen.</span><span class="sxs-lookup"><span data-stu-id="edd88-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="edd88-115">Brug feltet **Indkøbsordresamarbejde** under fanen **Generelt** på siden **Kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="edd88-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="edd88-116">Eksterne kreditorer, der bruger kreditorportalen, skal have følgende opsætning:</span><span class="sxs-lookup"><span data-stu-id="edd88-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="edd88-117">En brugerkonto i Microsoft Azure Active Directory (AAD) skal være registreret for kreditoren på siden **Brugere** i Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="edd88-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="edd88-118">Kreditoren skal have sikkerhedsrollen **Kreditor (ekstern)**, ikke rollen **Systembruger**.</span><span class="sxs-lookup"><span data-stu-id="edd88-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="edd88-119">**Bemærk!** Rollen **Systembruger** tildeles automatisk, når du opretter en ny brugerkonto i Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="edd88-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="edd88-120">Du skal derfor fjerne denne rolle og acceptere den advarselsmeddelelse, du modtager.</span><span class="sxs-lookup"><span data-stu-id="edd88-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="edd88-121">Kreditorbrugeren bør ikke gives tilladelse til at tilføje flere felter fra PO-tabellerne til deres PO-visning.</span><span class="sxs-lookup"><span data-stu-id="edd88-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="edd88-122">Under fanen **Brugertilpasning** skal du under fanen **Brugere** angive indstillingen **Eksplicit personlig tilpasning tilladt** for brugeren til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="edd88-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="edd88-123">Brugerkontoen skal være tilknyttet en kontakt, der er registreret.</span><span class="sxs-lookup"><span data-stu-id="edd88-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="edd88-124">Under fanen **Brugere** skal du vælge en kontakt i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="edd88-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="edd88-125">Den person, du vælger, skal have rollen **Kontakt** for den pågældende kreditor.</span><span class="sxs-lookup"><span data-stu-id="edd88-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="edd88-126">Hvis den samme person skal have adgang til kreditorportalen for flere kreditorkonti (måske for forskellige juridiske enheder), skal hver af den pågældende persons brugerkonti være knyttet til den samme registrerede kontakt.</span><span class="sxs-lookup"><span data-stu-id="edd88-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="edd88-127">Rollen **Kreditor (ekstern)** omfatter alle de grundlæggende funktioner, der er nødvendige for at kunne bruge de funktioner, der findes på kreditorportalen.</span><span class="sxs-lookup"><span data-stu-id="edd88-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="edd88-128">Denne opsætning sikrer, at den brugergrænseflade, som den eksterne bruger ser, kun er fokuseret på det ønskede scenarie.</span><span class="sxs-lookup"><span data-stu-id="edd88-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edd88-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="edd88-129">Additional resources</span></span>

[<span data-ttu-id="edd88-130">Samarbejde med kreditorer ved hjælp af kreditorportalen</span><span class="sxs-lookup"><span data-stu-id="edd88-130">Collaborate with vendors by using the Vendor portal</span></span>](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]