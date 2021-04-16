---
title: Oversigt over farligt materiale
description: Dette emne indeholder en oversigt over funktioner, der vedrører håndtering og dokumentation af farligt materiale under administration af produktoplysninger og lokationsstyring.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 15edf61cba03a57b9b4d2c939228fd064b797942
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829372"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="f6454-103">Oversigt over farligt materiale</span><span class="sxs-lookup"><span data-stu-id="f6454-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6454-104">For at overholde angivne standarder og transportreglementer skal organisationer, der leverer materialer, der er klassificeret som farligt gods, medsende ekstra papirarbejde med forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="f6454-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="f6454-105">Med funktionen til farlige materialer kan kunder lagre oplysninger, der er relateret til frigivne varer.</span><span class="sxs-lookup"><span data-stu-id="f6454-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="f6454-106">Disse oplysninger kan derefter bruges til at udarbejde forsendelsesdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f6454-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="f6454-107">En organisation, der leverer farligt gods, skal have sine egne processer og procedurer til administration af leveringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f6454-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="f6454-108">Microsoft Dynamics 365 Supply Chain Management er blot et værktøj, der kan hjælpe dig med at oprette de nødvendige dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f6454-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="f6454-109">I følgende diagram illustreres de trin, der er nødvendige for at konfigurere og bruge funktionen for farlige materialer.</span><span class="sxs-lookup"><span data-stu-id="f6454-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="f6454-110">![Opsætning og brug af funktionen for farligt materiale](media/hazmat-overview.png "Opsætning og brug af funktionen for farligt materiale")</span><span class="sxs-lookup"><span data-stu-id="f6454-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="f6454-111">Funktionen for farlige materialer konfigureres i administration af produktoplysninger og indeholder dokumenter, der kan udskrives via Lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="f6454-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="f6454-112">Disse områder er derfor generelt de to hovedområder, hvor du kan gennemse, konfigurere og bruge denne funktionalitet:</span><span class="sxs-lookup"><span data-stu-id="f6454-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="f6454-113">**Administration af produktoplysninger** – Konfigurer de koder, der anvendes til frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="f6454-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="f6454-114">**Lokationsstyring** – Brug yderligere forsendelsesdokumenter, der udskrives til forsendelser.</span><span class="sxs-lookup"><span data-stu-id="f6454-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6454-115">Funktionerne for farlige materialer i Supply Chain Management giver en samling nyttige produktoplysningsfelter og tilhørende funktioner, der kan hjælpe dig med at registrere og henvise til oplysninger, der er relateret til de farlige produkter.</span><span class="sxs-lookup"><span data-stu-id="f6454-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="f6454-116">Disse funktioner kan også være en hjælp til at designe og udskrive forsendelsesdokumenter, der indeholder nogle af de samme oplysninger om alle former for farligt materiale, som du skal levere.</span><span class="sxs-lookup"><span data-stu-id="f6454-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="f6454-117">Systemet er dog ikke automatisk kompatibelt med alle gældende regler og bestemmelser i dit land eller område.</span><span class="sxs-lookup"><span data-stu-id="f6454-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="f6454-118">Selvom disse værktøjer er beregnet til at hjælpe dig med at overholde de fælles regler, er de hverken tilstrækkelige i sig selv eller garanteret for at være det.</span><span class="sxs-lookup"><span data-stu-id="f6454-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="f6454-119">Din organisation er ansvarlig for at være opmærksom på alle gældende regler og skal træffe alle nødvendige foranstaltninger for at overholde dem.</span><span class="sxs-lookup"><span data-stu-id="f6454-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="f6454-120">Administration af produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="f6454-120">Product information management</span></span>

<span data-ttu-id="f6454-121">I Administration af produktoplysninger findes en række opsætningstabeller, hvor du kan angive referenceoplysninger til listen over farligt gods til vej-, luft-og søtransport.</span><span class="sxs-lookup"><span data-stu-id="f6454-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="f6454-122">Der refereredes til følgende almindelige forordninger, da denne funktion blev udviklet:</span><span class="sxs-lookup"><span data-stu-id="f6454-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="f6454-123">**ADR** – bestemmelser, der er relateret til international transport af farligt gods ad vej</span><span class="sxs-lookup"><span data-stu-id="f6454-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="f6454-124">**CFR 49** – bestemmelser i USA om transport af farligt gods</span><span class="sxs-lookup"><span data-stu-id="f6454-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="f6454-125">**IMDG** – den internationale kode for Marine Dangerous Goods (IMDG)</span><span class="sxs-lookup"><span data-stu-id="f6454-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="f6454-126">**IATA** – bestemmelser i den Internationale Luftfartssammenslutning (IATA) om farligt gods</span><span class="sxs-lookup"><span data-stu-id="f6454-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="f6454-127">Hvert sæt regler indeholder standardiserede lister over farligt gods og referencekoder.</span><span class="sxs-lookup"><span data-stu-id="f6454-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="f6454-128">Supply Chain Management indeholder derfor en referencetabel for de almindelige koder på disse lister.</span><span class="sxs-lookup"><span data-stu-id="f6454-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="f6454-129">Hver liste indeholder også nogle entydige koder, du kan definere.</span><span class="sxs-lookup"><span data-stu-id="f6454-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="f6454-130">Du kan finde flere oplysninger om, hvordan du konfigurerer regler og værdier for farligt materiale, og hvordan du tildeler værdierne på relevante produkter, i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="f6454-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="f6454-131">Konfigurere farlige materialer</span><span class="sxs-lookup"><span data-stu-id="f6454-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="f6454-132">Farlige materialer i produkter, ordrer, forsendelser og laster</span><span class="sxs-lookup"><span data-stu-id="f6454-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="f6454-133">Lagerstedsstyring</span><span class="sxs-lookup"><span data-stu-id="f6454-133">Warehouse management</span></span>

<span data-ttu-id="f6454-134">Når du forbereder en forsendelse i Lokationsstyring, kan du udskrive flere nye rapporter, der bruger de oplysninger, du har angivet i administration af produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="f6454-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="f6454-135">Yderligere oplysninger om de tilgængelige rapporter og om, hvordan du bruger dem, finder du i [Forespørgsler og rapporter om farligt materiale](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f6454-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]