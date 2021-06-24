---
title: Ændring af leveringsmetode i POS
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere og bruge ændringsmåden for leveringshandlinger i POS.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fd69d82536047c06e94ba4a7e860ef54680619a4
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193125"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="40394-103">Ændring af leveringsmetode i POS</span><span class="sxs-lookup"><span data-stu-id="40394-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40394-104">Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere og bruge funktionen "Skift leveringsmåde" i dit POS-miljø.</span><span class="sxs-lookup"><span data-stu-id="40394-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="40394-105">I Dynamics 365 Commerce version 10.0.10 og nyere kan handlingen **Ændring af leveringsmetode** (647) føjes til dine POS-skærmlayout.</span><span class="sxs-lookup"><span data-stu-id="40394-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="40394-106">Funktionen Ændring af leveringsmetode giver dig mulighed for at ændre leveringsmåden for en eller flere konfigurerede forsendelsessalgslinjer på POS-transaktionen.</span><span class="sxs-lookup"><span data-stu-id="40394-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="40394-107">I tidligere versioner af Commerce skulle du gå gennem de fulde konfigurationsstrømme **Send alle** eller **Send valgte**, hvis du vil ændre leveringsmåden på en eksisterende linje, der er konfigureret til forsendelse.</span><span class="sxs-lookup"><span data-stu-id="40394-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="40394-108">Denne proces var tidskrævende og kan resultere i utilsigtede ændringer af leveringsoprindelsen eller leveringsdatoerne for linjen.</span><span class="sxs-lookup"><span data-stu-id="40394-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="40394-109">Den nye funktionalitet er en alternativ metode til effektiv opdatering af leveringsmåden på disse salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="40394-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="40394-110">Du kan finde flere oplysninger om, hvordan du føjer en handling til en knap på din POS-knapmatrix, i [Skærmlayout for POS](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="40394-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](pos-screen-layouts.md).</span></span>

<span data-ttu-id="40394-111">Når denne funktion er konfigureret i POS, og du vælger **Skift leveringsmåde**, vises en listeside, hvor du kan vælge de linjer i transaktionen, som du vil ændre leveringsmåden for.</span><span class="sxs-lookup"><span data-stu-id="40394-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="40394-112">Du kan vælge nogle eller alle linjer eller afslutte uden at foretage nogen ændringer.</span><span class="sxs-lookup"><span data-stu-id="40394-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="40394-113">De salgslinjer, der tidligere er konfigureret til forsendelse, er de eneste linjer på listen, som du kan ændre.</span><span class="sxs-lookup"><span data-stu-id="40394-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="40394-114">Hvis du vil ændre en linje, der er angivet til afhentning eller til aflevering, skal du bruge handlingerne **Send alle** eller **Send valgte**.</span><span class="sxs-lookup"><span data-stu-id="40394-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="40394-115">Hvis du derimod vil ændre en linje, der er angivet som en forsendelse til en afhentning eller afsendelse, skal du bruge handlingerne **Afhent alle**, **Afhent valgte**, **Udfør alle** eller **Udfør valgte**.</span><span class="sxs-lookup"><span data-stu-id="40394-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="40394-116">Når du har valgt de linjer, du vil ændre, skal klikke på **Skift leveringsmåde** for at vælge indstillinger for leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="40394-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="40394-117">Hvis du har valgt flere linjer, der skal ændres, vil POS kun vise leveringsmåder, der er konfigureret som tilladte for alle de valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="40394-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="40394-118">Leveringsmåder kan konfigureres til at understøtte specifikke produkter og leveringsadresser.</span><span class="sxs-lookup"><span data-stu-id="40394-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="40394-119">Hvis der er en leveringsmåde, der er acceptabel for ét produkt og én adressekombination, men ikke er acceptabel for en anden valgt produkt- og adressekombination, er leveringsmåden ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="40394-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="40394-120">Du skal muligvis vælge én linje ad gangen og ændre leveringsmåden for hver linje separat, hvis du vil vælge en leveringsmåde for ét produkt, der ikke understøttes af et andet produkt.</span><span class="sxs-lookup"><span data-stu-id="40394-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="40394-121">Når du har valgt den nye leveringsmåde, vises siden Transaktion.</span><span class="sxs-lookup"><span data-stu-id="40394-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="40394-122">Hvis du vil have vist dine valg af nye leveringsmåder, skal du vælge fanen **Levering** på transaktionslisten.</span><span class="sxs-lookup"><span data-stu-id="40394-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40394-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="40394-123">Additional resources</span></span>

[<span data-ttu-id="40394-124">Oprette callcenter-ordrer</span><span class="sxs-lookup"><span data-stu-id="40394-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="40394-125">Tilpasse transaktionsmails efter leveringsmåde</span><span class="sxs-lookup"><span data-stu-id="40394-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]