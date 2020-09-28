---
title: Farlige materialer
description: Dette emne indeholder oplysninger om dokumenter og oplysninger om farligt materiale, der er gemt i dit miljø.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 54e5dca38b31c9310d44bdda5f5af14ca1515541
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802695"
---
# <a name="hazardous-materials"></a><span data-ttu-id="cecfe-103">Farlige materialer</span><span class="sxs-lookup"><span data-stu-id="cecfe-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cecfe-104">Oplysninger om farligt materiale konfigureres i Administration af produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="cecfe-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="cecfe-105">Dette modul har desuden også dokumenter, der kan udskrives via lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="cecfe-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="cecfe-106">Når du sender materialer, der klassificeres som farligt gods, kræves der flere papirer, der skal følge forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="cecfe-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="cecfe-107">Funktionen til farlige materialer giver kunder mulighed for at lagre klassifikationsoplysninger og knytte dem til frigivelse af varer.</span><span class="sxs-lookup"><span data-stu-id="cecfe-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="cecfe-108">Disse oplysninger kan derefter bruges til at udarbejde forsendelsesdokumentation.</span><span class="sxs-lookup"><span data-stu-id="cecfe-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cecfe-109">Funktionerne for farlige materialer i Microsoft Dynamics 365 Supply Chain Management giver en samling nyttige produktoplysningsfelter og tilhørende funktioner, der kan hjælpe dig med at registrere og henvise til oplysninger, der er relateret til de farlige produkter.</span><span class="sxs-lookup"><span data-stu-id="cecfe-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="cecfe-110">Disse funktioner kan også være en hjælp til at designe og udskrive forsendelsesdokumenter, der indeholder nogle af de samme oplysninger om alle former for farligt materiale, som du skal levere.</span><span class="sxs-lookup"><span data-stu-id="cecfe-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="cecfe-111">Systemet er dog ikke automatisk kompatibelt med alle gældende regler og bestemmelser i dit land eller område.</span><span class="sxs-lookup"><span data-stu-id="cecfe-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="cecfe-112">Selvom disse værktøjer er beregnet til at hjælpe dig med at overholde de fælles regler, er de hverken tilstrækkelige i sig selv eller garanteret for at være det.</span><span class="sxs-lookup"><span data-stu-id="cecfe-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="cecfe-113">Din organisation er ansvarlig for at være opmærksom på alle gældende regler og skal træffe alle nødvendige foranstaltninger for at overholde dem.</span><span class="sxs-lookup"><span data-stu-id="cecfe-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="cecfe-114">Før du kan bruge denne funktion, kræves følgende opsætning:</span><span class="sxs-lookup"><span data-stu-id="cecfe-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="cecfe-115">**Administration af produktoplysninger**: Konfigurer koder, der kan anvendes til frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="cecfe-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="cecfe-116">**Lokationsstyring**: Brug flere forsendelsesdokumenter til at udskrive forsendelsesoplysninger.</span><span class="sxs-lookup"><span data-stu-id="cecfe-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="cecfe-117">Administration af produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="cecfe-117">Product information management</span></span>

<span data-ttu-id="cecfe-118">I Administration af produktoplysninger findes der et interval af opsætningstabeller, hvor du kan tilføje referenceoplysninger, der findes på listen over farligt gods til vej-, luft-og søtransport.</span><span class="sxs-lookup"><span data-stu-id="cecfe-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="cecfe-119">Her er nogle af de bestemmelser, der ofte refereres til:</span><span class="sxs-lookup"><span data-stu-id="cecfe-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="cecfe-120">**ADR** – bestemmelser, der er relateret til international transport af farligt gods ad vej</span><span class="sxs-lookup"><span data-stu-id="cecfe-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="cecfe-121">**CFR 49** – bestemmelser i USA om transport af farligt gods</span><span class="sxs-lookup"><span data-stu-id="cecfe-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="cecfe-122">**IMDG** – den internationale kode for Marine Dangerous Goods (IMDG)</span><span class="sxs-lookup"><span data-stu-id="cecfe-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="cecfe-123">**IATA** – bestemmelser i den Internationale Luftfartssammenslutning (IATA) om farligt gods</span><span class="sxs-lookup"><span data-stu-id="cecfe-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="cecfe-124">Alle disse bestemmelser har en liste over farligt gods med referencekoder.</span><span class="sxs-lookup"><span data-stu-id="cecfe-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="cecfe-125">Listerne for hver transporttype kombineres i delte internationale klassifikationer.</span><span class="sxs-lookup"><span data-stu-id="cecfe-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="cecfe-126">Supply Chain Management indeholder en referencetabel for de delte koder på disse lister.</span><span class="sxs-lookup"><span data-stu-id="cecfe-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="cecfe-127">Hver liste indeholder også nogle entydige koder, der kan defineres.</span><span class="sxs-lookup"><span data-stu-id="cecfe-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="cecfe-128">Hvis du vil konfigurere disse oplysninger, skal du oprette en bestemmelse, som du kan bruge til at konfigurere de første parametre.</span><span class="sxs-lookup"><span data-stu-id="cecfe-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="cecfe-129">Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="cecfe-129">Warehouse management</span></span>

<span data-ttu-id="cecfe-130">Når en forsendelse udarbejdes, kan der udskrives flere nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="cecfe-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="cecfe-131">Disse rapporter bruger de oplysninger, du har angivet i Administration af produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="cecfe-131">These reports use the information that you set up in Product information management.</span></span>
