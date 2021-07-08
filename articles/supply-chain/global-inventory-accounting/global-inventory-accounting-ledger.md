---
title: Global Inventory Accounting-finansmodul
description: I dette emne beskrives Global Inventory Accounting-finansmodulet, som defineres af en kombination af en valuta, en kalender, et princip og en tilknytning til en juridisk enhed.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273130"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="308b0-103">Global Inventory Accounting-finansmodul</span><span class="sxs-lookup"><span data-stu-id="308b0-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="308b0-104">Global Inventory Accounting har sit eget sæt finansmoduler.</span><span class="sxs-lookup"><span data-stu-id="308b0-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="308b0-105">Hver gang en lagerrelateret postering behandles for en relevant juridisk enhed, kan systemet tage højde for denne postering i et vilkårligt antal Global Inventory Accounting-finansmoduler efter behov.</span><span class="sxs-lookup"><span data-stu-id="308b0-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="308b0-106">Et finansmodul er et register over debet- og kreditposter.</span><span class="sxs-lookup"><span data-stu-id="308b0-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="308b0-107">Disse poster klassificeres ved hjælp af omkostningselementer og reskontrokonti.</span><span class="sxs-lookup"><span data-stu-id="308b0-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="308b0-108">Et Global Inventory Accounting-finansmodul defineres af kombinationen af en valuta, en kalender, et princip og en tilknytning til en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="308b0-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="308b0-109">Hvis du vil oprette Global Inventory Accounting-finansmoduler, skal du gå til **Global Inventory Accounting \> Konfiguration \> Global Inventory Accounting-finansmoduler**.</span><span class="sxs-lookup"><span data-stu-id="308b0-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="308b0-110">For hvert finansmodul skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="308b0-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="308b0-111">**Navn** – Angiv navnet på finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="308b0-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="308b0-112">**Beskrivelse** – Indtast en beskrivelse af finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="308b0-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="308b0-113">**Regnskabskalender** – Angiv regnskabskalenderen til finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="308b0-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="308b0-114">**Valuta og valutakurstype** – Brug felterne i dette oversigtspanel til at vælge den regnskabsvaluta, som finansmodulet bruger, og valutakurstypen.</span><span class="sxs-lookup"><span data-stu-id="308b0-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="308b0-115">Den valuta, du vælger, kan være forskellig fra den valuta, som den juridiske enhed bruger.</span><span class="sxs-lookup"><span data-stu-id="308b0-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="308b0-116">I Global Inventory Accounting kan brugerne definere så mange finansmoduler til efterkalkulation, de har brug for.</span><span class="sxs-lookup"><span data-stu-id="308b0-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="308b0-117">Global Inventory Accounting understøtter lagerregnskab i flere valutaer og i flere vurderinger.</span><span class="sxs-lookup"><span data-stu-id="308b0-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="308b0-118">Angiv følgende felter:</span><span class="sxs-lookup"><span data-stu-id="308b0-118">Set the following fields:</span></span>

    - <span data-ttu-id="308b0-119">**Valuta** – Vælg den efterkalkulationsvaluta, som lagerrelaterede værdier vedligeholdes i.</span><span class="sxs-lookup"><span data-stu-id="308b0-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="308b0-120">Disse værdier omfatter lagerværdi, vareforbrug, lager under transport og alle variationer heraf.</span><span class="sxs-lookup"><span data-stu-id="308b0-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="308b0-121">**Valutakurstype** – Vælg den valutakurs, som systemet skal bruge til at omregne posteringsbeløbet i transaktionsvalutaen og standardomkostningerne for varerne til efterkalkulationsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="308b0-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="308b0-122">**Navn på princip** – Angiv et princip.</span><span class="sxs-lookup"><span data-stu-id="308b0-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="308b0-123">En princip er en samling politikker, der fastlægger, hvordan omkostninger skal bogføres i dette finansmodul.</span><span class="sxs-lookup"><span data-stu-id="308b0-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="308b0-124">**Juridisk enhed** – Finansmodulet posterer de dokumenter, der er bogført på den valgte juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="308b0-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="308b0-125">**Optimering** – Vælg, om lagerposteringer, der blev oprettet før finansmodulet blev oprettet, skal behandles i henhold til valutaen og princippet i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="308b0-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="308b0-126">Vælg en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="308b0-126">Select one of the following values:</span></span>

    - <span data-ttu-id="308b0-127">**Aktiveret** – Finansmodulet skal behandle de posteringer, der blev oprettet, før finansmodulet blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="308b0-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="308b0-128">**Deaktiveret** – Finansmodulet skal kun behandle de posteringer, der er oprettet, efter finansmodulet blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="308b0-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="308b0-129">Du kan **ikke** vende tilbage og angive dette felt, når du har indtastet nye dokumenter.</span><span class="sxs-lookup"><span data-stu-id="308b0-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="308b0-130">**Status** – Status angives automatisk til *Forbered* for nyoprettede finansposter.</span><span class="sxs-lookup"><span data-stu-id="308b0-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
