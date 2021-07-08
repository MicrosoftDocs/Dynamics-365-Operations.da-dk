---
title: Aktivere beskeder om kunders indtjekning i POS
description: Dette emne beskriver, hvordan du kan aktivere beskeder om kunders indtjekning i POS for Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271419"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="835b9-103">Aktivere beskeder om kunders indtjekning i POS</span><span class="sxs-lookup"><span data-stu-id="835b9-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="835b9-104">Dette emne beskriver, hvordan du kan aktivere beskeder om kunders indtjekning i POS for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="835b9-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="835b9-105">I deres mails angående "ordre klar til afhentning" kan organisationer give et link eller en knap, så kunderne kan give butikken besked om, at de er på stedet og venter på, at pakken bliver bragt ud til dem.</span><span class="sxs-lookup"><span data-stu-id="835b9-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="835b9-106">Kunderne modtager derefter en bekræftelse af deres indtjekning, og butikken modtager en besked som en opgave i POS-applikationen.</span><span class="sxs-lookup"><span data-stu-id="835b9-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="835b9-107">Denne opgave fungerer som en besked om, at en salgsmedarbejder skal levere ordren til kundens køretøj.</span><span class="sxs-lookup"><span data-stu-id="835b9-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="835b9-108">Derfor behøver kunden ikke at gå ind i butikken.</span><span class="sxs-lookup"><span data-stu-id="835b9-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="835b9-109">Arbejdsgangen for kundens indtjekning kan også konfigureres til at indsamle yderligere oplysninger fra kunder, f.eks. deres parkeringspladssnummer, mærket, modellen og farven på køretøjet samt leveringsinstruktionerne.</span><span class="sxs-lookup"><span data-stu-id="835b9-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="835b9-110">Medarbejderen i detailbutikken kan bruge disse oplysninger til at lette ordrehåndteringen.</span><span class="sxs-lookup"><span data-stu-id="835b9-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="835b9-111">Aktivere kunders indtjekning</span><span class="sxs-lookup"><span data-stu-id="835b9-111">Enable customer check-in</span></span>

<span data-ttu-id="835b9-112">Når funktionen til kunders indtjekning er aktiveret, genererer Commerce et ordrebekræftelses-id (også kaldet kanalreference-id'et).</span><span class="sxs-lookup"><span data-stu-id="835b9-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="835b9-113">Der genereres også ordrebekræftelses-d'er for ordrer, der oprettes via POS- eller callcenter-kanaler.</span><span class="sxs-lookup"><span data-stu-id="835b9-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="835b9-114">Benyt denne fremgangsmåde for at aktivere funktionen til kunders indtjekning i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="835b9-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="835b9-115">Gå til **Arbejdsområder \> Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="835b9-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="835b9-116">Søg efter funktionen **Generer et konsistent kanalreference-id-format på tværs af kanaler**.</span><span class="sxs-lookup"><span data-stu-id="835b9-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="835b9-117">Vælg funktionen, og vælg derefter **Aktiver nu** i egenskabsruden.</span><span class="sxs-lookup"><span data-stu-id="835b9-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="835b9-118">Oprette en side med bekræftelse af indtjekning</span><span class="sxs-lookup"><span data-stu-id="835b9-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="835b9-119">På dit e-handelswebsted skal du oprette en ny side, der kan bruges til bekræftelsen af indtjekning.</span><span class="sxs-lookup"><span data-stu-id="835b9-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="835b9-120">Med yderligere konfiguration kan siden også omfatte en formular, der indsamler yderligere oplysninger fra kunder for at lette ordrehåndteringen.</span><span class="sxs-lookup"><span data-stu-id="835b9-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="835b9-121">Du kan finde flere oplysninger om, hvordan du konfigurerer siden og modulet, i [Modul til kunders indtjekning](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="835b9-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="835b9-122">Konfigurere mail-skabelonen til transaktioner</span><span class="sxs-lookup"><span data-stu-id="835b9-122">Configure the transactional email template</span></span>

<span data-ttu-id="835b9-123">Du skal tilføje et link eller en knap for **Her er jeg** til skabelonen for den transaktionsmail, som kunder modtager, når deres ordre er klar til afhentning.</span><span class="sxs-lookup"><span data-stu-id="835b9-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="835b9-124">Kunder kan bruge dette link eller denne knap til at give butikken besked om, at de er ankommet for at hente deres ordre.</span><span class="sxs-lookup"><span data-stu-id="835b9-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="835b9-125">Tilføj linket eller knappen til den skabelon, der er knyttet til beskedtypen **Emballagering fuldført** og den leveringsmåde, du bruger til ordrehåndtering ved afhentning ved fortovskanten.</span><span class="sxs-lookup"><span data-stu-id="835b9-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="835b9-126">I skabelonen skal du oprette et HTML-link eller en knap, der peger på URL-adressen til den oprettede side for bekræftelsen af indtjekning.</span><span class="sxs-lookup"><span data-stu-id="835b9-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="835b9-127">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="835b9-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="835b9-128">Du kan finde flere oplysninger om, hvordan du konfigurerer mailskabeloner, i [Tilpasse transkationsmails efter leveringsmåde](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="835b9-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="835b9-129">Der oprettes en opgave til bekræftelse af indtjekning i POS</span><span class="sxs-lookup"><span data-stu-id="835b9-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="835b9-130">Når en kunde giver butikken besked om, at kunden er klar afhentningen, modtager kunden en beskræftelse af indtjekningen, og der oprettes en opgave på opgavelisten i POS for den butik, hvor kunden afhenter ordren.</span><span class="sxs-lookup"><span data-stu-id="835b9-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="835b9-131">Opgaven indeholder alle de kunde- og ordreoplysninger, der skal bruges til at opfylde ordren.</span><span class="sxs-lookup"><span data-stu-id="835b9-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="835b9-132">I opgaven viser feltet med instruktioner alle de oplysninger, der er indsamlet fra kunden via formularen til ekstra oplysninger.</span><span class="sxs-lookup"><span data-stu-id="835b9-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="835b9-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="835b9-133">Additional resources</span></span>

[<span data-ttu-id="835b9-134">Modul for indtjekning ved afhentning</span><span class="sxs-lookup"><span data-stu-id="835b9-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
