---
title: Notaintegration
description: I dette emne beskrives integrationen af notadata i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: beab7f2fc4fd96ce7a28734d2449445b3b5d4451
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750830"
---
# <a name="note-integration"></a><span data-ttu-id="e98dd-103">Notaintegration</span><span class="sxs-lookup"><span data-stu-id="e98dd-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e98dd-104">I løbet af Microsoft Dynamics 365-forretningsprocesserne indsamler brugere ofte oplysninger om deres kunder.</span><span class="sxs-lookup"><span data-stu-id="e98dd-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="e98dd-105">Oplysningerne registreres som aktiviteter og notater.</span><span class="sxs-lookup"><span data-stu-id="e98dd-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="e98dd-106">I dette emne beskrives integrationen af notadata i dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="e98dd-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="e98dd-107">Kundeoplysninger kan klassificeres på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="e98dd-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="e98dd-108">**Handlingsbare oplysninger, som en Dynamics 365-bruger håndterer på vegne af en kunde** - f.eks. udfører Contoso (en Dynamics 365-bruger) et spil show.</span><span class="sxs-lookup"><span data-stu-id="e98dd-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="e98dd-109">En af Contosos kunder (en kunde) ønsker at deltage i dette show.</span><span class="sxs-lookup"><span data-stu-id="e98dd-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="e98dd-110">Kunden beder en medarbejder hos Contoso om at booke en plads i spilopvisning for dem.</span><span class="sxs-lookup"><span data-stu-id="e98dd-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="e98dd-111">Reservationen sker i Contosos hændelseskalender.</span><span class="sxs-lookup"><span data-stu-id="e98dd-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="e98dd-112">**Oplysninger, der kan ageres på, for en Dynamics 365-bruger** - En kunde, der køber en Surface-enhed, angiver f.eks., at enheden skal være pakket ind som gave før levering.</span><span class="sxs-lookup"><span data-stu-id="e98dd-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="e98dd-113">Disse instruktioner er oplysninger, der kan anvendes, og som håndteres af den medarbejder hos Contoso, der er ansvarlig for emballagen.</span><span class="sxs-lookup"><span data-stu-id="e98dd-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="e98dd-114">**Oplysninger, der ikke kan ageres på** - En kunde besøger f.eks. Contoso-butikken, og under samtalen med en butiksmedarbejder udtrykkes interessen for *Halo*-spil og spiltilbehør.</span><span class="sxs-lookup"><span data-stu-id="e98dd-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="e98dd-115">Butikspartneren noterer sig disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e98dd-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="e98dd-116">Programmet til produktanbefalinger bruger det derefter til at komme med anbefalinger til kunden.</span><span class="sxs-lookup"><span data-stu-id="e98dd-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="e98dd-117">Generelt registreres handlingsbare oplysninger som *aktiviteter* i Finance and Operations-apps og kundetilfredshedsapps.</span><span class="sxs-lookup"><span data-stu-id="e98dd-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="e98dd-118">Oplysninger, der ikke kan ageres på, registreres som *noter* i Finance and Operations-apps, and som *bemærkninger* i kundetilfredshedsapps.</span><span class="sxs-lookup"><span data-stu-id="e98dd-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="e98dd-119">Notater er beregnet til oplysninger, der ikke kan handlings, men appsene forhindrer dig ikke i at bruge dem til at gemme og håndtere oplysninger, der kan handlings, hvis du vil bruge dem på den måde.</span><span class="sxs-lookup"><span data-stu-id="e98dd-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="e98dd-120">Microsoft frigiver i øjeblikket funktioner til noteintegration.</span><span class="sxs-lookup"><span data-stu-id="e98dd-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="e98dd-121">Funktioner til aktivitetsintegration frigives senere. Notatintegration er tilgængelig for debitorer, kreditorer, salgsordrer og indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="e98dd-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="e98dd-122">Oprette et notat i en kunde aftale-app</span><span class="sxs-lookup"><span data-stu-id="e98dd-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="e98dd-123">Hvis du vil oprette et notat i en kunde aftale-app og derefter synkronisere den med en Finance and Operations-app, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="e98dd-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="e98dd-124">Åbn kontoposten for en kunde i kundetilfredsheds-appen.</span><span class="sxs-lookup"><span data-stu-id="e98dd-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="e98dd-125">Vælg i ruden **Tidslinje** plustegnet (**+**), og vælg derefter **Notat** for at oprette et notat.</span><span class="sxs-lookup"><span data-stu-id="e98dd-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Oprette et notat i en kunde aftale-app](media/notes-ce-1.png)

3. <span data-ttu-id="e98dd-127">Vælg **Tilføj note**, og angiv derefter titel og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e98dd-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Angiv en titel og en beskrivelse.](media/notes-ce-2.png)

    <span data-ttu-id="e98dd-129">Det nye notat føjes til debitortidslinjen.</span><span class="sxs-lookup"><span data-stu-id="e98dd-129">The new note is added to the customer timeline.</span></span>

    ![Nyt notat på debitortidslinjen](media/notes-ce-3.png)

4. <span data-ttu-id="e98dd-131">Logge på appen Finance and Operations, og åbn den samme kundepost.</span><span class="sxs-lookup"><span data-stu-id="e98dd-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="e98dd-132">Bemærk, at knappen **Vedhæftede filer** (papirklipssymbolet) øverst til højre angiver, at posten er vedhæftet.</span><span class="sxs-lookup"><span data-stu-id="e98dd-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Besked om en vedhæftet fil](media/notes-ce-4.png)

5. <span data-ttu-id="e98dd-134">Vælg knappen **Vedhæftede filer** for at åbne siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="e98dd-135">Du skal finde det notat, du har oprettet i kundens aftale-app.</span><span class="sxs-lookup"><span data-stu-id="e98dd-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Notat fra customer aftale-appen](media/notes-ce-5.png)

<span data-ttu-id="e98dd-137">Eventuelle opdateringer af notatet synkroniseres frem og tilbage mellem Finance and Operations-appen og kundens aftale-app.</span><span class="sxs-lookup"><span data-stu-id="e98dd-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="e98dd-138">Oprette et notat i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="e98dd-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="e98dd-139">Du kan også oprette et notat i en Finance and Operations-app og derefter synkronisere den med en kundeaftale-app.</span><span class="sxs-lookup"><span data-stu-id="e98dd-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="e98dd-140">Hvis du vil oprette et notat i en Finance and Operations-app og derefter synkronisere den med en kundeaftale-app, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="e98dd-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="e98dd-141">I appen Finance and Operations på siden **Vedhæftede filer** skal du vælge **Ny** \> **Note**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Oprette et notat i en Finance and Operations-app](media/notes-fo-1.png)

2. <span data-ttu-id="e98dd-143">Angiv en titel og et kort sæt instruktioner, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Angiv en titel og beskrivelse.](media/notes-fo-2.png)

3. <span data-ttu-id="e98dd-145">Opdater posten i kundeengagementsappen.</span><span class="sxs-lookup"><span data-stu-id="e98dd-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="e98dd-146">Du skal finde det nye notat på tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="e98dd-146">You should find the new note on the timeline.</span></span>

    ![Nyt notat på tidslinjen i customer aftale-appen](media/notes-fo-3.png)

<span data-ttu-id="e98dd-148">Du kan klassificere en note som enten intern eller ekstern.</span><span class="sxs-lookup"><span data-stu-id="e98dd-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="e98dd-149">I Finance and Operations-appen på siden **Vedhæftede filer** skal du åbne noten og derefter i feltet **Begrænsning** vælge **Intern** eller **Ekstern**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Begrænsningsfelt](media/notes-fo-4.png)

<span data-ttu-id="e98dd-151">Du kan også oprette en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e98dd-151">You can also create a URL.</span></span>

1. <span data-ttu-id="e98dd-152">I appen Finance and Operations på siden **Vedhæftede filer** skal du vælge **Ny** \> **URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="e98dd-153">Angiv en titel og en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e98dd-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="e98dd-154">I feltet **Begrænsning** vælges **Intern** eller **Ekstern**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Opret en URL-adresse i Finance and Operations-app'en](media/notes-fo-5.png)

4. <span data-ttu-id="e98dd-156">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e98dd-156">Select **Save**.</span></span>

    <span data-ttu-id="e98dd-157">Da apps til kundeengagement ikke har en URL-type, er URL-adressen integreret med skriv som et notat.</span><span class="sxs-lookup"><span data-stu-id="e98dd-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL-adressen vises som et notat i en kundeaftale-app](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="e98dd-159">Filer, der er vedhæftede filer, understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="e98dd-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="e98dd-160">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="e98dd-160">Templates</span></span>

<span data-ttu-id="e98dd-161">Noteintegration omfatter en samling af tabeltilknytninger, der arbejder sammen i forbindelse med datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e98dd-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="e98dd-162">Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="e98dd-162">Finance and Operations app</span></span> | <span data-ttu-id="e98dd-163">Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="e98dd-163">Customer engagement app</span></span> | <span data-ttu-id="e98dd-164">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="e98dd-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="e98dd-165">Vedhæftede filer for debitorer</span><span class="sxs-lookup"><span data-stu-id="e98dd-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="e98dd-166">Anmærkning</span><span class="sxs-lookup"><span data-stu-id="e98dd-166">Annotations</span></span> | <span data-ttu-id="e98dd-167">Virksomheder, der bruger almindelig tekst og URL-adresser til at hente kundespecifikke oplysninger (for både organisationer og personer).</span><span class="sxs-lookup"><span data-stu-id="e98dd-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="e98dd-168">Vedhæftede kreditordokumenter</span><span class="sxs-lookup"><span data-stu-id="e98dd-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="e98dd-169">Anmærkning</span><span class="sxs-lookup"><span data-stu-id="e98dd-169">Annotations</span></span> | <span data-ttu-id="e98dd-170">Virksomheder, der bruger almindelig tekst og URL-adresser til at hente leverandørspecifikke oplysninger (for både organisationer og personer).</span><span class="sxs-lookup"><span data-stu-id="e98dd-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="e98dd-171">Vedhæftede dokumenter til salgsordrehoved</span><span class="sxs-lookup"><span data-stu-id="e98dd-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="e98dd-172">Anmærkning</span><span class="sxs-lookup"><span data-stu-id="e98dd-172">Annotations</span></span> | <span data-ttu-id="e98dd-173">Virksomheder, der bruger almindelig tekst og URL-adresser til at registrere salgsordrespecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e98dd-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="e98dd-174">Vedhæftede dokumenter til indkøbsordrehoved</span><span class="sxs-lookup"><span data-stu-id="e98dd-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="e98dd-175">Anmærkning</span><span class="sxs-lookup"><span data-stu-id="e98dd-175">Annotations</span></span> | <span data-ttu-id="e98dd-176">Virksomheder, der bruger almindelig tekst og URL-adresser til at registrere købsordrespecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e98dd-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="e98dd-177">Du kan finde flere oplysninger i [referencen til tilknytning af dobbeltskrivning](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e98dd-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
