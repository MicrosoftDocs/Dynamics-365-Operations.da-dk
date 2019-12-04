---
title: Hybride kundeordrer
description: En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan sælges ud af butikken af kunden, samt produkter, der skal afhentes eller sendes senere.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ef99a75d29b8fce46943213804239b237d384b07
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811896"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="3ce04-103">Hybride kundeordrer</span><span class="sxs-lookup"><span data-stu-id="3ce04-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ce04-104">En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan sælges ud af butikken af kunden, samt produkter, der skal afhentes eller sendes senere.</span><span class="sxs-lookup"><span data-stu-id="3ce04-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="3ce04-105">I Retail kan du vælge enten at udføre alle produkter eller udføre udvalgte produkter for en kundeordre.</span><span class="sxs-lookup"><span data-stu-id="3ce04-105">In Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="3ce04-106">De produktlinjer, der er markeret til udførelse, faktureres automatisk, efter at ordren er oprettet. På samme måde er dette det samme for en ordre, der skal afhentes, efter at ordren er oprettet.</span><span class="sxs-lookup"><span data-stu-id="3ce04-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="3ce04-107">Det skyldige beløb på hybrid ordrer bestemmes ved at tilføje indbetalingsprocenten på plukning og forsendelsesproduktlinjer med det fulde beløb for udførelseslinjerne.</span><span class="sxs-lookup"><span data-stu-id="3ce04-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="3ce04-108">For hybride ordrer skifter systemet mellem kundeordretilstanden og cash og carry-tilstand på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3ce04-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="3ce04-109">Hvis alle produkter i indkøbskurven er indstillet til **Udfør levering**, håndteres ordren som en postering af typen cash og carry.</span><span class="sxs-lookup"><span data-stu-id="3ce04-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="3ce04-110">Hvis nogle af eller alle linjer i kurven er indstillet til enten **Pluk** eller **Send levering**, skal ordren behandles som en debitorordretransaktion.</span><span class="sxs-lookup"><span data-stu-id="3ce04-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="3ce04-111">Hvis der er valgt en indkøbskurvlinje og **Pluk markerede**, **Afsendelse valgt** eller **Udfør valgte** er markeret, angives kun den specifikke indkøbskurvlinje med denne leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="3ce04-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="3ce04-112">I så fald fortsætter downstreamflowet af handlingen som sædvanligt.</span><span class="sxs-lookup"><span data-stu-id="3ce04-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="3ce04-113">Men hvis **Pluk markerede**, **Afsendelse valgt** eller **Udfør valgte** er valgt, uden at der er valgt en indkøbskurvlinje, åbnes en ny side, der viser alle indkøbskurvlinjerne.</span><span class="sxs-lookup"><span data-stu-id="3ce04-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="3ce04-114">På dette skærmbillede kan du vælge flere linjer på en gang for at angive leveringsmetoden.</span><span class="sxs-lookup"><span data-stu-id="3ce04-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="3ce04-115">Når du bruger denne metode til at markere linjer, tilsidesættes alle tidligere leveringsmetoder, der er knyttet til linjen.</span><span class="sxs-lookup"><span data-stu-id="3ce04-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ce04-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3ce04-116">Additional resources</span></span>

[<span data-ttu-id="3ce04-117">Kundeordrer i Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="3ce04-117">Customer orders in Retail Modern POS (MPOS)</span></span>](customer-orders-overview.md)
