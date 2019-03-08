---
title: Administrere validering af IBAN-kontonummer (International Bank Account Number)
description: I dette emne beskrives, hvordan du administrerer validering af IBAN-kontonumre.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 19e0528b95952de8e5503c361efcfeca4c529caf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "359997"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="78185-103">Administrere validering af IBAN-nummer (International Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="78185-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78185-104">Validering af IBAN-nummeret øger omfanget af den validering, der sker, når du føjer et IBAN-nummer til en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="78185-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="78185-105">Oplysninger om strukturen i det IBAN, der er gemt i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="78185-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="78185-106">Disse oplysninger indlæses automatisk, første gang du bruger IBAN-nummeret på bankkonti.</span><span class="sxs-lookup"><span data-stu-id="78185-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="78185-107">De indeholder længden af IBAN-nummeret, startplaceringen af bankkontonummeret og registreringsnummeret og længden af bankkontonummeret og registreringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="78185-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="78185-108">Oprette IBAN-strukturer</span><span class="sxs-lookup"><span data-stu-id="78185-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="78185-109">Gå til **Kontant- og bankstyring \> Opsætning \> IBAN-strukturer**.</span><span class="sxs-lookup"><span data-stu-id="78185-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="78185-110">Bemærk, at IBAN-strukturerne for hvert land eller område er oprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="78185-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="78185-111">Hvis du vil tilpasse strukturerne for et bestemt land eller område, kan du redigere dem.</span><span class="sxs-lookup"><span data-stu-id="78185-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="78185-112">Definitioner af strukturerne bliver en del af hver ny frigivelse.</span><span class="sxs-lookup"><span data-stu-id="78185-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="78185-113">Du kan bruge menuen **Nulstil strukturer** til at indlæse de nyeste definitioner efter hvert opdatering.</span><span class="sxs-lookup"><span data-stu-id="78185-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="78185-114">Validere IBAN-strukturen på en bankkonto</span><span class="sxs-lookup"><span data-stu-id="78185-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="78185-115">Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="78185-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="78185-116">Opret en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="78185-116">Create a bank account.</span></span>
3. <span data-ttu-id="78185-117">I oversigtspanelet **Flere oplysninger** skal du angive IBAN.</span><span class="sxs-lookup"><span data-stu-id="78185-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="78185-118">Hvis længden af IBAN-nummeret ikke svarer til den længde, der er defineret for hvert land eller område, vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="78185-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="78185-119">Du kan ikke fortsætte, hvis længden af IBAN ikke stemmer overens med den angivne længde i IBAN-strukturen.</span><span class="sxs-lookup"><span data-stu-id="78185-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="78185-120">Valideringen kontrollerer også, at nummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="78185-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="78185-121">Hvis bankkontonummeret ikke stemmer overens, vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="78185-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="78185-122">Denne meddelelse er kun en advarsel.</span><span class="sxs-lookup"><span data-stu-id="78185-122">This message is only a warning.</span></span> <span data-ttu-id="78185-123">Du kan fortsætte, selvom bankkontoen ikke stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="78185-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="78185-124">Valideringen kontrollerer også, at registreringsnummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankens registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="78185-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="78185-125">Registreringsnummeret omfatter et banknummer og ofte en ekstra bankafdeling.</span><span class="sxs-lookup"><span data-stu-id="78185-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="78185-126">Hvis bankens registreringsnummer ikke stemmer overens, vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="78185-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="78185-127">Denne meddelelse er kun en advarsel.</span><span class="sxs-lookup"><span data-stu-id="78185-127">This message is only a warning.</span></span> <span data-ttu-id="78185-128">Du kan fortsætte, selvom bankregistreringsnummeret ikke stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="78185-128">You can continue even if the bank routing number doesn't match.</span></span>
