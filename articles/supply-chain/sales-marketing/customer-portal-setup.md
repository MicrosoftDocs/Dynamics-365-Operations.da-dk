---
title: Installere, konfigurere og opdatere kundeportalen
description: Dette emne indeholder licensoplysninger og opsætningsinstruktioner til kundeportalen.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977732"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="1bc89-103">Installere, konfigurere og opdatere kundeportalen</span><span class="sxs-lookup"><span data-stu-id="1bc89-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="1bc89-104">Licenskrav</span><span class="sxs-lookup"><span data-stu-id="1bc89-104">Licensing requirements</span></span>

<span data-ttu-id="1bc89-105">Hvis du vil implementere kundeportalen, skal du have følgende licenser:</span><span class="sxs-lookup"><span data-stu-id="1bc89-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="1bc89-106">**Power Apps-portaler** – Denne licens kræves for at være vært for kundeportalen.</span><span class="sxs-lookup"><span data-stu-id="1bc89-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="1bc89-107">Portaler gives i licens baseret på brug.</span><span class="sxs-lookup"><span data-stu-id="1bc89-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="1bc89-108">Du kan finde flere oplysninger i [Licenskrav til Power Apps-portaler](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="1bc89-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="1bc89-109">**Dobbeltskrivning** – Du skal have de nødvendige licenser for at kunne aktivere dobbeltskrivning til Supply Chain Management-tabeller.</span><span class="sxs-lookup"><span data-stu-id="1bc89-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="1bc89-110">Du kan finde flere oplysninger under [Systemkrav til dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="1bc89-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="1bc89-111">Afhængigheder af dobbeltskrivning og Power Apps-portaler</span><span class="sxs-lookup"><span data-stu-id="1bc89-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="1bc89-112">Kundeportalen er afhængig af Power Apps-portaler og dobbeltskrivning som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="1bc89-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="1bc89-113">![Kundeportalafhængigheder](media/customer-portal-elements.png "Kundeportalafhængigheder")</span><span class="sxs-lookup"><span data-stu-id="1bc89-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="1bc89-114">I modsætning til andre funktioner i Supply Chain Management findes kundeportalskabelonen i Power Apps-portaler.</span><span class="sxs-lookup"><span data-stu-id="1bc89-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="1bc89-115">Derfor er kundeportalen begrænset af den funktionalitet og de funktioner, der leveres af Power Apps-portal og tabeller i dobbelskrivning.</span><span class="sxs-lookup"><span data-stu-id="1bc89-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="1bc89-116">Krævet opsætning for at aktivere kundeportalen</span><span class="sxs-lookup"><span data-stu-id="1bc89-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="1bc89-117">Når du har fundet ud af, om du har de påkrævede licenser, kan du konfigurere dobbeltskrivning som beskrevet i [Instruktioner for indledende synkronisering af dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="1bc89-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="1bc89-118">Sørg for at aktivere følgende tabeltilknytninger i dobbeltskrivning:</span><span class="sxs-lookup"><span data-stu-id="1bc89-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="1bc89-119">Salgsordreoverskrift</span><span class="sxs-lookup"><span data-stu-id="1bc89-119">Sales Order Header</span></span>
- <span data-ttu-id="1bc89-120">Salgsordredetaljer</span><span class="sxs-lookup"><span data-stu-id="1bc89-120">Sales Order Details</span></span>
- <span data-ttu-id="1bc89-121">Konti</span><span class="sxs-lookup"><span data-stu-id="1bc89-121">Accounts</span></span>
- <span data-ttu-id="1bc89-122">Kontakter</span><span class="sxs-lookup"><span data-stu-id="1bc89-122">Contacts</span></span>
- <span data-ttu-id="1bc89-123">Produkter</span><span class="sxs-lookup"><span data-stu-id="1bc89-123">Products</span></span>

<span data-ttu-id="1bc89-124">Når denne konfiguration er fuldført, kan du klargøre kundeportalskabelonen.</span><span class="sxs-lookup"><span data-stu-id="1bc89-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="1bc89-125">Klargøring af kundeportalen</span><span class="sxs-lookup"><span data-stu-id="1bc89-125">Provision the Customer portal</span></span>

<span data-ttu-id="1bc89-126">Før du går i gang, skal du sikre dig, at du allerede har fuldført den [krævede opsætning](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="1bc89-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="1bc89-127">Udfør derefter følgende trin for at klargøre kundeportalen.</span><span class="sxs-lookup"><span data-stu-id="1bc89-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="1bc89-128">Gå til [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="1bc89-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="1bc89-129">Sørg for at bruge det miljø, hvor du aktiverede dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="1bc89-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="1bc89-130">Under fanen **Opret** skal du rulle ned til sektionen **Start fra skabelon** og vælge den skabelon, der har navnet **Kundeportal**.</span><span class="sxs-lookup"><span data-stu-id="1bc89-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="1bc89-131">Følg vejledningen på skærmen.</span><span class="sxs-lookup"><span data-stu-id="1bc89-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="1bc89-132">Når klargøring er fuldført, kan du få adgang til kundeportalen i sektionen **Dine apps** på **Startsiden**.</span><span class="sxs-lookup"><span data-stu-id="1bc89-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="1bc89-133">Hvis dobbeltskrivningsløsningen ikke er installeret i det miljø, du arbejder i, får du vist en fejlmeddelelse, og kundeportalen vil ikke være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="1bc89-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="1bc89-134">Opdatering af kundeportalen</span><span class="sxs-lookup"><span data-stu-id="1bc89-134">Update the Customer portal</span></span>

<span data-ttu-id="1bc89-135">Der kan blive føjet flere funktioner til kundeportalen senere.</span><span class="sxs-lookup"><span data-stu-id="1bc89-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="1bc89-136">Eventuelle ændringer, som Microsoft foretager af de underliggende løsningskomponenter, vises automatisk i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="1bc89-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="1bc89-137">Det websted, der er klargjort i dit miljø, afspejler dog ikke automatisk ændringer, der er foretaget i konfigurationsdataene.</span><span class="sxs-lookup"><span data-stu-id="1bc89-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="1bc89-138">Du skal anvende disse ændringer manuelt ved at hente koden fra den nye skabelon og flette den med det klargjorte websted.</span><span class="sxs-lookup"><span data-stu-id="1bc89-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bc89-139">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1bc89-139">Additional resources</span></span>

<span data-ttu-id="1bc89-140">Hvis du vil vide, hvordan du kan konfigurere og tilpasse kundeportalen, skal du starte med at gennemgå følgende dokumentation for de underliggende teknologier:</span><span class="sxs-lookup"><span data-stu-id="1bc89-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="1bc89-141">Power Apps-dokumentationen til portaler</span><span class="sxs-lookup"><span data-stu-id="1bc89-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="1bc89-142">Dokumentationen til dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="1bc89-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="1bc89-143">For at kunne styre dine portaler effektivt skal du forstå Power Apps-portalerne og Microsoft Dataverse-livscyklus.</span><span class="sxs-lookup"><span data-stu-id="1bc89-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="1bc89-144">Du kan finde flere oplysninger i følgende ressourcer:</span><span class="sxs-lookup"><span data-stu-id="1bc89-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="1bc89-145">Om portalens livscyklus</span><span class="sxs-lookup"><span data-stu-id="1bc89-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="1bc89-146">Opgradering af en portal</span><span class="sxs-lookup"><span data-stu-id="1bc89-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="1bc89-147">Overflytning af portalkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1bc89-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="1bc89-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement-apps</span><span class="sxs-lookup"><span data-stu-id="1bc89-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
