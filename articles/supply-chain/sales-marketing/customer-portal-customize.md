---
title: Tilpasse og bruge debitorportalen
description: Dette emne forklarer, hvordan du kan tilpasse debitorportalen, efter at den er føjet til systemet.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 16d5c13c0fbff8c5033b0d1e9dd0d07851521126
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840767"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="6b7ab-103">Tilpasse og bruge debitorportalen</span><span class="sxs-lookup"><span data-stu-id="6b7ab-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6b7ab-104">I dette emne beskrives de forskellige sider, der er tilgængelige i debitorportalen lige fra starten.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="6b7ab-105">Her forklares, hvad siderne gør, og hvordan du kan tilpasse dem.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="6b7ab-106">Debitorportalen indeholder nogle websider og handlinger lige fra starten.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="6b7ab-107">Følgende webstedkort giver et overblik over disse websider og handlinger samt de roller, der kan udføre handlingerne.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="6b7ab-108">![Oversigt over kundeportalwebsted](media/customer-portal-site-map.png "Oversigt over kundeportalwebsted")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="6b7ab-109">Typiske tilpasninger</span><span class="sxs-lookup"><span data-stu-id="6b7ab-109">Typical customizations</span></span>

<span data-ttu-id="6b7ab-110">I følgende emner kan du finde grundlæggende oplysninger om Power Apps-portaler og oplysninger om, hvordan du kan tilpasse portaler:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="6b7ab-111">[Arbejde med skabeloner](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – Dette emne indeholder en generel oversigt over, hvordan Power Apps-portaler fungerer, og hvordan du kan foretage simple tilpasninger af portaler.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-111">[Work with templates](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="6b7ab-112">[Administrere portalindhold](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – Dette emne forklarer, hvordan du kan administrere og tilpasse det indhold, der skal vises i din portal.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-112">[Manage portal content](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="6b7ab-113">[Redigere CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – Dette emne hjælper dig med at lave mere komplekse tilpasninger af portalens brugergrænseflade (UI).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-113">[Edit CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="6b7ab-114">[Oprette et tema til din portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – Dette emne hjælper dig med at oprette et brugergrænsefladetema til din portal.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-114">[Create a theme for your portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="6b7ab-115">[Oprette og vise portalindhold nemt](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – Dette emne hjælper dig med at administrere de underliggende data og tabeller, du bruger til din portal.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-115">[Create and expose portal content easily](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="6b7ab-116">[Konfigurere en kontaktperson til brug i en portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – Dette emne forklarer, hvordan du opretter og tilpasser brugerroller, og hvordan sikkerhed og godkendelse fungerer i Power Apps-portaler.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-116">[Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="6b7ab-117">[Konfigurere noter til tabelformularer og webformularer på portaler](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – Dette emne forklarer, hvordan du kan føje dokumenter og yderligere lagerplads til din portal.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-117">[Configure notes for table forms and web forms on portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="6b7ab-118">[Fejlhåndtering for portalwebsted](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – Dette emne forklarer, hvordan du kan få vist logfilerne for portalfejl og gemme dem i din Microsoft Azure Blob-lagerkonto.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-118">[Error handling for portal website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="6b7ab-119">Tilpasse processen til oprettelse af ordrer</span><span class="sxs-lookup"><span data-stu-id="6b7ab-119">Customize the order creation process</span></span>

<span data-ttu-id="6b7ab-120">Når en bruger sender en ordre ved hjælp af debitorportalen, synkroniseres ordren automatisk til det relevante Dynamics 365 Supply Chain Management-miljø.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="6b7ab-121">Da brugeren er en ekstern kunde, er nogle af de påkrævede oplysninger bevidst skjult for ham eller hende.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="6b7ab-122">Disse oplysninger udfyldes automatisk, når formularen sendes.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="6b7ab-123">I dette afsnit kan du se, hvordan du skal oprette kontaktpersoner for at undgå fejl.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="6b7ab-124">Her forklares de felter, der automatisk defineres, og hvordan du om nødvendigt kan ændre værdien i disse felter.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="6b7ab-125">Indbygget proces for oprettelse af ordrer</span><span class="sxs-lookup"><span data-stu-id="6b7ab-125">The out-of-box order creation process</span></span>

<span data-ttu-id="6b7ab-126">Her er standardtrinnene for afsendelse af en ordre fra debitorportalen.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="6b7ab-127">På startsiden skal du vælge **Opret ordre** for at åbne guiden **Oprette ordre**.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="6b7ab-128">På siden **Ordreoplysninger** skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="6b7ab-129">**Ønsket modtagelsesdato** – Angiv leveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="6b7ab-130">**Leveringsadresse** – Angiv den adresse, som ordren skal leveres til.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="6b7ab-131">**Firma** – Vælg navnet på debitorfirmaet.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="6b7ab-132">Dette felt udfyldes automatisk for brugere, der ikke er administratorer.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="6b7ab-133">**Rekvisitionsnummer** – Angiv ordrens rekvisitionsnummer.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="6b7ab-134">Dette felt er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-134">This field isn't required.</span></span>
    - <span data-ttu-id="6b7ab-135">**Levér til land/område** – Angiv det land eller det område, som varerne skal leveres til.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="6b7ab-136">Dette felt udfyldes automatisk for brugere, der ikke er administratorer.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="6b7ab-137">![Siden Ordreoplysninger](media/customer-portal-order-information.png "Siden Ordreoplysninger")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="6b7ab-138">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-138">Select **Next**.</span></span>
1. <span data-ttu-id="6b7ab-139">På siden **Varer** skal du vælge **Tilføj vare**.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="6b7ab-140">![Siden varer](media/customer-portal-items.png "Siden varer")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="6b7ab-141">I dialogboksen **Vareoplysninger** indstilles følgende felter:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="6b7ab-142">**Produktnavn** – Find og vælg et produkt, der skal føjes til ordren.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="6b7ab-143">**Antal** – Angiv antal af det valgte produkt.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="6b7ab-144">**Enhed** – Angiv måleenheden (f.eks **ea**, **kg** eller **kasse**).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="6b7ab-145">**Forkalkuleret nettobeløb** – Værdien beregnes som den forkalkulerede pris for varen × antallet for den valgte enhed.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="6b7ab-146">![Dialogboksen Vareoplysninger](media/customer-portal-item-information.png "Dialogboksen Vareoplysninger")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="6b7ab-147">Vælg **Send** for at føje varen til ordren.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="6b7ab-148">Gentag trin 4 til 6, indtil du har tilføjet alle de varer, du vil bestille.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="6b7ab-149">Vælg **Næste** på siden **Varer**, når du er færdig med at tilføje varer.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="6b7ab-150">Siden **Ordreoplysninger** viser en oversigt over ordren.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="6b7ab-151">Gennemse ordreindholdet og leveringsoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="6b7ab-152">Hvis alt ser korrekt ud, skal du vælge **Send** for at sende ordren.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="6b7ab-153">![Siden Ordreoplysninger](media/customer-portal-order-submit.png "Siden Ordreoplysninger")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="6b7ab-154">Opsætning af standarddata</span><span class="sxs-lookup"><span data-stu-id="6b7ab-154">Standard data setup</span></span>

<span data-ttu-id="6b7ab-155">For at hjælpe med at sikre en problemfri brugeroplevelse udfylder debitorportalen automatisk værdier for flere obligatoriske felter.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="6b7ab-156">Disse værdier er baseret på oplysningerne i kontaktpersonposten for den kunde, der skal sende ordren.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="6b7ab-157">For hver [kontaktrække](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts), der tilhører en kunde, som skal bruge kundeportalen til at sende ordrer, skal der angives værdier for følgende obligatoriske felter.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-157">For each [contact row](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="6b7ab-158">Ellers opstår der fejl.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="6b7ab-159">**Firma** – Den juridiske enhed, som ordren tilhører</span><span class="sxs-lookup"><span data-stu-id="6b7ab-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="6b7ab-160">**Potentiel kunde** – Den kundekonto, der er tilknyttet ordren</span><span class="sxs-lookup"><span data-stu-id="6b7ab-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="6b7ab-161">**Prisliste** – Tilpasset prisliste til kunden</span><span class="sxs-lookup"><span data-stu-id="6b7ab-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="6b7ab-162">**Valuta** – Valutaen for prisen</span><span class="sxs-lookup"><span data-stu-id="6b7ab-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="6b7ab-163">**Levér til land/område** – Det land eller det område, som varerne skal leveres til</span><span class="sxs-lookup"><span data-stu-id="6b7ab-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="6b7ab-164">Følgende felter angives automatisk for salgsordretabellen:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="6b7ab-165">**Sprog** – Ordrens sprog (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-166">**Levér til land/område** – Det land eller område, som varerne vil blive leveret til (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-167">**Kontaktperson** – Den bruger, der kan kontaktes for at få oplysninger om ordren (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-168">**Firma** – Den juridiske enhed, som ordren tilhører (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-169">**Potentiel kunde** – Den debitorkonto, der er tilknyttet ordren (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-170">**Fakturakunde** – Odrens faktureringskonto (standardværdien er den potentielle kunde fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-171">**Salgsordrenavn** – Navnet på salgsordren (standardværdien er **salgsordre**).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="6b7ab-172">**Valuta** – Valutaen for prisen (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-173">**Prisliste** – Den tilpassede prisliste til kunden (som standard hentes værdien fra kontaktpersonposten).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="6b7ab-174">**Beskrivelse af leveringsadresse** – Salgsordrens leveringsadresse (standardværdien er **beskrivelse af leveringsadressen**).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="6b7ab-175">Tilpasning af processen til oprettelse af ordrer</span><span class="sxs-lookup"><span data-stu-id="6b7ab-175">Modify the order creation process</span></span>

<span data-ttu-id="6b7ab-176">Du kan frit ændre udseendet og brugergrænsefladen for debitorportalen, hvis du ikke ændrer grundprocessen for oprettelse af ordrer.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="6b7ab-177">Hvis du vil ændre processen for ordreoprettelse, er der nogle få punkter, som du skal huske.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="6b7ab-178">Du må ikke fjerne følgende kolonner fra salgsordretabellen i Microsoft Dataverse, da de skal bruges til at oprette en salgsordre med to skrivninger:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="6b7ab-179">**Firma** – Den juridiske enhed, som ordren tilhører</span><span class="sxs-lookup"><span data-stu-id="6b7ab-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="6b7ab-180">**Navn** – Navnet på salgsordren</span><span class="sxs-lookup"><span data-stu-id="6b7ab-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="6b7ab-181">**Valuta** – Valutaen for prisen</span><span class="sxs-lookup"><span data-stu-id="6b7ab-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="6b7ab-182">**Prisliste** – Tilpasset prisliste til kunden</span><span class="sxs-lookup"><span data-stu-id="6b7ab-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="6b7ab-183">**Levér til land/område** – Det land eller det område, som varerne skal leveres til</span><span class="sxs-lookup"><span data-stu-id="6b7ab-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="6b7ab-184">**Potentiel kunde** – Den kundekonto, der er tilknyttet ordren</span><span class="sxs-lookup"><span data-stu-id="6b7ab-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="6b7ab-185">**Sprog** – Ordresproget (typisk er dette sprog den potentielle kundes sprog).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="6b7ab-186">**Beskrivelse af leveringsadresse** – Salgsordrens leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="6b7ab-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="6b7ab-187">Følgende kolonner er påkrævet for varer:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="6b7ab-188">**Produkt** – Det produkt, der skal bestilles</span><span class="sxs-lookup"><span data-stu-id="6b7ab-188">**Product** – The product to order</span></span>
- <span data-ttu-id="6b7ab-189">**Antal** – Antallet af det valgte produkt</span><span class="sxs-lookup"><span data-stu-id="6b7ab-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="6b7ab-190">**Enhed** – Måleenheden (f.eks **ea**, **kg** eller **kasse**)</span><span class="sxs-lookup"><span data-stu-id="6b7ab-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="6b7ab-191">**Levér til land/område** – Leveringsland eller -område</span><span class="sxs-lookup"><span data-stu-id="6b7ab-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="6b7ab-192">**Beskrivelse af leveringsadresse** – Ordrens leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="6b7ab-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="6b7ab-193">Du skal sikre dig, at debitorportalen kan sende værdier for alle disse kolonner.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="6b7ab-194">Hvis du vil føje kolonner til siden eller fjerne kolonner, kan du finde flere oplysninger under [Oprette eller redigere formularer til hurtig oprettelse for en strømlinet dataindtastningsoplevelse](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="6b7ab-195">Hvis du vil ændre, hvordan kolonner forudindstilles, og hvordan værdier angives, når siden gemmes, skal du se følgende oplysninger i dokumentationen for Power Apps-portalerne:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="6b7ab-196">Udfyldning af felt på forhånd</span><span class="sxs-lookup"><span data-stu-id="6b7ab-196">Prepopulate field</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="6b7ab-197">Angive værdi ved lagring</span><span class="sxs-lookup"><span data-stu-id="6b7ab-197">Set Value On Save</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="6b7ab-198">Tilpasse startsiden</span><span class="sxs-lookup"><span data-stu-id="6b7ab-198">Customize the home page</span></span>

<span data-ttu-id="6b7ab-199">Alle kontrolelementer i debitorportalen er indbyggede kontrolelementer i Power Apps-portalerne.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="6b7ab-200">Du kan tilpasse dem ved at følge trinnene i [Oprette en side](https://docs.microsoft.com/powerapps/maker/portals/compose-page) i dokumentationen for Power Apps- portaler.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-200">You can customize them by following the steps in [Compose a page](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="6b7ab-201">Det eneste brugerdefinerede kontrolelement, der er medtaget i debitorportalskabelonen, bruges til at oprette felterne på startsiden.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="6b7ab-202">![Felter på startsiden](media/customer-portal-home-page-tiles.png "Felter på startsiden")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="6b7ab-203">Følg disse trin for at ændre felterne.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="6b7ab-204">Åbn [Portal Management-appen](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="6b7ab-204">Open the [Portal Management app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="6b7ab-205">Vælg **Sideskabeloner** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="6b7ab-206">![Navigationsruden Portalstyring](media/customer-portal-nav.png "Navigationsruden Portalstyring")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="6b7ab-207">Vælg den sideskabelon, der hedder **Start**.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="6b7ab-208">I feltet **Webskabelon** skal du vælge linket **Start** for at åbne kildekoden for denne side.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="6b7ab-209">![Feltet Webskabelon](media/customer-portal-web-template.png "Feltet Webskabelon")</span><span class="sxs-lookup"><span data-stu-id="6b7ab-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="6b7ab-210">Du kan nu se hele kildekoden for startsiden og ændre den efter behov.</span><span class="sxs-lookup"><span data-stu-id="6b7ab-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="6b7ab-211">Ressourcer</span><span class="sxs-lookup"><span data-stu-id="6b7ab-211">Resources</span></span>

<span data-ttu-id="6b7ab-212">Yderligere oplysninger om, hvordan du kan konfigurere og tilpasse debitorportalen, finder du i følgende ressourcer:</span><span class="sxs-lookup"><span data-stu-id="6b7ab-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="6b7ab-213">Power Apps-dokumentationen til portaler</span><span class="sxs-lookup"><span data-stu-id="6b7ab-213">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="6b7ab-214">Dokumentationen til dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="6b7ab-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="6b7ab-215">Om portalens livscyklus</span><span class="sxs-lookup"><span data-stu-id="6b7ab-215">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="6b7ab-216">Opgradering af en portal</span><span class="sxs-lookup"><span data-stu-id="6b7ab-216">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="6b7ab-217">Overflytning af portalkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6b7ab-217">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="6b7ab-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement-apps</span><span class="sxs-lookup"><span data-stu-id="6b7ab-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]