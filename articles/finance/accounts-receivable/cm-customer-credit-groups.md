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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b1e93d562e66cb8d4c5819a749459ea8783b1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237536"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="8df76-103">Kundekreditgrupper</span><span class="sxs-lookup"><span data-stu-id="8df76-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8df76-104">Du kan definere grupper af kunder, der har et delt kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="8df76-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="8df76-105">De enkelte kreditmaksimum, der er defineret på debitorfakturakontoen, tages også i betragtning.</span><span class="sxs-lookup"><span data-stu-id="8df76-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="8df76-106">Medlemmer af en kundekreditgruppe kan vælges fra forskellige juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="8df76-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="8df76-107">Når du føjer en kunde til listen over kunder i kundekreditgruppen, ændres udløbsdatoen for kreditmaksimum for de enkelte kunder til den udløbsdato, der er tildelt gruppen.</span><span class="sxs-lookup"><span data-stu-id="8df76-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="8df76-108">Du kan oprette kundekreditgrupper på siden **Kundekreditgrupper** (**Kreditstyring \> Kundekreditgrupper \> Kundekreditgrupper**).</span><span class="sxs-lookup"><span data-stu-id="8df76-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="8df76-109">Angiv en identifikator og en beskrivelse af gruppen i felterne **Gruppenummer** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="8df76-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="8df76-110">Angiv det kreditmaksimum og den valuta, der skal bruges, når systemet kontrollerer kreditmaksimum for et medlem af gruppen, i felterne **Kreditgrænse** og **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="8df76-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="8df76-111">Angiv den dato, hvor kreditgrænsen udløber, i feltet **Kreditmaksimum til dato**.</span><span class="sxs-lookup"><span data-stu-id="8df76-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="8df76-112">Kundekreditgrupper skal have en udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="8df76-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="8df76-113">Når du er færdig med at oprette en kundekreditgruppe, kan du føje debitorer til den ved at angive deres juridiske enhed og kundekonto-id'et.</span><span class="sxs-lookup"><span data-stu-id="8df76-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="8df76-114">Når du føjer en ny kunde til en kundekreditgruppe, søger systemet efter den samme kundekonto på tværs af alle juridiske enheder, og du bliver bedt om at føje den til kundekreditgruppen.</span><span class="sxs-lookup"><span data-stu-id="8df76-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="8df76-115">Brug menuen **Aldersfordelte saldi** til at få vist detaljer om den aldersfordelte saldo for alle fakturakunder i en kundekreditgruppe.</span><span class="sxs-lookup"><span data-stu-id="8df76-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="8df76-116">På siden **Aldersfordelt saldo** vises en oversigt over aldersfordelte saldi for debitorkontiene på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="8df76-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]