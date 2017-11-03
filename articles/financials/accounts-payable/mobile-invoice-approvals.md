---
title: Mobilfakturagodkendelser
description: Dette emne er beregnet til at give en praktisk tilgang til design af scenarier for mobilenheder i Dynamics 365 for Finance and Operations via en brugssag om godkendelser af kreditorfakturaer til mobilenheder.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c579db5a922d81a2781ec2011e148db54fac288d
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="fa4fb-103">Mobilfakturagodkendelser</span><span class="sxs-lookup"><span data-stu-id="fa4fb-103">Mobile invoice approvals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fa4fb-104">Med mobilfunktionaliteten i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kan forretningsbruger designe oplevelser til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition let a business user design mobile experiences.</span></span> <span data-ttu-id="fa4fb-105">I avancerede scenarier kan udviklere også udvide funktionerne, som de ønsker.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="fa4fb-106">Den mest effektive måde at lære nogle af de nye begreber til mobilenheder på er ved at gennemgå processen med at designe et par scenarier.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="fa4fb-107">Dette emne er beregnet til at give en praktisk tilgang til design af scenarier for mobilenheder via en brugssag om godkendelser af kreditorfakturaer til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="fa4fb-108">Dette emne kan hjælpe dig med at designe andre variationer af scenarier og kan også anvendes til andre scenarier, der ikke er relateret til kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="fa4fb-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="fa4fb-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="fa4fb-110">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="fa4fb-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="fa4fb-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="fa4fb-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4fb-112">Håndbog til forhåndslæsning om brug af mobilenhed</span><span class="sxs-lookup"><span data-stu-id="fa4fb-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="fa4fb-113">Mobilplatform</span><span class="sxs-lookup"><span data-stu-id="fa4fb-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="fa4fb-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fa4fb-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="fa4fb-115">Et miljø, der har Microsoft Dynamics 365 for Operations version 1611 og Microsoft Dynamics for Operations platformsopdatering 3 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="fa4fb-116">Installer hotfix-KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="fa4fb-117">Arbejdsrutineoptager kan fejlagtigt optage to Luk-kommandoer til rullelistedialogbokse. Dette er medtaget i Dynamics 365 for Operations platformsopdatering 3 (november 2016 opdatering)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="fa4fb-118">Installer hotfix-KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="fa4fb-119">Dette hotfix gør det muligt at se vedhæftede filer på mobilklienten. Dette er medtaget i Dynamics 365 for Operations platformsopdatering 3 (november 2016 opdatering).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="fa4fb-120">Installer hotfix-KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="fa4fb-121">Programkode til applikationen til godkendelse af kreditorfakturaer på mobilenheder. Dette er inkluderet i Microsoft Dynamics AX-programversion 7.0.1 (maj 2016).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="fa4fb-122">En Android eller iOS eller en Windows-enhed, hvor mobilappen til Finance and Operations er installeret</span><span class="sxs-lookup"><span data-stu-id="fa4fb-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="fa4fb-123">Søg efter appen i den relevante appbutik.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="fa4fb-124">Introduktion</span><span class="sxs-lookup"><span data-stu-id="fa4fb-124">Introduction</span></span>
<span data-ttu-id="fa4fb-125">Godkendelser af kreditorfakturaer på mobilenheder kræver tre de hotfixes, der er nævnt i afsnittet "Forudsætninger".</span><span class="sxs-lookup"><span data-stu-id="fa4fb-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="fa4fb-126">Disse hotfixes giver ikke et arbejdsområde til godkendelse af fakturaer.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="fa4fb-127">Hvis du vil vide, hvad er et arbejdsområde er i forbindelse med mobilenheder, skal du læse håndbogen til mobilenheder, der er nævnt i afsnittet "Forudsætninger".</span><span class="sxs-lookup"><span data-stu-id="fa4fb-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="fa4fb-128">Arbejdsområdet til godkendelse af fakturaer skal udformes.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="fa4fb-129">Hver organisation organiserer og definerer sin forretningsproces for kreditorfakturaer på sin egen måde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="fa4fb-130">Før du designer en mobiloplevelse til godkendelse af kreditorfakturaer, skal du overveje følgende aspekter af forretningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="fa4fb-131">Ideen er at bruge disse datapunkter så meget som muligt for at optimere brugeroplevelsen på enheden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="fa4fb-132">Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="fa4fb-133">Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="fa4fb-134">Hvor mange fakturalinjer er der i en faktura?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="fa4fb-135">Anvend 80-20-reglen her, og optimer til 80 procent.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="fa4fb-136">Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="fa4fb-137">Hvis svaret på dette spørgsmål er ja, skal du overveje følgende spørgsmål:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="fa4fb-138">Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer, opdelinger osv.) er der for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="fa4fb-139">Igen anvend 80-20-reglen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="fa4fb-140">Har fakturaerne også regnskabsfordelinger i fakturahovedet?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="fa4fb-141">I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="fa4fb-142">Dette emne forklarer ikke, hvordan du redigerer regnskabsfordelinger, fordi denne funktion i øjeblikket ikke understøttes for mobilscenarier.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="fa4fb-143">Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="fa4fb-144">Hvilke mobilfunktioner der skal bruges til godkendelse af fakturaer, afhænger af svarene på disse spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="fa4fb-145">Målet er at optimere brugeroplevelsen af forretningsprocessen på mobilenhederne i en organisation.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="fa4fb-146">I resten af dette emne ser vi på to scenarievariationer, der er baseret på forskellige svar på de foregående spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="fa4fb-147">Som hovedregel når du arbejder med designeren til mobilenheder skal du sørge for at "publicere" ændringerne for at undgå at miste opdateringerne.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="fa4fb-148">Designe et simpelt fakturagodkendelsesscenario til Contoso</span><span class="sxs-lookup"><span data-stu-id="fa4fb-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa4fb-149">Scenarieattribut</span><span class="sxs-lookup"><span data-stu-id="fa4fb-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="fa4fb-150">Besvar</span><span class="sxs-lookup"><span data-stu-id="fa4fb-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa4fb-151">Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="fa4fb-152">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="fa4fb-152">Vendor name</span></span></li>
<li><span data-ttu-id="fa4fb-153">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="fa4fb-153">Invoice total</span></span></li>
<li><span data-ttu-id="fa4fb-154">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="fa4fb-154">Invoice account</span></span></li>
<li><span data-ttu-id="fa4fb-155">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="fa4fb-155">Invoice number</span></span></li>
<li><span data-ttu-id="fa4fb-156">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-156">Invoice date</span></span></li>
<li><span data-ttu-id="fa4fb-157">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa4fb-157">Invoice description</span></span></li>
<li><span data-ttu-id="fa4fb-158">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-158">Due date</span></span></li>
<li><span data-ttu-id="fa4fb-159">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="fa4fb-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa4fb-160">Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="fa4fb-161">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="fa4fb-161">Procurement category</span></span></li>
<li><span data-ttu-id="fa4fb-162">Mængde</span><span class="sxs-lookup"><span data-stu-id="fa4fb-162">Quantity</span></span></li>
<li><span data-ttu-id="fa4fb-163">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="fa4fb-163">Unit price</span></span></li>
<li><span data-ttu-id="fa4fb-164">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-164">Line net amount</span></span></li>
<li><span data-ttu-id="fa4fb-165">1099-beløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa4fb-166">Hvor mange fakturalinjer er der i en faktura?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="fa4fb-167">Anvend 80-20-reglen her, og optimer til 80 procent.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="fa4fb-168">1</span><span class="sxs-lookup"><span data-stu-id="fa4fb-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa4fb-169">Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="fa4fb-170">Ja</span><span class="sxs-lookup"><span data-stu-id="fa4fb-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa4fb-171">Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer osv.) er der for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="fa4fb-172">Igen anvend 80-20-reglen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="fa4fb-173">Udvidet pris: 2 Moms: 0 Gebyrer: 0</span><span class="sxs-lookup"><span data-stu-id="fa4fb-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa4fb-174">Har fakturaerne også regnskabsfordelinger i fakturahovedet?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="fa4fb-175">I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="fa4fb-176">Bruges ikke</span><span class="sxs-lookup"><span data-stu-id="fa4fb-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa4fb-177">Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="fa4fb-178">Ja</span><span class="sxs-lookup"><span data-stu-id="fa4fb-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="fa4fb-179">Oprette arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-179">Create the workspace</span></span>

1.  <span data-ttu-id="fa4fb-180">Åbn Finance and Operations i en webbrowser, og log på.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="fa4fb-181">Når du har logget på, kan du tilføje **&mode=mobile** til URL-adressen som vist i følgende eksempel og opdatere siden: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="fa4fb-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span></span>
3.  <span data-ttu-id="fa4fb-182">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="fa4fb-183">Mobilappdesigneren skal vises på samme måde som Arbejdsrutineoptager vises.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="fa4fb-184">Klik på **Tilføj** for at oprette et nyt arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="fa4fb-185">I dette eksempel skal du navngive arbejdsområdet **Mine godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="fa4fb-186">Angiv en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-186">Enter a description.</span></span>
6.  <span data-ttu-id="fa4fb-187">Vælg en farve til arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-187">Select a workspace color.</span></span> <span data-ttu-id="fa4fb-188">Arbejdsområdets farve skal bruges til mobilfunktionernes overordnede udseende i dette arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="fa4fb-189">Vælg et ikon til arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="fa4fb-190">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-190">Click **Done**</span></span>
9.  <span data-ttu-id="fa4fb-191">Klik på **Publicer arbejdsområde** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="fa4fb-192">Kreditorfakturaer, der er tildelt til mig</span><span class="sxs-lookup"><span data-stu-id="fa4fb-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="fa4fb-193">Den første mobilenhedsside, du skal designe, er listen over de fakturaer, der er tildelt til brugeren til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="fa4fb-194">For at udforme denne mobilenhedsside skal du bruge siden **VendMobileInvoiceAssignedToMeListPage** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="fa4fb-195">Før du kan udføre denne procedure skal du sørge for, at mindst én kreditorfaktura er tildelt til dig til gennemsyn, og at fakturalinjen har to fordelinger.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="fa4fb-196">Denne opsætning opfylder kravene i dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="fa4fb-197">I URL-adressen til Finance and Operations skal du erstatte navnet på menupunktet med **VendMobileInvoiceAssignedToMeListPage** for at åbne mobilversionen af listesiden **Afventende kreditorfakturaer tildelt til mig** i **Kreditor**-modulet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="fa4fb-198">Afhængigt af antallet af fakturaer, der er tildelt til dig i dit system, viser denne side fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="fa4fb-199">Når du vil finde en bestemt faktura, kan du bruge filteret til venstre.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="fa4fb-200">Men vi har ikke brug for en bestemt faktura i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="fa4fb-201">Vi skal bare bruge en faktura, der er tildelt til dig, så du kan få adgang til at designe siden til mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="fa4fb-202">De nye sider, der er tilgængelige, er designet specifikt til udvikling af scenarier for kreditorfakturaer på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="fa4fb-203">Derfor skal du bruge disse sider.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="fa4fb-204">URL-adressen skal ligne følgende URL-adresse, og når du har angivet den, skal den side, der er vist i illustrationen, vises: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Afventende kreditorfakturaer, der er tildelt mig](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="fa4fb-205">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="fa4fb-206">Vælg dit arbejdsområde, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="fa4fb-207">Klik på **Tilføj side** for at oprette den første side til mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="fa4fb-208">Angiv et navn, f.eks. **Mine kreditorfakturaer**, og en beskrivelse, f.eks. **Kreditorfakturaer, der er tildelt til mig til gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="fa4fb-209">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-209">Click **Done**.</span></span>
7.  <span data-ttu-id="fa4fb-210">I designeren til mobilenheder skal du under fanen **Felter** klikke på **Vælg felter**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="fa4fb-211">Kolonnerne på listesiden skal ligne den følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="fa4fb-212">[![Kolonner i de afventende kreditorfakturaer, der er tildelt mig](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="fa4fb-213">Tilføj de kolonner, der kræves, fra den listeside, der skal vises for brugere på mobilenhedssiden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="fa4fb-214">Den rækkefølge, som du tilføjer i, er den rækkefølge, som felterne bliver vist i for slutbrugeren.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="fa4fb-215">Den eneste måde at ændre rækkefølgen af felterne er ved igen at vælge alle felter.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="fa4fb-216">Baseret på kravene til dette scenario er de følgende otte felter obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="fa4fb-217">Men nogle brugere vil mene, at otte felter er for mange oplysninger på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="fa4fb-218">Derfor vil vi kun vise de vigtigste felter i listevisningen til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="fa4fb-219">De resterende felter vises i detaljevisningen, som vi udformer senere.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="fa4fb-220">Nu skal vi tilføje følgende felter.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-220">For now, we will add the following fields.</span></span> <span data-ttu-id="fa4fb-221">Klik på plustegnet (**+**) i disse kolonner for at føje dem til siden på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="fa4fb-222">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="fa4fb-222">Vendor name</span></span>
    - <span data-ttu-id="fa4fb-223">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="fa4fb-223">Invoice total</span></span>
    - <span data-ttu-id="fa4fb-224">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="fa4fb-224">Invoice account</span></span>
    - <span data-ttu-id="fa4fb-225">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="fa4fb-225">Invoice number</span></span>
    - <span data-ttu-id="fa4fb-226">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-226">Invoice date</span></span>

    <span data-ttu-id="fa4fb-227">Når felterne er tilføjet, skal siden ligne følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="fa4fb-228">[![Side, efter at der er tilføjet felter](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="fa4fb-229">Du skal også tilføje følgende kolonner nu, så vi senere kan aktivere arbejdsganghandlinger.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="fa4fb-230">Vis fuldført opgave</span><span class="sxs-lookup"><span data-stu-id="fa4fb-230">Show complete task</span></span>
    - <span data-ttu-id="fa4fb-231">Vis delegeret opgave</span><span class="sxs-lookup"><span data-stu-id="fa4fb-231">Show delegate task</span></span>
    - <span data-ttu-id="fa4fb-232">Vis tilbagekaldelsesopgave</span><span class="sxs-lookup"><span data-stu-id="fa4fb-232">Show recall task</span></span>
    - <span data-ttu-id="fa4fb-233">Vis afvist opgave</span><span class="sxs-lookup"><span data-stu-id="fa4fb-233">Show reject task</span></span>
    - <span data-ttu-id="fa4fb-234">Vis anmodningsfuldførelsesopgave</span><span class="sxs-lookup"><span data-stu-id="fa4fb-234">Show request completion task</span></span>
    - <span data-ttu-id="fa4fb-235">Vis send igen-opgave</span><span class="sxs-lookup"><span data-stu-id="fa4fb-235">Show resubmit task</span></span>

10. <span data-ttu-id="fa4fb-236">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="fa4fb-237">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="fa4fb-238">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="fa4fb-239">Aktiver **Vis fakturatotal på ventende kreditorfakturaliste** i formen med kreditorparametre under **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="fa4fb-240">Bemærk, at kun hvis denne parameter aktiveres, beregnes fakturatotaler og vises på listesiden over ventende kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="fa4fb-241">Dette er en ny funktion som en del af det nødvendige hot fix 3208224.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="fa4fb-242">Detaljer i kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="fa4fb-242">Vendor invoice details</span></span>

<span data-ttu-id="fa4fb-243">Når du vil designe siden med fakturadetaljer til mobilenheder, skal du bruge siden **VendMobileInvoiceHeaderDetails** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="fa4fb-244">Bemærk, at afhængigt af antallet af fakturaer, du har i dit system, viser denne side den ældste faktura (faktura, der blev oprettet først).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="fa4fb-245">Når du vil finde en bestemt faktura, kan du bruge filteret til venstre.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="fa4fb-246">Men vi har ikke brug for en bestemt faktura i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="fa4fb-247">Vi skal blot bruge nogle fakturadata, så vi kan designe siden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="fa4fb-248">[![Siden Arbejdsgang](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1.  <span data-ttu-id="fa4fb-249">I URL-adressen til Finance and Operations skal du erstatte navnet på menupunktet med **VendMobileInvoiceHeaderDetails** for at åbne formen</span><span class="sxs-lookup"><span data-stu-id="fa4fb-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2.  <span data-ttu-id="fa4fb-250">Åbn designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="fa4fb-251">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4.  <span data-ttu-id="fa4fb-252">Vælg siden **Mine kreditorfakturaer**, som du oprettede tidligere, og klik derefter på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-252">Select the **My vendor invoices **page that you created earlier, and then click **Edit**.</span></span>
5.  <span data-ttu-id="fa4fb-253">Under fanen **Felter** skal du klikke på kolonneoverskriften **Gitter**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6.  <span data-ttu-id="fa4fb-254">Klik på **Egenskaber** &gt; **Tilføj side**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-254">Click **Properties** &gt; **Add page**.</span></span> <span data-ttu-id="fa4fb-255">**Bemærk:** Når du klikker på overskriften **Gitter** og tilføjer en side, oprettes relationen med detaljesiden automatisk.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7.  <span data-ttu-id="fa4fb-256">Angiv en sidetitel, f.eks. **Fakturadetaljer** og en beskrivelse som **Vis fakturahoved og linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8.  <span data-ttu-id="fa4fb-257">Klik på **Vælg felter**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-257">Click **Select fields**.</span></span> <span data-ttu-id="fa4fb-258">Bemærk, at den rækkefølge, som du tilføjer i, er den rækkefølge, som felterne bliver vist i for slutbrugeren.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="fa4fb-259">Den eneste måde at ændre rækkefølgen af felterne er ved igen at vælge alle felter.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9.  <span data-ttu-id="fa4fb-260">Baseret på kravene til dette scenario skal du tilføje følgende felter fra hovedet:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
    - <span data-ttu-id="fa4fb-261">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="fa4fb-261">Vendor name</span></span>
    - <span data-ttu-id="fa4fb-262">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="fa4fb-262">Invoice total</span></span>
    - <span data-ttu-id="fa4fb-263">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="fa4fb-263">Invoice account</span></span>
    - <span data-ttu-id="fa4fb-264">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="fa4fb-264">Invoice number</span></span>
    - <span data-ttu-id="fa4fb-265">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-265">Invoice date</span></span>
    - <span data-ttu-id="fa4fb-266">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa4fb-266">Invoice description</span></span>
    - <span data-ttu-id="fa4fb-267">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-267">Due date</span></span>
    - <span data-ttu-id="fa4fb-268">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="fa4fb-268">Invoice currency</span></span>

10. <span data-ttu-id="fa4fb-269">Tilføj følgende felter fra gitterlinjerne på siden:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="fa4fb-270">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="fa4fb-270">Procurement category</span></span>
    - <span data-ttu-id="fa4fb-271">Mængde</span><span class="sxs-lookup"><span data-stu-id="fa4fb-271">Quantity</span></span>
    - <span data-ttu-id="fa4fb-272">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="fa4fb-272">Unit price</span></span>
    - <span data-ttu-id="fa4fb-273">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-273">Line net amount</span></span>
    - <span data-ttu-id="fa4fb-274">1099-beløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-274">1099 amount</span></span>

11. <span data-ttu-id="fa4fb-275">Når alle felter fra de forrige to trin er tilføjet, skal du klikke på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="fa4fb-276">Siden skal ligne følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-276">The page must resemble the following illustration.</span></span>
<span data-ttu-id="fa4fb-277">[![Side, efter at der er tilføjet felter](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="fa4fb-278">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="fa4fb-279">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="fa4fb-280">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="fa4fb-281">Arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="fa4fb-281">Workflow actions</span></span>

<span data-ttu-id="fa4fb-282">Brug siden **VendMobileInvoiceHeaderDetails** i Finance and Operations til at føje arbejdsgangshandlinger.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="fa4fb-283">Erstat navnet på menupunktet i URL-adressen, hvis du vil åbne denne side, som du gjorde tidligere.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="fa4fb-284">Åbn derefter designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="fa4fb-285">Følg disse trin for at føje arbejdsgangshandlinger til detaljesiden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="fa4fb-286">Der skal være tildelt fakturaer til dig, der er i en tilstand, der kan gøre de arbejdsgangshandlinger, du skal udforme, tilgængelige for dig.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="fa4fb-287">Registrere arbejdsgangshandlinger</span><span class="sxs-lookup"><span data-stu-id="fa4fb-287">Record workflow actions</span></span>
1.  <span data-ttu-id="fa4fb-288">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="fa4fb-289">Vælg siden **Fakturadetaljer**, som du oprettede tidligere, og klik derefter på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="fa4fb-290">Klik på **Tilføj handling** under fanen **Handlinger**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="fa4fb-291">Angiv en titel til handlingen, f.eks. **Godkend**, og en beskrivelse, f.eks. **Godkend faktura**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="fa4fb-292">Bemærk, at den handlingstitel, du angiver her, bliver navnet på den handling, der vises for brugeren i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="fa4fb-293">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-293">Click **Done**.</span></span>
6.  <span data-ttu-id="fa4fb-294">Klik på **Vælg felter**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="fa4fb-295">Gennemgå arbejdsgangen på siden **VendMobileInvoiceHeaderDetails**, og udfør den handling, du ønskede at registrere.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="fa4fb-296">Sørg for at indtaste kommentarer til arbejdsgangen under denne proces, så et kommentarfelt også er inkluderet i mobiloplevelsen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="fa4fb-297">Når du har kørt arbejdsgangshandlingen, skal du klikke på **Udført** for at fuldføre opgaven Vælg felter.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="fa4fb-298">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="fa4fb-299">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="fa4fb-300">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="fa4fb-301">Gentag de foregående trin for at registrere de påkrævede arbejdsgangshandlinger.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="fa4fb-302">Oprette en .js-fil</span><span class="sxs-lookup"><span data-stu-id="fa4fb-302">Create a .js file</span></span>
1. <span data-ttu-id="fa4fb-303">Åbn Notesblok eller Microsoft Visual Studio, og indsæt følgende kode.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="fa4fb-304">Gem filen som en .js-fil.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-304">Save the file as a .js file.</span></span> <span data-ttu-id="fa4fb-305">Denne kode gør følgende:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-305">This code does the following:</span></span>
    - <span data-ttu-id="fa4fb-306">Den skjuler de ekstra arbejdsgang-relaterede kolonner, som vi tidligere tilføjede på listeside til mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="fa4fb-307">Vi tilføjede disse kolonner, så appen har disse oplysninger i den rette sammenhæng og kan udføre det næste trin.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="fa4fb-308">Baseret på, hvilket trin i arbejdsgangen der er aktivt, anvender den regler, så kun disse handlinger viser.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="fa4fb-309">Navnet på siderne og andre kontrolelementer i koden skal være det samme som navnene i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="fa4fb-310">Overfør kodefilen til arbejdsområdet ved at vælge fanen **Regel**</span><span class="sxs-lookup"><span data-stu-id="fa4fb-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="fa4fb-311">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="fa4fb-312">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="fa4fb-313">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="fa4fb-314">Vedhæftede filer i kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="fa4fb-314">Vendor invoice attachments</span></span>

1.  <span data-ttu-id="fa4fb-315">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne af siden, og klik derefter på **Mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2.  <span data-ttu-id="fa4fb-316">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3.  <span data-ttu-id="fa4fb-317">Vælg siden **Fakturadetaljer**, som du oprettede tidligere, og klik derefter på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-317">Select the **Invoice details **page that you created earlier, and then click **Edit**.</span></span>
4.  <span data-ttu-id="fa4fb-318">Indstil **Dokumentstyring** til **Ja** som vist nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="fa4fb-319">**Bemærk:** Hvis der er ikke er krav om at vise vedhæftede filer på mobilenheden, kan du lade denne indstilling være sat til **Nej**, som er standardindstillingen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
<span data-ttu-id="fa4fb-320">![Dokumentstyring](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-320">![Document management](./media/docmanagement-216x300.png)</span></span>
6.  <span data-ttu-id="fa4fb-321">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-321">Click **Done** to exit edit mode.</span></span>
7.  <span data-ttu-id="fa4fb-322">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-322">Click **Back** and then **Done** to exit the workspace</span></span>
8.  <span data-ttu-id="fa4fb-323">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="fa4fb-324">Fordelinger af kreditorfakturalinjer</span><span class="sxs-lookup"><span data-stu-id="fa4fb-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="fa4fb-325">Kravene til dette scenario bekræfter, at der kun skal være fordelinger på linjeniveau, og at en faktura har altid kun én linje.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="fa4fb-326">Da dette scenario er enkelt, skal brugeroplevelsen på mobilenheden også være så enkel, at brugeren ikke behøver at foretage detaljeopløftning på flere niveauer for at få vist fordelingerne.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="fa4fb-327">Kreditorfakturaer i Finance and Operations omfatter muligheden for at vise alle fordelinger fra fakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="fa4fb-328">Det er denne oplevelse, vi har brug for til scenariet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="fa4fb-329">Derfor benytter vi siden **VendMobileInvoiceAllDistributionTree** til at designe denne del af scenariet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="fa4fb-330">Når vi kender kravene, hjælper det os med at afgøre, hvilken specifik side vi skal bruge, og hvordan nøjagtigt vi skal optimere mobiloplevelsen for brugeren, når vi udformer scenariet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="fa4fb-331">I det andet scenario bruger vi en anden side til at vise fordelingerne, da kravene til dette scenario er anderledes.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="fa4fb-332">I URL-adressen skal du erstatte navnet på menupunktet, som du gjorde tidligere.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="fa4fb-333">Den side, der vises, skal ligne følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="fa4fb-334">[![Siden Alle fordelinger](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="fa4fb-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="fa4fb-335">Åbn designeren til mobilenheder fra knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="fa4fb-336">Klik på knappen **Rediger** for at starte redigeringstilstand i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="fa4fb-337">**Bemærk:** Du kan se, at to nye sider blev oprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="fa4fb-338">Systemet opretter disse sider, fordi du aktiverede dokumentstyring i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="fa4fb-339">Du kan ignorere disse nye sider.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="fa4fb-340">Klik på **Tilføj side**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="fa4fb-341">Angiv en titel som **Vis regnskab** og en beskrivelse som **Vis regnskab for fakturaen**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="fa4fb-342">Klik på **Udført**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-342">Click **Done**.</span></span>
7.  <span data-ttu-id="fa4fb-343">Under fanen **Felter** skal du klikke på **Vælg felter** og vælge følgende felter fra fordelingssiden og derefter klikke på **Udført**:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="fa4fb-344">Beløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-344">Amount</span></span>
    2.  <span data-ttu-id="fa4fb-345">Valuta</span><span class="sxs-lookup"><span data-stu-id="fa4fb-345">Currency</span></span>
    3.  <span data-ttu-id="fa4fb-346">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="fa4fb-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="fa4fb-347">Vi ikke har valgt kolonnen **Beskrivelse** fra fordelingsgitteret, fordi kravene til dette scenario bekræftede, at den udvidede pris er det eneste beløb, vil der være fordelinger for.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="fa4fb-348">Brugeren har derfor ikke brug et andet felt til at bestemme den beløbstype, som vedrører fordelingen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="fa4fb-349">Men i det næste scenario **bruger** vi disse oplysninger, fordi kravene til dette scenarie angiver, at andre beløbstyper har fordelinger (for eksempel moms).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="fa4fb-350">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="fa4fb-351">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="fa4fb-352">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="fa4fb-353">Siden **Vis regnskab** til mobilenheder er ikke aktuelt knyttet til nogen af de sider til mobilenheder, vi har udviklet indtil videre.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="fa4fb-354">Da brugeren skal kunne navigere til siden **Vis regnskab** fra siden **Fakturaoplysninger** på mobilenheden, skal vi sørge for navigation fra siden **Fakturadetaljer** til siden **Vis regnskab**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="fa4fb-355">Vi opretter denne navigation ved hjælp af yderligere logik via JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="fa4fb-356">Åbn den .js-fil, du oprettede tidligere, og tilføj de linjer, der er fremhævet i følgende kode.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="fa4fb-357">Denne kode gør to ting:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-357">This code does two things:</span></span>
    1.  <span data-ttu-id="fa4fb-358">Det hjælper med at sikre, at brugerne ikke kan navigere direkte fra arbejdsområdet til siden **Vis regnskab**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="fa4fb-359">Det etablerer et navigationskontrolelement fra siden **Fakturadetaljer** til siden **Vis regnskab**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="fa4fb-360">Navnet på siderne og andre kontrolelementer i koden skal være det samme som navnene i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="fa4fb-361">Overfør kodefilen til arbejdsområdett ved at vælge fanen **Regel** for at overskrive den tidligere kode</span><span class="sxs-lookup"><span data-stu-id="fa4fb-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="fa4fb-362">Klik på **Udført** for at afslutte redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="fa4fb-363">Klik på **Tilbage** og derefter på **Udført** for at afslutte arbejdsområdet</span><span class="sxs-lookup"><span data-stu-id="fa4fb-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="fa4fb-364">Klik på **Publicer arbejdsområde** for at gemme dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="fa4fb-365">Validering</span><span class="sxs-lookup"><span data-stu-id="fa4fb-365">Validation</span></span>

<span data-ttu-id="fa4fb-366">Åbn appen fra din mobilenhed, og opret forbindelse til din Finance and Operations-forekomst.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="fa4fb-367">Sørg for at logge på det firma, hvor kreditorfakturaerne er tildelt til dig til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="fa4fb-368">Du skal kunne udføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="fa4fb-369">Se arbejdsområdet **Mine godkendelser**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="fa4fb-370">Foretage detailudledning i arbejdsområdet **Mine godkendelser** og se siden **Mine kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="fa4fb-371">Foretage detailudledning på siden **Mine kreditorfakturaer** og se listen over fakturaer, der er tildelt til dig.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="fa4fb-372">Foretage detailudledning i en af fakturaerne, og se fakturahovedets detaljer og linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="fa4fb-373">På detaljesiden kan du se et link til vedhæftede filer, som du kan bruge til at gå til listen over vedhæftede filer for at få vist filerne.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="fa4fb-374">På detaljesiden kan du se et link til siden **Vis regnskab**. Du kan bruge linket til at gå til siden over fordelinger og se fordelingerne.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="fa4fb-375">På detaljesiden skal du klikke på menuen **Handlinger** forneden og udføre handlinger for arbejdsgange, der gælder for trinnet i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="fa4fb-376">Designe et komplekst fakturagodkendelsesscenario til Fabrikam</span><span class="sxs-lookup"><span data-stu-id="fa4fb-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa4fb-377">Scenarieattribut</span><span class="sxs-lookup"><span data-stu-id="fa4fb-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="fa4fb-378">Besvar</span><span class="sxs-lookup"><span data-stu-id="fa4fb-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa4fb-379">Hvilke felter fra fakturahovedet ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="fa4fb-380">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="fa4fb-380">Vendor name</span></span></li>
<li><span data-ttu-id="fa4fb-381">Fakturabeløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-381">Invoice amount</span></span></li>
<li><span data-ttu-id="fa4fb-382">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="fa4fb-382">Invoice account</span></span></li>
<li><span data-ttu-id="fa4fb-383">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="fa4fb-383">Invoice number</span></span></li>
<li><span data-ttu-id="fa4fb-384">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-384">Invoice date</span></span></li>
<li><span data-ttu-id="fa4fb-385">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="fa4fb-385">Invoice description</span></span></li>
<li><span data-ttu-id="fa4fb-386">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="fa4fb-386">Due date</span></span></li>
<li><span data-ttu-id="fa4fb-387">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="fa4fb-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa4fb-388">Hvilke felter fra fakturalinjer ønsker brugeren at se i mobiloplevelsen og i hvilken rækkefølge?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="fa4fb-389">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="fa4fb-389">Procurement category</span></span></li>
<li><span data-ttu-id="fa4fb-390">Mængde</span><span class="sxs-lookup"><span data-stu-id="fa4fb-390">Quantity</span></span></li>
<li><span data-ttu-id="fa4fb-391">Enhedspris</span><span class="sxs-lookup"><span data-stu-id="fa4fb-391">Unit price</span></span></li>
<li><span data-ttu-id="fa4fb-392">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-392">Line net amount</span></span></li>
<li><span data-ttu-id="fa4fb-393">1099-beløb</span><span class="sxs-lookup"><span data-stu-id="fa4fb-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa4fb-394">Hvor mange fakturalinjer er der i en faktura?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="fa4fb-395">Anvend 80-20-reglen her, og optimer til 80 procent.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="fa4fb-396">5</span><span class="sxs-lookup"><span data-stu-id="fa4fb-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa4fb-397">Ønsker brugerne at se regnskabsfordelinger (fakturakodning) på mobilenheden under gennemsyn?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="fa4fb-398">Ja</span><span class="sxs-lookup"><span data-stu-id="fa4fb-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa4fb-399">Hvor mange regnskabsfordelinger (udvidet pris, moms, gebyrer osv.) er der for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="fa4fb-400">Igen anvend 80-20-reglen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="fa4fb-401">Udvidet pris: 2 Moms: 2 Gebyrer: 2</span><span class="sxs-lookup"><span data-stu-id="fa4fb-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa4fb-402">Har fakturaerne også regnskabsfordelinger i fakturahovedet?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="fa4fb-403">I så fald, skal disse regnskabsfordelinger være tilgængelige på enheden?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="fa4fb-404">Bruges ikke</span><span class="sxs-lookup"><span data-stu-id="fa4fb-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa4fb-405">Ønsker brugere at se vedhæftede filer til fakturaen på enheden?</span><span class="sxs-lookup"><span data-stu-id="fa4fb-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="fa4fb-406">Ja</span><span class="sxs-lookup"><span data-stu-id="fa4fb-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="fa4fb-407">Næste trin</span><span class="sxs-lookup"><span data-stu-id="fa4fb-407">Next steps</span></span>

<span data-ttu-id="fa4fb-408">Kan du udføre følgende variationer i scenario 1, baseret på kravene til scenario 2.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="fa4fb-409">Du kan bruge dette afsnit til at forbedre din mobilappoplevelse.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="fa4fb-410">Fordi der forventes flere fakturalinjer i scenario 2, hjælper følgende ændringer i designet med at optimere brugeroplevelsen på mobilenheden:</span><span class="sxs-lookup"><span data-stu-id="fa4fb-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="fa4fb-411">I stedet for at få vist fakturalinjer på siden med detaljer (som i eksempel 1), kan brugerne vælge at få vist linjer på en separat mobilenhedsside.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="fa4fb-412">Da der forventes mere end én fakturalinje i dette scenario, hvis siden **VendMobileInvoiceAllDistributionTree** bruges til at designe fordelingssiden for mobilenheder (som i eksempel 1), kan det være forvirrende for brugeren at koordinere linjer til fordeling.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="fa4fb-413">Derfor skal du bruge siden **VendMobileInvoiceLineDistributionTree** til at designe fordelingssiden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="fa4fb-414">Ideelt set skal fordelingerne vises i forbindelse med en fakturalinje i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="fa4fb-415">Sørg derfor for, at brugeren kan dykke ned i en linje for at se fordelingssiden.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="fa4fb-416">Brug sidelinkfunktionen til at oprette detaljeadgang, ligesom du gjorde for hoved- og detaljesiderne i scenario 1.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="fa4fb-417">Da mere end én beløbstype forventes for fordelinger i scenario 2 (moms, gebyrer osv.), vil det være nyttigt at få vist beskrivelsen af beløbstypen.</span><span class="sxs-lookup"><span data-stu-id="fa4fb-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="fa4fb-418">(Vi har udeladt disse oplysninger i scenario 1).</span><span class="sxs-lookup"><span data-stu-id="fa4fb-418">(We omitted this information in scenario 1.)</span></span>





