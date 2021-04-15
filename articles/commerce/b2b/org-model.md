---
title: Oprette organisationsmodelhierarkier for B2B-organisationer
description: Dette emne indeholder en beskrivelse af, hvordan du kan oprette organisationsmodelhierarkier for business-to-business (B2B-organisationer).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799823"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="b9169-103">Oprette organisationsmodelhierarkier for B2B-organisationer</span><span class="sxs-lookup"><span data-stu-id="b9169-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9169-104">Dette emne indeholder en beskrivelse af, hvordan du kan oprette organisationsmodelhierarkier for business-to-business (B2B-organisationer) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9169-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b9169-105">I Commerce Headquarters repræsenteres organisationer af forretningspartnerlande af debitor- og debitorhierarkienheder.</span><span class="sxs-lookup"><span data-stu-id="b9169-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="b9169-106">Forretningspartnerorganisationen og dens brugere er repræsenteret som kunder, og der bruges debitorhierarkier til at knytte disse kunder til hinanden.</span><span class="sxs-lookup"><span data-stu-id="b9169-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="b9169-107">Når en forretningspartneranmodning om at deltage i et B2B-e-handelswebsted godkendes, udføres følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="b9169-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="b9169-108">Der oprettes to nye kundeposter i systemet: en kundepost af typen **Organisation** for partnerorganisationen for forretningspartneren og en kundepost af typen **Person** for anmoderen (dvs. den forretningspartnerbruger, der indsendte anmodningen).</span><span class="sxs-lookup"><span data-stu-id="b9169-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="b9169-109">Der oprettes en ny debitorhierarkipost under **Debitor \> Debitorhierarki**.</span><span class="sxs-lookup"><span data-stu-id="b9169-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="b9169-110">Denne post har følgende overskriftsegenskaber:</span><span class="sxs-lookup"><span data-stu-id="b9169-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="b9169-111">**Debitorhierarki-id** – et entydigt id for debitorhierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b9169-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="b9169-112">Dette id bruger den nummerserie, der er defineret i Delte parametre for Commerce i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b9169-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="b9169-113">**Navn** – Forretningspartnerens organisationsnavn, som det er angivet i anmodningen om onboarding.</span><span class="sxs-lookup"><span data-stu-id="b9169-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="b9169-114">**Formål** – Denne egenskab er angivet til den foruddefinerede værdi **B2B-organisation**.</span><span class="sxs-lookup"><span data-stu-id="b9169-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="b9169-115">**Organisation** – Forretningspartnerens debitor-id.</span><span class="sxs-lookup"><span data-stu-id="b9169-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="b9169-116">Her er detaljer om debitorhierarkiposten:</span><span class="sxs-lookup"><span data-stu-id="b9169-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="b9169-117">Debitorposten for anmoderen er knyttet til debitorhierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b9169-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="b9169-118">Administratorrollen er tilknyttet anmoderen.</span><span class="sxs-lookup"><span data-stu-id="b9169-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="b9169-119">Når administratoren tilføjer flere brugere, føjes til forretningspartnerorganisationen på et B2B-websted, oprettes der en ny kundepost for hver bruger i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b9169-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="b9169-120">Denne kundepost føjes også til den relevante kundehierarkipost for forretningspartneren og har rollen som "bruger".</span><span class="sxs-lookup"><span data-stu-id="b9169-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="b9169-121">I de fleste tilfælde skal de tilsvarende egenskabsværdier for alle debitorposter i et hierarki være ens.</span><span class="sxs-lookup"><span data-stu-id="b9169-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="b9169-122">Da alle forretningspartnerbrugere f.eks. skal få ens priser for produkter, skal deres prisgruppe og tilknyttede konfigurationer stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="b9169-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="b9169-123">Systemet gennemtvinger dog ikke denne konsistens.</span><span class="sxs-lookup"><span data-stu-id="b9169-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="b9169-124">De relevante brugere i handelshovedkvarteret er derfor ansvarlige for at sikre, at egenskabsværdierne og -konfigurationerne er ens for alle debitorer i et bestemt hierarki.</span><span class="sxs-lookup"><span data-stu-id="b9169-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="b9169-125">Brugere i Commerce Headquarters kan se på egenskabsværdierne for alle debitorposter i hierarkiet ved siden af hinanden.</span><span class="sxs-lookup"><span data-stu-id="b9169-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="b9169-126">Vælg de relevante egenskaber for debitorposten ved at vælge fanenavnene i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="b9169-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="b9169-127">Brugerne kan få vist og redigere egenskabsværdierne fra denne visning.</span><span class="sxs-lookup"><span data-stu-id="b9169-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="b9169-128">Du kan også anvende alle værdierne fra administratorkundeposten på alle brugerkundeposter ved at vælge Tilsidesæt i oplysningerne **Tilsidesæt** i oplysningerne om debitorhierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b9169-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9169-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b9169-129">Additional resources</span></span>

[<span data-ttu-id="b9169-130">Konfigurere et B2B-e-handelswebsted</span><span class="sxs-lookup"><span data-stu-id="b9169-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="b9169-131">Administrere forretningspartnerbrugere på B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="b9169-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="b9169-132">Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="b9169-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="b9169-133">Angive produktantalsgrænser for B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="b9169-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]