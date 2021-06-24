---
title: Returnere serienummerstyrede produkter i POS
description: Dette emne indeholder en beskrivelse af funktionerne til validering af serienummerede varer som en del af returneringsprocessen i Microsoft Dynamics 365 Commerce POS-programmet.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129799"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="71498-103">Returnere serienummerstyrede produkter i POS</span><span class="sxs-lookup"><span data-stu-id="71498-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="71498-104">Dette emne indeholder en beskrivelse af funktionerne til validering af serienummerede varer som en del af returneringsprocessen i Microsoft Dynamics 365 Commerce POS-programmet.</span><span class="sxs-lookup"><span data-stu-id="71498-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="71498-105">I Commerce version 10.0.20 og senere findes der en ny funktion med navnet **Samlet behandling af returneringer i POS**.</span><span class="sxs-lookup"><span data-stu-id="71498-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="71498-106">Hvis du vil bruge serienummervalidering under behandling af returordre i POS, skal du aktivere denne funktion.</span><span class="sxs-lookup"><span data-stu-id="71498-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="71498-107">Du kan finde oplysninger om andre egenskaber, som denne funktion har, når den er slået til, under [Oprette returneringer i POS](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="71498-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="71498-108">Når funktionen er aktiveret, kan den ikke deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="71498-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="71498-109">Indstillinger til validering af serialiserede returneringer</span><span class="sxs-lookup"><span data-stu-id="71498-109">Options for validating serialized returns</span></span>

<span data-ttu-id="71498-110">Når funktionen **Samlet behandling af returneringer i POS** er aktiveret, kan organisationer udføre validering af returneringer af serienummerstyrede varer via POS.</span><span class="sxs-lookup"><span data-stu-id="71498-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="71498-111">Denne egenskab kan advare brugerne, hvis det serienummer, der returneres, adskiller sig fra det oprindelige serienummer, der blev solgt.</span><span class="sxs-lookup"><span data-stu-id="71498-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="71498-112">I Commerce version 10.0.20 og senere er den meddelelse, som brugerne modtager, kun en advarsel.</span><span class="sxs-lookup"><span data-stu-id="71498-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="71498-113">Brugerne kan fortsætte med at behandle en returnering i forhold til et serienummer, der er forskelligt fra det serienummer, der oprindeligt blev solgt.</span><span class="sxs-lookup"><span data-stu-id="71498-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="71498-114">Hvis du vil konfigurere validering af serienummer for en organisation, efter at funktionen **Samlet returnering i POS** er aktiveret, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="71498-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="71498-115">Under fanen **Lager** i oversigtspanelet **Lagerbeholdningshandlinger** skal du angive indstillingen **Aktivér validering af serienumre på POS-returneringer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="71498-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="71498-116">Behandle returneringer af serialiserede varer i POS</span><span class="sxs-lookup"><span data-stu-id="71498-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="71498-117">Hvis indstillingen **Aktivér validering af serienumre på POS-returneringer** er angivet til **Ja**, når en vare, der styres af et serienummer, returneres via POS, kan brugeren angive serienummeret for returlinjen i detaljeruden på siden **Produkter, der kan returneres**.</span><span class="sxs-lookup"><span data-stu-id="71498-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="71498-118">Hvis det indtastede serienummer ikke svarer til det oprindelige serienummer, der blev solgt for salgstransaktionen, modtager brugeren en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="71498-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="71498-119">Programmet forhindrer dog ikke brugeren i at fortsætte med at bogføre returneringen.</span><span class="sxs-lookup"><span data-stu-id="71498-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="71498-120">I øjeblikket understøtter POS kun validering af serienumre på returlinjer, hvor det oprindeligt bestilte antal ikke er mere end ét.</span><span class="sxs-lookup"><span data-stu-id="71498-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="71498-121">Hvis den oprindelige salgsordrelinje er oprettet i en ikke-POS-kanal, og hvis det antal, der blev bestilt til den serialiserede vare på en bestemt salgslinje, er mere end én, kan varen ikke returneres korrekt via POS.</span><span class="sxs-lookup"><span data-stu-id="71498-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71498-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="71498-122">Additional resources</span></span>

[<span data-ttu-id="71498-123">Oprette returneringer i POS</span><span class="sxs-lookup"><span data-stu-id="71498-123">Create returns in POS</span></span>](POS-returns.md)
