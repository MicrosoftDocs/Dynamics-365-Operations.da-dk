---
title: Kundekreditgrupper
description: Dette emne indeholder oplysninger om arbejdsgangen for kundekreditgrupper.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977953"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="b9088-103">Kundekreditgrupper</span><span class="sxs-lookup"><span data-stu-id="b9088-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9088-104">Du kan definere grupper af kunder, der har et delt kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="b9088-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="b9088-105">De enkelte kreditmaksimum, der er defineret på debitorfakturakontoen, tages også i betragtning.</span><span class="sxs-lookup"><span data-stu-id="b9088-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="b9088-106">Medlemmer af en kundekreditgruppe kan vælges fra forskellige juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="b9088-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="b9088-107">Når du føjer en kunde til listen over kunder i kundekreditgruppen, ændres udløbsdatoen for kreditmaksimum for de enkelte kunder til den udløbsdato, der er tildelt gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9088-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="b9088-108">Du kan oprette kundekreditgrupper på siden **Kundekreditgrupper** (**Kreditstyring \> Kundekreditgrupper \> Kundekreditgrupper**).</span><span class="sxs-lookup"><span data-stu-id="b9088-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="b9088-109">Angiv en identifikator og en beskrivelse af gruppen i felterne **Gruppenummer** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b9088-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="b9088-110">Angiv det kreditmaksimum og den valuta, der skal bruges, når systemet kontrollerer kreditmaksimum for et medlem af gruppen, i felterne **Kreditgrænse** og **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="b9088-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="b9088-111">Angiv den dato, hvor kreditgrænsen udløber, i feltet **Kreditmaksimum til dato**.</span><span class="sxs-lookup"><span data-stu-id="b9088-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="b9088-112">Kundekreditgrupper skal have en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="b9088-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="b9088-113">Når du er færdig med at oprette en kundekreditgruppe, kan du føje debitorer til den ved at angive deres juridiske enhed og kundekonto-id'et.</span><span class="sxs-lookup"><span data-stu-id="b9088-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="b9088-114">Når du føjer en ny kunde til en kundekreditgruppe, søger systemet efter den samme kundekonto på tværs af alle juridiske enheder, og du bliver bedt om at føje den til kundekreditgruppen.</span><span class="sxs-lookup"><span data-stu-id="b9088-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="b9088-115">Brug menuen **Aldersfordelte saldi** til at få vist detaljer om den aldersfordelte saldo for alle fakturakunder i en kundekreditgruppe.</span><span class="sxs-lookup"><span data-stu-id="b9088-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="b9088-116">På siden **Aldersfordelt saldo** vises en oversigt over aldersfordelte saldi for debitorkontiene på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b9088-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
