---
title: Modtagelse af nummerplade via lagerstedsappen
description: I dette emne beskrives, hvordan du konfigurerer lagerstedsappen til at understøtte brug af en nummerplademodtagelsesproces for at modtage fysisk lager.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346370"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="1a2fd-103">Modtagelse af nummerplade via lagerstedsappen</span><span class="sxs-lookup"><span data-stu-id="1a2fd-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="1a2fd-104">I dette emne beskrives, hvordan du konfigurerer lagerstedsappen, så den understøtter brug af en nummerplademodtagelsesproces for at modtage fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="1a2fd-105">Du kan bruge denne funktion til hurtigt at registrere modtagelsen af det indgående lager, der er knyttet til en ASN (Advance Ship Notice).</span><span class="sxs-lookup"><span data-stu-id="1a2fd-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="1a2fd-106">Systemet opretter automatisk en ASN, når der bruges lokationsstyringsprocesser til at levere en flytteordre.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="1a2fd-107">I forbindelse med indkøbsordreprocessen kan en ASN registreres manuelt, eller den kan importeres automatisk ved hjælp af en indgående ASN-dataenhedsproces.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="1a2fd-108">ASN-dataene er knyttet til laster og forsendelser via *pakkestrukturerne*, hvor paller (overordnede nummerplader) kan indeholde kasser (indlejrede nummerplader).</span><span class="sxs-lookup"><span data-stu-id="1a2fd-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="1a2fd-109">Systemet registrerer den fysiske disponible lagerbeholdning på den overordnede nummerplade for at reducere antallet af lagertransaktioner, når der bruges pakkestrukturer med indlejrede nummerplader.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="1a2fd-110">Den mobile enhed skal angive et menupunkt, der er baseret på processerne til oprettelse af *Pak til indlejrede nummerplader*, for at udløse bevægelsen af den fysiske disponible lagerbeholdning fra den overordnede nummerplade til de indlejrede nummerplader baseret på pakkestrukturdataene.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="1a2fd-111">Få vist eller spring over siden til opsummering af modtagelse</span><span class="sxs-lookup"><span data-stu-id="1a2fd-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="1a2fd-112">Du kan bruge funktionen *Kontrolelementet til at få vist en side med status for modtagelse på mobilenheder* for at udnytte et mere detaljeret flow i lagerstedsappen som del af nummerplademodtagelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="1a2fd-113">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1a2fd-114">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="1a2fd-115">I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="1a2fd-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="1a2fd-116">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="1a2fd-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1a2fd-117">**Funktionsnavn:** *Bestem, om der skal vises en side med en oversigt på mobilenheder*</span><span class="sxs-lookup"><span data-stu-id="1a2fd-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="1a2fd-118">Når denne funktion er slået til, indeholder den mobile enhed menupunkter til modtagelse af nummerplader, og læg-på-lager, der viser indstillingen **Oversigtsside til visning af modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="1a2fd-119">Denne indstilling har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="1a2fd-119">This setting has the following options:</span></span>

- <span data-ttu-id="1a2fd-120">**Få vist en detaljeret oversigt** – når du modtager nummerplader, vil arbejderne få vist en ekstra side, der viser fuldstændige ASN-oplysninger.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="1a2fd-121">**Spring oversigt over** – Arbejdere kan ikke få vist de fuldstændige ASN-oplysninger.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="1a2fd-122">Lagermedarbejderne kan heller ikke angive en dispositionskode eller tilføje undtagelser under modtagelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="1a2fd-123">Undgå, at afsendte, ordreforsendte nummerplader bliver brugt i andre lagersteder end destinationslagerstedet</span><span class="sxs-lookup"><span data-stu-id="1a2fd-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="1a2fd-124">Der kan ikke bruges en proces til modtagelse af nummerplader, hvis en ASN indeholder et nummerplade-id, der allerede findes, og som har fysiske beholdningsdata på en anden lagerlokation end den lagerlokation, hvor der sker registrering af nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="1a2fd-125">I forbindelse med overflytningsordrescenarier, hvor forsendelseslagerstedet ikke sporer nummerplader (og derfor ikke sporer fysisk disponibel lagerbeholdning pr. nummerplade), kan du bruge metoden *Undgå afsendte, ordreforsendte nummerplader fra at blive brugt på andre lagersteder end destinationslagerstedet* for at forhindre fysisk disponible opdateringer af nummerplader, der er undervejs.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="1a2fd-126">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1a2fd-127">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="1a2fd-128">I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="1a2fd-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="1a2fd-129">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="1a2fd-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1a2fd-130">**Funktionsnavn:** *Undgå, at afsendte, ordreforsendte nummerplader fra at blive brugt i andre lagersteder end destinationslagerstedet*</span><span class="sxs-lookup"><span data-stu-id="1a2fd-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="1a2fd-131">Hvis du vil administrere funktionaliteten, når denne funktion er tilgængelig, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="1a2fd-132">Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="1a2fd-133">Under fanen **Generelt** i oversigtspanelet **Nummerplader** skal du angive feltet **Politik for transitlagersteds nummerplade** til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="1a2fd-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="1a2fd-134">**Tillad genbrug af nummerplade, der ikke er sporet** – Systemet fungerer på samme måde, som det fungerer, når *Undgå afsendelse af ordreafsendte nummerplader fra at blive brugt på andre lagersteder end destinationslagerstedet* ikke er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="1a2fd-135">Denne værdi er standardindstillingen, når du første gang aktiverer funktionen.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="1a2fd-136">**Undgå genbrug af ikke-sporet nummerplade** – Det er kun de disponible opdateringer, der er relateret til en leveret nummerplade, som tillades på destinationslagerstedet, indtil flytteordren er modtaget.</span><span class="sxs-lookup"><span data-stu-id="1a2fd-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="1a2fd-137">Flere oplysninger</span><span class="sxs-lookup"><span data-stu-id="1a2fd-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="1a2fd-138">Du kan få flere oplysninger om menupunkter på mobilenheder, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="1a2fd-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
