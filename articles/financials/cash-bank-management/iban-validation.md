---
title: Administrere validering af IBAN-kontonummer (International Bank Account Number)
description: I dette emne beskrives, hvordan du administrerer validering af IBAN-kontonumre.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: da-dk
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="3a9b9-103">Administrere validering af IBAN-kontonummer (International Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="3a9b9-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a9b9-104">Validering af IBAN-kontonummeret øger omfanget af den validering, der sker, når du føjer et IBAN til en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="3a9b9-105">IBAN-strukturen gemmes i Microsoft Dynamics 365 for Finance and Operations og indlæses automatisk, første gang du bruger IBAN-nummeret på bankkonti.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="3a9b9-106">Bankkontonummeret er en del af den struktur, der er defineret for et IBAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="3a9b9-107">Hvis placeringen og længden af kontonummeret i IBAN ikke stemmer med den placering, der er defineret i strukturen for hvert land eller område, får du vist advarselsmeddelelser baseret på denne struktur.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="3a9b9-108">Oprette IBAN-strukturer</span><span class="sxs-lookup"><span data-stu-id="3a9b9-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="3a9b9-109">Gå til **Kontant- og bankstyring \> Opsætning \> IBAN-strukturer**.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="3a9b9-110">Bemærk, at IBAN-strukturerne for hvert land eller område er oprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="3a9b9-111">Hvis du skal tilpasse strukturerne for et bestemt land eller område, kan du redigere dem.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="3a9b9-112">Definitioner af strukturerne bliver en del af hver ny frigivelse.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="3a9b9-113">Du kan bruge menuen **Nulstil strukturer** til at indlæse de nyeste definitioner efter hvert opdatering.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="3a9b9-114">Validere IBAN-strukturen på en bankkonto</span><span class="sxs-lookup"><span data-stu-id="3a9b9-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="3a9b9-115">Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="3a9b9-116">Opret en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-116">Create a bank account.</span></span>
3. <span data-ttu-id="3a9b9-117">I oversigtspanelet **Flere oplysninger** skal du angive IBAN.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="3a9b9-118">Hvis placeringen og længden af kontonummeret i IBAN ikke stemmer med den placering, der er defineret i strukturen for hvert land eller område, får du vist meddelelse.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="3a9b9-119">Du kan ikke fortsætte, hvis længden af IBAN ikke stemmer overens med længden i IBAN-strukturen.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="3a9b9-120">Valideringen kontrollerer også, at nummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="3a9b9-121">Hvis bankkontonummeret ikke stemmer overens, modtager du en advarsel.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="3a9b9-122">Denne meddelelse er kun en advarsel.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-122">This message is only a warning.</span></span> <span data-ttu-id="3a9b9-123">Du kan fortsætte, selvom bankkontoen ikke stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="3a9b9-123">You can continue even if the bank account number doesn't match.</span></span>

