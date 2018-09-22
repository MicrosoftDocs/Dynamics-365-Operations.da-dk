---
title: Listesiden Kreditortransaktion
description: Dette emne indeholder oplysninger om listesiden Kreditortransaktion til Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: da-dk
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a><span data-ttu-id="1b63d-103">Listesiden Kreditortransaktion</span><span class="sxs-lookup"><span data-stu-id="1b63d-103">Vendor transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="1b63d-104">Vis udligninger</span><span class="sxs-lookup"><span data-stu-id="1b63d-104">View settlements</span></span>

<span data-ttu-id="1b63d-105">Fanen **Vis udligninger** i handlingsruden giver hurtig adgang til udligningshistorikken og yderligere oplysninger om hele udligningsposteringen.</span><span class="sxs-lookup"><span data-stu-id="1b63d-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="1b63d-106">Du kan også vise ekstra posteringer, der vedrører den valgte postering, enten fordi de var en del af samme udligning, eller fordi de er betalinger, der er oprettet i samme betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="1b63d-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="1b63d-107">Vælg **Kreditor \> Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="1b63d-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="1b63d-108">Vælg en kreditor med posteringer, og vælg derefter **Kreditor \> Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="1b63d-108">Select a vendor that has transactions, and then select **Vendor \> Transactions**.</span></span>
3. <span data-ttu-id="1b63d-109">Vælg en postering, der skal undersøges.</span><span class="sxs-lookup"><span data-stu-id="1b63d-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="1b63d-110">Vælg fanen **Vis udligninger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1b63d-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="1b63d-111">Dialogboksen **Vis udligninger** åbnes og viser den valgte postering og alle dokumenter, der er udlignet mod den.</span><span class="sxs-lookup"><span data-stu-id="1b63d-111">The **View settlements** dialog box opens and shows the selected transaction and all documents that are settled against it.</span></span> <span data-ttu-id="1b63d-112">Denne dialogboks ligner udligningshistorikvisningen, men den omfatter alle relaterede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="1b63d-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

5. <span data-ttu-id="1b63d-113">Du kan udføre forskellige opgaver i denne dialogboks.</span><span class="sxs-lookup"><span data-stu-id="1b63d-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="1b63d-114">Vælg en eller flere bilag, og vælg derefter en af følgende menuer:</span><span class="sxs-lookup"><span data-stu-id="1b63d-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="1b63d-115">**Vis regnskab** – Alle bilag, der har relation til de valgte dokumenter, vises.</span><span class="sxs-lookup"><span data-stu-id="1b63d-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="1b63d-116">Vælg **Luk** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1b63d-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="1b63d-117">**Eksporter** – Eksporter de valgte bilag til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1b63d-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="1b63d-118">**Vis relaterede betalinger** – Alle betalingskladdeposterne, der er oprettet i den betalingskladde, som er relateret til det valgte dokument, vises.</span><span class="sxs-lookup"><span data-stu-id="1b63d-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="1b63d-119">Derudover vises alle de udligninger, der er knyttet til disse betalinger.</span><span class="sxs-lookup"><span data-stu-id="1b63d-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="1b63d-120">Navnet på denne menu ændres også til **Vis udligninger**.</span><span class="sxs-lookup"><span data-stu-id="1b63d-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="1b63d-121">Vælg **Vis udligninger** for kun at vise de posteringer, der blev vist, da du oprettede dialogboksen **Vis udligninger**.</span><span class="sxs-lookup"><span data-stu-id="1b63d-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="1b63d-122">**Udlign posteringer** – Denne menu vises, hvis det oprindelige dokument, der blev valgt, ikke blev fuldt udlignet.</span><span class="sxs-lookup"><span data-stu-id="1b63d-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="1b63d-123">Når du vælger det, vises dialogboksen **Udlign posteringer**, hvor du kan vælge transaktioner til udligning.</span><span class="sxs-lookup"><span data-stu-id="1b63d-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="1b63d-124">**Fortryd udligning** – Denne menu vises, hvis det oprindelige dokument, der blev valgt, blev fuldt udlignet.</span><span class="sxs-lookup"><span data-stu-id="1b63d-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="1b63d-125">Når du vælger det, vises dialogboksen **Fortryd udligning**, hvor du kan fortryde udligninger, der blev udført for det pågældende dokument.</span><span class="sxs-lookup"><span data-stu-id="1b63d-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

