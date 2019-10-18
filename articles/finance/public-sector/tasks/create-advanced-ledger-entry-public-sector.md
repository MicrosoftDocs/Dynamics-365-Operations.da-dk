---
title: Oprette en avanceret finanspost i den offentlige sektor
description: Organisationer i den offentlige sektor kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AdvancedLedgerEntry, AdvancedLedgerEntryCreate, ProjTableLookup, ProjCategoryLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500cb3e1a6a6014b335ec3275675e1e9eb8a0dd4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183501"
---
# <a name="create-an-advanced-ledger-entry-in-the-public-sector"></a><span data-ttu-id="15966-103">Oprette en avanceret finanspost i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="15966-103">Create an advanced ledger entry in the public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15966-104">Organisationer i den offentlige sektor kan bruge avancerede finansposter til at oprette, tilpasse og tilbageføre finansposter.</span><span class="sxs-lookup"><span data-stu-id="15966-104">Public-sector organizations can use advanced ledger entries to create, adjust, and reverse ledger entries.</span></span> <span data-ttu-id="15966-105">For eksempel kan avancerede finansposter bruges til at ompostere udgifter, hvis fakturaer fejlagtigt er blevet bogført til den forkerte konto eller det forkerte projekt.</span><span class="sxs-lookup"><span data-stu-id="15966-105">For example, advanced ledger entries can be used to reclassify expenditures if invoices are mistakenly posted to the wrong account or project.</span></span> <span data-ttu-id="15966-106">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="15966-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="15966-107">Gå til Finans > Kladdeposteringer > Avancerede finansposter.</span><span class="sxs-lookup"><span data-stu-id="15966-107">Go to General ledger > Journal entries > Advanced ledger entries.</span></span>
2. <span data-ttu-id="15966-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="15966-108">Click New.</span></span>
3. <span data-ttu-id="15966-109">Angiv en dato i datofeltet Regnskab.</span><span class="sxs-lookup"><span data-stu-id="15966-109">In the Accounting date field, enter a date.</span></span>
4. <span data-ttu-id="15966-110">Klik på rullelisten i feltet Posteringstekst for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15966-110">In the Transaction text field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="15966-111">På listen skal du klikke på posteringsteksten for denne avancerede finanspost.</span><span class="sxs-lookup"><span data-stu-id="15966-111">In the list, click the transaction text for this advanced ledger entry.</span></span>
6. <span data-ttu-id="15966-112">Klik på rullelisten i feltet Bogføringsdefinition for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15966-112">In the Posting definition field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="15966-113">På listen skal du klikke på Bogføringsdefinition for denne avancerede finanspost.</span><span class="sxs-lookup"><span data-stu-id="15966-113">In the list, click the Posting definition for this advanced ledger entry.</span></span>
8. <span data-ttu-id="15966-114">Klik på rullelisten i feltet Årsagskode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15966-114">In the Reason code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="15966-115">På listen skal du klikke på Årsagskode for denne avancerede finanspost.</span><span class="sxs-lookup"><span data-stu-id="15966-115">In the list, click the Reason code for this advanced ledger entry.</span></span>
10. <span data-ttu-id="15966-116">Skriv en værdi i feltet Årsagskommentar.</span><span class="sxs-lookup"><span data-stu-id="15966-116">In the Reason comment field, type a value.</span></span>
11. <span data-ttu-id="15966-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="15966-117">Click OK.</span></span>
12. <span data-ttu-id="15966-118">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="15966-118">Click Add line.</span></span>
13. <span data-ttu-id="15966-119">Klik på rullelisten i feltet Projekt-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15966-119">In the Project ID field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="15966-120">Klik på et projekt-id på listen.</span><span class="sxs-lookup"><span data-stu-id="15966-120">In the list, click a project ID.</span></span>
15. <span data-ttu-id="15966-121">Klik på rullelisten i feltet Projektkategori for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="15966-121">In the Project category field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="15966-122">Klik på en projektkategori på listen.</span><span class="sxs-lookup"><span data-stu-id="15966-122">In the list, click a project category.</span></span>
    * <span data-ttu-id="15966-123">Hvis du vælger projektkategorien, angives finanskontoen automatisk.</span><span class="sxs-lookup"><span data-stu-id="15966-123">If you select the project category, the ledger account is entered automatically.</span></span>  
    * <span data-ttu-id="15966-124">Føj et debetbeløb eller kreditbeløb til linjen.</span><span class="sxs-lookup"><span data-stu-id="15966-124">Add a debit or a credit amount to this line.</span></span> <span data-ttu-id="15966-125">Hvis det er nødvendigt, skal du klikke på Tilføj linje for at tilføje flere linjer.</span><span class="sxs-lookup"><span data-stu-id="15966-125">If needed, click Add line to add more lines.</span></span>  
17. <span data-ttu-id="15966-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="15966-126">Click Save.</span></span>

