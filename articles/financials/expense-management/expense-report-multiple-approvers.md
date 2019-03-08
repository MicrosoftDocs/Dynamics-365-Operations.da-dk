---
title: Udgiftsrapporter og flere godkendere
description: Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af mere end én person.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "362412"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="409fc-103">Udgiftsrapporter og flere godkendere</span><span class="sxs-lookup"><span data-stu-id="409fc-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="409fc-104">Afhængigt af organisationens politikker for godkendelse af udgifter kan det være nødvendigt med mere end én person til at godkende en udgiftsrapport, der er sendt af en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="409fc-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="409fc-105">Når du opretter arbejdsgangsprocessen til godkendelse af udgiftsrapporter, kan du tilføje arbejdsgangelementer, der omfatter opgaver eller trin for en eller flere godkendere af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="409fc-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="409fc-106">Du kan f.eks. kræve, at alle udgiftsrapporter først godkendes af chefen for den medarbejder, der har indsendt rapporten, og derefter af kreditorkoordinatoren.</span><span class="sxs-lookup"><span data-stu-id="409fc-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="409fc-107">Hvis du beslutter at kræve flere godkendere af udgiftsrapporter, kan du tilføje arbejdsgangelementer på en af følgende måder:</span><span class="sxs-lookup"><span data-stu-id="409fc-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="409fc-108">Tilføj ét godkendelseselement, der har ét trin.</span><span class="sxs-lookup"><span data-stu-id="409fc-108">Add one approval element that has one step.</span></span> <span data-ttu-id="409fc-109">Trinnet kan f.eks. kræve, at der tildeles en udgiftsrapport til en brugergruppe, og at den godkendes af 50 procent af medlemmerne af brugergruppen.</span><span class="sxs-lookup"><span data-stu-id="409fc-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="409fc-110">Tilføj ét godkendelseselement, der har flere trin.</span><span class="sxs-lookup"><span data-stu-id="409fc-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="409fc-111">Godkendelseselementet kan f.eks. have følgende trin:</span><span class="sxs-lookup"><span data-stu-id="409fc-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="409fc-112">Chefen for den medarbejder, som har indsendt udgiftsrapporten, godkender den.</span><span class="sxs-lookup"><span data-stu-id="409fc-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="409fc-113">Kreditormedarbejderen kontrollerer kvitteringerne og posterne i udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="409fc-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="409fc-114">Ejeren af budgettet godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="409fc-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="409fc-115">Tilføj flere godkendelseselementer, som hver har ét trin.</span><span class="sxs-lookup"><span data-stu-id="409fc-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="409fc-116">For eksempel kan du tilføje et separat godkendelseselement for hver af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="409fc-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="409fc-117">Medarbejderens chef godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="409fc-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="409fc-118">Ejeren af budgettet godkender udgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="409fc-118">The budget owner approves the expense report.</span></span>
