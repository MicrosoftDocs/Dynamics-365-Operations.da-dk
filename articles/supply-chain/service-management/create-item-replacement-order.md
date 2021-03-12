---
title: Oprette en genanskaffelsesordre for en vare
description: Der oprettes normalt en genanskaffelsesordre for en vare, når et produkt er returneret og kontrolleret.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0006ea9ec64cd95a709ec91509cb3a9828df160
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996645"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="58da1-103">Oprette en genanskaffelsesordre for en vare</span><span class="sxs-lookup"><span data-stu-id="58da1-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="58da1-104">Der oprettes normalt en genanskaffelsesordre for en vare, når et produkt er returneret og kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="58da1-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="58da1-105">Når en vare skal erstattes, inden den er returneret, eller når den oprindelige vare ikke vil blive returneret, kan du oprette en genanskaffelsesordre for en vare, straks du opretter en returordre.</span><span class="sxs-lookup"><span data-stu-id="58da1-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="58da1-106">Oprette en erstatningsordre, når du modtaget en returneret vare</span><span class="sxs-lookup"><span data-stu-id="58da1-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="58da1-107">Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="58da1-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="58da1-108">Opret en ny returordre, eller vælg en returordre fra listen for at åbne formularen **Returordre - RMA-nummer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="58da1-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="58da1-109">Klik på **Returlinje**, og vælg derefter **Erstatningsvare**.</span><span class="sxs-lookup"><span data-stu-id="58da1-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="58da1-110">Vælg den vare, der skal erstatte den returnerede vare.</span><span class="sxs-lookup"><span data-stu-id="58da1-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="58da1-111">Angiv varespecifikationer, og klik derefter på **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="58da1-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="58da1-112">Klik på **Følgeseddel** for at generere en følgeseddel til returordren.</span><span class="sxs-lookup"><span data-stu-id="58da1-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="58da1-113">Der oprettes en salgsordre for den valgte erstatningsvare.</span><span class="sxs-lookup"><span data-stu-id="58da1-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="58da1-114">Når salgsordren er oprettet for erstatningsvaren, søges der automatisk i salgsaftaler, og hvis der findes en relevant salgsaftale, anvendes den på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="58da1-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="58da1-115">Oprette en erstatningsordre, før du modtager en vare, der returneres</span><span class="sxs-lookup"><span data-stu-id="58da1-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="58da1-116">Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="58da1-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="58da1-117">Opret en ny returordre, eller vælg en returordre fra listen for at åbne formularen **Returordre - RMA-nummer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="58da1-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="58da1-118">Klik på **Find salgsordre**, hvis du vil identificere salgsordren for den returnerede vare.</span><span class="sxs-lookup"><span data-stu-id="58da1-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="58da1-119">Udfyld formularen **Find salgsordre**, og klik derefter på **OK** for at lukke formularen og vende tilbage til formularen **Returordre - RMA-nummer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="58da1-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="58da1-120">Salgsordrelinjen for den returnerede vare kopieres til returordren.</span><span class="sxs-lookup"><span data-stu-id="58da1-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="58da1-121">Klik på **Erstatningsordre** for at åbne formularen **Opret salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="58da1-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="58da1-122">Marker afkrydsningsfeltet **Kopier returordrelinjer** for at overføre detaljer fra den returordre, du markerede i formularen **Returordre - RMA-nummer: %1, %2**, til denne salgsordre.</span><span class="sxs-lookup"><span data-stu-id="58da1-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="58da1-123">Angiv eller tilpas detaljerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="58da1-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="58da1-124">Hvis du identificerede salgsordren i trin 3 i , og hvis salgsordrelinjen for den returnerede vare er knyttet til en salgsaftale, vises id'et for den relevante salgsaftale for vareerstatningsordren automatisk i feltet **Salgsaftale-id**.</span><span class="sxs-lookup"><span data-stu-id="58da1-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="58da1-125">Klik på **OK** for at lukke formularen **Opret salgsordre** og åbne formularen **Salgsordre**, hvor du kan fortsætte med at angive oplysninger for den nye salgsordre.</span><span class="sxs-lookup"><span data-stu-id="58da1-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="58da1-126">Alle gældende returordrelinjer kopieres til den nye salgsordre.</span><span class="sxs-lookup"><span data-stu-id="58da1-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="58da1-127">Hvis id'et for salgsaftalen vises automatisk i feltet **Salgsaftale-id**, er salgsaftalen blevet knyttet til salgsordrehovedet for vareerstatningsordren.</span><span class="sxs-lookup"><span data-stu-id="58da1-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="58da1-128">Hvis der er en gældende forpligtelse i salgsaftalen, som endnu ikke er opfyldt, og salgsordren er oprettet, før salgsaftalen udløber, oprettes der et link mellem salgsaftalelinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="58da1-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="58da1-129">Derfor kopieres oplysninger fra salgsaftalen som f.eks. varepris, til den nye salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="58da1-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


