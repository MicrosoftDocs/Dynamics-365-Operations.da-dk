---
title: Opret checks, der har statussen Blank
description: Dette emne forklarer, hvordan du kan oprette blanke checks for en bankkonto på siden Checks.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aa1c4c33b977c0173da98aee409389b9242980fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976440"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="2ad65-103">Opret checks, der har statussen Blank</span><span class="sxs-lookup"><span data-stu-id="2ad65-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ad65-104">Dette emne forklarer, hvordan du kan oprette blanke checks.</span><span class="sxs-lookup"><span data-stu-id="2ad65-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="2ad65-105">Du kan f.eks. oprette en blank check for at registrere en check, der er blevet beskadiget og ikke kan bruges til betaling.</span><span class="sxs-lookup"><span data-stu-id="2ad65-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="2ad65-106">På siden **Checks** kan du udføre vedligeholdelsesopgaver for checks.</span><span class="sxs-lookup"><span data-stu-id="2ad65-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="2ad65-107">Du kan f.eks. oprette nye checknumre og slette checks.</span><span class="sxs-lookup"><span data-stu-id="2ad65-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="2ad65-108">Du kan også oprette checks med statussen **Blank**.</span><span class="sxs-lookup"><span data-stu-id="2ad65-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="2ad65-109">Når blanke checks er oprettet, kan de ikke slettes eller genbruges i systemet.</span><span class="sxs-lookup"><span data-stu-id="2ad65-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="2ad65-110">Denne funktion er kun tilgængelig på siden **Checks**, hvis du aktiverer funktionen **Opret checks med statussen Blank på siden Checks** på siden **Administration af funktioner**.</span><span class="sxs-lookup"><span data-stu-id="2ad65-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="2ad65-111">Hvis funktionen ikke er aktiveret, kan der kun oprettes checks, der har statussen **Blank**, fra dialogboksen **Betaling med check** under processen til oprettelse af betaling i Kreditor.</span><span class="sxs-lookup"><span data-stu-id="2ad65-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="2ad65-112">Hvis du vil åbne siden **Checks**, skal du gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**, og derefter i handlingsruden vælge **Checks** på fanen **Administrer betalinger** i gruppen **Relaterede oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="2ad65-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="2ad65-113">Du kan også gå **Kontant- og bankstyring \> Forespørgsler og rapporter \> Checks**.</span><span class="sxs-lookup"><span data-stu-id="2ad65-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="2ad65-114">Hvis du derefter vil oprette checks med statussen **Blank**, skal du vælge **Create blank checks** (Opret blanke checks) i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2ad65-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="2ad65-115">Når systemet opretter blanke checks, er den tilknyttede bankkonto midlertidigt deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="2ad65-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="2ad65-116">Dette reducerer risikoen for, at der genereres betalinger, samtidig med at der oprettes checks.</span><span class="sxs-lookup"><span data-stu-id="2ad65-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="2ad65-117">Når behandlingen er fuldført, aktiveres den tilknyttede bankkonto igen.</span><span class="sxs-lookup"><span data-stu-id="2ad65-117">When the processing is completed, the associated bank account is reactivated.</span></span>
