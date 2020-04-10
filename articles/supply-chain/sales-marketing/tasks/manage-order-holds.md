---
title: Administrere ordrer på hold
description: Denne procedure viser, hvordan du sætter kundesalgsordrer på hold, hvordan du arbejder med udtjekning af ordrehold, og hvordan du fjerner ordrehold.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16e11be633cdffbc8ee3e206eb42e7e1a2f72b9c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146439"
---
# <a name="manage-order-holds"></a><span data-ttu-id="3af1b-103">Administrere ordrer på hold</span><span class="sxs-lookup"><span data-stu-id="3af1b-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3af1b-104">Denne procedure viser, hvordan du sætter kundesalgsordrer på hold, hvordan du arbejder med udtjekning af ordrehold, og hvordan du fjerner ordrehold.</span><span class="sxs-lookup"><span data-stu-id="3af1b-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="3af1b-105">En ordre kan sættes på hold af en række årsager.</span><span class="sxs-lookup"><span data-stu-id="3af1b-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="3af1b-106">Du kan for eksempel holde en ordre tilbage, indtil en kundeadresse eller betalingsmetode er kontrolleret, eller indtil en chef kan gennemse kundens kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="3af1b-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="3af1b-107">Mens ordren er på hold, kan den ikke behandles af lagerstedet til forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3af1b-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="3af1b-108">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="3af1b-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="3af1b-109">Konfigurere salgsordrer på hold</span><span class="sxs-lookup"><span data-stu-id="3af1b-109">Set up order holds</span></span>
1. <span data-ttu-id="3af1b-110">Gå til **Navigationsrude > Moduler > Salg og marketing > Opsætning > Salgsordrer > Koder for ordrehold**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="3af1b-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-111">Click **New**.</span></span>
3. <span data-ttu-id="3af1b-112">Indtast en værdi i feltet **Holdkode**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="3af1b-113">Skriv f.eks. 'Tilbagekald'.</span><span class="sxs-lookup"><span data-stu-id="3af1b-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="3af1b-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="3af1b-115">For eksempel: Ordre tilbageholdes, venter på kundes tilbagekald.</span><span class="sxs-lookup"><span data-stu-id="3af1b-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="3af1b-116">Du kan eventuelt markere afkrydsningsfeltet **Fjern reservationer** for at fjerne eventuelle fysiske reservationer fra ordren, når holdkoden tilføjes.</span><span class="sxs-lookup"><span data-stu-id="3af1b-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="3af1b-117">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="3af1b-118">Placere ordre på hold</span><span class="sxs-lookup"><span data-stu-id="3af1b-118">Place order on hold</span></span>
1. <span data-ttu-id="3af1b-119">Gå til **Navigationsrude > Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="3af1b-120">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-120">Click **New**.</span></span>
3. <span data-ttu-id="3af1b-121">Indtast eller vælg en værdi i feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="3af1b-122">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-122">Click **OK**.</span></span>
5. <span data-ttu-id="3af1b-123">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="3af1b-124">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="3af1b-125">Klik på **Salgsordre** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="3af1b-126">Klik på **Ordrer på hold**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="3af1b-127">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-127">Click **New**.</span></span>
10. <span data-ttu-id="3af1b-128">Vælg den kode, du har oprettet i den tidligere underopgave, i feltet **Holdkode**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="3af1b-129">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-129">Click **Save**.</span></span>
12. <span data-ttu-id="3af1b-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3af1b-130">Close the page.</span></span>
13. <span data-ttu-id="3af1b-131">Gå til **Salg og marketing > Salgsordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="3af1b-132">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-132">In the list, mark the selected row.</span></span> <span data-ttu-id="3af1b-133">Ordrer, der er på hold, har felterne "Udfør ikke behandling" og "Hold" markeret.</span><span class="sxs-lookup"><span data-stu-id="3af1b-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="3af1b-134">Klik på **Pluk og pak** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3af1b-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="3af1b-135">Administrere ordrer på hold</span><span class="sxs-lookup"><span data-stu-id="3af1b-135">Manage order holds</span></span>
1. <span data-ttu-id="3af1b-136">Gå til **Salg og marketing > Salgsordrer > Åbne ordrer > Ordrer på hold**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="3af1b-137">Siden **Ordrer på hold** fungerer som et panel, hvor du kan få en oversigt over alle aktuelle og behandlede hold og håndtere dem og tilknyttede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="3af1b-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="3af1b-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3af1b-139">Klik på **Hold på udtjekning** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="3af1b-140">Klik på **Check ud**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-140">Click **Check out**.</span></span>
5. <span data-ttu-id="3af1b-141">Fjern markeringen af den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="3af1b-142">Feltet **Udtjekningen til** viser nu dit bruger-id.</span><span class="sxs-lookup"><span data-stu-id="3af1b-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="3af1b-143">Klik på **Ryd udtjekning**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="3af1b-144">Klik på **Ryd På hold** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="3af1b-145">Når du er klar til at fjerne holdet og lade ordren fortsætte til næste trin i opfyldelsen, skal du rydde holdet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="3af1b-146">Hvis ordren ikke kræver nogen ændringer, kan du køre handlingen Ryd På hold.</span><span class="sxs-lookup"><span data-stu-id="3af1b-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="3af1b-147">Du kan dog bruge handlingen Ryd og rediger, hvis ordren skal opdateres, når du fjerner et hold.</span><span class="sxs-lookup"><span data-stu-id="3af1b-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="3af1b-148">Handlingen **Ryd og send** er kun gældende, når du bruger callcenter-funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="3af1b-149">Klik på **Ryd På hold**.</span><span class="sxs-lookup"><span data-stu-id="3af1b-149">Click **Clear holds**.</span></span> <span data-ttu-id="3af1b-150">Holdet er nu ryddet fra ordren og fjernet fra listen over aktive hold.</span><span class="sxs-lookup"><span data-stu-id="3af1b-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="3af1b-151">Hvis du vil se alle hold eller deres delsæt i henhold til en bestemt status, skal du ændre værdien i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="3af1b-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

