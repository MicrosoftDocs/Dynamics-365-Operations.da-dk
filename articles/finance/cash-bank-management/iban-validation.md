---
title: Administrere validering af IBAN-kontonummer (International Bank Account Number)
description: I dette emne beskrives, hvordan du administrerer validering af IBAN-kontonumre.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e44b855165752baeb42d3c9952c35982ef24b0f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815854"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="adb4b-103">Administrere validering af IBAN-kontonummer (International Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="adb4b-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adb4b-104">Validering af IBAN-nummeret øger omfanget af den validering, der sker, når du føjer et IBAN-nummer til en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="adb4b-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="adb4b-105">Oplysninger om strukturen af IBAN er gemt i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="adb4b-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="adb4b-106">Disse oplysninger indlæses automatisk, første gang du bruger IBAN-nummeret på bankkonti.</span><span class="sxs-lookup"><span data-stu-id="adb4b-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="adb4b-107">De indeholder længden af IBAN-nummeret, startplaceringen af bankkontonummeret og registreringsnummeret og længden af bankkontonummeret og registreringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="adb4b-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="adb4b-108">Oprette IBAN-strukturer</span><span class="sxs-lookup"><span data-stu-id="adb4b-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="adb4b-109">Gå til **Kontant- og bankstyring \> Opsætning \> IBAN-strukturer**.</span><span class="sxs-lookup"><span data-stu-id="adb4b-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="adb4b-110">Bemærk, at IBAN-strukturerne for hvert land eller område er oprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="adb4b-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="adb4b-111">Hvis du vil tilpasse strukturerne for et bestemt land eller område, kan du redigere dem.</span><span class="sxs-lookup"><span data-stu-id="adb4b-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="adb4b-112">Definitioner af strukturerne bliver en del af hver ny frigivelse.</span><span class="sxs-lookup"><span data-stu-id="adb4b-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="adb4b-113">Du kan bruge menuen **Nulstil strukturer** til at indlæse de nyeste definitioner efter hvert opdatering.</span><span class="sxs-lookup"><span data-stu-id="adb4b-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="adb4b-114">Validere IBAN-strukturen på en bankkonto</span><span class="sxs-lookup"><span data-stu-id="adb4b-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="adb4b-115">Gå til **Kontant- og bankstyring \> Bankkonti \> Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="adb4b-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="adb4b-116">Opret en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="adb4b-116">Create a bank account.</span></span>
3. <span data-ttu-id="adb4b-117">I oversigtspanelet **Flere oplysninger** skal du angive IBAN.</span><span class="sxs-lookup"><span data-stu-id="adb4b-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="adb4b-118">Hvis længden af IBAN-nummeret ikke svarer til den længde, der er defineret for hvert land eller område, vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb4b-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="adb4b-119">Du kan ikke fortsætte, hvis længden af IBAN ikke stemmer overens med den angivne længde i IBAN-strukturen.</span><span class="sxs-lookup"><span data-stu-id="adb4b-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="adb4b-120">Valideringen kontrollerer også, at nummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="adb4b-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="adb4b-121">Hvis bankkontonummeret ikke stemmer overens, vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb4b-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="adb4b-122">Denne meddelelse er kun en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb4b-122">This message is only a warning.</span></span> <span data-ttu-id="adb4b-123">Du kan fortsætte, selvom bankkontoen ikke stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="adb4b-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="adb4b-124">Valideringen kontrollerer også, at registreringsnummeret på bankkontoen svarer til den del af IBAN, der repræsenterer bankens registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="adb4b-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="adb4b-125">Registreringsnummeret omfatter et banknummer og ofte en ekstra bankafdeling.</span><span class="sxs-lookup"><span data-stu-id="adb4b-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="adb4b-126">Hvis bankens registreringsnummer ikke stemmer overens, vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb4b-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="adb4b-127">Denne meddelelse er kun en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb4b-127">This message is only a warning.</span></span> <span data-ttu-id="adb4b-128">Du kan fortsætte, selvom bankregistreringsnummeret ikke stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="adb4b-128">You can continue even if the bank routing number doesn't match.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]