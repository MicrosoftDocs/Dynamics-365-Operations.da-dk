---
title: Svar på leverandørspørgsmål i forbindelse med tilbudsanmodninger
description: Leverandører, der har spørgsmål til en RFP, kan sende deres spørgsmål og læse svarene på siden til **Kreditorsamarbejde**.
author: velofog
manager: tfehr
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQVendQuestionAnswer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: public sector
ms.author: kamaybac
ms.search.validFrom: 2020-1-22
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2f56d34a06a207767214204f79e9da0bafdd93d7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992105"
---
# <a name="responding-to-vendor-questions-on-request-for-quotations"></a><span data-ttu-id="2977f-103">Svar på leverandørspørgsmål i forbindelse med tilbudsanmodninger</span><span class="sxs-lookup"><span data-stu-id="2977f-103">Responding to vendor questions on Request for quotations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2977f-104">Når dit kontor har sendt en tilbudsanmodning, har leverandørerne nogle gange spørgsmål, der vedrører anmodningen.</span><span class="sxs-lookup"><span data-stu-id="2977f-104">When your agency has sent a request for quotation (RFQ), vendors sometimes have questions that pertain to the request.</span></span> <span data-ttu-id="2977f-105">Leverandører, der har spørgsmål til en RFP, kan sende deres spørgsmål og læse svarene på siden til **Kreditorsamarbejde**, når du gør siden tilgængelig for dem.</span><span class="sxs-lookup"><span data-stu-id="2977f-105">Vendors that have questions related to an RFP can submit their questions and read the answers on **Vendor collaboration** page, when you make that page available to them.</span></span> <span data-ttu-id="2977f-106">Når leverandørspørgsmål er accepteret, er **Spørgsmål og svar** tilgængelige på siden **Bud på tilbudsanmodning** i **Kreditorsamarbejde** og for dit kontor via siden **Tilbudsanmodning** i **Spørgsmål og svar**.</span><span class="sxs-lookup"><span data-stu-id="2977f-106">When vendor questions are accepted, **Questions and answers** is available on the **Request for quotation bid** page on **Vendor collaboration**, and for your agency through the **Request for quotation** page, **Questions and answers**.</span></span> 

<span data-ttu-id="2977f-107">Brugerne kan udgive svar på leverandørspørgsmål mere end én gang.</span><span class="sxs-lookup"><span data-stu-id="2977f-107">Users can publish answers to vendor questions more than once.</span></span> <span data-ttu-id="2977f-108">Kreditorer kan ikke længere postere spørgsmål, når en leverandør er valgt, og tilbudsanmodningen er tildelt, eller når skæringsdatoen for spørgsmål er nået.</span><span class="sxs-lookup"><span data-stu-id="2977f-108">Vendors can't no longer post questions after a vendor is selected and the RFQ is awarded, or after the cutoff date for questions is reached.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="2977f-109">Slå funktionen til</span><span class="sxs-lookup"><span data-stu-id="2977f-109">Turn on the feature</span></span>

<span data-ttu-id="2977f-110">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="2977f-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2977f-111">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="2977f-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="2977f-112">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="2977f-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2977f-113">**Modul:** *Indkøb og forsyning*</span><span class="sxs-lookup"><span data-stu-id="2977f-113">**Module:** *Procurement and sourcing*</span></span>
- <span data-ttu-id="2977f-114">**Funktionsnavn:** *Spørgsmål og svar vedrørende tilbudsanmodninger*</span><span class="sxs-lookup"><span data-stu-id="2977f-114">**Feature name:** *RFQ questions and answers*</span></span>

## <a name="allow-questions-and-answers-to-be-used-in-rfqs"></a><span data-ttu-id="2977f-115">Tillad, at spørgsmål og svar bruges i tilbudsanmodninger</span><span class="sxs-lookup"><span data-stu-id="2977f-115">Allow questions and answers to be used in RFQs</span></span>

1. <span data-ttu-id="2977f-116">Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.</span><span class="sxs-lookup"><span data-stu-id="2977f-116">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="2977f-117">Åbn fanen **Tilbudsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="2977f-117">Open the **Request for quotation** tab.</span></span>
1. <span data-ttu-id="2977f-118">Angiv følgende indstillinger efter behov:</span><span class="sxs-lookup"><span data-stu-id="2977f-118">Set the following options as needed:</span></span>
    - <span data-ttu-id="2977f-119">**Tillad leverandørspørgsmål**: Aktiverer eller deaktiverer leverandørspørgsmål om tilbudsanmodningssager.</span><span class="sxs-lookup"><span data-stu-id="2977f-119">**Allow vendor questions**: Enables or disables vendor questions for RFQ cases.</span></span> <span data-ttu-id="2977f-120">Du skal indstille denne til *Ja*, hvis du vil bruge de funktioner, der er beskrevet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="2977f-120">You must set this to *Yes* to use the features described in this topic.</span></span>
    - <span data-ttu-id="2977f-121">**Direkte standardsvar**: Når du besvarer et spørgsmål, kan du vælge at besvare alle de leverandører, der har modtaget tilbudsanmodningen, eller kun at svare den bestemte leverandør, som har sendt spørgsmålet.</span><span class="sxs-lookup"><span data-stu-id="2977f-121">**Default direct response**: When you reply to a question, you can choose to reply to all vendors who received the RFQ or to reply only to the specific vendor who submitted the question.</span></span> <span data-ttu-id="2977f-122">Du kan vælge denne indstilling, hver gang du svarer, men denne indstilling styrer standardindstillingen.</span><span class="sxs-lookup"><span data-stu-id="2977f-122">You can make choose this option each time you reply, but this setting controls the default.</span></span> <span data-ttu-id="2977f-123">Hvis du normalt besvarer alle leverandører, skal du vælge *Nej*.</span><span class="sxs-lookup"><span data-stu-id="2977f-123">If you usually reply to all vendors, set this to *No*.</span></span> <span data-ttu-id="2977f-124">Hvis du normalt besvarer leverandører hver for sig, skal du vælge *Ja*.</span><span class="sxs-lookup"><span data-stu-id="2977f-124">If you usually reply to individual vendors, set this to *Yes*.</span></span>

## <a name="setting-up-for-vendor-questions"></a><span data-ttu-id="2977f-125">Opsætning af leverandørspørgsmål</span><span class="sxs-lookup"><span data-stu-id="2977f-125">Setting up for vendor questions</span></span>

<span data-ttu-id="2977f-126">Når du opretter en tilbudsanmodning, bestemmer du, om leverandører kan stille spørgsmål til tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="2977f-126">When creating a request for quotation, you determine whether vendors can ask questions about the RFQ.</span></span>

1. <span data-ttu-id="2977f-127">Gå til **Indkøb og forsyning > Tilbudsanmodninger**, og klik på **Ny > Tilbudsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="2977f-127">Navigate to **Procurement and sourcing > Requests for quotations** then click **New > Request for quotation**</span></span> 
1. <span data-ttu-id="2977f-128">På siden **Ny tilbudsanmodning** skal **Hoved** angives til **Indstillinger for leverandørspørgsmål** for at tillade spørgsmål før en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="2977f-128">In the **New request for quotation** page, **Header** to set the **Vendor question options** fields to allow questions before a certain date.</span></span>
1. <span data-ttu-id="2977f-129">Angiv indstillingen **Tillad leverandørspørgsmål** til **Ja**, så leverandørerne kan skrive spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="2977f-129">Set the **Allow vendor question** option to **Yes** so the vendors can enter questions.</span></span> <span data-ttu-id="2977f-130">Brugerne kan angive og besvare spørgsmål og udpege ofte stillede spørgsmål til udgivelse for leverandører, når tilbudsanmodningen er sendt til leverandørerne.</span><span class="sxs-lookup"><span data-stu-id="2977f-130">Users can enter and answer questions and designate commonly asked questions to publish for vendors when the RFQ is sent to vendors.</span></span>
1. <span data-ttu-id="2977f-131">Valgfrit: Definer feltet **Skæringsdato**, hvor spørgsmål senest skal indsendes.</span><span class="sxs-lookup"><span data-stu-id="2977f-131">Optional: In the **Cutoff date** field, define the final date by which questions must be submitted.</span></span> <span data-ttu-id="2977f-132">Hvis der ikke angives en skæringsdato, accepteres spørgsmålene, så længe tilbudsanmodningen er åben og accepterer bud.</span><span class="sxs-lookup"><span data-stu-id="2977f-132">If no cutoff date is entered, questions are accepted as long as the RFQ is open and accepting bids.</span></span>
1. <span data-ttu-id="2977f-133">Klik på **Gem** for at gemme tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="2977f-133">Click **Save** to save the RFQ.</span></span>
1. <span data-ttu-id="2977f-134">Klik på **Send** for at sende tilbudsanmodningen til leverandører.</span><span class="sxs-lookup"><span data-stu-id="2977f-134">Click **Send** to send the RFQ to the vendors for bidding.</span></span>

## <a name="entering-and-replying-to-vendor-questions"></a><span data-ttu-id="2977f-135">Angive og besvare leverandørspørgsmål</span><span class="sxs-lookup"><span data-stu-id="2977f-135">Entering and replying to vendor questions</span></span>

<span data-ttu-id="2977f-136">Leverandører skriver spørgsmål i **Kreditorsamarbejde > Bud på tilbudsanmodning**, oversigtspanelet **Leverandørspørgsmål**.</span><span class="sxs-lookup"><span data-stu-id="2977f-136">Vendors enter questions in the **Vendor Collaboration > Request for quotations bid** page, **Vendor questions** FastTab.</span></span> <span data-ttu-id="2977f-137">Spørgsmålet er kun synligt for leverandøren og brugerne.</span><span class="sxs-lookup"><span data-stu-id="2977f-137">The question is visible only to the vendor and users.</span></span>

## <a name="entering-a-vendor-question"></a><span data-ttu-id="2977f-138">Angive et leverandørspørgsmål</span><span class="sxs-lookup"><span data-stu-id="2977f-138">Entering a vendor question</span></span>

1. <span data-ttu-id="2977f-139">I Kreditorsamarbejde skal du på siden **Bud på tilbudsanmodning** klikke på **Spørgsmål og svar** og derefter klikke på **+ Stil et spørgsmål**.</span><span class="sxs-lookup"><span data-stu-id="2977f-139">In Vendor collaboration, in the **Request for quotation bid** page, click **Questions and answers**, and then click **+ Ask a question**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2977f-140">Alternativt kan en bruger skrive spørgsmål til en leverandør på siden **Tilbudsanmodning** ved at klikke **Administrer svar**, **Rediger svar på tilbudsanmodning** og derefter klikke på **Spørgsmål og svar**.</span><span class="sxs-lookup"><span data-stu-id="2977f-140">Alternately, a user can enter questions for a vendor on the **Request for quotation** page, by clicking **Manage replies**, **Edit RFQ reply** then clicking **Questions and asnwers**.</span></span>

2. <span data-ttu-id="2977f-141">Skriv teksten til spørgsmålet i feltet **Spørgsmål**.</span><span class="sxs-lookup"><span data-stu-id="2977f-141">On the **Question** field, enter the question text.</span></span>
3. <span data-ttu-id="2977f-142">Klik på **Send**.</span><span class="sxs-lookup"><span data-stu-id="2977f-142">Click the **Submit**.</span></span> <span data-ttu-id="2977f-143">Gentag trin 1-3 for at tilføje et spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="2977f-143">Repeat steps 1-3 to add a question.</span></span>
4. <span data-ttu-id="2977f-144">Når du er færdig, skal du klikke på **Gem** for at gemme dine spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="2977f-144">When done, click **Save** to save your questions.</span></span>

## <a name="replying-to-a-single-vendor"></a><span data-ttu-id="2977f-145">Besvare en enkelt leverandør</span><span class="sxs-lookup"><span data-stu-id="2977f-145">Replying to a single vendor</span></span>

<span data-ttu-id="2977f-146">Spørgsmål og svar er kun synlige for leverandøren og brugerne.</span><span class="sxs-lookup"><span data-stu-id="2977f-146">The question and answer are visible only to the vendor and users.</span></span>

1. <span data-ttu-id="2977f-147">På siden **Tilbudsanmodning** skal du klikke på **Spørgsmål og svar** for at åbne siden **Spørgsmål og svar**.</span><span class="sxs-lookup"><span data-stu-id="2977f-147">On the **Request for quotations** page, click the **Questions and answers** to display the **Questions and answers** page.</span></span>
1. <span data-ttu-id="2977f-148">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="2977f-148">Click **Edit**.</span></span>
1. <span data-ttu-id="2977f-149">Indtast tekst i **Svar**-feltet for at svare på leverandørspørgsmålet.</span><span class="sxs-lookup"><span data-stu-id="2977f-149">Enter text in the **Answer** field to respond to the vendor's question.</span></span>
1. <span data-ttu-id="2977f-150">Markér feltet **Direkte svar**.</span><span class="sxs-lookup"><span data-stu-id="2977f-150">Check the **Direct response** box.</span></span>
1. <span data-ttu-id="2977f-151">Klik på **Gem** for at gemme svarene.</span><span class="sxs-lookup"><span data-stu-id="2977f-151">Click **Save** to save your replies.</span></span>
1. <span data-ttu-id="2977f-152">Klik på **Send svar** for at sende svarene til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="2977f-152">Click **Send answers** to send the answers to the vendor.</span></span>

## <a name="replying-to-all-vendors"></a><span data-ttu-id="2977f-153">Besvare alle leverandører</span><span class="sxs-lookup"><span data-stu-id="2977f-153">Replying to all vendors</span></span>

<span data-ttu-id="2977f-154">Hvis du modtager samme spørgsmål fra flere leverandører, kan du gruppere spørgsmålene og reagere med det samme svar.</span><span class="sxs-lookup"><span data-stu-id="2977f-154">If you receive the same question from multiple vendors, you can group the questions and respond with one answer.</span></span> <span data-ttu-id="2977f-155">Alle leverandører modtager en besked, når de ofte stillede spørgsmål og svar udgives.</span><span class="sxs-lookup"><span data-stu-id="2977f-155">All vendors receive notification when the commonly asked questions and answers are published.</span></span> <span data-ttu-id="2977f-156">Leverandørerne og alle, der har adgang til tilbudsanmodningen, kan få vist oversigten over spørgsmål og svar.</span><span class="sxs-lookup"><span data-stu-id="2977f-156">The vendors and anyone with access to the request for quotation can view the summary of questions and answers.</span></span>

1. <span data-ttu-id="2977f-157">På siden **Tilbudsanmodning** skal du klikke på **Spørgsmål og svar** for at åbne siden **Spørgsmål og svar**.</span><span class="sxs-lookup"><span data-stu-id="2977f-157">On the **Request for quotations** page, click the **Questions and answers** to display the **Questions and answers** page.</span></span>
2. <span data-ttu-id="2977f-158">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="2977f-158">Click **Edit**.</span></span>
3. <span data-ttu-id="2977f-159">Vælg en kode for det almindelige spørgsmål, f.eks. bogstavet 'a'.</span><span class="sxs-lookup"><span data-stu-id="2977f-159">Choose a code for the common question, such as the letter 'a.'</span></span>
4. <span data-ttu-id="2977f-160">For hver linje, der stiller et lignende spørgsmål, skal du angive koden i feltet **Gruppekode**.</span><span class="sxs-lookup"><span data-stu-id="2977f-160">For each line that asks a similar question, enter the code in the **Group code** field.</span></span> <span data-ttu-id="2977f-161">For hver linje, der spørger til varens farve, skal du f.eks. angive 'a'.</span><span class="sxs-lookup"><span data-stu-id="2977f-161">For example, for each line asking about item color, enter 'a.'</span></span>
5. <span data-ttu-id="2977f-162">Vælg en af linjerne med kodeværdien, og angiv det spørgsmål og svar, som de skal læse i oversigten, og som skal være tilgængeligt, når spørgsmålene og svarene publiceres (**Gruppespørgsmål, Gruppesvar** som felter).</span><span class="sxs-lookup"><span data-stu-id="2977f-162">Choose one of the lines with the code value, and enter the question and answer the way you want them to read in the summary that will be available when the questions and answers are published (**Group question, Group answer** fields).</span></span>
6. <span data-ttu-id="2977f-163">Valgfrit: Du kan markere afkrydsningsfeltet **Direkte svar** for kun at sende svarene til de valgte leverandører.</span><span class="sxs-lookup"><span data-stu-id="2977f-163">Optional: You can mark the **Direct response** check box to send the answers only to the selected vendors.</span></span>
7. <span data-ttu-id="2977f-164">Klik på **Gem** for at gemme svarene.</span><span class="sxs-lookup"><span data-stu-id="2977f-164">Click **Save** to save your answers.</span></span>
8. <span data-ttu-id="2977f-165">Valgfrit: Du kan ændre spørgsmålene og svarene til de tidligere udgivne værdier, hvis du vil fortryde dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="2977f-165">Optional: You can revert the questions and answers to the previously published values if you want to undo your changes.</span></span>
9. <span data-ttu-id="2977f-166">Klik på **Send svar** for at sende svarene til leverandørerne.</span><span class="sxs-lookup"><span data-stu-id="2977f-166">Click **Send answers** to send your answers to the vendors.</span></span>

## <a name="changing-rfq-to-allow-or-disallow-questions"></a><span data-ttu-id="2977f-167">Ændre tilbudsanmodning for at tillade eller forbyde spørgsmål</span><span class="sxs-lookup"><span data-stu-id="2977f-167">Changing RFQ to allow or disallow questions</span></span>

<span data-ttu-id="2977f-168">Du kan foretage ændringer for at tillade eller ikke tillade spørgsmål til tilbudsanmodninger, indtil tilbudsanmodningen er belønnet.</span><span class="sxs-lookup"><span data-stu-id="2977f-168">You can make changes to allow or disallow questions to RFQs until the RFQ is awarded.</span></span> <span data-ttu-id="2977f-169">Du kan også udvide eller forkorte den tidsramme, som leverandørerne kan indsende spørgsmål i.</span><span class="sxs-lookup"><span data-stu-id="2977f-169">You can also extend or shorten the time frame in which vendors can submit questions.</span></span>
<span data-ttu-id="2977f-170">I forbindelse med publicerede tilbudsanmodninger skal du redigere en tilbudsanmodning for at tillade eller ikke tillade leverandørspørgsmål eller justere tidsrammen for spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="2977f-170">For published RFQs, you must modify a request for quotation  to allow or disallow vendor questions or adjust the time frame for questions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2977f-171">Hvis du ændrer en eksisterende tilbudsanmodning med det formål at tillade leverandørspørgsmål, rydder systemet alle eksisterende svar, når du sender tilbudsanmodningen igen.</span><span class="sxs-lookup"><span data-stu-id="2977f-171">If you amend an existing RFQ for the purpose of allowing vendor questions, the system will clear all existing responses when you resend the RFQ.</span></span>
