---
title: Mobilfakturagodkendelser
description: Dette emne er beregnet til at give en praktisk tilgang til design af scenarier for mobilenheder via en brugssag om godkendelser af kreditorfakturaer til mobilenheder.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dd72c8a54498cc6ffae7125c5c2f44bfac5a5995
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658638"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="783cb-103">Mobilfakturagodkendelser</span><span class="sxs-lookup"><span data-stu-id="783cb-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="783cb-104">Virksomhedsbrugere kan designe mobiloplevelser med mobilfunktioner.</span><span class="sxs-lookup"><span data-stu-id="783cb-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="783cb-105">I avancerede scenarier kan udviklere også udvide funktionerne, som de ønsker.</span><span class="sxs-lookup"><span data-stu-id="783cb-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="783cb-106">Den mest effektive måde at lære nogle af de nye begreber til mobilenheder på er ved at gennemgå processen med at designe et par scenarier.</span><span class="sxs-lookup"><span data-stu-id="783cb-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="783cb-107">Dette emne er beregnet til at give en praktisk tilgang til design af scenarier for mobilenheder via en brugssag om godkendelser af kreditorfakturaer til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="783cb-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="783cb-108">Dette emne kan hjælpe dig med at designe andre variationer af scenarier og kan også anvendes til andre scenarier, der ikke er relateret til kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="783cb-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="783cb-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="783cb-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="783cb-110">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="783cb-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="783cb-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="783cb-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="783cb-112">Håndbog til forhåndslæsning om brug af mobilenhed</span><span class="sxs-lookup"><span data-stu-id="783cb-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="783cb-113">Mobilplatform</span><span class="sxs-lookup"><span data-stu-id="783cb-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="783cb-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="783cb-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="783cb-115">Et miljø, der har version 1611 og Platform update 3 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="783cb-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="783cb-116">Installer hotfix-KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="783cb-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="783cb-117">Arbejdsrutineoptager kan fejlagtigt optage to Luk-kommandoer til rullelistedialogbokse. Dette er medtaget i Platform update 3 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="783cb-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="783cb-118">Installer hotfix-KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="783cb-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="783cb-119">Dette hotfix gør det muligt at se vedhæftede filer på mobilklienten. Dette er medtaget i Platform update 3 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="783cb-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="783cb-120">Installer hotfix-KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="783cb-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="783cb-121">Programkode til applikationen til godkendelse af kreditorfakturaer på mobilenheder. Dette er inkluderet i version 7.0.1 (maj 2016).</span><span class="sxs-lookup"><span data-stu-id="783cb-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="783cb-122">En Android- eller iOS- eller en Windows-enhed, hvor mobilappen til er installeret.</span><span class="sxs-lookup"><span data-stu-id="783cb-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="783cb-123">Søg efter appen i den relevante appbutik.</span><span class="sxs-lookup"><span data-stu-id="783cb-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="783cb-124">Introduktion</span><span class="sxs-lookup"><span data-stu-id="783cb-124">Introduction</span></span>
<span data-ttu-id="783cb-125">Godkendelser af kreditorfakturaer på mobilenheder kræver tre de hotfixes, der er nævnt i afsnittet "Forudsætninger".</span><span class="sxs-lookup"><span data-stu-id="783cb-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="783cb-126">Disse hotfixes giver ikke et arbejdsområde til godkendelse af fakturaer.</span><span class="sxs-lookup"><span data-stu-id="783cb-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="783cb-127">Hvis du vil vide, hvad er et arbejdsområde er i forbindelse med mobilenheder, skal du læse håndbogen til mobilenheder, der er nævnt i afsnittet "Forudsætninger".</span><span class="sxs-lookup"><span data-stu-id="783cb-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="783cb-128">Arbejdsområdet til godkendelse af fakturaer skal udformes.</span><span class="sxs-lookup"><span data-stu-id="783cb-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="783cb-129">Hver organisation organiserer og definerer sin forretningsproces for kreditorfakturaer på sin egen måde.</span><span class="sxs-lookup"><span data-stu-id="783cb-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="783cb-130">Før du designer en mobiloplevelse til godkendelse af kreditorfakturaer, skal du overveje følgende aspekter af forretningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="783cb-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="783cb-131">Ideen er at bruge disse datapunkter så meget som muligt for at optimere brugeroplevelsen på enheden.</span><span class="sxs-lookup"><span data-stu-id="783cb-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="783cb-132">Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="783cb-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="783cb-133">Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="783cb-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="783cb-134">Hvor mange fakturalinjer er der i en faktura?</span><span class="sxs-lookup"><span data-stu-id="783cb-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="783cb-135">Anvend 80-20-reglen her, og optimer til 80 procent.</span><span class="sxs-lookup"><span data-stu-id="783cb-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="783cb-136">Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</span><span class="sxs-lookup"><span data-stu-id="783cb-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="783cb-137">Hvis svaret på dette spørgsmål er ja, skal du overveje følgende spørgsmål:</span><span class="sxs-lookup"><span data-stu-id="783cb-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="783cb-138">Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer, opdelinger osv.) er der for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="783cb-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="783cb-139">Igen anvend 80-20-reglen.</span><span class="sxs-lookup"><span data-stu-id="783cb-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="783cb-140">Har fakturaerne også regnskabsfordelinger i fakturahovedet?</span><span class="sxs-lookup"><span data-stu-id="783cb-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="783cb-141">I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</span><span class="sxs-lookup"><span data-stu-id="783cb-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="783cb-142">Dette emne forklarer ikke, hvordan du redigerer regnskabsfordelinger, fordi denne funktion i øjeblikket ikke understøttes for mobilscenarier.</span><span class="sxs-lookup"><span data-stu-id="783cb-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="783cb-143">Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</span><span class="sxs-lookup"><span data-stu-id="783cb-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="783cb-144">Hvilke mobilfunktioner der skal bruges til godkendelse af fakturaer, afhænger af svarene på disse spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="783cb-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="783cb-145">Målet er at optimere brugeroplevelsen af forretningsprocessen på mobilenhederne i en organisation.</span><span class="sxs-lookup"><span data-stu-id="783cb-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="783cb-146">I resten af dette emne ser vi på to scenarievariationer, der er baseret på forskellige svar på de foregående spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="783cb-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="783cb-147">Som hovedregel når du arbejder med designeren til mobilenheder skal du sørge for at "publicere" ændringerne for at undgå at miste opdateringerne.</span><span class="sxs-lookup"><span data-stu-id="783cb-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="783cb-148">Designe et simpelt fakturagodkendelsesscenario til Contoso</span><span class="sxs-lookup"><span data-stu-id="783cb-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783cb-149">Scenarieattribut</span><span class="sxs-lookup"><span data-stu-id="783cb-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="783cb-150">Besvar</span><span class="sxs-lookup"><span data-stu-id="783cb-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="783cb-151">Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="783cb-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="783cb-152">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="783cb-152">Vendor name</span></span></li>
<li><span data-ttu-id="783cb-153">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="783cb-153">Invoice total</span></span></li>
<li><span data-ttu-id="783cb-154">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="783cb-154">Invoice account</span></span></li>
<li><span data-ttu-id="783cb-155">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="783cb-155">Invoice number</span></span></li>
<li><span data-ttu-id="783cb-156">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="783cb-156">Invoice date</span></span></li>
<li><span data-ttu-id="783cb-157">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="783cb-157">Invoice description</span></span></li>
<li><span data-ttu-id="783cb-158">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="783cb-158">Due date</span></span></li>
<li><span data-ttu-id="783cb-159">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="783cb-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="783cb-160">Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="783cb-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="783cb-161">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="783cb-161">Procurement category</span></span></li>
<li><span data-ttu-id="783cb-162">Mængde</span><span class="sxs-lookup"><span data-stu-id="783cb-162">Quantity</span></span></li>
<li><span data-ttu-id="783cb-163">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="783cb-163">Unit price</span></span></li>
<li><span data-ttu-id="783cb-164">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="783cb-164">Line net amount</span></span></li>
<li><span data-ttu-id="783cb-165">1099-beløb</span><span class="sxs-lookup"><span data-stu-id="783cb-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="783cb-166">Hvor mange fakturalinjer er der i en faktura?</span><span class="sxs-lookup"><span data-stu-id="783cb-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="783cb-167">Anvend 80-20-reglen her, og optimer til 80 procent.</span><span class="sxs-lookup"><span data-stu-id="783cb-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="783cb-168">1</span><span class="sxs-lookup"><span data-stu-id="783cb-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="783cb-169">Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</span><span class="sxs-lookup"><span data-stu-id="783cb-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="783cb-170">Ja</span><span class="sxs-lookup"><span data-stu-id="783cb-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="783cb-171">Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer osv.) er der for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="783cb-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="783cb-172">Igen anvend 80-20-reglen.</span><span class="sxs-lookup"><span data-stu-id="783cb-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="783cb-173">Udvidet pris: 2 Moms: 0 Gebyrer: 0</span><span class="sxs-lookup"><span data-stu-id="783cb-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="783cb-174">Har fakturaerne også regnskabsfordelinger i fakturahovedet?</span><span class="sxs-lookup"><span data-stu-id="783cb-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="783cb-175">I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</span><span class="sxs-lookup"><span data-stu-id="783cb-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="783cb-176">Bruges ikke</span><span class="sxs-lookup"><span data-stu-id="783cb-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="783cb-177">Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</span><span class="sxs-lookup"><span data-stu-id="783cb-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="783cb-178">Ja</span><span class="sxs-lookup"><span data-stu-id="783cb-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="783cb-179">Oprette arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-179">Create the workspace</span></span>

1.  <span data-ttu-id="783cb-180">I en browser, og log på programmet.</span><span class="sxs-lookup"><span data-stu-id="783cb-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="783cb-181">Når du har logget på, kan du tilføje **&mode=mobile** til URL-adressen som vist i følgende eksempel og opdatere siden: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="783cb-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="783cb-182">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="783cb-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="783cb-183">Mobilappdesigneren skal vises på samme måde som Arbejdsrutineoptager vises.</span><span class="sxs-lookup"><span data-stu-id="783cb-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="783cb-184">Klik på **Tilføj** for at oprette et nyt arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="783cb-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="783cb-185">I dette eksempel skal du navngive arbejdsområdet **Mine godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="783cb-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="783cb-186">Angiv en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="783cb-186">Enter a description.</span></span>
6.  <span data-ttu-id="783cb-187">Vælg en farve til arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-187">Select a workspace color.</span></span> <span data-ttu-id="783cb-188">Arbejdsområdets farve skal bruges til mobilfunktionernes overordnede udseende i dette arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="783cb-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="783cb-189">Vælg et ikon til arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="783cb-190">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="783cb-190">Click **Done**</span></span>
9.  <span data-ttu-id="783cb-191">Klik på **Publicer arbejdsområde** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="783cb-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="783cb-192">Kreditorfakturaer, der er tildelt til mig</span><span class="sxs-lookup"><span data-stu-id="783cb-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="783cb-193">Den første mobilenhedsside, du skal designe, er listen over de fakturaer, der er tildelt til brugeren til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="783cb-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="783cb-194">For at udforme denne mobilside skal du bruge siden **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="783cb-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="783cb-195">Før du kan udføre denne procedure skal du sørge for, at mindst én kreditorfaktura er tildelt til dig til gennemsyn, og at fakturalinjen har to fordelinger.</span><span class="sxs-lookup"><span data-stu-id="783cb-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="783cb-196">Denne opsætning opfylder kravene i dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="783cb-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="783cb-197">I URL-adressen skal du erstatte navnet på menupunktet med **VendMobileInvoiceAssignedToMeListPage** for at åbne mobilversionen af listesiden **Afventende kreditorfakturaer tildelt til mig** i **Kreditor**-modulet.</span><span class="sxs-lookup"><span data-stu-id="783cb-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="783cb-198">Afhængigt af antallet af fakturaer, der er tildelt til dig i dit system, viser denne side fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="783cb-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="783cb-199">Når du vil finde en bestemt faktura, kan du bruge filteret til venstre.</span><span class="sxs-lookup"><span data-stu-id="783cb-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="783cb-200">Men vi har ikke brug for en bestemt faktura i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="783cb-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="783cb-201">Vi skal bare bruge en faktura, der er tildelt til dig, så du kan få adgang til at designe siden til mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="783cb-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="783cb-202">De nye sider, der er tilgængelige, er designet specifikt til udvikling af scenarier for kreditorfakturaer på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="783cb-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="783cb-203">Derfor skal du bruge disse sider.</span><span class="sxs-lookup"><span data-stu-id="783cb-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="783cb-204">URL-adressen skal ligne følgende URL-adresse, og når du har angivet den, skal den side, der er vist i illustrationen, vises: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="783cb-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="783cb-205">[![Siden Afventende kreditorfakturaer tildelt til mig](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="783cb-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="783cb-206">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="783cb-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="783cb-207">Vælg dit arbejdsområde, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="783cb-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="783cb-208">Klik på **Tilføj side** for at oprette den første side til mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="783cb-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="783cb-209">Angiv et navn, f.eks. **Mine kreditorfakturaer**, og en beskrivelse, f.eks. **Kreditorfakturaer, der er tildelt til mig til gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="783cb-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="783cb-210">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="783cb-210">Click **Done**.</span></span>
7.  <span data-ttu-id="783cb-211">I designeren til mobilenheder skal du under fanen **Felter** klikke på **Vælg felter**.</span><span class="sxs-lookup"><span data-stu-id="783cb-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="783cb-212">Kolonnerne på listesiden skal ligne den følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="783cb-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="783cb-213">[![Kolonner i de afventende kreditorfakturaer, der er tildelt mig](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="783cb-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="783cb-214">Tilføj de kolonner, der kræves, fra den listeside, der skal vises for brugere på mobilenhedssiden.</span><span class="sxs-lookup"><span data-stu-id="783cb-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="783cb-215">Den rækkefølge, som du tilføjer i, er den rækkefølge, som felterne bliver vist i for slutbrugeren.</span><span class="sxs-lookup"><span data-stu-id="783cb-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="783cb-216">Den eneste måde at ændre rækkefølgen af felterne er ved igen at vælge alle felter.</span><span class="sxs-lookup"><span data-stu-id="783cb-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="783cb-217">Baseret på kravene til dette scenario er de følgende otte felter obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="783cb-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="783cb-218">Men nogle brugere vil mene, at otte felter er for mange oplysninger på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="783cb-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="783cb-219">Derfor vil vi kun vise de vigtigste felter i listevisningen til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="783cb-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="783cb-220">De resterende felter vises i detaljevisningen, som vi udformer senere.</span><span class="sxs-lookup"><span data-stu-id="783cb-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="783cb-221">Nu skal vi tilføje følgende felter.</span><span class="sxs-lookup"><span data-stu-id="783cb-221">For now, we will add the following fields.</span></span> <span data-ttu-id="783cb-222">Klik på plustegnet (**+**) i disse kolonner for at føje dem til siden på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="783cb-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="783cb-223">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="783cb-223">Vendor name</span></span>
    - <span data-ttu-id="783cb-224">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="783cb-224">Invoice total</span></span>
    - <span data-ttu-id="783cb-225">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="783cb-225">Invoice account</span></span>
    - <span data-ttu-id="783cb-226">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="783cb-226">Invoice number</span></span>
    - <span data-ttu-id="783cb-227">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="783cb-227">Invoice date</span></span>

  <span data-ttu-id="783cb-228">Når felterne er tilføjet, skal siden ligne følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="783cb-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
   <span data-ttu-id="783cb-229">[![Side, efter at der er tilføjet felter](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="783cb-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="783cb-230">Du skal også tilføje følgende kolonner nu, så vi senere kan aktivere arbejdsganghandlinger.</span><span class="sxs-lookup"><span data-stu-id="783cb-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="783cb-231">Vis fuldført opgave</span><span class="sxs-lookup"><span data-stu-id="783cb-231">Show complete task</span></span>
    - <span data-ttu-id="783cb-232">Vis delegeret opgave</span><span class="sxs-lookup"><span data-stu-id="783cb-232">Show delegate task</span></span>
    - <span data-ttu-id="783cb-233">Vis tilbagekaldelsesopgave</span><span class="sxs-lookup"><span data-stu-id="783cb-233">Show recall task</span></span>
    - <span data-ttu-id="783cb-234">Vis afvist opgave</span><span class="sxs-lookup"><span data-stu-id="783cb-234">Show reject task</span></span>
    - <span data-ttu-id="783cb-235">Vis anmodningsfuldførelsesopgave</span><span class="sxs-lookup"><span data-stu-id="783cb-235">Show request completion task</span></span>
    - <span data-ttu-id="783cb-236">Vis send igen-opgave</span><span class="sxs-lookup"><span data-stu-id="783cb-236">Show resubmit task</span></span>

10. <span data-ttu-id="783cb-237">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="783cb-238">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="783cb-239">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="783cb-240">Aktiver **Vis fakturatotal på ventende kreditorfakturaliste** i formen med kreditorparametre under **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="783cb-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="783cb-241">Bemærk, at kun hvis denne parameter aktiveres, beregnes fakturatotaler og vises på listesiden over ventende kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="783cb-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="783cb-242">Dette er en ny funktion som en del af det nødvendige hot fix 3208224.</span><span class="sxs-lookup"><span data-stu-id="783cb-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="783cb-243">Detaljer i kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="783cb-243">Vendor invoice details</span></span>

<span data-ttu-id="783cb-244">Når du vil designe siden med fakturadetaljer til mobilenheder, skal du bruge siden **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="783cb-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="783cb-245">Bemærk, at afhængigt af antallet af fakturaer, du har i dit system, viser denne side den ældste faktura (faktura, der blev oprettet først).</span><span class="sxs-lookup"><span data-stu-id="783cb-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="783cb-246">Når du vil finde en bestemt faktura, kan du bruge filteret til venstre.</span><span class="sxs-lookup"><span data-stu-id="783cb-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="783cb-247">Men vi har ikke brug for en bestemt faktura i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="783cb-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="783cb-248">Vi skal blot bruge nogle fakturadata, så vi kan designe siden.</span><span class="sxs-lookup"><span data-stu-id="783cb-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="783cb-249">[![Siden Arbejdsgang](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="783cb-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="783cb-250">I URL-adressen til skal du erstatte navnet på menupunktet med **VendMobileInvoiceHeaderDetails** for at åbne formen</span><span class="sxs-lookup"><span data-stu-id="783cb-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="783cb-251">Åbn designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="783cb-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="783cb-252">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="783cb-253">Vælg siden **Mine kreditorfakturaer**, som du oprettede tidligere, og klik derefter på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="783cb-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="783cb-254">Under fanen **Felter** skal du klikke på kolonneoverskriften **Gitter**.</span><span class="sxs-lookup"><span data-stu-id="783cb-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="783cb-255">Klik på **Egenskaber &gt; Tilføj side**.</span><span class="sxs-lookup"><span data-stu-id="783cb-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="783cb-256">**Bemærk:** Når du klikker på overskriften **Gitter** og tilføjer en side, oprettes relationen med detaljesiden automatisk.</span><span class="sxs-lookup"><span data-stu-id="783cb-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="783cb-257">Angiv en sidetitel, f.eks. **Fakturadetaljer** og en beskrivelse som **Vis fakturahoved og linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="783cb-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="783cb-258">Klik på **Vælg felter**.</span><span class="sxs-lookup"><span data-stu-id="783cb-258">Click **Select fields**.</span></span> <span data-ttu-id="783cb-259">Bemærk, at den rækkefølge, som du tilføjer i, er den rækkefølge, som felterne bliver vist i for slutbrugeren.</span><span class="sxs-lookup"><span data-stu-id="783cb-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="783cb-260">Den eneste måde at ændre rækkefølgen af felterne er ved igen at vælge alle felter.</span><span class="sxs-lookup"><span data-stu-id="783cb-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="783cb-261">Baseret på kravene til dette scenario skal du tilføje følgende felter fra hovedet:</span><span class="sxs-lookup"><span data-stu-id="783cb-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="783cb-262">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="783cb-262">Vendor name</span></span>
   - <span data-ttu-id="783cb-263">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="783cb-263">Invoice total</span></span>
   - <span data-ttu-id="783cb-264">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="783cb-264">Invoice account</span></span>
   - <span data-ttu-id="783cb-265">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="783cb-265">Invoice number</span></span>
   - <span data-ttu-id="783cb-266">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="783cb-266">Invoice date</span></span>
   - <span data-ttu-id="783cb-267">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="783cb-267">Invoice description</span></span>
   - <span data-ttu-id="783cb-268">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="783cb-268">Due date</span></span>
   - <span data-ttu-id="783cb-269">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="783cb-269">Invoice currency</span></span>

10. <span data-ttu-id="783cb-270">Tilføj følgende felter fra gitterlinjerne på siden:</span><span class="sxs-lookup"><span data-stu-id="783cb-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="783cb-271">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="783cb-271">Procurement category</span></span>
    - <span data-ttu-id="783cb-272">Mængde</span><span class="sxs-lookup"><span data-stu-id="783cb-272">Quantity</span></span>
    - <span data-ttu-id="783cb-273">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="783cb-273">Unit price</span></span>
    - <span data-ttu-id="783cb-274">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="783cb-274">Line net amount</span></span>
    - <span data-ttu-id="783cb-275">1099-beløb</span><span class="sxs-lookup"><span data-stu-id="783cb-275">1099 amount</span></span>

11. <span data-ttu-id="783cb-276">Når alle felter fra de forrige to trin er tilføjet, skal du klikke på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="783cb-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="783cb-277">Siden skal ligne følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="783cb-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="783cb-278">[![Side, efter at der er tilføjet felter](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="783cb-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="783cb-279">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="783cb-280">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="783cb-281">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="783cb-282">Arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="783cb-282">Workflow actions</span></span>

<span data-ttu-id="783cb-283">Brug siden **VendMobileInvoiceHeaderDetails** for at tilføje arbejdsgangshandlinger.</span><span class="sxs-lookup"><span data-stu-id="783cb-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="783cb-284">Erstat navnet på menupunktet i URL-adressen, hvis du vil åbne denne side, som du gjorde tidligere.</span><span class="sxs-lookup"><span data-stu-id="783cb-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="783cb-285">Åbn derefter designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="783cb-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="783cb-286">Følg disse trin for at føje arbejdsgangshandlinger til detaljesiden.</span><span class="sxs-lookup"><span data-stu-id="783cb-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="783cb-287">Der skal være tildelt fakturaer til dig, der er i en tilstand, der kan gøre de arbejdsgangshandlinger, du skal udforme, tilgængelige for dig.</span><span class="sxs-lookup"><span data-stu-id="783cb-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="783cb-288">Registrere arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="783cb-288">Record workflow actions</span></span>
1.  <span data-ttu-id="783cb-289">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="783cb-290">Vælg siden **Fakturadetaljer**, som du oprettede tidligere, og klik derefter på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="783cb-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="783cb-291">Klik på **Tilføj handling** under fanen **Handlinger**.</span><span class="sxs-lookup"><span data-stu-id="783cb-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="783cb-292">Angiv en titel til handlingen, f.eks. **Godkend**, og en beskrivelse, f.eks. **Godkend faktura**.</span><span class="sxs-lookup"><span data-stu-id="783cb-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="783cb-293">Bemærk, at den handlingstitel, du angiver her, bliver navnet på den handling, der vises for brugeren i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="783cb-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="783cb-294">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="783cb-294">Click **Done**.</span></span>
6.  <span data-ttu-id="783cb-295">Klik på **Vælg felter**.</span><span class="sxs-lookup"><span data-stu-id="783cb-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="783cb-296">Gennemgå arbejdsgangen på siden **VendMobileInvoiceHeaderDetails**, og udfør den handling, du ønskede at registrere.</span><span class="sxs-lookup"><span data-stu-id="783cb-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="783cb-297">Sørg for at indtaste kommentarer til arbejdsgangen under denne proces, så et kommentarfelt også er inkluderet i mobiloplevelsen.</span><span class="sxs-lookup"><span data-stu-id="783cb-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="783cb-298">Når du har kørt arbejdsgangshandlingen, skal du klikke på **Udført** for at fuldføre opgaven Vælg felter.</span><span class="sxs-lookup"><span data-stu-id="783cb-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="783cb-299">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="783cb-300">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="783cb-301">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="783cb-302">Gentag de foregående trin for at registrere de påkrævede arbejdsgangshandlinger.</span><span class="sxs-lookup"><span data-stu-id="783cb-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="783cb-303">Oprette en .js-fil</span><span class="sxs-lookup"><span data-stu-id="783cb-303">Create a .js file</span></span>
1. <span data-ttu-id="783cb-304">Åbn Notesblok eller Microsoft Visual Studio, og indsæt følgende kode.</span><span class="sxs-lookup"><span data-stu-id="783cb-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="783cb-305">Gem filen som en .js-fil.</span><span class="sxs-lookup"><span data-stu-id="783cb-305">Save the file as a .js file.</span></span> <span data-ttu-id="783cb-306">Denne kode gør følgende:</span><span class="sxs-lookup"><span data-stu-id="783cb-306">This code does the following:</span></span>
    - <span data-ttu-id="783cb-307">Den skjuler de ekstra arbejdsgang-relaterede kolonner, som vi tidligere tilføjede på listeside til mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="783cb-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="783cb-308">Vi tilføjede disse kolonner, så appen har disse oplysninger i den rette sammenhæng og kan udføre det næste trin.</span><span class="sxs-lookup"><span data-stu-id="783cb-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="783cb-309">Baseret på, hvilket trin i arbejdsgangen der er aktivt, anvender den regler, så kun disse handlinger viser.</span><span class="sxs-lookup"><span data-stu-id="783cb-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="783cb-310">Navnet på siderne og andre kontrolelementer i koden skal være det samme som navnene i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="783cb-311">Overfør kodefilen til arbejdsområdet ved at vælge fanen **Regel**</span><span class="sxs-lookup"><span data-stu-id="783cb-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="783cb-312">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="783cb-313">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="783cb-314">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="783cb-315">Vedhæftede filer i kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="783cb-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="783cb-316">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="783cb-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="783cb-317">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="783cb-318">Vælg siden <strong>Fakturadetaljer\*\*, som du oprettede tidligere, og klik derefter på \*\*Rediger</strong>.</span><span class="sxs-lookup"><span data-stu-id="783cb-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="783cb-319">Indstil **Dokumentstyring** til **Ja** som vist nedenfor.</span><span class="sxs-lookup"><span data-stu-id="783cb-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="783cb-320">**Bemærk:** Hvis der er ikke er krav om at vise vedhæftede filer på mobilenheden, kan du lade denne indstilling være sat til **Nej**, som er standardindstillingen.</span><span class="sxs-lookup"><span data-stu-id="783cb-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Dokumentstyring](./media/docmanagement-216x300.png)

5. <span data-ttu-id="783cb-322">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="783cb-323">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="783cb-324">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="783cb-325">Fordelinger af kreditorfakturalinjer</span><span class="sxs-lookup"><span data-stu-id="783cb-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="783cb-326">Kravene til dette scenario bekræfter, at der kun skal være fordelinger på linjeniveau, og at en faktura har altid kun én linje.</span><span class="sxs-lookup"><span data-stu-id="783cb-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="783cb-327">Da dette scenario er enkelt, skal brugeroplevelsen på mobilenheden også være så enkel, at brugeren ikke behøver at foretage detaljeopløftning på flere niveauer for at få vist fordelingerne.</span><span class="sxs-lookup"><span data-stu-id="783cb-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="783cb-328">Kreditorfakturaer omfatter muligheden for at se alle fordelinger fra fakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="783cb-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="783cb-329">Det er denne oplevelse, vi har brug for til scenariet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="783cb-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="783cb-330">Derfor benytter vi siden **VendMobileInvoiceAllDistributionTree** til at designe denne del af scenariet.</span><span class="sxs-lookup"><span data-stu-id="783cb-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="783cb-331">Når vi kender kravene, hjælper det os med at afgøre, hvilken specifik side vi skal bruge, og hvordan nøjagtigt vi skal optimere mobiloplevelsen for brugeren, når vi udformer scenariet.</span><span class="sxs-lookup"><span data-stu-id="783cb-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="783cb-332">I det andet scenario bruger vi en anden side til at vise fordelingerne, da kravene til dette scenario er anderledes.</span><span class="sxs-lookup"><span data-stu-id="783cb-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="783cb-333">I URL-adressen skal du erstatte navnet på menupunktet, som du gjorde tidligere.</span><span class="sxs-lookup"><span data-stu-id="783cb-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="783cb-334">Den side, der vises, skal ligne følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="783cb-334">The page that appears should resemble the following illustration.</span></span>

<span data-ttu-id="783cb-335">[![Siden Alle fordelinger](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="783cb-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="783cb-336">Åbn designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="783cb-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="783cb-337">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="783cb-338">**Bemærk:** Du kan se, at to nye sider blev oprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="783cb-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="783cb-339">Systemet opretter disse sider, fordi du aktiverede dokumentstyring i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="783cb-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="783cb-340">Du kan ignorere disse nye sider.</span><span class="sxs-lookup"><span data-stu-id="783cb-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="783cb-341">Klik på **Tilføj side**.</span><span class="sxs-lookup"><span data-stu-id="783cb-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="783cb-342">Angiv en titel som **Vis regnskab** og en beskrivelse som **Vis regnskab for fakturaen**.</span><span class="sxs-lookup"><span data-stu-id="783cb-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="783cb-343">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="783cb-343">Click **Done**.</span></span>

7.  <span data-ttu-id="783cb-344">Under fanen **Felter** skal du klikke på **Vælg felter** og vælge følgende felter fra fordelingssiden og derefter klikke på **Udført**:</span><span class="sxs-lookup"><span data-stu-id="783cb-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="783cb-345">Beløb</span><span class="sxs-lookup"><span data-stu-id="783cb-345">Amount</span></span>
    2.  <span data-ttu-id="783cb-346">Valuta</span><span class="sxs-lookup"><span data-stu-id="783cb-346">Currency</span></span>
    3.  <span data-ttu-id="783cb-347">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="783cb-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="783cb-348">Vi ikke har valgt kolonnen **Beskrivelse** fra fordelingsgitteret, fordi kravene til dette scenario bekræftede, at den udvidede pris er det eneste beløb, vil der være fordelinger for.</span><span class="sxs-lookup"><span data-stu-id="783cb-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="783cb-349">Brugeren har derfor ikke brug et andet felt til at bestemme den beløbstype, som vedrører fordelingen.</span><span class="sxs-lookup"><span data-stu-id="783cb-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="783cb-350">Men i det næste scenario **bruger** vi disse oplysninger, fordi kravene til dette scenarie angiver, at andre beløbstyper har fordelinger (for eksempel moms).</span><span class="sxs-lookup"><span data-stu-id="783cb-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="783cb-351">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="783cb-352">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="783cb-353">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-353">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="783cb-354">Siden **Vis regnskab** til mobilenheder er ikke aktuelt knyttet til nogen af de sider til mobilenheder, vi har udviklet indtil videre.</span><span class="sxs-lookup"><span data-stu-id="783cb-354">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="783cb-355">Da brugeren skal kunne navigere til siden **Vis regnskab** fra siden **Fakturaoplysninger** på mobilenheden, skal vi sørge for navigation fra siden **Fakturadetaljer** til siden **Vis regnskab**.</span><span class="sxs-lookup"><span data-stu-id="783cb-355">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="783cb-356">Vi opretter denne navigation ved hjælp af yderligere logik via JavaScript.</span><span class="sxs-lookup"><span data-stu-id="783cb-356">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="783cb-357">Åbn den .js-fil, du oprettede tidligere, og tilføj de linjer, der er fremhævet i følgende kode.</span><span class="sxs-lookup"><span data-stu-id="783cb-357">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="783cb-358">Denne kode gør to ting:</span><span class="sxs-lookup"><span data-stu-id="783cb-358">This code does two things:</span></span>
    1.  <span data-ttu-id="783cb-359">Det hjælper med at sikre, at brugerne ikke kan navigere direkte fra arbejdsområdet til siden **Vis regnskab**.</span><span class="sxs-lookup"><span data-stu-id="783cb-359">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="783cb-360">Det etablerer et navigationskontrolelement fra siden **Fakturadetaljer** til siden **Vis regnskab**.</span><span class="sxs-lookup"><span data-stu-id="783cb-360">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="783cb-361">Navnet på siderne og andre kontrolelementer i koden skal være det samme som navnene i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="783cb-361">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="783cb-362">Overfør kodefilen til arbejdsområdett ved at vælge fanen **Regel** for at overskrive den tidligere kode</span><span class="sxs-lookup"><span data-stu-id="783cb-362">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="783cb-363">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="783cb-363">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="783cb-364">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="783cb-364">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="783cb-365">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="783cb-365">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="783cb-366">Validering</span><span class="sxs-lookup"><span data-stu-id="783cb-366">Validation</span></span>

<span data-ttu-id="783cb-367">Åbn appen fra din mobilenhed, og opret forbindelse til din forekomst.</span><span class="sxs-lookup"><span data-stu-id="783cb-367">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="783cb-368">Sørg for at logge på det firma, hvor kreditorfakturaerne er tildelt til dig til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="783cb-368">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="783cb-369">Du skal kunne udføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="783cb-369">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="783cb-370">Se arbejdsområdet **Mine godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="783cb-370">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="783cb-371">Foretage detailudledning i arbejdsområdet **Mine godkendelser** og se siden **Mine kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="783cb-371">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="783cb-372">Foretage detailudledning på siden **Mine kreditorfakturaer** og se listen over fakturaer, der er tildelt til dig.</span><span class="sxs-lookup"><span data-stu-id="783cb-372">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="783cb-373">Foretage detailudledning i en af fakturaerne, og se fakturahovedets detaljer og linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="783cb-373">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="783cb-374">På detaljesiden kan du se et link til vedhæftede filer, som du kan bruge til at gå til listen over vedhæftede filer for at få vist filerne.</span><span class="sxs-lookup"><span data-stu-id="783cb-374">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="783cb-375">På detaljesiden kan du se et link til siden **Vis regnskab**. Du kan bruge linket til at gå til siden over fordelinger og se fordelingerne.</span><span class="sxs-lookup"><span data-stu-id="783cb-375">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="783cb-376">På detaljesiden skal du klikke på menuen **Handlinger** forneden og udføre handlinger for arbejdsgange, der gælder for trinnet i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="783cb-376">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="783cb-377">Designe et komplekst fakturagodkendelsesscenario til Fabrikam</span><span class="sxs-lookup"><span data-stu-id="783cb-377">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="783cb-378">Scenarieattribut</span><span class="sxs-lookup"><span data-stu-id="783cb-378">Scenario attribute</span></span></th>
<th><span data-ttu-id="783cb-379">Besvar</span><span class="sxs-lookup"><span data-stu-id="783cb-379">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="783cb-380">Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="783cb-380">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="783cb-381">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="783cb-381">Vendor name</span></span></li>
<li><span data-ttu-id="783cb-382">Fakturabeløb</span><span class="sxs-lookup"><span data-stu-id="783cb-382">Invoice amount</span></span></li>
<li><span data-ttu-id="783cb-383">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="783cb-383">Invoice account</span></span></li>
<li><span data-ttu-id="783cb-384">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="783cb-384">Invoice number</span></span></li>
<li><span data-ttu-id="783cb-385">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="783cb-385">Invoice date</span></span></li>
<li><span data-ttu-id="783cb-386">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="783cb-386">Invoice description</span></span></li>
<li><span data-ttu-id="783cb-387">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="783cb-387">Due date</span></span></li>
<li><span data-ttu-id="783cb-388">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="783cb-388">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="783cb-389">Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="783cb-389">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="783cb-390">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="783cb-390">Procurement category</span></span></li>
<li><span data-ttu-id="783cb-391">Mængde</span><span class="sxs-lookup"><span data-stu-id="783cb-391">Quantity</span></span></li>
<li><span data-ttu-id="783cb-392">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="783cb-392">Unit price</span></span></li>
<li><span data-ttu-id="783cb-393">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="783cb-393">Line net amount</span></span></li>
<li><span data-ttu-id="783cb-394">1099-beløb</span><span class="sxs-lookup"><span data-stu-id="783cb-394">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="783cb-395">Hvor mange fakturalinjer er der i en faktura?</span><span class="sxs-lookup"><span data-stu-id="783cb-395">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="783cb-396">Anvend 80-20-reglen her, og optimer til 80 procent.</span><span class="sxs-lookup"><span data-stu-id="783cb-396">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="783cb-397">5</span><span class="sxs-lookup"><span data-stu-id="783cb-397">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="783cb-398">Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</span><span class="sxs-lookup"><span data-stu-id="783cb-398">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="783cb-399">Ja</span><span class="sxs-lookup"><span data-stu-id="783cb-399">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="783cb-400">Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer osv.) er der for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="783cb-400">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="783cb-401">Igen anvend 80-20-reglen.</span><span class="sxs-lookup"><span data-stu-id="783cb-401">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="783cb-402">Udvidet pris: 2 Moms: 2 Gebyrer: 2</span><span class="sxs-lookup"><span data-stu-id="783cb-402">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="783cb-403">Har fakturaerne også regnskabsfordelinger i fakturahovedet?</span><span class="sxs-lookup"><span data-stu-id="783cb-403">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="783cb-404">I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</span><span class="sxs-lookup"><span data-stu-id="783cb-404">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="783cb-405">Bruges ikke</span><span class="sxs-lookup"><span data-stu-id="783cb-405">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="783cb-406">Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</span><span class="sxs-lookup"><span data-stu-id="783cb-406">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="783cb-407">Ja</span><span class="sxs-lookup"><span data-stu-id="783cb-407">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="783cb-408">Næste trin</span><span class="sxs-lookup"><span data-stu-id="783cb-408">Next steps</span></span>

<span data-ttu-id="783cb-409">Kan du udføre følgende variationer i scenario 1, baseret på kravene til scenario 2.</span><span class="sxs-lookup"><span data-stu-id="783cb-409">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="783cb-410">Du kan bruge dette afsnit til at forbedre din mobilappoplevelse.</span><span class="sxs-lookup"><span data-stu-id="783cb-410">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="783cb-411">Fordi der forventes flere fakturalinjer i scenario 2, hjælper følgende ændringer i designet med at optimere brugeroplevelsen på mobilenheden:</span><span class="sxs-lookup"><span data-stu-id="783cb-411">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="783cb-412">I stedet for at få vist fakturalinjer på siden med detaljer (som i eksempel 1), kan brugerne vælge at få vist linjer på en separat mobilenhedsside.</span><span class="sxs-lookup"><span data-stu-id="783cb-412">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="783cb-413">Da der forventes mere end én fakturalinje i dette scenario, hvis siden **VendMobileInvoiceAllDistributionTree** bruges til at designe fordelingssiden for mobilenheder (som i eksempel 1), kan det være forvirrende for brugeren at koordinere linjer til fordeling.</span><span class="sxs-lookup"><span data-stu-id="783cb-413">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="783cb-414">Derfor skal du bruge siden **VendMobileInvoiceLineDistributionTree** til at designe fordelingssiden.</span><span class="sxs-lookup"><span data-stu-id="783cb-414">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="783cb-415">Ideelt set skal fordelingerne vises i forbindelse med en fakturalinje i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="783cb-415">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="783cb-416">Sørg derfor for, at brugeren kan dykke ned i en linje for at se fordelingssiden.</span><span class="sxs-lookup"><span data-stu-id="783cb-416">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="783cb-417">Brug sidelinkfunktionen til at oprette detaljeadgang, ligesom du gjorde for hoved- og detaljesiderne i scenario 1.</span><span class="sxs-lookup"><span data-stu-id="783cb-417">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="783cb-418">Da mere end én beløbstype forventes for fordelinger i scenario 2 (moms, gebyrer osv.), vil det være nyttigt at få vist beskrivelsen af beløbstypen.</span><span class="sxs-lookup"><span data-stu-id="783cb-418">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="783cb-419">(Vi har udeladt disse oplysninger i scenario 1).</span><span class="sxs-lookup"><span data-stu-id="783cb-419">(We omitted this information in scenario 1.)</span></span>




