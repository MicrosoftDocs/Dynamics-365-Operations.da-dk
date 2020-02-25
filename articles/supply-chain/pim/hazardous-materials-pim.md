---
title: Farlige materialer
description: Dette emne indeholder oplysninger om dokumenter og oplysninger om farligt materiale, der er gemt i dit miljø.
author: lachlancashMS
manager: AnnBe
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
ms.openlocfilehash: 76dd6539e39bb77c546e613b290fc5decba9457f
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982302"
---
# <a name="hazardous-materials"></a><span data-ttu-id="49229-103">Farlige materialer</span><span class="sxs-lookup"><span data-stu-id="49229-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49229-104">Oplysninger om farligt materiale konfigureres i Administration af produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="49229-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="49229-105">Dette modul har desuden også dokumenter, der kan udskrives via lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="49229-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="49229-106">Når du sender materialer, der klassificeres som farligt gods, kræves der flere papirer, der skal følge forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="49229-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="49229-107">Funktionen til farlige materialer giver kunder mulighed for at lagre klassifikationsoplysninger og knytte dem til frigivelse af varer.</span><span class="sxs-lookup"><span data-stu-id="49229-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="49229-108">Disse oplysninger kan derefter bruges til at udarbejde forsendelsesdokumentation.</span><span class="sxs-lookup"><span data-stu-id="49229-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49229-109">Som en hjælp til at administrere forsendelser af farligt gods kan du med Microsoft Dynamics 365 Supply Chain Management konfigurere yderligere referenceoplysninger, der er relateret til produkter.</span><span class="sxs-lookup"><span data-stu-id="49229-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="49229-110">Du kan også oprette flere forsendelsesdokumenter.</span><span class="sxs-lookup"><span data-stu-id="49229-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="49229-111">Systemet er dog ikke automatisk kompatibelt med regler og bestemmelser i dit land eller område.</span><span class="sxs-lookup"><span data-stu-id="49229-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="49229-112">Det er i stedet et værktøj, der kan hjælpe det overordnede program.</span><span class="sxs-lookup"><span data-stu-id="49229-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="49229-113">Før du kan bruge denne funktion, kræves følgende opsætning:</span><span class="sxs-lookup"><span data-stu-id="49229-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="49229-114">**Administration af produktoplysninger**: Konfigurer koder, der kan anvendes til frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="49229-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="49229-115">**Lokationsstyring**: Brug flere forsendelsesdokumenter til at udskrive forsendelsesoplysninger.</span><span class="sxs-lookup"><span data-stu-id="49229-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="49229-116">Administration af produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="49229-116">Product information management</span></span>

<span data-ttu-id="49229-117">I Administration af produktoplysninger findes der et interval af opsætningstabeller, hvor du kan tilføje referenceoplysninger, der findes på listen over farligt gods til vej-, luft-og søtransport.</span><span class="sxs-lookup"><span data-stu-id="49229-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="49229-118">Her er nogle af de bestemmelser, der ofte refereres til:</span><span class="sxs-lookup"><span data-stu-id="49229-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="49229-119">**ADR** – bestemmelser, der er relateret til international transport af farligt gods ad vej</span><span class="sxs-lookup"><span data-stu-id="49229-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="49229-120">**CFR 49** – bestemmelser i USA om transport af farligt gods</span><span class="sxs-lookup"><span data-stu-id="49229-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="49229-121">**IMDG** – den internationale kode for Marine Dangerous Goods (IMDG)</span><span class="sxs-lookup"><span data-stu-id="49229-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="49229-122">**IATA** – bestemmelser i den Internationale Luftfartssammenslutning (IATA) om farligt gods</span><span class="sxs-lookup"><span data-stu-id="49229-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="49229-123">Alle disse bestemmelser har en liste over farligt gods med referencekoder.</span><span class="sxs-lookup"><span data-stu-id="49229-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="49229-124">Listerne for hver transporttype kombineres i delte internationale klassifikationer.</span><span class="sxs-lookup"><span data-stu-id="49229-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="49229-125">Supply Chain Management indeholder en referencetabel for de delte koder på disse lister.</span><span class="sxs-lookup"><span data-stu-id="49229-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="49229-126">Hver liste indeholder også nogle entydige koder, der kan defineres.</span><span class="sxs-lookup"><span data-stu-id="49229-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="49229-127">Hvis du vil konfigurere disse oplysninger, skal du oprette en bestemmelse, som du kan bruge til at konfigurere de første parametre.</span><span class="sxs-lookup"><span data-stu-id="49229-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="49229-128">Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="49229-128">Warehouse management</span></span>

<span data-ttu-id="49229-129">Når en forsendelse udarbejdes, kan der udskrives flere nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="49229-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="49229-130">Disse rapporter bruger de oplysninger, du har angivet i Administration af produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="49229-130">These reports use the information that you set up in Product information management.</span></span>
